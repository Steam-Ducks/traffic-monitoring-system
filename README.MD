# <p align="center"> Tráfegou! – Monitoramento de Tráfego Inteligente</p>

Portal para consolidação de indicadores de mobilidade, atribui **níveis por região** e dispara **alertas vinculados a protocolos de ação**. Projeto proposto para atender a Prefeitura de São José dos Campos.

<p align="center"> <a href="#integrantes-da-equipe">👥 Integrantes da Equipe</a> • <a href="#descricao-do-desafio">📝 Descrição do Desafio</a> • <a href="#objetivo-do-projeto">🎯 Objetivo do Projeto</a> • <a href="#requisitos-funcionais">📋 Requisitos Funcionais</a> • <a href="#cronograma">📅 Cronograma</a> • <a href="#backlog-do-produto">🗂️ Backlog do Produto</a> • <a href="#dor">🏃‍ DoR</a> • <a href="#dod">🏆 DoD</a> • <a href="#indicadores-e-notas">📊 Indicadores & Notas</a> • <a href="#alertas-e-protocolos">🚨 Alertas & Protocolos</a> • <a href="#documentacao">📚 Documentação</a> • <a href="#boas-praticas">📋 Boas Práticas</a> • <a href="#tecnologias-utilizadas">🛠️ Tecnologias Utilizadas</a> </p>

<br>
<br><div style="display: flex; justify-content: center; gap: 80px; align-items: center; margin-top: 20px; margin-bottom: 20px;">
    <img src="./assets/SteamDucksLogo.png" alt="Logotipo Steam Ducks" width="40%">
    <img src="./assets/LogoTrafegou.png" alt="Logotipo Trafegou" width="40%">
</div>

<br>


## <a id="integrantes-da-equipe">Integrantes da Equipe</a>

| LinkedIn & GitHub | Integrantes | Função        |
|-------------------|-------------|---------------|
| <a href="https://www.linkedin.com/in/lucas-h-acosta?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/Lucas-heck-acosta" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>      | Lucas Acosta      | Product Owner |
| <a href="https://www.linkedin.com/posts/cruz-rafaella_%C3%A9-um-prazer-compartilhar-que-finalizei-meu-activity-7212665413376081921-mEAy?utm_source=share&utm_medium=member_desktop" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/arafaellacruz" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a> | Rafaella Cruz     | Scrum Master  |
| <a href="https://www.linkedin.com/in/alexander-silva-lima-96a0432a6?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/alexttz" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>   | Alexander Silva  | Dev Team      |
| <a href="https://www.linkedin.com/in/carlos-daniel-9516952b4/" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/darloscaniel" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a> | Carlos Daniel     | Dev Team      |
| <a href="https://www.linkedin.com/in/felipe-reiss/" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/felpzreiz" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>   | Felipe Reis      | Dev Team      |
| <a href="https://www.linkedin.com/in/isabelly-sousa?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/61isabelly" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>               | Isabelly Sousa    | Dev Team      |
| <a href="https://www.linkedin.com/in/luiz-henrique-rabello-ferreira-3600752ba?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/LuizHRFerreira" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a> | Luiz Henrique     | Dev Team      |
| <a href="https://www.linkedin.com/in/samuel-prado-9142381b6?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app" target="_blank"><img src="https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white" alt="Linkedin"></a> <a href="https://github.com/Samuelprado99" target="_blank"><img src="https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>  | Samuel Prado      | Dev Team      |


---
## 📒 <a id="descricao-do-desafio">Descrição do Desafio</a>

A Prefeitura de São José dos Campos necessita de uma solução que:

* **Monitore indicadores e parâmetros** de controle previamente definidos;
* **Gere alertas automáticos** no sistema, **vinculados a protocolos de ação**;
* **Permita resposta dos gestores** aos alertas, registrando providências e encerrando o chamado.


---

## 🎯 <a id="objetivo-do-projeto">Objetivo do Projeto</a>
O objetivo do projeto é construir um sistema de monitoramento contínuo do tráfego urbano, oferecendo uma visão ampla e detalhada da situação da cidade em tempo real. A plataforma permitirá a visualização de indicadores de desempenho por região e também de um índice consolidado geral da cidade, apresentados em mapas interativos e cards informativos. Além disso, o sistema será capaz de detectar e notificar automaticamente alterações críticas no tráfego, garantindo respostas rápidas a situações emergenciais. Cada nota ou nível atribuído será transparente, permitindo ao usuário acessar o detalhamento dos indicadores que compõem a avaliação. Por fim, a solução possibilitará que gestores respondam a determinados alertas, registrando suas ações e encerrando ocorrências de forma organizada e rastreável.


---

## 📋 <a id="requisitos-funcionais">Requisitos Funcionais</a>

| **ID** | **Funcionalidade**                  | **Descrição**                                                                                          |
|:------:|:------------------------------------|:-------------------------------------------------------------------------------------------------------|
|  RF1   | **Tratamento de Dados**             | Processar os dados recebidos em planilha CSV, validando, limpando e transformando para uso no sistema. |
|  RF2   | **Indicadores de Tráfego**          | Criar métricas de acompanhamento do tráfego, como velocidade média, volume e variação por região.      |
|  RF3   | **Níveis de Monitoramento**         | Estabelecer níveis de classificação para avaliar as regiões.                                           |
|  RF4   | **Dashboard com Georreferenciado**  | Exibir o tráfego de forma simples e lúdica, com mapas interativos e cards representando as regiões.    |
|  RF5   | **Dados Externos Complementares**   | Possibilitar a integração de fontes de dados externas que enriqueçam a análise do tráfego.             |
|  RF6   | **Sistema de Alertas e Protocolos** | Disparar notificações automáticas em caso de mudanças críticas e permitir o acionamento de protocolos. |


---

## 📆 <a id="cronograma">Cronograma</a>

| Fase                     | Início     | Entrega    | Status | Documentação                                              |
|--------------------------|------------|------------|--------|-----------------------------------------------------------| 
| Kick off                 | 25/08/2025 | 29/08/2025 | ✅      | -                                                         |
| Sprint 1                 | 08/09/2025 | 28/09/2025 | ✅      | [📋 Sprint 1](./documentation/sprint-backlog.md#sprint-1) |
| Sprint Review / Planning | 29/09/2025 | 03/10/2025 | ✅      | -                                                         |
| Sprint 2                 | 06/10/2025 | 26/10/2025 | ✅      | [📋 Sprint 2](./documentation/sprint-backlog.md#sprint-2) |
| Sprint Review / Planning | 27/10/2025 | 31/10/2025 | ✅      | -                                                         |
| Sprint 3                 | 03/11/2025 | 23/11/2025 | ✅     | [📋 Sprint 3](./documentation/sprint-backlog.md#sprint-3) |
| Sprint review            | 24/11/2025 | 28/11/2025 | 🔄      | -                                                         |
| Feira de Soluções        | 04/12/2025 | 04/12/2025 | 🔄      | -                                                         |

---

## 🗂️ <a id="backlog-do-produto">Backlog do Produto</a>

| **Rank** | **Prioridade** | **User Story**                                                                                                                                                            | **Story Points** | **Sprint** | **Requisito** | **Status** |
|:--------:|:--------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------:|:----------:|:-------------:|:---------:|
|    1     |      Alta      | Como Administrador, quero que o sistema consulte novos dados a cada 10 minutos para que sejam exibidos os dados mais recentes                                             |        8         |     1      |      RF1      |     ✅     |
|    2     |      Alta      | Como Gestor, quero visualizar o índice geral da cidade em um card destacado com cores de alerta para ter uma visão rápida da situação do tráfego                          |        8         |     1      |    RF2,RF3    |     ✅     |
|    3     |      Alta      | Como Gestor, quero visualizar cards individuais das minhas regiões com níveis atualizados para identificar rapidamente áreas problemáticas                                |        5         |     1      |    RF3,RF4    |     ✅     |
|    4     |      Alta      | Como Gestor, quero visualizar um mapa básico da cidade com regiões coloridas conforme níveis para análise geográfica                                                      |        8         |     1      |      RF4      |     ✅     |
|    5     |      Alta      | Como Gestor, quero poder interagir com o mapa aplicando filtros por região para analisar localidades com mais precisão                                                    |        8         |     2      |      RF4      |     ✅     |
|    6     |      Alta      | Como Gestor, quero receber alertas automáticos via sistema quando níveis críticos são atingidos para reagir rapidamente a emergências                                     |        8         |     2      |      RF6      |     ✅     |
|    7     |     Média      | Como Gestor, quero acessar uma seção de indicadores detalhados que compõem a nota geral e local, para entender o que está impactando o nível                              |        5         |     2      |      RF2      |     ✅     |
|    8     |     Média      | Como Administrador, quero cadastrar gestores locais no sistema e atribuí-los a regiões específicas para distribuir responsabilidades de monitoramento                     |        5         |     2      |      RF6      |     ✅     |
|    9     |     Média      | Como Gestor, quero visualizar quais são as ruas com o pior desempenho dentro de cada região para direcionar ações específicas                                            |        8         |     3      |      RF2      |     ✅     |
|    10    |     Média      | Como Gestor, quero marcar alertas como resolvidos após tomar ação, para poder acompanhar os acontecimentos ao longo do tempo                                              |        8         |     3      |      RF6      |     ✅     |
|    11    |     Baixa      | Como Administrador, quero enriquecer os cálculos com dados externos para aumentar a precisão das análises de tráfego.                                                       |        5         |     3      |      RF5      |     ✅     |
|    12    |     Baixa      | Como Gestor, quero visualizar facilmente se os indicadores estão melhorando / piorando em relação ao periodo anterior para entender se ações tomadas estão sendo efetivas |        3         |     3      |      RF4      |     ✅     |


---
## 🏃‍ <a id="dor">DoR - Definition of Ready</a>

* User Stories com **Critérios de Aceitação**
* Subtarefas divididas **a partir das US**
* Design no **Figma**
* Modelagem do **Banco de Dados**
* Modelo de cálculo dos **indicadores e níveis**
* Definicão dos **protocolos**

---

## 🏆 <a id="dod">DoD - Definition of Done</a>

* Manual de Usuário
* Manual da Aplicação
* Documentação da API (Application Programming Interface)
* Código completo
* Vídeos de cada etapa de entrega

---

## 📊 <a id="indicadores-e-notas">Indicadores & Notas</a>

### Sistema de Níveis
O sistema utiliza uma escala de **1 a 5** para classificar o nível de tráfego por região:

| **Nível** | **Cor** | **Descrição** | **Ação Requerida** |
|:---------:|:-------:|:--------------|:-------------------|
| 1 | 🟢 Verde | Tráfego fluindo normalmente | Monitoramento passivo |
| 2 | 🟡 Amarelo | Tráfego lento, mas controlado | Atenção básica |
| 3 | 🟠 Laranja | Congestionamento moderado | Monitoramento ativo |
| 4 | 🔴 Vermelho | Congestionamento severo | **Alerta automático** |
| 5 | 🟣 Roxo | Tráfego crítico/parado | **Emergência - Ação imediata** |

### Detalhamento dos Cálculos

Para entender como os níveis são calculados, consulte a documentação completa dos indicadores:

📊 [**Cálculo dos Indicadores de Tráfego**](./documentation/calculo-indicadores.md)

O documento inclui:
* **4 Indicadores principais** (Velocidade Média, Taxa de Conformidade, Densidade de Tráfego, Condições Climáticas)
* **Fórmulas detalhadas** de cada cálculo
* **Pesos e ponderações** utilizados
* **Thresholds de categorização** para cada nível


---

## 🚨 <a id="alertas-e-protocolos">Alertas & Protocolos</a>

### Gatilhos de Alerta
Os alertas são disparados automaticamente quando:

* **Nível 4 ou 5** é atingido em qualquer região
* **Mudança súbita** de 2+ níveis em menos de 10 minutos


### Canais de Notificação
* 📱 **Telegram** - Mensagens diretas para gestores


### Protocolos de Ação

#### **Sistema de Responsabilidades**

O sistema de notificações do Tráfegou funciona através de um modelo hierárquico de **cargos e regiões**:

##### **🏢 Estrutura Organizacional**
* **Cargos** podem ser criados e configurados conforme a necessidade da prefeitura
* Cada **cargo** pode ser atribuído a **múltiplas regiões** da cidade
* **Pessoas cadastradas** possuem um cargo específico
* Cada pessoa recebe **atualizações sobre todas as regiões** do seu cargo

##### **👥 Exemplos de Cargos e Responsabilidades**

| **Cargo** | **Regiões de Atuação** | **Responsabilidades** |
|:----------|:-----------------------|:----------------------|
| **Coordenador Geral** | Todas as regiões | Supervisão geral, decisões estratégicas |
| **Gestor Zona Norte** | Centro, Vila Industrial | Coordenação local, ações operacionais |
| **Gestor Zona Sul** | Jardim das Colinas, Vila Adyana | Coordenação local, ações operacionais |
| **Operador de Trânsito** | Regiões específicas | Ajustes de semáforos, orientação de tráfego |

##### **📱 Fluxo de Notificações**
1. **Sistema detecta** nível crítico (4 ou 5) em uma região
2. **Identifica automaticamente** todos os cargos vinculados àquela região
3. **Envia notificação via Telegram** para todas as pessoas desses cargos
4. **Registra o alerta** no histórico do sistema
5. **Monitora continuamente** até normalização

##### **⚙️ Configuração Flexível**
* Administradores podem **criar novos cargos** conforme necessário
* **Vincular/desvincular regiões** a cargos existentes
* **Cadastrar/editar pessoas** e seus respectivos cargos


---

## 📃 <a id="documentacao">Documentação</a>

* 📊 [**Cálculo dos Indicadores de Tráfego**](./documentation/calculo-indicadores.md) - Detalhamento completo das fórmulas, pesos e categorização
* 📋 [**Backlog das Sprints**](./documentation/sprint-backlog.md) - Planejamento e objetivos de cada sprint
* 📄 [**Boas Práticas de Desenvolvimento**](./Boas%20praticas.md) - Padrões de código e organização
* **Manual do Usuário** - Guia de utilização do sistema
* **Dados CSV** - Estrutura e formato dos dados de entrada
* **Burndown & Métricas de Entrega** - Acompanhamento do progresso

---

## 📋 <a id="boas-praticas">Boas Práticas</a>

Para manter a qualidade e consistência do código, nossa equipe segue diretrizes específicas de desenvolvimento. Consulte o documento completo de boas práticas:

📄 [**Boas Práticas de Desenvolvimento**](./Boas%20praticas.md)

O documento inclui:
* **Padrões de Commit** - Estrutura padronizada para mensagens de commit
* **Templates para Pull Request** - Formato para revisões de código
* **Orientações para Dailys** - Estrutura para reuniões diárias
* **Organização de Cards no JIRA** - Padrões para gestão de tarefas

---

## 🏗️ <a id="arquitetura">Arquitetura do Sistema</a>

### Visão Geral
O **Tráfegou** é uma aplicação web completa com arquitetura em **três camadas**:

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   Banco de      │
│   (Vue.js)      │◄──►│   (Spring Boot) │◄──►│   Dados         │
│                 │    │                 │    │   (Oracle)      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### Componentes Principais

#### **Frontend (tms-client)**
- **Framework**: Vue.js 3 com TypeScript
- **Mapa Interativo**: Leaflet.js para visualização geográfica
- **Gráficos**: Chart.js para dashboards

#### **Backend (tms-server)**
- **Framework**: Spring Boot 3 com Java 17
- **API REST**: Endpoints para CRUD e consultas
- **Scheduler**: Jobs automáticos para coleta de dados

#### **Banco de Dados**
- **SGBD**: Oracle Database
- **Conexão**: Pool de conexões via HikariCP

### Fluxo de Dados
1. **Coleta** - Sistema consulta APIs externas a cada 2 minutos
2. **Processamento** - Dados são validados e transformados
3. **Cálculo** - Indicadores e níveis são recalculados
4. **Armazenamento** - Resultados persistidos no banco
5. **Exibição** - Frontend atualiza dashboards em tempo real
6. **Alertas** - Sistema dispara notificações se necessário

---

## ⚙️ <a id="instalacao">Instalação e Execução</a>

### Pré-requisitos
- **Docker** e **Docker Compose**
- **Java 17+** (para desenvolvimento)
- **Node.js 18+** (para desenvolvimento)

### 🚀 Execução com Docker (Recomendado)

1. **Clone o repositório**
```bash
git clone https://github.com/seu-usuario/API4Semestre.git
cd API4Semestre
```

2. **Execute o ambiente completo**
```bash
# Subir todos os serviços
docker-compose up -d

# Verificar logs
docker-compose logs -f
```

3. **Acesse a aplicação**
- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:8080

### 🛠️ Desenvolvimento Local

#### **Backend**
```bash
cd tms-server/spring-app
./mvnw spring-boot:run
```

#### **Frontend**
```bash
cd tms-client
npm install
npm run dev
```

### 🔧 Configuração do Banco

O sistema utiliza **Oracle Database**. Configure as variáveis de ambiente

##

---

##  🛠️ <a id="tecnologias-utilizadas">Tecnologias Utilizadas</a>

### **Back-end**

* **Java 17**
* **Spring Boot**
* **Maven**
* **Oracle**

### **Front-end**

* **Vue.js 3**

### **Infra**

* **Docker**
* **Git/GitHub**

---

<div align="center">
    <img src="assets/footer.png" alt="footer" width="100%" />
</div>
