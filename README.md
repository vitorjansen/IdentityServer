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

***

### OpenId Connect com IdentityServer4

É uma camada de identidade simples que fica no topo do protocolo OAuth.

A principal diferença entre o OAuth e o OpenId, é que o primeiro tem acesso apenas a um token de acesso para os recursos do cliente no servidor enquanto o segundo além do token de acesso recebe também um Id token (que pode conter mais informções sobre o Resource Owner)

**Implicit Flow**

É um modelo de autorização depreciado, já que é menos seguro uma vez que retorna os token (de acesso e Id) direto na autorização ao invés de retornar através de um endpoint de token específico para isso.

**Authorization Code (Code Flow)**

É o padrão utilizado pois corrige o fluxo do Implicit Flow adicionando mais uma camada de segurança antes de retornar o token. Na prática, o token não é mais enviado junto com a autorização e sim posteriormente em uma endpoint separada.

