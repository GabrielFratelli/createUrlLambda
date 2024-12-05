# Criar Encurtador de URL

Criar Encurtador de URL é uma função AWS Lambda baseada em Java, projetada para criar e gerenciar URLs curtas. Este projeto é construído usando Maven e é direcionado para o Java 17.

## Visão Geral do Projeto

Esta função Lambda faz parte de um serviço de encurtador de URL. Ela provavelmente cria URLs curtas e as armazena no Amazon S3 para recuperação e redirecionamento posteriores.

## Dependências

O projeto usa as seguintes dependências principais:

- AWS Lambda Java Core (1.2.1)
- AWS Lambda Java Log4j2 (1.4.0)
- AWS SDK for Java v2 - S3 (2.17.106)
- Lombok (1.18.34)
- Jackson Databind (2.12.3)

## Construindo o Projeto

Este projeto usa Maven para gerenciamento de dependências e construção. Para construir o projeto, use o seguinte comando:

```bash
mvn clean package
```

Isso irá compilar o código, executar os testes e criar um arquivo JAR sombreado que inclui todas as dependências, pronto para ser implantado no AWS Lambda.

## Configuração

O arquivo `pom.xml` contém as seguintes configurações principais:

- A compatibilidade da versão do Java é definida para a versão 17.
- A codificação da fonte é definida como UTF-8.
- O plugin Maven Shade é utilizado para criar um uber-JAR com todas as dependências incluídas.

## Implantação

Após construir o projeto, faça a implantação do arquivo JAR gerado para o AWS Lambda. Certifique-se de configurar a função Lambda com o método de manipulador apropriado e configurar quaisquer variáveis de ambiente ou funções IAM necessárias para o acesso ao S3.

## Contribuindo

Contribuições para este projeto são bem-vindas. Por favor, certifique-se de seguir o estilo de código existente e incluir testes apropriados para qualquer nova funcionalidade.