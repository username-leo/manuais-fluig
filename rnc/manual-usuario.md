---
title: Manual do Usuário
parent: RNC — Registro de Não Conformidade
nav_order: 1
---

# Manual do Usuário - RNC Registro de Não Conformidade

## O que é o processo RNC?

O processo de **Registro de Não Conformidade (RNC)** é utilizado para registrar, tratar e acompanhar ocorrências de qualidade que envolvem fornecedores, clientes ou operações internas da Moldemaq. Ele garante que cada não conformidade seja analisada, tratada com um plano de ação e verificada quanto à sua eficácia.

---

## Acesso ao processo

1. Acesse o Fluig e vá até **Processos** e depois em **Iniciar Solicitações**
2. Localize o processo **RNC - Registro de Não Conformidade**
3. Clique no processo para abrir uma nova solicitação

---

## Campos de abertura (comuns a todas as origens)

| Campo | Descrição |
|---|---|
| Data da Ocorrência | Data em que a não conformidade foi identificada |
| Origem da Ocorrência | Define o fluxo: **Fornecedor**, **Cliente** ou **Interno** |
| Descrição Detalhada | Descreva com clareza o problema identificado |

A **Origem da Ocorrência** determina quais campos serão exibidos e qual sequência de atividades o processo seguirá.

---

---

# Fluxo: Origem Fornecedor

Utilizado quando o problema foi causado por um fornecedor externo.

---

## Etapa 1 - Abertura da Solicitação

**Campos obrigatórios:**

| Campo | Descrição |
|---|---|
| Tipo de Ocorrência | Ex: Componente defeituoso, Dimensional fora do especificado, etc. |
| Fornecedor | Selecione via zoom o fornecedor responsável |
| Nota Fiscal de Entrada | Número da NF do produto com problema |
| Prioridade | Baixo / Médio / Alto / Crítico |
| Tipo de Controle | Ordem de Produção, Pedido de Compra ou Nº de Série |
| Resolução | **Interna** (sem devolução) ou **Externa** (com devolução ao fornecedor) |
| Tabela de Produtos | Adicione os itens envolvidos (produto, quantidade, valor) |

**Se a resolução for Externa, preencha também:**

| Campo | Descrição |
|---|---|
| Armazém | Local de armazenamento dos itens |
| Volumes | Quantidade de volumes para remessa |
| Peso (Kg) | Peso total da remessa |
| Dimensões (cm) | Dimensões da embalagem |
| Responsável pela Remessa | Moldemaq ou Fornecedor |

---

## Etapa 2 - Tratativa com Fornecedor

A equipe responsável define como a não conformidade será tratada:

- **Disposição:** devolução, sucateamento, retrabalho, etc.
- **Frete:** CIF ou FOB
- **Transportadora:** selecione via zoom
- **Autorização de Envio:** Sim ou Não
- **Frete por conta de:** Fornecedor ou Moldemaq
- **E-mail do Fornecedor:** obrigatório para envio da solicitação de resposta

> Ao avançar, o sistema envia automaticamente um e-mail ao fornecedor com os detalhes da RNC e um formulário de resposta.

---

## Etapa 3 - Resposta do Fornecedor

O fornecedor recebe um e-mail com os dados da ocorrência e responde com:

- Disposição acordada
- Ação Corretiva
- Ação Preventiva
- Prazo de retorno
- Observações

A equipe registra a resposta nos campos correspondentes e valida a **Garantia** (Aprovada ou Reprovada).

**Se garantia Aprovada com resolução Externa, preencha também:**
- Disposição
- Frete e Transportadora
- Autorização de Envio
- Frete por conta de
- Prazo de Retorno por item

---

## Etapa 4 - Faturamento *(quando aplicável)*

Preencha os dados da nota fiscal de faturamento:

| Campo | Obrigatório |
|---|---|
| Nota Fiscal | Sim |
| Pedido | Sim |

---

## Etapa 5 - Expedição

Registra o envio físico dos itens ao fornecedor. Nesta etapa, o responsável pela expedição confirma que os itens foram separados, embalados e entregues à transportadora conforme acordado na tratativa. Após a confirmação, avance a tarefa para registrar o envio no processo.

---

## Etapa 6 - Recebimento

Registre o recebimento dos itens devolvidos:

- **Nota Fiscal de Retorno** (obrigatória, exceto para troca física)
- **Quantidade Recebida** por item: deve ser igual à quantidade original

> O sistema bloqueia o avanço caso haja divergência de quantidades.

---

---

# Fluxo: Origem Cliente

Utilizado para registrar ocorrências relatadas por clientes. Selecione o **Tipo de Registro** conforme o caso.

---

## Etapa 1 - Abertura da Solicitação

### Tipo: Atendimento

| Campo | Obrigatório |
|---|---|
| Nº do Atendimento | Sim |
| Telefone | Sim |
| Produto Garantia | Sim |
| Segmento do Problema | Sim |
| Problema | Sim |
| Horas Trabalhadas | Sim |
| Acompanha Entrega | Sim |
| Garantia ou Bonificação | Sim |
| Tabela de Produtos | Sim (mínimo 1 item) |

### Tipo: Reclamação

| Campo | Obrigatório |
|---|---|
| Cliente | Sim |
| Telefone | Sim |
| Produto Garantia | Sim |
| Segmento do Problema | Sim |
| Problema | Sim |
| Garantia / Bonificação | Deve ser marcado como **Bonificação** |

### Tipo: Mão de Obra

| Campo | Obrigatório |
|---|---|
| Cliente | Sim |
| Telefone | Sim |
| Produto Garantia | Sim |
| Tipo de Controle | Sim (OP, Pedido de Compra ou Nº de Série) |
| Tabela de Produtos | Sim (mínimo 1 item) |

---

## Etapa 2 - Acompanhamento de Entrega *(quando marcado na solicitação)*

Controle da entrega das peças ao cliente. Preencha os dados e mantenha-os sempre atualizados conforme o andamento da entrega.

| Campo | Obrigatório |
|---|---|
| Status | Sim |
| Transportadora | Sim |
| Data de Entrega | Sim |
| Código de Rastreio | Sim |

> Esta atividade deve permanecer nesta etapa até que a entrega seja concluída. Para salvar sem movimentar o processo, clique na seta ao lado do botão **Enviar** e selecione **Somente Salvar**.

---

## Etapa 3 - Aguardando Retorno das Peças

Controle do retorno das peças defeituosas para análise técnica. Preencha os campos e movimente a atividade quando o retorno for confirmado.

| Campo | Obrigatório |
|---|---|
| Nota Fiscal de Retorno | Sim |
| Data de Retorno | Sim |

---

*Após esta etapa, o processo segue para a seção de **Análise de Processo e Plano de Ação** descrita ao final deste manual.*

---

---

# Fluxo: Origem Interno

Utilizado para registrar não conformidades identificadas internamente na Moldemaq. Este é o fluxo mais simples: após a abertura da solicitação, o processo vai diretamente para as atividades de **Análise de Processo e Plano de Ação**, sem etapas intermediárias de tratativa ou expedição.

---

## Etapa 1 - Abertura da Solicitação

| Campo | Obrigatório |
|---|---|
| Tipo de Ocorrência | Sim |
| Centro de Custo | Sim |
| Funcionário | Sim |
| Tabela de Produtos | Sim (mínimo 1 item) |

---

*Após esta etapa, o processo segue diretamente para a seção de **Análise de Processo e Plano de Ação** descrita abaixo.*

---

---

# Análise de Processo e Plano de Ação

> Esta seção é aplicável às origens **Cliente** e **Interno**.

---

## Etapa 1 - Análise de Processo

A equipe de Qualidade realiza a análise técnica da não conformidade:

- Preencha os campos de análise com a causa raiz identificada
- Registre as conclusões técnicas do processo

---

## Etapa 2 - Plano de Ação

Quando necessário, a equipe de Qualidade abre um ou mais **Planos de Ação** utilizando o cadastro padrão de tarefas do Fluig (AdHoc). Cada Plano de Ação é um processo independente criado diretamente pela Central de Tarefas, onde são definidos:

- **Assunto** do plano
- **Responsável** pela execução
- **Prazo** de conclusão
- **Detalhamento** das ações a serem tomadas

Os responsáveis recebem a tarefa em seu painel na Central de Tarefas e devem concluí-la dentro do prazo estabelecido. O acompanhamento dos planos abertos pode ser feito diretamente no formulário da RNC, na seção de Plano de Ação.

---

## Etapa 3 - Verificar Eficácia

Etapa final de verificação realizada pela Qualidade:

- Avalie se as ações corretivas e preventivas foram eficazes
- Preencha os campos de verificação e conclua o processo

---

---

## Apêndice - Tipos de Ocorrência

| Código | Descrição |
|---|---|
| Componente Defeituoso | Componente danificado ou quebrado |
| Estética / Superfície | Defeito de estética, pintura ou avaria |
| Dimensional | Fora do especificado |
| Projeto / Documentação | Erro de projeto ou documentação |
| Identificação | Falha de identificação ou etiqueta |
| Montagem / Solda | Falha de montagem ou solda |
| Material Incorreto | Item ou material incorreto |
| Faltantes | Itens faltantes |
| Vazamento | Hidráulico, ar ou óleo |

---

## Dúvidas frequentes

**Posso salvar e continuar depois?**
Sim. Use o botão **Salvar** para gravar os dados sem movimentar a tarefa.

**O que acontece se eu avançar sem preencher campos obrigatórios?**
O sistema exibirá uma mensagem de erro listando os campos que precisam ser corrigidos.

**Como sei em qual etapa o processo está?**
Acesse o processo pela Central de Tarefas. O campo de atividade atual indica a etapa vigente, e o histórico de movimentações mostra todas as etapas percorridas.

**Quem recebe a tarefa do Plano de Ação?**
O usuário informado no campo **Responsável** de cada linha da tabela de Plano de Ação recebe a tarefa diretamente em sua Central de Tarefas no Fluig.
