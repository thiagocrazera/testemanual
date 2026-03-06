# Test Case 4blue
# Teste Técnico – QA Tester – 4blue

## Ambiente de Teste
Sistema testado: https://qa-play-sim.lovable.app/

Navegador utilizado: Google Chrome  
Sistema operacional: Windows  

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

**Severidade:** Alto

**Prioridade:** Alta


