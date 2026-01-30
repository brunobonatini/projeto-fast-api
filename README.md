# Etapas de Desenvolvimento do Projeto

Este projeto será desenvolvido de forma incremental, partindo do zero até a preparação para um ambiente de produção. Cada etapa foi pensada para consolidar fundamentos importantes do desenvolvimento backend moderno com Python e FastAPI, aplicando boas práticas amplamente utilizadas no mercado.

# Configuração do Ambiente e Gerenciamento do Projeto Python

A primeira etapa do projeto consiste na configuração completa do ambiente de desenvolvimento, estabelecendo uma base sólida para todo o restante da aplicação.

Serão definidos e configurados:

    Um ambiente Python isolado, garantindo reprodutibilidade

    Um gerenciador de dependências e projetos, facilitando o controle das bibliotecas utilizadas

    Um task manager para padronizar e automatizar tarefas recorrentes

    Ferramentas de análise estática de código, visando qualidade e prevenção de erros

    Ferramentas de formatação automática, garantindo consistência no estilo do código

Essa etapa tem como objetivo aplicar boas práticas desde o início do projeto, evitando problemas comuns de organização, dependências e padronização à medida que o sistema cresce.

# Primeiros Passos com FastAPI

Com o ambiente configurado, iniciaremos o desenvolvimento da aplicação utilizando FastAPI, introduzindo os principais conceitos do desenvolvimento web com o framework.

Nesta fase, abordaremos:

    Criação da aplicação FastAPI

    Definição de endpoints e rotas

    Implementação das operações CRUD (Create, Read, Update e Delete)

    Uso de injeção de dependência para desacoplamento e reutilização de código

    Criação de schemas para validação e serialização de dados

    Organização inicial da estrutura do projeto

Essa etapa estabelece os fundamentos necessários para evoluir a aplicação de forma estruturada e escalável.

# Autenticação e Autorização em FastAPI

Com a base da aplicação pronta, será implementado um sistema completo de autenticação e autorização, garantindo segurança no acesso aos recursos.

Serão abordados:

    Criação de fluxo de cadastro e autenticação de usuários

    Proteção de rotas sensíveis

    Controle de acesso baseado em autenticação

    Validação de credenciais e gerenciamento de sessão/token

    Boas práticas de segurança em APIs REST

Essa etapa é fundamental para tornar o sistema utilizável em cenários reais, onde controle de acesso é indispensável.

# Foco em Testes e Qualidade de Código

Nesta fase, o projeto passa a ter foco em qualidade, confiabilidade e manutenibilidade.

Serão introduzidos:

    Conceitos de desenvolvimento orientado a testes (TDD)

    Criação de testes automatizados com pytest

    Medição de cobertura de testes utilizando coverage

    Estruturação de testes para APIs FastAPI

    Configuração de um pipeline de Integração Contínua (CI) com GitHub Actions

O objetivo é garantir que novas funcionalidades não quebrem comportamentos existentes e que o código mantenha um padrão de qualidade consistente.

# Conteinerização e Deploy da Aplicação FastAPI

Por fim, a aplicação será preparada para um ambiente de produção.

Nesta etapa, aprenderemos:

    Criação de um container Docker para a aplicação

    Configuração do ambiente de execução

    Boas práticas para imagens Docker em aplicações Python

    Processo de deploy da aplicação utilizando Fly.io

    Considerações básicas sobre ambientes produtivos

Essa etapa finaliza o ciclo de desenvolvimento, levando a aplicação do ambiente local até a publicação em produção.

# Ambiente de Desenvolvimento

O ambiente de desenvolvimento deste projeto foi configurado com ferramentas amplamente utilizadas no ecossistema Python e no desenvolvimento de aplicações modernas, garantindo produtividade, padronização e facilidade de colaboração.

## Editor de Código – VS Code

O Visual Studio Code (VS Code) foi escolhido como editor de código principal devido à sua leveza, extensibilidade e excelente suporte ao desenvolvimento em Python.

## Terminal

O terminal é utilizado para executar comandos de:

    Gerenciamento de dependências

    Execução da aplicação

    Execução de testes automatizados

    Versionamento de código

    Conteinerização e deploy

## Python 3.10+

O projeto utiliza Python 3.12.10 ou superior, aproveitando recursos modernos da linguagem, como:

    Tipagem mais expressiva

    Melhorias em desempenho

    Compatibilidade com versões atuais das bibliotecas utilizadas no ecossistema FastAPI

## Git

O Git é utilizado para controle de versão do código-fonte, permitindo:

    Histórico claro de alterações

    Trabalho incremental e organizado

    Facilidade de colaboração

    Integração com pipelines de CI/CD

## Docker

O Docker é utilizado para padronizar o ambiente de execução da aplicação, garantindo que o sistema funcione da mesma forma em diferentes máquinas e ambientes.

## GitHub CLI (gh)

A GitHub CLI (gh) é utilizada para facilitar a interação com o GitHub diretamente pelo terminal.

## Gerenciamento de Ferramentas com pipx

Para o gerenciamento de ferramentas globais em Python, este projeto utiliza o pipx. Essa ferramenta permite instalar e executar aplicações Python em ambientes isolados, evitando conflitos entre dependências globais e projetos específicos.

### O que é o pipx?

O pipx é uma ferramenta projetada para instalar aplicações Python de linha de comando em ambientes virtuais isolados, garantindo:

    Isolamento de dependências

    Ambiente global limpo e organizado

    Facilidade na instalação e atualização de ferramentas

    Redução de conflitos entre versões de bibliotecas

# Histórico de Comandos Executados (Setup do Ambiente)

Esta seção documenta, em ordem cronológica, os comandos utilizados para configurar o ambiente de desenvolvimento do projeto.
Todos os comandos devem ser executados no Terminal (Windows) como administrador, ou em outro Shell no Linux.

- Instalação do pyenv-win

Invoke-WebRequest -UseBasicParsing `
  -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" `
  -OutFile "./install-pyenv-win.ps1"

&"./install-pyenv-win.ps1"

Validação:
pyenv --version


- Instalação da versão do Python do projeto
pyenv install 3.12.10

- Definição da versão do Python no projeto
pyenv local 3.12.10

Validação:
python --version


- Instalação do pipx (gerenciamento de ferramentas globais)
py -m pip install --user pipx

- Configuração do PATH para o pipx
py -m pipx ensurepath

Validação da instalação
pipx --version


- Instalação do Poetry via pipx
pipx install poetry

- Instalação da extensão para habilitar o shell do Poetry
poetry self add poetry-plugin-shell

Validação:
poetry --version


- Criação do projeto com Poetry
poetry new nome-do-projeto

- Acesso ao diretório do projeto
cd nome-do-pojeto

- Criando o ambiente virtual
poetry install 

- Instalando o FastAPI
poetry add fastapi
