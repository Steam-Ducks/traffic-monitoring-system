<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
<div align="center">
<img src="../assets/header.png" alt="capa-readme" width="100%" />
</div>

# User Stories das Sprint

<details>
<summary>Sprint 1</summary>

## User Stories da Sprint

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 1 | ALTA | PS-1 | Como Administrador, quero que o sistema consulte novos dados a cada 10 minutos para que sejam exibidos os dados mais recentes. | 8 | 1 | RF1 |

### Meta de Entrega
Manter o sistema constantemente atualizado com os dados mais recentes, sem necessidade de ação de nenhum usuário.

### Indicadores
- Consultas realizadas a cada 10 minutos.
- Banco de dados reflete apenas os dados de consulta mais recentes.
- Em caso de falha, os dados da última consulta bem-sucedida são mantidos.

### Regras de negócio
- Os dados consumidos não devem ser mantidos a longo prazo -> sistema não duplica a base de registro das câmeras.
- Dados atualizados de 10 em 10 minutos -> sempre exibindo a situação atual do trânsito na cidade.

### Definition of Ready:
- Estrutura de banco definida (tabelas, chaves primárias e estrangeiras).
- Endpoint da API das câmeras identificados e documentados.
- Modelo de processamento de dados definido.

### Definition of Done:
- API de consulta às câmeras implementada e funcionando.
- Processamento de dados validado.
- Persistência no banco de dados funcionando.
- Testes de integração realizados com sucesso.
- Atualização em tempo real validada.


---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 2 | ALTA | PS-2 | Como Gestor, quero visualizar o índice geral da cidade em um card destacado com cores de alerta para ter uma visão rápida da situação do tráfego. | 8 | 1 | RF2, RF3 |

### Meta de Entrega
Fornecer aos gestores e a população uma visualização rápida e clara da situação do tráfego na cidade.

### Indicadores
- Nível é calculado com base em todas as regiões da cidade.
- Card muda de cor automaticamente de acordo com o nível calculado.

## Regras de Negócio
- Alteração de indicadores regionais → índice geral recalculado e card atualizado automaticamente.
- Níveis seguem uma numeração de 1 a 5, e possuem cores atribuídas (Verde - Amarelo - Laranja - Vermelho - Roxo).

### Definition of Ready:
- Fórmula de cálculo do acúmulo das regiões gerando o nível da cidade definida.
- Layout do card aprovado no Figma.
- Critérios de cores por nível estabelecidos.

### Definition of Done:
- Card exibe índice corretamente calculado.
- Cores seguem o nível.
- Nível da cidade sempre reflete o acúmulo das regiões.
- Atualização validada em testes de simulação.



---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 3 | ALTA | PS-3 | Como Gestor, quero visualizar cards individuais das minhas regiões com níveis atualizados para identificar rapidamente áreas problemáticas. | 5 | 1 | RF3, RF4 |

### Meta de Entrega
Permitir que gestores e a população monitorem o tráfego de regiões específicas da cidade separadamente.

### Indicadores
- Nível é calculado com base em uma série de indicadores pré-definidos.
- Cada card representa o nível de sua região associada.

### Regras de negócio
- Ao receber novos dados das câmeras de trânsito, indicadores por região são recalculados e geram um novo nível para cada região.
- Cada região tem seu próprio nível independente dos outros e de fácil identificação.
- Níveis seguem uma numeração de 1 a 5, e possuem cores atribuídas (Verde - Amarelo - Laranja - Vermelho - Roxo).

### Definition of Ready:
- Regiões da cidade definidas e delimitadas.
- Fórmula de cálculo dos indicadores definida.
- Fórmula de acúmulo dos indicadores em um nível de 1 a 5.
- Layout dos cards aprovado no Figma.
- Dados de teste para múltiplas regiões disponíveis.

### Definition of Done:
- Cards exibem os níveis corretamente calculados.
- Cores aplicadas conforme regras de negócio.
- Cada nível representa um acúmulo dos indicadores individuais.
- Atualização validada em testes de simulação.

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 4 | ALTA | PS-4 | Como Gestor, quero visualizar um mapa básico da cidade com regiões coloridas conforme níveis para análise geográfica. | 8 | 1 | RF4 |

### Meta de Entrega
Permitir análise geográfica das condições de tráfego por região, facilitando a tomada de decisões e associação de um nível a um local.

### Indicadores
- Mapa exibe divisões geográficas das regiões da cidade.
- Cada região é colorida conforme seu nível atual.

### Regras de negócio
- Divisão das regiões segue mapa da prefeitura de São José dos Campos.
- Níveis seguem uma numeração de 1 a 5, e possuem cores atribuídas (Verde - Amarelo - Laranja - Vermelho - Roxo).

### Definition of Ready:
- Base cartográfica da cidade carregada.
- Divisões das regiões georreferenciadas.
- Dados de teste com níveis por região disponíveis.
- Layout do componente de mapa aprovado.

### Definition of Done:
- Mapa carrega corretamente com todas as regiões.
- Cores das regiões refletem níveis em tempo real.
- Interações com o mapa exibem mais detalhes da região.
- Atualização validada em testes de simulação.


---

</details>




<details>
<summary>Sprint 2</summary>

## User Stories da Sprint

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 5 | ALTA | PS-5 | Como gestor, quero visualizar um mapa interativo da cidade com cores por região e filtros por período, para analisar o tráfego geograficamente. | - | 2 | - |

### Requisitos
- O mapa exibe regiões com cores representando o nível atual.
- Filtros aplicáveis por região, período e indicador.
- Atualização em tempo real.

### Definition of ready:
- Base cartográfica carregada.
- Dados georreferenciados disponíveis.

### Definition of done:
- Filtros funcionando corretamente.
- Cores refletem níveis em tempo real.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Aplicar filtro por período → mapa atualiza. |
| Alteração de nível → cor da região no mapa muda. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 6 | ALTA | PS-6 | Como gestor, quero receber alertas automáticos quando níveis críticos forem atingidos, para reagir rapidamente a emergências. | - | 2 | - |

### Requisitos
- Alerta disparado em nível crítico.
- Alerta contém região, indicador e nível.

### Definition of ready:
- Critérios de alerta definidos.
- Canal de envio configurado (e-mail ou push).

### Definition of done:
- Alertas disparados e recebidos corretamente.
- Histórico de alertas armazenado.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Nível sobe para crítico → alerta enviado. |
| Nível normalizado → alerta de normalização enviado. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 7 | MÉDIA | PS-7 | Como administrador, quero configurar regras de alerta personalizadas por indicador e região, para automatizar notificações críticas. | - | 2 | - |

### Requisitos
- Regras criadas, editadas e excluídas.
- Notificação respeita regras configuradas.

### Definition of ready:
- Lista de indicadores disponível.
- Critérios de alerta documentados.

### Definition of done:
- Regras configuráveis e testadas.
- Alertas funcionam conforme configuração.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Criar regra → alerta dispara corretamente. |
| Desativar regra → alerta não dispara. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 8 | MÉDIA | PS-8 | Como gestor, quero acessar indicadores detalhados que compõem a nota geral e local, para entender o que está impactando o nível. | - | 2 | - |

### Requisitos
- Exibição de indicadores individuais com histórico.
- Filtros por região e período funcionando.

### Definition of ready:
- Dados históricos disponíveis.
- Layout aprovado.

### Definition of done:
- Indicadores detalhados exibidos corretamente.
- Filtros aplicando alterações.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Filtro por região → indicadores atualizam. |
| Alteração de indicador recalcula nível local. |

---

</details>




<details>
<summary>Sprint 3</summary>

## User Stories da Sprint

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 9 | BAIXA | PS-9 | Como administrador, quero permitir a integração de dados externos, para enriquecer as análises com dados complementares. | - | 3 | - |

### Requisitos
- Dados externos validados antes de integrar.
- Indicadores recalculados após integração.

### Definition of ready:
- Endpoints de API disponíveis.
- Dados de teste providos.

### Definition of done:
- Integração funcionando e validada.
- Recalculo automático dos indicadores.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| API externa retorna dados válidos → sistema integra. |
| API externa indisponível → erro tratado. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 10 | BAIXA | PS-10 | Como cidadão, quero acessar um portal público com mapa simplificado e índice geral da cidade sem login, para acompanhar a situação do tráfego. | - | 3 | - |

### Requisitos
- Apenas dados resumidos exibidos.
- Nenhum dado sensível exposto.
- Filtros simples por região ou indicador.

### Definition of ready:
- Layout do portal aprovado.
- Dados resumidos disponíveis.

### Definition of done:
- Portal funcionando corretamente.
- Testes realizados para garantir que dados sensíveis não vazem.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Página abre → mapa e índice carregam. |
| Filtro aplicado → mapa atualizado. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 11 | MÉDIA | PS-11 | Como administrador, quero gerenciar usuários do sistema (criar, editar, desativar), para controlar quem tem acesso às funcionalidades. | - | 3 | - |

### Requisitos
- Criar, editar, desativar usuários funcionando.
- Permissões aplicadas corretamente.

### Definition of ready:
- Perfis e permissões definidos.

### Definition of done:
- CRUD funcionando e validado.
- Permissões aplicadas corretamente em testes.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Criar usuário → acesso liberado. |
| Desativar usuário → acesso bloqueado. |

---

</details>

</body>
</html>

