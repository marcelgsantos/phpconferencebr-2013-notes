# Palestra

* **Nome:** SOLID: Bom Design em Orientação a Objeto  
* ***Palestrante:*** Mario Rezende
* ***Dia:*** 1

## Anotações


* O que é um bom design em orientação a objetos? Os princípios do SOLID? Onde ele se encaixa? E quais são exemplos de códigos?
* O bom desgin considera mudança de requisitos e gestão de dependências.
* A mudança de requisitos é importante para o negócio.
* A gestão de dependências acontece também a partir da mudança de requisitos. É importante conhecer a forma como os objetos se relacionam ou como uns são dependentes dos outros.
* O desenvolvimento em camadas facilita o gerenciamento de dependências entre os objetos da aplicação.
* Evitar dependências espalhadas é melhor para o gerenciamento de dependências. Isso cria pontos de controle que é bem melhor e evita o acoplamento.
* Um bom design orientado a objeto é ágil para responder a mudanças.
* Os princípios SOLID foram propostos pelo Robert C. Martin (ou Uncle Bob) no seu livro Agile Software Development.
* Os principios SOLID são:
	1. Single Responsibility;
	2. Open/Closed;
	3. Liskov Substitution;
	4. Interface Segreagtion;
	5. Dependency Inversion (não confundir com Dependency Injection);
* Onde o SOLID se encaixa?
	1. Princípios de Orientação a Objetos
		* Abstração
		* Encapsulamento
		* Herança
		* Composição
		* Modularidade
		* Polimorfismo
	2. Princípios de Design de Classe (onde o SOLID se encaixa)
		* Coesão
		* Baixo Acoplamento
		* Ortogonalidade
		* Design por contrato
		* Lei de Demeter
	3. Padrões de Design
		* Solução genérica
		* Problema recorrente
		* Programe por interface
		* Prefira composição
	4. Arquitetura de camadas
		* MVC
		* DDD
		* Framework
	5. Arquitetura Distribuída
		* SOA
		* EBS
		* SaaS
* No **princípio da responsabilidade única** (SRP) uma classe deve ter uma única razão para mudar.
* O SRP é o mais simples, mas é o mais difícil de se fazer certo. E os outros princípios dependem do SRP.
* No **princípio aberto/fechado** (OCP) as entidades, classes e métodos devem ser abertas para extensão e fechadas para modificação.
* O OCP esta no coração do projeto orientado a objetos e traz flexilidade, reutilização e manutenibilidade.
* Recomenda-se não aplicar abstração de forma abusiva no código.
* A utilização de padrões e princípios de projeto traz mais complexidade para o projeto.
* No **princípio de substituição de Liskov** (LSP) descreve a possibilidade de substituir a classe base pela sua derivada.
* É o principal facilitador do OCP.
* Não peça demais, nao prometa de menos.
* "A verdadeira definição de subtipo e ser substituível."
* No **princípio de segregação de interface** (ISP) deve-se quebrar grandes interfaces em interfaces menores e mais específicas.
* Evitar a criação de "fat classes".
* No **princípio de inversão de dependência** (DIP), módulos de alto nível não devem depender módulos de baixo nível, ambos devem depender de abstrações.
* Regras e detalhes devem depender de abstrações, que são definidas do ponto de vista do uso.
* Quando as abstrações e detalhes estão isolados é mais fácil de dar manutenção no código.