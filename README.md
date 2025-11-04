# Arquitetura Completa de Aplicação Web na AWS

Este projeto apresenta uma arquitetura moderna utilizando **Angular**, **Spring Boot**, **MongoDB** e serviços da **AWS**.

## Componentes

- **Frontend:** Angular hospedado no Amazon S3 com distribuição via CloudFront.
- **Autenticação:** Amazon Cognito para login seguro.
- **API Gateway:** Exposição das APIs com segurança.
- **Load Balancer:** Distribui tráfego para instâncias do backend.
- **Backend:** Spring Boot (Java) rodando em ECS ou EC2.
- **Banco de Dados:** MongoDB (AWS DocumentDB ou Atlas).
- **VPC:** Isolamento e segurança da rede.
- **Monitoramento:** Amazon CloudWatch.

## Fluxo da Arquitetura

1. Usuário acessa a aplicação via navegador.
2. Conteúdo estático (Angular) é servido pelo S3 via CloudFront.
3. API Gateway recebe requisições e encaminha para o Load Balancer.
4. Load Balancer direciona para o backend (Spring Boot).
5. Backend acessa o banco MongoDB.
6. Autenticação é feita via Cognito.

## Diagrama

!Arquitetura

## Benefícios

- **Escalabilidade:** Cada camada pode ser escalada independentemente.
- **Segurança:** Uso de VPC, grupos de segurança e autenticação via Cognito.
- **Alta Disponibilidade:** Serviços gerenciados pela AWS.

---

### Como usar este repositório

1. Clone este repositório.
2. Abra o arquivo `arquitetura.png` para visualizar o diagrama.
3. Leia este README para entender os componentes.
