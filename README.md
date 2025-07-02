# Level 1 - Assistente de IA Especialista

Este repositório é dedicado ao projeto **Level 1**, uma solução de software que implementa um assistente de IA especialista com base em documentos fornecidos pelo usuário. O sistema utiliza uma arquitetura RAG (Geração Aumentada por Recuperação) mais LLM (Modelos de linguagem de grande escala) para permitir que os usuários "conversem" com seus próprios documentos após realizarem o upload deles via PDFs ou URLs, obtendo respostas melhor contextualizadas e de forma mais dinâmica a partir da própria documentação fornecida. A documentação completa do projeto, incluindo detalhes de arquitetura e guias, pode ser encontrada na [Wiki deste repositório](https://github.com/Marcos-gjr/Level-1/wiki).

##  Funcionalidades Principais

* **Base de Conhecimento Customizável**: Permite que o usuário faça o upload de múltiplos documentos em formato PDF ou insira links de conteúdo web para criar uma base de conhecimento temporária e especializada.
* **Interação Inteligente via Chat**: Oferece uma interface de chat intuitiva, desenvolvida com Streamlit, onde o usuário pode fazer perguntas em linguagem natural e receber respostas rápidas e diretas.
* **Respostas Precisas com RAG**: Garante que todas as respostas sejam estritamente baseadas no conteúdo dos documentos fornecidos, utilizando um pipeline RAG com a API da OpenAI para embeddings e FAISS para busca vetorial, mitigando o risco de informações incorretas.
* **Feedback de Status em Tempo Real**: O sistema informa visualmente ao usuário quando os documentos estão sendo processados, garantindo transparência sobre o que está acontecendo no backend.

##  Stack Tecnológica

O projeto como um todo faz uso das seguintes tecnologias:

<div align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit" />
</div>

### **Backend**
<a href="https://sonarcloud.io/project/overview?id=Marcos-gjr_backend-level-1" target="_blank"><img src="https://img.shields.io/sonar/quality_gate/Marcos-gjr_backend-level-1?server=https%3A%2F%2Fsonarcloud.io&style=for-the-badge&logo=sonarcloud" alt="SonarCloud Quality Gate"/></a>
* **Python**: Linguagem de programação principal, escolhida por sua simplicidade e pelo vasto ecossistema de bibliotecas para IA e desenvolvimento web.
* **Flask & Flask-RESTX**: Frameworks para a construção da API REST, escolhidos pela leveza e pela facilidade de documentação automática com Swagger (OpenAPI).
* **OpenAI API**: Utilizada para gerar os *embeddings* vetoriais (`text-embedding-3-large`) e para a geração final das respostas com o modelo de chat (`gpt-3.5-turbo`).
* **FAISS (Facebook AI Similarity Search)**: Biblioteca para busca de similaridade em vetores de alta dimensão, utilizada como o motor do nosso índice de busca semântica.
* **Pdfplumber & BeautifulSoup**: Bibliotecas para extração de texto de arquivos PDF e de conteúdo HTML de URLs, respectivamente.

### **Frontend**
<a href="https://sonarcloud.io/project/overview?id=Marcos-gjr_backend-level-1" target="_blank"><img src="https://img.shields.io/sonar/quality_gate/Marcos-gjr_frontend-level-1?server=https%3A%2F%2Fsonarcloud.io&style=for-the-badge&logo=sonarcloud" alt="SonarCloud Quality Gate"/></a>
  
* **Python com Streamlit**: Framework open-source para a criação rápida de interfaces web interativas e data apps, utilizado para construir a interface de chat.

### **Infraestrutura e Deploy**
<img src="https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" alt="AWS" />

* **AWS (Amazon Web Services)**: Plataforma de nuvem utilizada para o deploy e hospedagem das aplicações de backend e frontend através do serviço **Elastic Beanstalk**.

##  Ferramentas de Desenvolvimento
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit" />
</div>

* **GitHub Actions (CI/CD)**: Ferramenta de automação para criar os pipelines de Integração Contínua (CI) e Entrega Contínua (CD), automatizando o deploy na AWS.
* **SonarCloud**: Plataforma de análise estática de código para identificar vulnerabilidades e manter a qualidade do código nos repositórios.
* **Pytest**: Framework para a escrita e execução de testes unitários e de integração em Python, utilizado em ambos os projetos.

##  Links

* **Documentação do Projeto:**
    * [Wiki](https://github.com/Marcos-gjr/Level-1/wiki) - Guias detalhados, arquitetura e documentação completa.
    <!-- * [Documentação da API (Swagger UI)](http://<seu-link-do-backend-na-aws>/docs) - Interface interativa para testar os endpoints da API. -->
* **Repositórios:**
    * [Backend](https://github.com/Marcos-gjr/backend-level-1) - Repositório do código da API em Flask.
    * [Frontend](https://github.com/Marcos-gjr/frontend-level-1) - Repositório do código da interface em Streamlit.
* **Monitoramento da Qualidade:**
    * [SonarCloud - Backend](https://sonarcloud.io/project/overview?id=Marcos-gjr_backend-level-1) - Análise de qualidade do código do backend.
    * [SonarCloud - Frontend](https://sonarcloud.io/project/overview?id=Marcos-gjr_frontend-level-1) - Análise de qualidade do código do frontend.
 
##  Licença

Este projeto está licenciado sob a [Licença MIT](https://github.com/Marcos-gjr/Level-1/blob/main/LICENSE).

