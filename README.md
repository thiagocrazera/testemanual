# Test Case 4blue
# Teste Técnico – QA Tester – 4blue

## Ambiente de Teste
Sistema testado: https://qa-play-sim.lovable.app/

Navegador utilizado: Google Chrome - Versão 145.0.7632.160 (Versão oficial) 64 bits

Sistema operacional: Microsoft Windows 11 Pro

## Metodologia de Teste

Durante a análise do sistema foram aplicadas técnicas de:

- Testes exploratórios
- Testes funcionais
- Testes negativos (validação de campos)
- Avaliação básica de segurança
- Avaliação de experiência do usuário (UX)

---

# Bugs Encontrados

## 1. Cadastro permite envio de campos obrigatórios vazios

**Descrição:**

O sistema permite criar conta mesmo sem preencher os campos obrigatórios.

**Passos para reproduzir:**

1 - Acessar tela "Criar conta"

2 - Deixar campos vazios

3 - Clicar em "Criar conta"

**Resultado atual:**

A conta é criada e o sistema redireciona para a tela de sucesso.

**Resultado esperado:**

O sistema deve impedir o cadastro e apresentar mensagens de validação informando que os campos são obrigatórios.

**Evidência em vídeo:**  

[Ver Video](./evidencias/bug-01-cadastro-sem-validacao.mp4)

**Severidade:** Alto
**Prioridade:** Alta

---

## 2. Cadastro aceita senha que não atende aos requisitos mínimos

**Descrição:**

A interface informa que a senha precisa ter no mínimo **8 caracteres e 1 caractere especial**, porém o sistema permite criar conta utilizando senhas que não atendem a esses critérios.

**Passos para reproduzir:**

1 - Acessar tela "Criar conta"

2 - Preencher os campos obrigatórios

3 - Inserir uma senha inválida (exemplo: 123)

4 - Confirmar a senha

5 - Clicar em "Criar conta"

**Resultado atual** 

A conta é criada normalmente mesmo utilizando senha que não atende aos requisitos informados na interface.

**Resultado esperado** 

O sistema deve impedir a criação da conta e apresentar mensagem informando que a senha precisa ter no mínimo 8 caracteres e 1 caractere especial.

**Evidência em video:** 

[Ver Video](./evidencias/bug-02-senha-sem-validacao.mp4)

**Severidade:** Alto
**Prioridade:** Alta

---

## 3. Campo confirmar senha não valida correspondência com a senha informada

**Descrição:**

O sistema permite criar conta mesmo quando os campos "Senha" e "Confirmar senha" possuem valores diferentes.

**Passos para reproduzir:**

1 - Acessar tela "Criar conta"

2 - Preencher os campos obrigatórios

3 - Informar uma senha no campo "Senha"

4 - Informar um valor diferente no campo "Confirmar senha"

5 - Clicar em "Criar conta"

**Resultado atual**

O sistema aceita o cadastro e cria a conta normalmente.

**Resultado esperado**

O sistema deve impedir o cadastro e apresentar mensagem informando que os campos de senha não coincidem.

**Severidade:** Alto
**Prioridade:** Alta

---

## 4. Campo e-mail aceita formato inválido

**Descrição:**

O campo e-mail aceita valores que não seguem o formato padrão de endereço de e-mail.

**Passos para reproduzir:**

1 - Acessar tela "Criar conta"

2 - Preencher os campos obrigatórios

3 - No campo e-mail inserir valor inválido (exemplo: teste)

4 - Clicar em "Criar conta"

**Resultado atual**

O sistema aceita o valor informado e permite a criação da conta.

**Resultado esperado**

O sistema deve validar o formato do e-mail e impedir o cadastro quando o valor informado não estiver em um formato válido de endereço de e-mail.

**Evidência:** 

[Ver Video](./evidencias/bug-04-email-invalido.mp4)

**Severidade:** Médio
**Prioridade:** Média

---

## 5. Campo telefone aceita caracteres inválidos

**Descrição:**

O campo telefone permite a inserção de letras e caracteres inválidos, quando deveria aceitar apenas números ou validar corretamente o formato de telefone.

**Passos para reproduzir:**

1 - Acessar tela "Criar conta"

2 - Preencher os campos obrigatórios

3 - No campo telefone inserir letras (exemplo: abcdef)

4 - Clicar em "Criar conta"

**Resultado atual**

O sistema aceita o valor informado no campo telefone e permite a criação da conta.

**Resultado esperado**

O sistema deve permitir apenas números no campo telefone ou validar corretamente o formato de telefone.

**Evidência:** 

[Ver Video](./evidencias/bug-05-telefone-aceita-letras.mp4)

**Severidade:** Médio
**Prioridade:** Média

---

## 6. Sistema exibe mensagem de erro após login bem-sucedido

**Descrição:**

Após realizar login com sucesso, o sistema exibe simultaneamente uma mensagem de erro "Erro inesperado", gerando inconsistência de informação para o usuário.

**Passos para reproduzir:**

1 - Criar uma conta no sistema

2 - Realizar login com as credenciais criadas

3 - Aguardar redirecionamento para a tela de sucesso

**Resultado atual**

O sistema apresenta a mensagem "Login realizado com sucesso", porém também exibe uma notificação de erro "Erro inesperado".

**Resultado esperado**

Após login bem-sucedido, o sistema deve exibir apenas a mensagem de sucesso, sem apresentar mensagens de erro.

**Evidência:** 

[Ver Print](./evidencias/bug-06-erro-inesperado-login.png)

**Severidade:** Médio
**Prioridade:** Média

---

## 7. Campos do formulário apresentam quebra de layout

**Descrição:**

Os campos do formulário de cadastro apresentam problemas de layout, ultrapassando os limites do container do formulário e causando desalinhamento visual na interface.

**Passos para reproduzir:**

1 - Acessar tela "Criar conta"

2 - Observar os campos do formulário

3 - Verificar que os campos "Telefone" e "Confirmar senha" ultrapassam os limites do layout

**Resultado atual**

Os campos do formulário ficam desalinhados e ultrapassam o limite visual do container, causando quebra de layout.

**Resultado esperado**

Os campos devem permanecer alinhados dentro do container do formulário, respeitando o layout da interface.

**Evidência:** 

[Ver Print](./evidencias/bug-07-quebra-layout-formulario.png)

**Severidade:** Baixo
**Prioridade:** Baixa