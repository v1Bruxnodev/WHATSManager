# WHATSManager - Automatizador de Envios para WhatsApp

## Envie mensagens personalizadas em massa para seus contatos de forma simples e rápida, diretamente do seu computador.

### O que é?
O **WHATSManager** é uma ferramenta de desktop que automatiza o envio de mensagens pelo WhatsApp. Você pode enviar mensagens de texto simples ou imagens com legenda, personalizando cada mensagem com informações específicas de uma planilha (como nome, cidade, etc.).

### Pré-requisitos
Antes de começar, você precisa ter:
*   O programa `WHATSManager.exe`.
*   **WhatsApp Desktop instalado** no seu computador e com o login já efetuado na sua conta.
*   Uma planilha de contatos no formato `.csv`.

---

## 1. Preparando sua Planilha de Contatos (`.csv`)

Este é o passo mais importante! Para o programa funcionar corretamente, sua planilha **DEVE** seguir estas regras:

*   **Formato:** O arquivo deve ser salvo como **CSV (Separado por vírgulas)**. Ao salvar no Excel, ele pode usar ponto e vírgula (`;`) como separador, o que é **correto para este programa**.

*   **Coluna `"numero"` (Obrigatória):**
    *   Sua planilha **PRECISA** ter uma coluna com o nome exato `numero`.
    *   Os números devem incluir o código do país (DDI) e o DDD, **sem espaços, traços ou o sinal `+`**.
    *   **Exemplo Correto:** `5511999999999` (para um número de São Paulo, Brasil).
    *   **Exemplo Incorreto:** `+55 (11) 99999-9999`.

*   **Colunas de Personalização (Opcionais):**
    *   Você pode adicionar outras colunas para personalizar sua mensagem (ex: `nome`, `cidade`, `produto`, `vencimento`).
    *   Os nomes das colunas não devem ter espaços ou caracteres especiais. Use `nome_cliente` em vez de `Nome do Cliente`.

#### Exemplo de Planilha Válida:
| numero        | nome           | cidade         | produto |
| :------------ | :------------- | :------------- | :------ |
| `5511987654321` | `João Silva`     | `São Paulo`      | `Plano A` |
| `5521123456789` | `Maria Oliveira` | `Rio de Janeiro` | `Plano B` |
| `5531988887777` | `Pedro Costa`    | `Belo Horizonte` | `Plano C` |

---

## 2. Como Usar o Programa (Passo a Passo)

1.  **Abra o WHATSManager:** Dê um duplo clique no arquivo `WHATSManager.exe`.

2.  **Carregue sua Planilha:**
    *   Clique no botão **`Carregar CSV`**.
    *   Selecione o seu arquivo de contatos (`.csv`).
    *   O programa mostrará uma mensagem de sucesso, como: `3 contatos com 4 colunas carregados!`.

3.  **Escreva sua Mensagem:**
    *   No campo "Mensagem / Legenda", digite o texto que deseja enviar.
    *   Para personalizar, use o nome das colunas da sua planilha entre chaves `{}`.
    *   **Exemplo:** `Olá {nome}, tudo bem? Notamos que você é de {cidade} e tem interesse no nosso {produto}.`
    *   O programa substituirá `{nome}`, `{cidade}` e `{produto}` pelos dados de cada linha da sua planilha.

4.  **Escolha o Tipo de Envio:**
    *   **Apenas Texto:** Deixe esta opção marcada para enviar somente a mensagem escrita.
    *   **Imagem com Legenda:** Marque esta opção para enviar uma imagem. O campo para selecionar o arquivo aparecerá. Clique em `Procurar...` para escolher a imagem no seu computador. O texto que você escreveu será enviado como legenda da imagem.

5.  **Inicie o Envio:**
    *   Clique no botão **`Iniciar Envio`**.
    *   Uma nova janela do seu navegador ou do WhatsApp Desktop será aberta.

> **Atenção!**
>
> **NÃO TOQUE NO MOUSE OU TECLADO DURANTE O PROCESSO!**
> O programa irá controlar seu computador para digitar os números, colar a mensagem e enviar. Qualquer interferência pode causar erros.

6.  **Acompanhe o Progresso:**
    *   A caixa de "Log" mostrará em tempo real o que está acontecendo: qual número está sendo processado, se o envio foi um sucesso ou se houve falha.
    *   A barra de progresso indicará o andamento geral dos envios.

7.  **Finalização:**
    *   Ao final de todos os envios, uma mensagem de "Processo Concluído!" aparecerá. Agora você pode voltar a usar seu computador normalmente.

---

## Dicas e Solução de Problemas

*   **"O WhatsApp não abre ou dá erro no início"**: Verifique se o WhatsApp Desktop está instalado, aberto e logado na sua conta antes de iniciar o envio.
*   **"Erro de Placeholder"**: Se você receber este erro, significa que usou uma `{coluna}` na sua mensagem que não existe na sua planilha. Verifique se os nomes batem exatamente.
*   **"O envio falhou para alguns números"**: O log informará quais números falharam. Verifique se eles estão formatados corretamente na sua planilha (DDI + DDD + Número, tudo junto).
*   **"O programa parece lento"**: As pausas entre os envios são propositais. Elas servem para garantir que a página do WhatsApp carregue completamente e para reduzir o risco de sua conta ser bloqueada por atividade excessiva.

---

> **AVISO LEGAL:** O uso de ferramentas de automação para envio em massa pode violar os Termos de Serviço do WhatsApp e resultar no bloqueio da sua conta. Use esta ferramenta com responsabilidade e apenas para se comunicar com contatos que consentiram em receber suas mensagens. Eu não me responsabilizo por qualquer uso indevido ou consequências.

![image](https://github.com/user-attachments/assets/b549d58a-5f65-40ce-85fa-bac9ab4cc506)

