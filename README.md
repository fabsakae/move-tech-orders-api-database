#  Move Tech Orders API - Cloud-Native & DevOps Architecture

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/FastAPI-0.110+-green?style=for-the-badge&logo=fastapi" alt="FastAPI">
  <img src="https://img.shields.io/badge/PostgreSQL-16-orange?style=for-the-badge&logo=postgresql" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Kubernetes-K3s-blueviolet?style=for-the-badge&logo=kubernetes" alt="Kubernetes">
  <img src="https://img.shields.io/badge/Magalu%20Cloud-DBaaS%20%26%20VM-orange?style=for-the-badge" alt="Magalu Cloud">
  <img src="https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-yellow?style=for-the-badge&logo=githubactions" alt="GitHub Actions">
</p>

##  Sobre o Projeto

Este projeto consiste em uma API de gerenciamento de pedidos (*Orders API*) desenvolvida em **FastAPI** e integrada a um banco de dados relacional **PostgreSQL**. A arquitetura foi concebida seguindo os princípios de microsserviços, containerização e práticas modernas de **DevOps e Cloud Computing**, sendo totalmente implantada e orquestrada em um cluster **Kubernetes (K3s)** hospedado na **Magalu Cloud**.

---

##  Arquitetura e Componentes de Infraestrutura

A solução utiliza um ecossistema robusto de infraestrutura em nuvem:

* **Computação e Orquestração:** Máquina Virtual rodando **Ubuntu** com cluster **K3s (Kubernetes)** para gerenciamento de pods em Alta Disponibilidade (High Availability).
* **Banco de Dados (DBaaS):** Instância gerenciada de **PostgreSQL 16** na Magalu Cloud, garantindo persistência desacoplada e segura através de camadas de rede e segredos criptografados.
* **Container Registry:** Hospedagem e versionamento de imagens de contêiner no **Magalu Cloud Container Registry**.
* **Segurança e Gestão de Segredos:** Configuração de `Kubernetes Secrets` isolados e credenciais gerenciadas por variáveis de ambiente injetadas dinamicamente.

---

##  Pipeline de CI/CD (GitHub Actions)

O projeto conta com uma esteira de integração e entrega contínua totalmente automatizada que executa as seguintes etapas a cada alteração no repositório:

1. **Testes e Build:** Validação do código da aplicação.
2. **Autenticação no Registry:** Login automatizado no Container Registry da Magalu Cloud.
3. **Empacotamento:** Construção (*Build*) e envio (*Push*) da imagem Docker otimizada.
4. **Deploy Automatizado:** Configuração do contexto do cluster (`kubectl`), injeção segura de segredos de banco de dados e atualização (*Rollout*) controlada dos pods no Kubernetes.

---

##  Tecnologias Utilizadas

* **Linguagem:** Python 3.11, SQLAlchemy, Pydantic, Uvicorn
* **Banco de Dados:** PostgreSQL 16 (Magalu Cloud DBaaS)
* **Infraestrutura & Cloud:** Magalu Cloud (VMs, Container Registry, PostgreSQL DBaaS)
* **Orquestração:** Kubernetes (K3s), kubectl
* **Automação:** GitHub Actions (CI/CD)
* **Containerização:** Docker

---

