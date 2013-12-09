# Palestra

* **Nome:** Design Patterns de uma vez por todas
* ***Palestrante:*** Michael Humberto Castillo Granados
* **Dia**: 1

## Anotações

* O que é design pattern? São "regras" que resolvem determinados problemas conhecidos sobre projetos orientados a objetos.
* O Gang of Four são os autores do livro icônico sobre design patterns.
* Informações importantes a serem consideradas: 
	1. Separe as coisas que mudam das coisas que permanecem as mesmas.
	2. Programe para uma interface e não para uma implementação.
	3. Prefira composição no lugar de harança.
	4. Delegue, delegue, delegue. Crie objetos para desconto, objetos para juros e não uma classe "Util", por exemplo.
* Os design patterns são divididos em criação, estruturais e comportamentais.
* Template Method.
* Strategy - apesar do template method resolver o problema de forma simples e direta as vezes queremos mudar grande parte do script.
* Observer - integrar vários objetos a apenas um para que eles executem determinada ação a partir da ação executada pelo primeiro objeto.
* Singleton - garante que a aplicação inteira possua apenas uma instância do objeto, mantendo um ponto global de acesso ao objeto.
* Iterator - criar uma estrutura de objetos similares em forma de uma coleção a fim de poder acessar todos de uma só vez.
* Pode-se utilizar a SPL do PHP 5.3 para se implementar o Iterator.