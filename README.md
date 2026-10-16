# 📚 Automação de Cadastro de Tarefas de Estudo com n8n e Gmail

Este projeto foi desenvolvido como parte de um Desafio Criativo da **DIO (Digital Innovation One)** com o objetivo de planejar, validar e executar um fluxo de automação no **n8n** utilizando boas práticas de prompt engineering e estruturação de workflows.

---

## 🎯 Objetivo

Receber dados de tarefas de estudo por meio de um formulário interativo, validar se todos os campos obrigatórios foram preenchidos e enviar uma notificação formatada por e-mail (via Gmail) somente quando os dados estiverem completos.

---

## 🛠️ Ferramentas e Tecnologias

- **n8n:** Orquestração e execução do fluxo de automação.
- **n8n Form Trigger:** Captura dos dados da tarefa via formulário web.
- **n8n If Node:** Lógica condicional e validação dos dados obrigatórios.
- **Gmail (OAuth2 / API):** Envio seguro das notificações por e-mail.

---

## 🔄 Fluxo de Funcionamento

1. **Captura:** O formulário recebe o *Nome da Tarefa*, *Matéria/Curso*, *Prazo* e *E-mail de Destino*.
2. **Validação:** O nó de condição (`If`) verifica se os campos obrigatórios (*Nome*, *Prazo* e *E-mail*) contêm informação (`is not empty`).
3. **Aprovação (`True`):** Se os campos obrigatórios estiverem preenchidos, um e-mail de confirmação é enviado ao destinatário.
4. **Reprovação (`False`):** Se faltar qualquer informação obrigatória, o fluxo é interrompido com segurança sem disparar notificações.

---

## 📁 Como Importar este Workflow no seu n8n

1. Baixe o arquivo `workflow.json` deste repositório.
2. Abra a interface do seu **n8n**.
3. Crie um novo workflow.
4. No menu superior (`...`), clique em **`Import from File`** e selecione o arquivo baixado.
5. Configure suas credenciais de e-mail e ative o workflow!

---

👨‍💻 Desenvolvido por **Mateus Iensen**
