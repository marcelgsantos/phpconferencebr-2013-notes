# Palestra

* **Nome:** De um a um milhão de usuários - o caminho para a escalabilidade
* ***Palestrante:*** Felipe Ribeiro
* **Dia**: 2

## Anotações

* O que não é escalabilidade?
	1. não é performance
	2. não é arquitetura de hardware
	3. não é linguagem de programação
* O que é escalabilidade?
	* é a capacidade de suportar o aumento de carga sem degradar a performance
* A web é um dos mercados com menor barreira de entrada.
* Problemas de escalabilidade são problemas bons.
* Dinheiro resolve alguns problemas de escalabilidade (ou é necessário repensar a arquitetura).
* Hospedagem compartilhada
	* Prós
		1. comodidade
		2. "one-click" install 
		3. baixo custo de operação 
		4. arquitetura simples
		5. desenvolvimento rápido
	* Contras
		1. todos os recursos são compartilhados
		2. performance é afetada por outros sites
		3. suporta algumas (poucas) centenas de usuários
		4. sem redundância
* VPS ou Cloud (ambientes virtualizados) ainda compartilham alguns recursos como processador e I/O.
* Se a arquitetura não foi pensada para escalar, tudo o que pode ser feito é criar uma instância com maior capacidade (escalar verticalmente).
* Repensar a arquitetura:
	1. Separar servidor web do servidor de banco de dados; 
		* se houver poucos usuários fica lento por causa da latência de rede
		* pode-se utilizar mais servidores para base de dados;
	2. Adicionar um processador com cache para base de dados (memcached ou Redis);
		* cache key-value é mais rápido que consulta SQL
		* memória é mais rápido do que disco 
		* LRU - Least Recently Used (política de cache mais utilizada, o mais antigo é limpo para liberar espaço)
		* lembrar-se de invalidar o cache na escrita
		* cache negativo - informar coisas inexistentes como página de erro
	3. SPOF (Single Point Of Failure) - se determinado ponto falha, a aplicação para de funcionar;
		* dois pontos de falhas óbvios são servidor web e o servidor de banco de dados, pois se algum falha, a aplicação pode não funcionar normalmente
		* É importante analisar e remover pontos únicos de falha
		* Utilizar mais servidores web para evitar SPOF
	4. Utilizar Shared-Nothing Architecture
	5. Se você não guarda estado no servidor, é fácil substituir um servidor web que falha;
		* Gerenciamento de sessão precisa mudar (memcached, Redis ou banco de dados)
	6. O SPOF passa a ser o DNS;
		* para isso, adiciona-se o balanceador de carga (pega o request e distribui para as máquinas);
		* Exemplos de Load Balancer: HAProxy, nginx e AWS Elastic Load Balancer
	7. Remover o SPOF do banco de dados;
		* pode-se utilizar replicação ou sharding com bancos de dados relacionais que suportam estas tecnologias ou bancos de dados NoSQL;
		* Sharding: particionamento horizontal (a aplicação deve saber qual sharding os dados devem estar);
	8. Escalar o cache para evitar carga para a base de dados no caso de queda do cache;
		* Consistent hashing;
	9. Utilizar CDN é importante pois é mais rápido para o usuário e diminui muito o tráfego na rede;
	10. Arquitetura orientada a serviços - a camada web pode falar com serviços que cuidam do back-end;
	11. Utilizar a ferramenta certa para o problema certo;
	 	* Busca textual usando Solr ou ElasticSearch;
	 	* Cache usando o memcached ou Redis;
	 	* É fácil escalar sites onde o usuário não gera conteúdo, mas caso contrário, as ações precisam ser enfileiradas.
	 		* Gearman
	 		* RabbitMQ
	 		* Redis
	 		* Amazon Simple Queue Service
	 	* Ser rápido ou parecer rápido? O usuário envia conteúdo e quer vê-lo imediatamente na página (utilizar truque para parecer rápido).
	12. Infra-estrutura própria;
		* quando você chega a uma escala de centenas ou milhares de servidores, você vai poder bancar sua própria infra-estrutura;
		* Maior controle (hardware próprio, sem interferência externa); 
		* Maior responsabilidade;
	13. Escalabilidade promove mudança na cultura de trabalho;
		* Equipes mais independentes usando as stacks apropriadas para suas features;
		* Meça primeiro, mude depois.
		* "Premature optimization is the root of all evil" - D. Knuth
		* Quando se tem uma infra-estrutura grande, deve-se fazer o monitoramento;
		* É difícil fazer o deploy para uma infra-estutura grande;