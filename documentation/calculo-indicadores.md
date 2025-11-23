# 📊 Cálculo dos Indicadores de Tráfego

Este documento detalha o processo de cálculo de todos os indicadores utilizados pelo sistema **Tráfegou** para determinar o nível de tráfego de cada região da cidade.

## ⏱️ Frequência de Atualização

O sistema coleta e processa dados a **cada 2 minutos**, garantindo informações em tempo real sobre a situação do tráfego.

---

## 📈 Indicadores Principais

O sistema calcula **4 indicadores** para cada região da cidade:

1. **Velocidade Média** (peso: 40%)
2. **Taxa de Conformidade** (peso: 25%)
3. **Densidade de Tráfego** (peso: 20%)
4. **Condições Climáticas** (peso: 15%)

---

## 🚗 1. Velocidade Média

Mede o quão bem o tráfego está fluindo em relação aos limites de velocidade estabelecidos.

### Processo de Cálculo

#### **Passo 1: Velocidade Média por Câmera**
```
Velocidade Média = Σ Velocidades / Quantidade de Registros
```

#### **Passo 2: Normalização**
Normaliza o resultado com base no limite de velocidade da via:
```
Valor Normalizado = Velocidade Média / Limite de Velocidade da Via
```

#### **Passo 3: Soma Ponderada**
Pondera cada câmera pelo volume de veículos detectados:
```
Soma Ponderada = Σ (Valor Normalizado × Total de Veículos)
```

#### **Passo 4: Média Regional**
Divide pela quantidade total de registros na região:
```
Resultado = (Soma Ponderada / Total de Registros) × 100
```

### Categorização

| **Valor** | **Nível** | **Classificação** | **Cor** |
|:---------:|:---------:|:------------------|:-------:|
| ≥ 85% | 1 | Ótimo | 🟢 |
| ≥ 70% | 2 | Bom | 🟡 |
| ≥ 55% | 3 | Regular | 🟠 |
| ≥ 40% | 4 | Ruim | 🔴 |
| < 40% | 5 | Crítico | 🟣 |

**Peso no Cálculo Final: 40%**

---

## ⚠️ 2. Taxa de Conformidade

Mede a porcentagem de veículos que excedem o limite de velocidade permitido.

### Processo de Cálculo

#### **Passo 1: Contagem de Infrações**
Conta todos os registros onde a velocidade ultrapassou o limite:
```
Total Acima do Limite = Σ Registros com (Velocidade > Limite)
```

#### **Passo 2: Cálculo da Taxa**
Divide pelo total de registros e converte para percentual:
```
Taxa de Conformidade = (Total Acima / Total de Registros) × 100
```

### Categorização

| **Taxa** | **Nível** | **Classificação** | **Cor** |
|:--------:|:---------:|:------------------|:-------:|
| 0 - 1% | 1 | Ótimo | 🟢 |
| 1,1 - 2,9% | 2 | Bom | 🟡 |
| 3 - 3,9% | 3 | Regular | 🟠 |
| 4 - 4,9% | 4 | Ruim | 🔴 |
| ≥ 5% | 5 | Crítico | 🟣 |

**Peso no Cálculo Final: 25%**

---

## 🚦 3. Densidade de Tráfego

Mede o volume de veículos por câmera, indicando o nível de congestionamento.

### Processo de Cálculo

#### **Passo 1: Total de Registros**
Soma todos os registros de veículos na região:
```
Total de Registros = Σ Registros da Região
```

#### **Passo 2: Contagem de Câmeras Ativas**
Conta quantas câmeras registraram pelo menos um veículo:
```
Câmeras Ativas = Quantidade de Câmeras com Registros > 0
```

#### **Passo 3: Registros por Câmera**
Calcula a média de registros por câmera:
```
Registros por Câmera = Total de Registros / Câmeras Ativas
```

#### **Passo 4: Normalização**
Normaliza o resultado dividindo por 100:
```
Resultado = Registros por Câmera / 100
```

### Categorização

| **Valor** | **Nível** | **Classificação** | **Cor** |
|:---------:|:---------:|:------------------|:-------:|
| ≤ 2 | 1 | Ótimo | 🟢 |
| ≤ 5 | 2 | Bom | 🟡 |
| ≤ 7 | 3 | Regular | 🟠 |
| ≤ 10 | 4 | Ruim | 🔴 |
| > 10 | 5 | Crítico | 🟣 |

**Peso no Cálculo Final: 20%**

---

## 🌦️ 4. Condições Climáticas

Mede o impacto das condições meteorológicas na qualidade do tráfego.

### Processo de Cálculo

#### **Passo 1: Coleta de Dados**
O sistema consulta uma API de clima externa para obter as condições atuais da cidade.

#### **Passo 2: Análise das Condições**
Avalia fatores como:
- Precipitação (chuva, neve, granizo)
- Visibilidade
- Intensidade do vento
- Condições gerais (ensolarado, nublado, tempestade)

### Categorização

| **Condição** | **Nível** | **Classificação** | **Impacto** |
|:-------------|:---------:|:------------------|:-----------:|
| Ensolarado, céu limpo | 1 | Ótimo | Nenhum |
| Parcialmente nublado | 2 | Bom | Mínimo |
| Nublado, vento moderado | 3 | Regular | Moderado |
| Chuva leve, neblina | 4 | Ruim | Alto |
| Chuva forte, tempestade | 5 | Crítico | Muito Alto |

**Peso no Cálculo Final: 15%**

---

## 🎯 Cálculo do Nível Final

O **nível final** de cada região é calculado através de uma **média ponderada** dos 4 indicadores:

```
Nível Final = (Velocidade Média × 0,40) + 
              (Taxa de Conformidade × 0,25) + 
              (Densidade de Tráfego × 0,20) + 
              (Condições Climáticas × 0,15)
```

### Distribuição de Pesos

| **Indicador** | **Peso** | **Justificativa** |
|:--------------|:--------:|:------------------|
| Velocidade Média |   40%    | Principal indicador de fluidez do tráfego |
| Taxa de Conformidade |   25%    | Importante para segurança viária |
| Densidade de Tráfego |   20%    | Complementa a análise de congestionamento |
| Condições Climáticas |   15%    | Fator externo que impacta o tráfego |

### Arredondamento

O resultado final é arredondado para o **nível inteiro mais próximo** (1 a 5).

---

## 📍 Nível Geral da Cidade

O **nível geral da cidade** é calculado como a **média aritmética simples** dos níveis finais de todas as regiões:

```
Nível Geral = Σ Níveis das Regiões / Quantidade de Regiões
```

Esse valor também é arredondado para o nível inteiro mais próximo.

---

## 🔄 Fluxo de Atualização

```
┌─────────────────────────────────────────────────────┐
│  A cada 2 minutos                                   │
└─────────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────────┐
│  1. Coleta de dados de tráfego e clima             │
└─────────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────────┐
│  2. Cálculo dos 4 indicadores por região           │
└─────────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────────┐
│  3. Aplicação da média ponderada                   │
└─────────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────────┐
│  4. Determinação do nível final (1-5)              │
└─────────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────────┐
│  5. Cálculo do nível geral da cidade               │
└─────────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────────┐
│  6. Verificação de gatilhos de alerta              │
└─────────────────────────────────────────────────────┘
                      ↓
┌─────────────────────────────────────────────────────┐
│  7. Atualização dos dashboards e notificações      │
└─────────────────────────────────────────────────────┘
```


---

## 📝 Notas Importantes

* Os **thresholds de categorização** foram ajustados durante o desenvolvimento para proporcionar maior variabilidade nos resultados apresentados
* O sistema mantém **histórico completo** de todos os cálculos para análises futuras
* Os **pesos dos indicadores** podem ser ajustados conforme necessidades operacionais da prefeitura
* A inclusão do **indicador climático** (15%) reduz proporcionalmente o peso dos outros indicadores, mantendo o total em 100%

---


