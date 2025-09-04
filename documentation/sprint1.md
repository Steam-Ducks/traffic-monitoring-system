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
ass
# User Stories das Sprint

<details>
<summary>Sprint 1</summary>

## User Stories da Sprint

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 1 | ALTA | PS-1 | Como administrador, quero que o sistema armazene no banco de dados os dados de tráfego, regiões e indicadores, para garantir a persistência das informações e permitir análises futuras. | - | 1 | - |

### Requisitos
- O sistema armazena dados de tráfego, regiões e indicadores no banco de dados.
- Garante a persistência das informações.
- Permite análises futuras.

### Definition of ready:
- Estrutura de banco definida (tabelas, chaves primárias e estrangeiras).
- Dados de teste disponíveis.

### Definition of done:
- CRUD de dados implementado.
- Testes de inserção e atualização realizados com sucesso.
- Persistência validada em ambiente de teste.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Dados de tráfego, regiões e indicadores salvos de forma consistente no banco. |
| Histórico mantido para consultas futuras. |
| Operações de leitura e escrita funcionando sem perda de dados. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 2 | ALTA | PS-2 | Como gestor, quero visualizar o índice geral da cidade em um card destacado com cores de alerta, para ter uma visão rápida da situação do tráfego. | - | 1 | - |

### Requisitos
- O card exibe o índice geral calculado a partir de todas as regiões.
- A cor do card muda conforme o nível crítico (verde, amarelo, vermelho).
- Atualização em tempo quase real.

### Definition of ready:
- Fórmula de cálculo do índice definida.
- Layout do card aprovado.

### Definition of done:
- Card exibe índice corretamente.
- Atualização validada em testes de simulação.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Alteração de indicadores regionais → índice geral recalculado e card atualizado. |
| Nível crítico → card exibe cor correta. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 3 | ALTA | PS-3 | Como gestor, quero visualizar cards individuais das minhas regiões com níveis atualizados, para identificar rapidamente áreas problemáticas. | - | 1 | - |

### Requisitos
- Cada card exibe o nível da respectiva região.
- Cores indicam o estado da região.
- Cards possuem link para detalhes.

### Definition of ready:
- Lista de regiões do gestor disponível.
- Layout dos cards aprovado.

### Definition of done:
- Cards atualizam automaticamente ao alterar dados de região.
- Links para detalhes funcionando.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Região com nível normal → card verde. |
| Região com nível crítico → card vermelho. |

---

| Rank | Prioridade | ID | User Story | Estimativa | Sprint | Requisito do parceiro |
|------|------------|----|------------|------------|--------|-----------------------|
| 4 | MÉDIA | PS-4 | Como administrador, quero cadastrar gestores locais e atribuí-los a regiões específicas, para distribuir responsabilidades de monitoramento. | - | 1 | - |

### Requisitos
- CRUD de gestores implementado.
- Cada gestor pode ser atribuído a uma ou mais regiões.
- Permissões aplicadas corretamente.

### Definition of ready:
- Estrutura de permissões definida.
- Lista de regiões disponível.

### Definition of done:
- Gestores cadastrados e vinculados às regiões com sucesso.
- Permissões validadas em teste.

## Regras de Negócio

| Definições do Cliente |
|---------------------------------------------------------------------------------------------------------------------|
| Cadastro de novo gestor → aparece na lista. |
| Alteração de regiões atribuídas → refletida no sistema. |

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

