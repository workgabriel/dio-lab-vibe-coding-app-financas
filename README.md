# 💸 App de Organização de Finanças Pessoais com Vibe Coding

---

> Seu **prompt final** (PRD);  

# Documento de Requisitos do Produto (PRD)

**Produto:** WebApp de Finanças - MVP Conversacional Determinístico
**Data:** Março de 2026

## 1. Visão Geral do Produto

Um WebApp de controle financeiro pessoal disfarçado de aplicativo de mensagens. O objetivo é eliminar a fricção dos formulários tradicionais através de um fluxo guiado de perguntas e respostas predefinidas. Não haverá uso de Inteligência Artificial; o sistema seguirá uma árvore de decisão fixa para garantir 100% de previsibilidade, velocidade e baixo custo de infraestrutura.

## 2. Público-Alvo e Problema

* **Público:** Iniciantes em organização financeira que desistem de apps complexos devido à exigência de muita entrada manual em telas cheias de campos.
* **Problema:** A interface padrão de planilhas e formulários gera fadiga.
* **Solução:** Uma interface de chat onde o usuário responde a apenas 3 perguntas sequenciais para registrar qualquer movimentação.

## 3. Escopo Funcional (O Fluxo de Registro)

A principal funcionalidade é o "Loop de Registro". Ao iniciar uma nova transação (clicando em um botão `+`), o sistema assume o controle da conversa e guia o usuário em 3 etapas estritas:

1. **Etapa 1: Nome da Operação (Texto)**
* **Sistema:** *"O que você quer registrar agora?"*
* **Usuário:** Digita em texto livre (ex: "Aluguel", "Mercado", "Salário"). O teclado padrão do celular é exibido.

2. **Etapa 2: Valor (Numérico)**
* **Sistema:** *"Qual foi o valor?"*
* **Usuário:** Digita o número. O teclado numérico é forçado na tela, com máscara automática de moeda (R$ 0,00).

3. **Etapa 3: Tipo e Categoria (Seleção Fechada)**
* **Sistema:** *"Isso é uma Entrada ou Saída? Qual a categoria?"*
* **Usuário:** O teclado de digitação é ocultado. A interface exibe botões rápidos (Quick Replies). Primeiro, seleciona entre [Entrada] (verde) ou [Saída] (vermelha). Em seguida, escolhe a categoria a partir de uma lista pré-definida fechada.

4. **Conclusão:**
* **Sistema:** Gera um "Card de Recibo" na timeline do chat confirmando o registro e exibe o saldo atualizado.

## 4. Detalhamento de Telas (UI/UX)

O design deve ser minimalista, focando exclusivamente na linha do tempo da conversa.

* **Tela Principal (Chat):**
* **Timeline:** Histórico das inserções, formatado como balões de mensagem.
* **Área de Input Variável:** O rodapé da tela deve se adaptar à etapa do fluxo (teclado de texto, teclado numérico ou botões de múltipla escolha).
* **Gerenciamento de Registros (Edição/Exclusão):** Para aplicar melhorias de gerenciamento sem afetar o design limpo da interface de chat, os balões de "Card de Recibo" devem suportar gestos (como um deslize lateral / *swipe*) para revelar opções de renomear, editar o valor ou deletar aquela transação específica.

* **Tela de Dashboard / Relatórios:**
* Um painel acessível via ícone discreto (ex: um gráfico de pizza no topo da tela).
* **Componentes:** * Card de Saldo Geral.
* Gráfico de barras simples comparando Entradas vs. Saídas do mês atual.
* Lista das top 3 categorias com maiores gastos.

## 5. Requisitos Técnicos e Arquitetura de Dados

* **Frontend Leve:** O WebApp deve carregar instantaneamente. Na Etapa 3 (seleção de categorias), para evitar componentes pesados em JavaScript, a interface pode utilizar a tag HTML nativa `<datalist>`. Conectando o atributo `id` da lista ao atributo `list` do campo de entrada, cria-se uma experiência rápida onde o usuário pode selecionar opções predefinidas com excelente performance em navegadores mobile.
* **Estruturação de Dados:** O banco de dados deve funcionar como um catálogo rigorosamente organizado. A lógica do chat serve justamente para extrair os dados da interação do usuário e estruturá-los perfeitamente no backend (data, nome, valor, tipo e categoria). Isso garante que relatórios futuros possam ser extraídos, filtrados ou ordenados alfabeticamente com facilidade.
* **Categorias Fixas:** Para evitar a desorganização comum em usuários iniciantes, o banco de dados das categorias deve ser imutável no MVP (ex: Moradia, Alimentação, Transporte, Saúde, Lazer, Educação, Outros). O usuário não pode criar novas categorias neste momento.

## 6. Métricas de Sucesso (KPIs)

* **Taxa de Conclusão do Fluxo:** Porcentagem de vezes que o usuário inicia a Etapa 1 e chega até o "Card de Recibo" (meta: > 95%).
* **Retenção Semanal:** Quantidade de usuários ativos na Semana 1 que retornam para lançar novos gastos na Semana 2.
* **Tempo Médio de Registro:** Tempo decorrido entre o acionamento do botão `+` e a finalização da Etapa 3 (meta: < 8 segundos).

---


> Prints ou pequenos vídeos das interações com a IA;  



---

> Um resumo do que o seu **App de Finanças Pessoais** faz;  
Um WebApp de controle financeiro pessoal disfarçado de aplicativo de mensagens. O objetivo é eliminar a fricção dos formulários tradicionais através de um fluxo guiado de perguntas e respostas predefinidas. Não haverá uso de Inteligência Artificial; o sistema seguirá uma árvore de decisão fixa para garantir 100% de previsibilidade, velocidade e baixo custo de infraestrutura.

---

> Uma breve **reflexão sobre o processo**:
  - O que funcionou bem?
    - A interface e ux ficou muito boa
  - O que não funcionou como o esperado?  
    - Por ser apenas um mockup, não salva corretamente as informações e não sincroniza online
  - O que aprendeu sobre conversar com IAs?
    - Que IAs são poderosas
