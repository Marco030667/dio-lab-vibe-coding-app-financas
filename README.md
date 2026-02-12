# 💸 App de Organização de Finanças Pessoais de Marco Donnici com Vibe Coding

## ✨ O que é Vibe Coding

**Vibe Coding** é uma forma leve e criativa de desenvolver com IA, baseada em **conversas naturais e bem estruturadas**. Você não precisa escrever código linha por linha. Em vez disso, aprende a **guiar a IA** descrevendo suas ideias de forma clara, com **intenção e contexto**. Em outras palavras:

> Você mostra a vibe da sua ideia e a IA transforma em solução (ou em um caminho para ela).

## 🎯 Desafio

Problema: Muitas pessoas não conseguem manter um controle financeiro porque os aplicativos exigem muita entrada de dados manual, e a criação de orçamentos é vista como algo tedioso. 

Precisamos de uma solução que permita **controlar as finanças por meio de uma conversa simples**, com **agentes de IA** capazes de criar **planos de economia personalizados e automatizados**. Você deve utilizar as ideias de **Vibe Coding** e **MVP (Produto Mínimo Viável)** para desenvolver o **conceito de um aplicativo** que resolva o problema citado.

## 🪄 Etapas do Desafio

### 1. Saber o que Pedir é a Chave! Otimize seus Prompts!

Antes de pedir para a IA "criar um app", é importante definir com clareza o que você quer construir e por quê. Para isso, você vai criar um **PRD (Product Requirements Document)** simplificado, uma especificação que serve como _briefing_ para a IA entender sua ideia.

Um bom PRD deve descrever o problema, quem será beneficiado, as principais funcionalidades e o que você espera que a IA entregue:

```markdown
# PRD – Aplicativo de Organização de Finanças Pessoais  
**Autor: Marco Donnici**

---

## 1. Contexto
O objetivo é criar um aplicativo de Organização de Finanças Pessoais que funcione por meio de conversas em linguagem natural.  
A proposta é simplificar o controle financeiro, eliminando a necessidade de formulários complexos ou planilhas manuais, tornando a experiência mais fluida e acessível.

---

## 2. Problema
Atualmente, muitos usuários desistem de controlar seus gastos porque:
- Os aplicativos exigem entrada manual excessiva.  
- Há pouca personalização na experiência.  

O aplicativo busca resolver isso oferecendo uma interação conversacional e recomendações automáticas de economia, tornando o processo mais natural e motivador.

---

## 3. Público-Alvo
- Pessoas que desejam iniciar o controle financeiro de forma prática e sem complicações.  
- Usuários iniciantes que não têm familiaridade com planilhas ou ferramentas tradicionais.  
- Indivíduos que valorizam simplicidade, acessibilidade e personalização.  

---

## 4. Requisitos Funcionais
- Registro de gastos via chat em linguagem natural.  
- Classificação automática das transações (alimentação, transporte, lazer etc.).  
- Definição e acompanhamento de metas financeiras (ex.: poupar R$200/mês).  
- Agente Financeiro inteligente que fornece dicas de economia personalizadas.  
- Relatórios simples e personalizados, com visão clara dos gastos.  
- Design Universal, garantindo acessibilidade para diferentes perfis de usuários.  
- Visualização gráfica (estatísticas, comparativos, evolução de metas).  
- Apelo visual moderno, com cores harmoniosas e nuances em 3D.  
- Mensagens destacadas, para rápida percepção de alertas e recomendações.  

---

## 5. Entregável da IA
A IA deve gerar um plano de MVP contendo:
- Principais telas do aplicativo.  
- Recursos essenciais para a primeira versão.  
- Esboço de validação inicial com usuários.  
- Linguagem acessível e educativa, em português.  

---

# Plano de MVP

## Principais Telas
- **Tela de Conversa**: interface principal para registrar gastos e interagir com o Agente Financeiro.  
- **Tela de Metas**: definição e acompanhamento de objetivos financeiros.  
- **Tela de Relatórios**: visão geral dos gastos, gráficos e estatísticas.  
- **Tela de Configurações**: personalização de categorias, alertas e preferências visuais.  

---

## Recursos Essenciais
- Processamento de linguagem natural para registrar gastos.  
- Algoritmo de classificação automática de transações.  
- Sistema de metas financeiras com notificações.  
- Relatórios básicos com gráficos simples.  
- Interface acessível e responsiva (Design Universal).  

---

## Validação Inicial
- Testar com um grupo pequeno de usuários iniciantes.  
- Avaliar clareza da interação via chat.  
- Medir engajamento com as metas financeiras.  
- Coletar feedback sobre usabilidade e visual.  


# Conceitos Didáticos

### Vibe Coding
Abordagem de desenvolvimento que busca criar experiências digitais **humanas e envolventes**, transmitindo uma sensação positiva ao usuário.

### PRD (Product Requirements Document)
Documento que descreve **o que o produto deve fazer**, incluindo contexto, problema, público-alvo e requisitos.  
Serve como guia para o time de desenvolvimento.

### Design Universal
Princípios que garantem que o produto seja **acessível ao maior número possível de pessoas**, independentemente de idade ou limitações.  
Exemplo: contraste adequado, fontes legíveis, navegação simples.

### MVP (Minimum Viable Product)
Primeira versão funcional de um produto, com apenas os recursos essenciais para **validar a ideia com usuários reais**.  
Objetivo: testar hipóteses rapidamente e evoluir com base em feedback.

---

# DIÁLOGO COM A IA Lovable para criação do Aplicativo:

## Histórico Técnico – Problemas e Soluções com a IA Lovable

---

## Problemas Identificados
- **Registro de transações**: gastos e receitas não estavam sendo salvos corretamente.  
- **Layout/Scroll**: chat ocupava toda a tela, escondendo navegação e funções.  
- **Relatórios**: não eram gerados, receitas não acumulavam e saldo não era calculado (apenas mostrava gastos).  
- **Chat**: travado no fim da rolagem, sem acesso ao campo de entrada do usuário.  
- **Metas financeiras**: valores guardados eram somados às receitas em vez de subtraídos do saldo e adicionados às metas.  
- **Gerenciamento de usuário**: não havia opção para alterar senha ou excluir conta.  
- **Warning React**: `AlertDialogFooter` não suportava `ref`.  

---

## Soluções Aplicadas
- **Backend**: ajuste no hook de chat e edge function para salvar transações corretamente.  
- **Layout fixo**: navegação e resumo sempre visíveis; apenas mensagens do chat rolam dentro de container fixo.  
- **Receitas e saldo**: cálculo atualizado para considerar receitas - despesas.  
- **Chat**: correção do auto-scroll para não prender no fim; campo de entrada fixo e sempre visível.  
- **Metas**: introdução de marcador `[GOAL_DEPOSIT]` para registrar depósitos como despesa e atualizar metas.  
- **Configurações**: adicionadas opções de alterar senha e excluir conta (com confirmação e exclusão completa dos dados).  
- **Correção React**: uso de `forwardRef` para eliminar warning no `AlertDialogFooter`.  

---

## Resultado Final
- Aplicativo funcional, com todas as telas fixas e acessíveis.  
- Chat responsivo e integrado ao restante das funções.  
- Cálculo financeiro correto (saldo = receitas - despesas - valores guardados em metas).  
- Gerenciamento de usuário completo (alteração de senha e exclusão de conta).  
- Código limpo, sem erros de rede ou falhas funcionais.  

# APLICATIVO FINAL CARACTERÍSTICAS E APLICABILIDADE

# Acesso Aplicativo "Finança Fácil": https://finance-converser.lovable.app/auth

# Telas Principais

![Tela de Login Chat   Save Finance](https://github.com/user-attachments/assets/5a09a188-ba3f-4adf-8fd9-93e04a31cd44)

![Tela Aplicativo Ativo](https://github.com/user-attachments/assets/f6c46f3f-e462-485f-8e27-b76e104247ef)


- Prints ou pequenos vídeos das interações com a IA;  
- Um resumo do que o seu **App de Finanças Pessoais** faz;  
- Uma breve **reflexão sobre o processo**:
  - O que funcionou bem?  
  - O que não funcionou como o esperado?  
  - O que aprendeu sobre conversar com IAs?

> [!TIP]
> Publique seu repositório e compartilhe o link na plataforma da DIO! Sua entrega é a prova de que você domina o raciocínio de Vibe Coding, mesmo sem escrever uma única linha de código.

## 💬 Conclusão

Vibe Coding é sobre clareza, curiosidade e criatividade, não sobre perfeição técnica. O verdadeiro objetivo aqui é aprender a pensar junto com a IA, transformando ideias em conceitos reais e enxergando a tecnologia como uma extensão do seu raciocínio criativo. Cada interação é um experimento, quanto mais clara for sua intenção, mais surpreendente será o resultado.
