# Identity Server

É um framework que implementa os protocolos de autenticação OpenID Connect e OAuth 2.0 para ASP.NET Core.

Função: "Oferece controle de acesso para as APIs"

**Características**

- Customização (É possível escrever features para escrever seu próprio SSO).
- Single Sign-on (Apenas 1 autenticação para se  logar com diferntes plataformas).
- Single Sign-out (Logoff integrado de diferentes plataformas ao mesmo tempo).
- Federation Gateway (Processo de login através de um provedor externo. ex.: "Logar com o Google").
- São gerados JWT que retornam `Audience` e `Scopes` (são recursos para validar o usuário).

> Vale a pena?
>
> O Indetity Server 4 necessita de conhecimento técnico avançado, ou seja, inicialmente gasta mais com mão-de-obra para construí-lo e mantê-lo mas ganha-se ser por ser Open Source (diferente de outras opções mais fáceis de implementar mas que tem um custo por requisição).

