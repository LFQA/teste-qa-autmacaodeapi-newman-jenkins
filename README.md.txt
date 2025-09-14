# Projeto de Automação de Testes de API - ServeRest

## Descrição do Projeto
Este projeto demonstra a automação de testes de API usando o Postman e o Newman. O objetivo é garantir a qualidade e a funcionalidade do endpoint `/usuarios` e `login` de uma API REST.

Os testes cobrem cenários de sucesso e de erro, validando respostas, status codes e a estrutura dos dados.

## Tecnologias Utilizadas
* **Postman:** Ferramenta para criação e execução dos testes de API.
* **Newman:** Executor de linha de comando do Postman, utilizado para rodar os testes em ambientes de CI.
* **Jenkins:** Ferramenta de CI/CD para automatizar a execução dos testes.
* **Node.js & npm:** Ambiente de execução para o Newman.

## Como Rodar os Testes
### Localmente
1.  Certifique-se de que o **Node.js** e o **Newman** estão instalados globalmente.
2.  Inicie o servidor da API em `http://localhost:3000`.
3.  Abra o terminal na pasta do projeto e execute o comando:
    ```bash
    newman run "ServeRest - Novo.postman_collection.json" -e "New Environment.postman_environment.json" -r htmlextra
    ```
### Via CI/CD (Jenkins)
A pipeline de testes é definida no arquivo `Jenkinsfile`. O Jenkins executa o `newman` automaticamente a cada nova atualização do código.

## Relatório dos Testes
Os relatórios detalhados dos testes são gerados em HTML e disponibilizados como artefatos na pipeline do Jenkins. Você pode visualizá-los ao final de cada execução.
