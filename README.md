# Gerador_de_Curriculos_ATS_Friendly
App web para matchmaking de vagas de emprego e geração de currículos otimizados para sistemas ATS utilizando Lovable.

# 📄 MatchCV

> Link de Acesso: https://job-fit-resume-studio.lovable.app

> **Aumente suas chances de entrevista otimizando seu currículo para os robôs recrutadores (Sistemas ATS).**

## 💡 Sobre o Projeto
O **MatchCV** é um aplicativo web focado em ajudar candidatos a superarem os filtros automatizados de currículos (Applicant Tracking Systems). A ferramenta permite que o usuário compare seu currículo base com a descrição de uma vaga específica, receba uma análise de compatibilidade (Match) e gere automaticamente uma versão do currículo formatada em texto simples (ATS-Friendly), pronta para ser lida por qualquer sistema de recrutamento.

Este MVP foi inicialmente idealizado e prototipado utilizando [Lovable](https://lovable.dev/).

## ✨ Funcionalidades (MVP)
- **📊 Dashboard Interativo:** Visão geral das vagas analisadas e histórico de aplicações com a porcentagem de match.
<img width="1873" height="898" alt="image" src="https://github.com/user-attachments/assets/d88a6380-37b9-4172-a414-6b101da52b28" />

- **👤 Perfil Base:** Formulário para inserção e armazenamento local dos dados do usuário (Experiência, Formação e Habilidades).
<img width="1852" height="896" alt="image" src="https://github.com/user-attachments/assets/a0e0ea06-91e6-450b-9f7b-d24c02367f5b" />
<img width="1825" height="892" alt="image" src="https://github.com/user-attachments/assets/225b36ab-686a-49e4-8d93-25f697e2ae79" />

- **🎯 Análise de Matchmaking:** Comparação de palavras-chave entre o currículo do usuário e a descrição da vaga.
<img width="1787" height="905" alt="image" src="https://github.com/user-attachments/assets/844cfd43-ee50-44e3-95f8-aae9c79efee6" />

- **✨ Gerador de Currículo ATS-Friendly:** Transformação do currículo visual em um formato linear, sem tabelas ou colunas, 100% otimizado para leitura de software.
<img width="1835" height="897" alt="image" src="https://github.com/user-attachments/assets/e6d8dd31-3ee2-448f-a533-7835966cc331" />

- **📥 Exportação Rápida:** Cópia direta para a área de transferência ou download em formato `.txt` e `.pdf`

## 🛠️ Tecnologias Utilizadas
O projeto foi construído com foco em performance, acessibilidade e design limpo (estilo SaaS):
- **Frontend:** React (Hooks: `useState`, `useEffect`)
- **Estilização:** Tailwind CSS
- **Design System & Componentes:** [shadcn/ui](https://ui.shadcn.com/)
- **Ícones:** Lucide React

## 🎨 Design System
A interface foi projetada para ser minimalista e profissional, focada na legibilidade:
- **Cor Fundo:** Branco (`#FFFFFF`) para clareza e contraste.
- **Cor Primária:** Azul Claro (Trazendo confiança e profissionalismo).
- **Cor de Destaque:** Amarelo Claro (Para alertas, avisos e feedback sem ser agressivo).

## 🚀 Prompts Utilizados

> Megaprompt

Contexto do Projeto
Crie um aplicativo web completo do zero focado em Matchmaking de Vagas de Emprego e Otimização de Currículos para ATS (Applicant Tracking System). O objetivo da ferramenta é permitir que o usuário insira seu currículo base, cole a descrição de uma vaga desejada e receba uma análise de compatibilidade (match), além de uma versão do seu currículo totalmente otimizada e formatada para passar em filtros ATS.

Design System & UI/UX
Design System: Utilize exclusivamente os componentes do shadcn/ui para formulários, botões, modais, cards, tabelas, alertas e navegação.
Ícones: Utilize a biblioteca Lucide React.
Estilo Geral: O design deve ser limpo, profissional, moderno e minimalista (estilo SaaS).
Paleta de Cores:
Fundo Principal: Branco (#FFFFFF).
Cor Primária: Azul Claro (tons como bg-blue-100, text-blue-600, bg-blue-500 para botões primários).
Cor Secundária/Destaques: Amarelo Claro (tons como bg-yellow-50 para alertas, bg-yellow-200 para tags ou avisos de atenção).
Texto: Cinza escuro/Chumbo para garantir alta legibilidade e contraste no fundo branco.
Funcionalidades Principais (Páginas e Componentes)
1. Dashboard (Página Inicial)
Um header simples com o logo/nome do app e navegação.
Um painel com estatísticas simuladas (ex: "Vagas analisadas", "Média de Match", "Currículos Otimizados").
Um botão de Call to Action (CTA) principal em azul: "Nova Análise de Vaga".
Uma lista/tabela (usando shadcn Table ou Cards) mostrando o "Histórico de Aplicações" com o cargo, empresa, data e a % de match obtida.
2. Perfil / Currículo Base
Um formulário completo (usando shadcn Forms, Inputs e Textareas) onde o usuário pode preencher ou colar seu currículo original (Dados Pessoais, Experiência Profissional, Formação Acadêmica e Habilidades).
Opção de salvar essas informações usando o estado local (React state) para serem usadas como base nas próximas análises.
3. Fluxo de Matchmaking e Otimização (Core App)
Esta deve ser a tela principal de interação, dividida nos seguintes passos (pode usar um componente de Tabs ou um Stepper vertical/horizontal):

Passo 1: Inserir a Vaga. Um campo de texto grande (Textarea) para colar a descrição completa da vaga de emprego, acompanhado de campos para "Nome da Empresa" e "Cargo".
Passo 2: Análise e Match. Ao clicar em "Analisar Compatibilidade", mostre um estado de carregamento bonito (Skeleton ou Spinner do shadcn). Depois, exiba um Card de Resultado mostrando a Porcentagem de Match (ex: 75%), listando "Palavras-chave encontradas no seu currículo" e "Palavras-chave faltando".
Passo 3: Gerador ATS-Friendly. Um botão "Gerar Currículo Otimizado". Ao clicar, simule a geração de um currículo text-based (sem colunas complexas, fontes estilizadas ou gráficos, focando 100% no padrão texto que os sistemas ATS conseguem ler).
Passo 4: Visualização e Exportação. Mostre o currículo otimizado gerado em um bloco de texto formatado (pre-wrap). Inclua um botão "Copiar para a Área de Transferência" e um botão "Baixar como .txt".
Requisitos Técnicos e de Código
Implemente toda a lógica de estado usando React Hooks (useState, useEffect).
Como o app será 100% no Lovable (frontend puro neste momento), crie dados mockados (simulados) altamente realistas para demonstrar a lógica de match e a geração do currículo otimizado caso o usuário interaja com a ferramenta.
Garanta que o layout seja totalmente responsivo (Mobile-first usando as classes do Tailwind CSS).
Mantenha a interface amigável, com tooltips (shadcn/Tooltip) explicando o que é o ATS para leigos, e use Toast notifications (shadcn/Toast) para dar feedback de ações (ex: "Currículo salvo", "Texto copiado").
Gere o código completo para criar esta experiência interativa e funcional.

> Segundo Prompt

quero adicionar uma funcionalidade de exportação do currículo em formato pdf
