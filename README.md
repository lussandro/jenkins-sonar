# jenkins-sonar

Este é um ambiente para CI e QA com docker.

## Ambiente:

Você precisa ter o docker na ultima versão e o docker-composer instalados em seu PC, independente do sistema Operacional (Linux, Windows ou MAC-OS)

## Começando
    Basta Clonar o projeto, entrar na pasta e digitar o seguinte comando:
    `docker-compose up . `
    Inicia o Jenkins na porta 8080 e o SonarQube na porta 9000. O SonarQube irá salvar os dados em um container PostgreSQL, criado exclusivamente para esta finalidade.
    Requer a instalação do Maven, Java e SonarQube Scanner no Jenkins. Para habilitar o SonarQube Scanner, consulte https://docs.sonarqube.org/display/SCAN/Analyzing+with+SonarQube+Scanner+for+Jenkins .
    Para um projeto maven no Jenkins, em Build options, defina os seguintes objetivos do maven clean test install $SONAR_MAVEN_GOAL -Dsonar.host.url=http://sonarqube:9000. Ele executará os testes e fará uma análise de código com o SonarQube. Depois veja no SonarQube o resultado da análise.