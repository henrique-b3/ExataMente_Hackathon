# ExataMente_Hackathon - Accenture Hackathon 2026
<div align="center">
  <img src="src/img/logo.png" alt="ExataMente Logo" width="200"/>
  <h1>ExataMente (TutorMathIA)</h1>
  <p><strong>Solução de Orquestração Multi-Agente para Raciocínio Lógico e Tutoria Matemática</strong></p>
  <p><em>Desenvolvido durante o Hackathon da Accenture Portugal (Coimbra)</em> 🚀</p>
</div>

---

## 📌 O Problema
[cite_start]Atualmente, as Large Language Models (LLMs) enfrentam barreiras críticas ao lidar com lógica matemática rigorosa[cite: 246]. Identificamos quatro falhas estruturais:
* [cite_start]**Alucinações Matemáticas:** A geração de dados factualmente incorretos apresentados como verdades absolutas[cite: 247].
* [cite_start]**Saltos Lógicos (Omissão de Etapas):** A IA ignora o processo intermediário, dificultando a validação humana e a auditoria do resultado[cite: 248].
* [cite_start]**Inabilidade de Resolução Complexa:** Dificuldade em manter a coerência em problemas que exigem múltiplos passos interdependentes[cite: 249].
* [cite_start]**Saídas de Resultado Único:** A entrega direta do resultado final sem a explicação do "porquê", limitando o valor educativo e profissional[cite: 250].

## 💡 A Nossa Solução
[cite_start]O **ExataMente** não é apenas "outra IA", mas sim um **Ecossistema Especializado**[cite: 254]. 
[cite_start]Implementamos uma arquitetura onde as tarefas são divididas e validadas por agentes distintos[cite: 255]. [cite_start]O raciocínio é decomposto, forçando a IA a "pensar em voz alta" [cite: 258][cite_start], o que garante uma redução drástica de alucinações (fiabilidade operacional) [cite: 264] [cite_start]e proporciona total transparência pedagógica[cite: 266].

---

## 🏗️ Arquitetura do Sistema e Workflow dos Agentes

[cite_start]O projeto utiliza um fluxo de orquestração com múltiplos agentes especializados[cite: 257]:

1. [cite_start]🚪 **Orquestrador (Gestor de Infraestrutura):** Atua como a "gateway" ou porta de entrada principal de todo o ecossistema[cite: 209]. [cite_start]Recebe as solicitações do utilizador (texto ou imagem/OCR) [cite: 210] [cite_start]e faz a triagem inicial e encaminhamento[cite: 211, 212].
2. [cite_start]🧠 **Professor (O Explicador Autêntico):** É o agente com interface direta para o utilizador, desenhado para ser didático[cite: 216]. [cite_start]Identifica a natureza da equação [cite: 217] [cite_start]e coordena os especialistas específicos necessários para resolver cada parte do problema[cite: 218].
3. [cite_start]📚 **Especialistas de Domínio (Base de Conhecimento):** Módulos focados em áreas como Integração, Álgebra e Trigonometria[cite: 222, 227, 232]. [cite_start]Eles consultam identidades, regras e tabelas fornecidas nos nossos documentos base para embasar tecnicamente a resposta[cite: 224, 229, 234].
4. 🧮 **Calculadora (Motor Simbólico):** Blinda o sistema contra erros de cálculo da IA, delegando a resolução exata à biblioteca Python `SymPy`.
5. [cite_start]👨‍🏫 **Tutor (Síntese Pedagógica):** Elabora uma solução passo a passo, explicando cada conceito aplicado de forma clara e motivadora para o utilizador[cite: 219].

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python 3.x
* **Orquestração e IA:** LangChain / Google Gemini Generative AI (`gemini-2.5-flash`)
* **Motor Matemático:** SymPy (Resolução matemática exata)
* **Gestão de Conhecimento (RAG Local):** Parsing de ficheiros Markdown e extração estruturada (JSON) para consulta rígida a `.pdf` e `.md` de suporte.

## 🏆 Contexto do Hackathon
[cite_start]Este projeto foi desenvolvido de raiz por uma **equipa de 4 pessoas** e submetido ao abrigo da categoria *Bring Your Own Use Case* [cite: 196] no **Hackathon da Accenture Portugal em Coimbra**. [cite_start]A arquitetura cumpre rigorosamente os critérios exigidos pelo regulamento[cite: 197]:
* [cite_start]✅ **Abordagem baseada em Agentes:** Utiliza mais de 2 agentes de IA com responsabilidades distintas[cite: 198].
* [cite_start]✅ **Viável em 6 horas:** O *core flow* foi construído e tornado demonstrável dentro do evento[cite: 198].
* [cite_start]✅ **Ferramentas Gratuitas / Open Source:** Todos os *frameworks* (LangChain, SymPy) e APIs (Gemini em Free Tier) são gratuitos[cite: 198].
* [cite_start]✅ **Sem dados confidenciais:** Toda a informação provém de bases de conhecimento públicas (tabelas e identidades matemáticas)[cite: 198].

## 🚀 Como Configurar e Executar

1. **Instalar as Dependências**
   Recomenda-se a criação de um ambiente virtual (Virtualenv).
   ```bash
   pip install sympy langchain-google-genai
