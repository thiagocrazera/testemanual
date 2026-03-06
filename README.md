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

[Bug 01](./evidencias/bug-01-cadastro-sem-validacao.mp4)

**Severidade:** Alto

**Prioridade:** Alta

---

## 2. Cadastro aceita senha que não atende aos requisitos mínimos

**Descrição:**

A interface informa que a senha precisa ter no mínimo **8 caracteres e 1 caractere especial**, porém o sistema permite criar conta utilizando senhas que não atendem a esses critérios.

**Passos para reproduzir:**

1 - Acessar tela "Criar conta"

2 - Preencher os campos obrigatórios

3 - Inserir uma senha inválida (exemplo: 123456)

4 - Confirmar a senha

5 - Clicar em "Criar conta"

**Resultado atual** 

A conta é criada normalmente mesmo utilizando senha que não atende aos requisitos informados na interface.

**Resultado esperado** 

O sistema deve impedir a criação da conta e apresentar mensagem informando que a senha precisa ter no mínimo 8 caracteres e 1 caractere especial.

**Evidência em video:** 

[Bug 02](./evidencias/bug-02-senha-sem-validacao.mp4)

**Severidade:** Alto  
**Prioridade:** Alta
