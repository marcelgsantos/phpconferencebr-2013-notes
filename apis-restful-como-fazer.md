# Palestra

* **Nome:** API's ReST(Ful): Como fazer
* ***Palestrante:*** Alex Piaz
* **Dia**: 1

## Anotações

* ReST (Representational State Transfer) é um estilo arquitetural baseado nos limites que o protocolo HTTP nos impõe (RFC 2616).
* Características principais do PHP:
	1. Cliente/servidor (separação de interesses);
	2. Interface uniforme (ambiente comum para saber como as coisas funcionam);
	3. Camadas (várias camadas entre a requisição e a resposta);
	4. Stateless (sem estado, ou seja, uma requisição deve conter todas as informações para o servidor processar a requisição; o servidor não vai reconhecer as requisições feitas anteriormente);
	5. Cache (provedor da informação deve informar sobre o tempo que o recurso deve ser válido);
* Quais são as restrições do ReST?
	1. Tem que ser cliente/servidor;
	2. Tem que ter interface uniforme;
	3. Você pode informar seu cliente que se pode fazer cache;
	4. Stateless;
	5. Camadas;
	6. Código sobre demanda;
* Código sobre demanda é um código que o cliente sabe como utilizar;
* A interface uniforme trata de verbos HTTP e URL (PUT criar ou atualizar um recurso e o HEAD pode enviar informacoes de cabecalho tais como o tamanho de um do* cumento ou meta informacoes, OPTIONS pede as opcoes XML, JSON, HTML). 
* Media types.
* Mensagens auto-descritivas: cabeçalho e código de status HTTP.
* COdigo
* 101 - Informativo; 2xx - sucesso; 3xx - redirecionamento; 4xx - erro do cliente; 5xx - erro do servidor;
* HATEOAS para aplicacao restful e navegacao dos recursos.
* Richardson Maturity Model criou benchmark das APIs:
	1. Level 0 - The Swamp of POX (sem nenhum organização, utilizando RPC)
	2. Level 1 - Resources
	3. Level 2 - HTTP Verbs (utlizacao de verbos HTTP)
	4. Level 3 - Hypermedia Controls (utilizacao de hipermidia)
* Dica 0 - ferramentas basicas (Silex, Slim, ZF, Symfony2)
* Dica 1 - HTTPS é de utilização obrigatória;
* Dica 2 - Elementos chaves 
	1. API endpoint
	2. Manipulacao via revcurso;
	3. verbos HTTP;
* Dica 3 - URL:
* site.com/ufo-api/v1/casos/1
* NS / V / C /D
* Napespace ou endpoint, a barra indica hierarquia.
* ufo-api.site.com
* URL controller no rest - acao /v1/distancia/calcular?params
* Recurso e uma coisa, e coisa e substantivo
* Geralmente tem 2 urls por recursos (recursos arquetipos - um para colecao e outro para documento casos e casos/1)
* 4. Versões de APIs:
	1. Opção 1: {v}/casos/1 (na hierarquia, muito utilizado mas recusado por puristas)
	2. Opção 2: casos/1?v={v} (via string de consulta)
	3. Opção 3: X-API-Version: {v} (via cabeçalhos HTTP)
* 5. Media types: é o cliente quem diz o que ele quer receber
	Request ()
	Accept: application/json;q=1,text/xml;q=0,8
	Response ()
	Content-type: application/json
* Manipulando uma representacao dos recursos.
* dica 6. cache;
* Dica 7 - Autenticação;
	1. Basic Auth (simples e insegura);
	2. Digest Auth (um pouco mais avancada)
	3. OAuth 2;
* Dica 8 - documentacao; swagger a apiary