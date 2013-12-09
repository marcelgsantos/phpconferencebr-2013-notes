# Palestra

* **Nome:** Refatorando Códigos PHP  
* ***Palestrante:*** Levi Ferreira
* ***Dia:*** 1

## Anotações

* Refatoração é um **processo** para **aperfeiçoar** o código fonte **sem alterar a funcionalidade da aplicação**;
* Por que é necessário fazer refatoração?
	1. Porque todos os softwares estão sujeitos a mudanças para aperfeiçoamento e melhorias;
    2. Por que muitos não sabem OO;
    3. Porque o raciocínio é estático;
    4. Utilizar linguagem nova com hábitos antigos;
* O que a refatoração traz de benefícios?
	1. Diminuir a complexidade do código;
  	2. Dinimuir o risco de falhas;
  	3. Melhora a organização do código separando os domínios e camadas do código;
  	4. Melhora a modularização do código e, consequentemente, a reutilização do código;
  5. Facilita a manutenção do código por diminuir a complexidade do código;
* Por onde deveremos começar a refatoração?
	1. Começar pelas camadas mais externas da aplicação;
	2. Fazer testes pois não tem como alterar o código sem ter a garantia de que ele vai funcionar (utilize TDD);
	3. Começar o procurar problemas para iniciar a refatoração (ou seja, as coisas que cheiram mal);
		* Começar a eliminar o código duplicado;
		* Manter seu código (classes e métodos) pequenos (nada de controllers gigantes);
		* Dê os nomes certos aos parâmetros, variáveis e métodos;
		* Substituir números mágicos por constantes;
		* Dividir as responsabilidades (um método ou classe deve fazer somente o que deve ser feito); Evitar métodos e classes "faz-tudo";
		* Simplificar as condições;
		* Não tenha medo de remover a funcionalidade de uma classe;
		* Faça os objetos se comportarem como coleções (evitar usar array demasiadamente e utilizar classes da SPL);
		* Comentar códigos corretamente e utilizar type hints;
		* Faça programação em par;