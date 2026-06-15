---
title: Manual do Usuário
parent: KANBAN de Movimentação
nav_order: 1
---

# Manual do Usuário - KANBAN de Movimentação

## O que é o processo KANBAN?

O processo **KANBAN de Transferência de Estoque** é utilizado para controlar a movimentação de materiais entre armazéns da Moldemaq por meio de cartões físicos identificados com QR Code. O processo é composto por dois fluxos independentes: o **cadastro do cartão** (que gera e imprime a etiqueta) e a **transferência de estoque** (que movimenta o material no Protheus a partir da leitura do QR Code).

---

## Visão geral dos fluxos

| Fluxo | Função |
|---|---|
| **1 — Cadastro do Cartão** | Registra um novo cartão KANBAN e imprime a etiqueta com QR Code |
| **2 — Transferência de Estoque** | Lê o QR Code do cartão e executa a movimentação no Protheus |

---

---

# Fluxo 1: Cadastro do Cartão KANBAN

Utilizado para criar um novo cartão e gerar sua etiqueta de identificação.

---

## Acesso ao processo

1. Acesse o Fluig e vá até **Processos** e depois em **Iniciar Solicitações**
2. Localize o processo **KANBAN - Cadastro do Cartão**
3. Clique no processo para abrir uma nova solicitação

---

## Etapa 1 - Preenchimento dos dados

**Campos obrigatórios:**

| Campo | Descrição |
|---|---|
| Código do Produto | Selecione via zoom o produto do cartão. A descrição e o endereçamento são preenchidos automaticamente |
| Armazém de Origem | Selecione via zoom o armazém de onde o material sai |
| Armazém de Destino | Selecione via zoom o armazém para onde o material vai |
| Quantidade | Quantidade de itens do cartão (deve ser maior que zero) |
| Kanban | Tipo do cartão: **Transferência** ou **Produção** |
| Ponto de Uso | Selecione via zoom o centro de custo / ponto de uso do material |

**Campos opcionais:**

| Campo | Descrição |
|---|---|
| Endereço no Armazém | Localização física no armazém (até 6 caracteres, ex: B-25) |
| Observação | Informações adicionais sobre o cartão |

> O Armazém de Origem e o Armazém de Destino não podem ser iguais.

---

## Etapa 2 - Impressão da Etiqueta

Após enviar a solicitação, o cartão recebe um número único (ex: **KANBAN-458**) e o formulário exibe o botão **Imprimir Etiqueta**.

1. Clique em **Imprimir Etiqueta**
2. Uma janela com a etiqueta no tamanho 100x50mm será aberta
3. Selecione a impressora **Argox S214 Plus** e confirme a impressão

A etiqueta contém todos os dados do cartão e um **QR Code** que será utilizado no fluxo de transferência.

---

---

# Fluxo 2: Transferência de Estoque

Utilizado para movimentar o material entre os armazéns a partir da leitura do cartão.

---

## Acesso ao processo

1. Acesse o Fluig e vá até **Processos** e depois em **Iniciar Solicitações**
2. Localize o processo **KANBAN - Transferência de Estoque**
3. Clique no processo para abrir uma nova solicitação

---

## Etapa 1 - Leitura do Cartão

Há duas formas de informar o cartão:

**Por leitura do QR Code (recomendado no celular):**

1. Clique no botão **Scan**
2. A câmera do dispositivo será aberta
3. Aponte para o QR Code da etiqueta do cartão
4. Os campos são preenchidos automaticamente

**Por busca manual:**

1. No campo **Cartão KANBAN**, busque pelo número do cartão (ex: KANBAN-458)
2. Selecione o cartão na lista
3. Os campos são preenchidos automaticamente

Após a leitura, confira os dados exibidos (produto, armazéns e quantidade) e clique em **Enviar**.

---

## Etapa 2 - Movimentação no Protheus

Ao enviar, o sistema chama automaticamente a API do Protheus (MATA261) que executa a transferência entre os armazéns informados. Em caso de sucesso, o processo é encerrado e o número do documento gerado fica registrado na solicitação. Em caso de erro, a mensagem de retorno é registrada e a ocorrência é notificada para acompanhamento.

---

---

## Dúvidas frequentes

**O QR Code não está sendo lido pela câmera. O que fazer?**
A leitura por câmera exige conexão segura (HTTPS). Caso a câmera não abra, utilize a busca manual pelo número do cartão.

**O que acontece se o armazém de origem não tiver saldo?**
A API do Protheus rejeita a transferência e exibe a mensagem de erro correspondente. Nenhuma movimentação é realizada.

**Posso reimprimir a etiqueta de um cartão já cadastrado?**
Sim. Acesse a solicitação do cartão pela Central de Tarefas e utilize novamente o botão **Imprimir Etiqueta**.

**O Armazém de Origem e Destino podem ser iguais?**
Não. O sistema bloqueia o cadastro e a transferência caso origem e destino sejam iguais.
