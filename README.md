# API Rest com Spring

Descrição breve do projeto e seus recursos.

## Requisitos

- Java JDK (versão 17)
- Maven 
- PostgreSQL 

## Configuração

1. Clone o repositório:

   ```bash
   git clone [https://github.com/seu-usuario/nome-do-repositorio](https://github.com/freitasDavi/api-spring.git)
   ```
   
2. Configure o banco de dados PostgreSQL:

Crie um banco de dados vazio no PostgreSQL.
Atualize as configurações de conexão com o banco de dados no arquivo application.properties ou application.yml.

3. Execute o projeto:

```bash
mvn spring-boot:run
``` 

4. Uso: 

Autenticação
POST /api/v1/auth/register - Cria um usuário e retorna um token de acesso.
Parâmetros de entrada: 
```batch 
  { 
    "firstname": "Seu nome",
    "lastname": "Sobrenome",
    "email": "seu-usuario", 
    "password": "sua-senha" 
   }
```
Resposta: { "access_token": "seu-access-token", "refresh_token": "seu-refresh-token" }

POST /api/v1/auth/authenticate - Realiza o login e obtém o token de acesso.
Parâmetros de entrada: { "email": "seu-usuario", "password": "sua-senha" }
Resposta: { "access_token": "seu-access-token", "refresh_token": "seu-refresh-token" }

POST /api/v1/auth/refresh-token - Retorna um token de acesso novo
Resposta: { "access_token": "seu-access-token" }

Exemplo de Endpoint
GET /api/v1/demo - Retorna uma mensagem caso autenticado.
Parâmetros de entrada: Nenhum.
Resposta: Mensagem de sucesso caso autenticado, 403 caso não informe o token.

5. Contribuição: 
Se você quiser contribuir com este projeto, siga as etapas abaixo:

Faça um fork do repositório.
Crie uma nova branch com sua feature ou correção de bug: git checkout -b minha-feature
Faça suas alterações e adicione os arquivos modificados: git add .
Faça o commit das suas alterações: git commit -m 'Adiciona minha feature'
Faça o push para o repositório remoto: git push origin minha-feature
Crie um novo pull request no repositório original.
