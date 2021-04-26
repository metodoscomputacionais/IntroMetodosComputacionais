|**MÉTODO COMPUTACIONAIS**|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.001.png)|
| :- | -: |

![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.002.png)ssssss

**MÉTODO DA BISSEÇÃO**

O método da bisseção faz parte dos métodos numéricos para determinar-se solução de equações. Basicamente aqui estamos falando de determinar o zero de uma função (também chamado de raiz -  REF \_Ref69134256 \h  \\* MERGEFORMAT Figura 1). 


|Figura  SEQ Figura \\* ARABIC 1 – Ilustração de equações com nenhuma, uma ou várias soluções  ADDIN ZOTERO\_ITEM CSL\_CITATION {"citationID":"LjAj0PSL","properties":{"formattedCitation":"[1]","plainCitation":"[1]","noteIndex":0},"citationItems":[{"id":1144,"uris":["http://zotero.org/users/6863133/items/4I7F6YX4"],"uri":["http://zotero.org/users/6863133/items/4I7F6YX4"],"itemData":{"id":1144,"type":"book","ISBN":"978-85-7780-297-5","language":"Portuguese","note":"OCLC: 882498806","source":"Open WorldCat","title":"Métodos numéricos para engenheiros e cientistas: uma introdução com aplicações usando o MATLAB","title-short":"Métodos numéricos para engenheiros e cientistas","URL":"http://site.ebrary.com/id/10839672","author":[{"family":"Gilat","given":"Amos"},{"family":"Suramanian","given":"Vish"}],"accessed":{"date-parts":[["2021",4,12]]},"issued":{"date-parts":[["2008"]]}}}],"schema":"https://github.com/citation-style-language/schema/raw/master/csl-citation.json"} [1].|
| :-: |
|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.003.png)|

Quando a equação é simples, é comum o emprego de técnicas ou fórmulas pré-estabelecidas que permitem a solução da equação de forma rápida. São exemplos:

- Fórmula de Bhaskara;
- Método de Briot-Ruffini.

Para equações que possuem “grau de complexidade” elevado essa determinação pode ser feita de maneira numérica por meio de aproximações. Dentro desse apanhado de técnicas de aproximação de raízes surgem os **modelos numéricos de redução sucessiva de intervalos** (também chamado de métodos de confinamento), são exemplos de métodos com essa característica:

- Método da bisseção;
- Método da seção áurea.

**O MÉTODO DA BISSEÇÃO**

O método da bisseção consiste em determinar o valor da solução de uma função dentro de um intervalo pré-estabelecido. Portanto o método explora esse intervalo dada uma função contínua f: a, b→R. Porém para obter-se uma raiz dentro desse intervalo deve-se respeitar a condição de existência dada pelo **Teorema de Bolzano**:

Seja uma função f(x) contínua em um intervalo a, b, tal que, f(a).f(b)<0. Então a função f(x) **possui pelo menos uma raiz** no intervalo a, b.

Na  REF \_Ref69137923 \h  \\* MERGEFORMAT Figura 2 é possível verificar que para a equação citada anteriormente o valor do f(0).f(4)=<0 é de aproximadamente -107,24.


|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.004.png)Figura  SEQ Figura \\* ARABIC 2 – Gráfico da função *f(x) = 8-4,50.(x-senx)* ADDIN ZOTERO\_ITEM CSL\_CITATION {"citationID":"XnoSvtro","properties":{"formattedCitation":"[1]","plainCitation":"[1]","noteIndex":0},"citationItems":[{"id":1144,"uris":["http://zotero.org/users/6863133/items/4I7F6YX4"],"uri":["http://zotero.org/users/6863133/items/4I7F6YX4"],"itemData":{"id":1144,"type":"book","ISBN":"978-85-7780-297-5","language":"Portuguese","note":"OCLC: 882498806","source":"Open WorldCat","title":"Métodos numéricos para engenheiros e cientistas: uma introdução com aplicações usando o MATLAB","title-short":"Métodos numéricos para engenheiros e cientistas","URL":"http://site.ebrary.com/id/10839672","author":[{"family":"Gilat","given":"Amos"},{"family":"Suramanian","given":"Vish"}],"accessed":{"date-parts":[["2021",4,12]]},"issued":{"date-parts":[["2008"]]}}}],"schema":"https://github.com/citation-style-language/schema/raw/master/csl-citation.json"} [1].|
| :- |
|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.005.png)|
Sabendo que existe uma raiz da função no intervalo é possível a determinação utilizando o algoritmo de bisseção que toma como principio reduções sucessivas do intervalo pela metade do seu valor. 

As reduções sucessivas do intervalo seguem o seguinte critério:

|xt+1=at+bt2||` `SEQ Equação \\* ARABIC 1|
| - | -: | -: |
|fxt+1.fat<0|Novo intervalo:* at,xt+1|` `SEQ Equação \\* ARABIC 2|
|fxt+1.fat>0|Novo intervalo:* xt+1, bt|` `SEQ Equação \\* ARABIC 3|



|Figura  SEQ Figura \\* ARABIC 3 – interpretação gráfica da função e do intervalo [2, 3].|
| :-: |
|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.006.png)|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.007.png)|
|Estado inicial|Após t = 1 iterações|
![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.004.png)Percorrendo algumas iterações São obtidos os valores das reduções de intervalo:

|x1=2+32=2,5|||
| - | -: | -: |
|fx1.f2=-15,04|||
|Novo intervalo:* 2,  2,5|||
A erro de cada iteração para esse método é dada pela avaliação do novo intervalo conforme equação  REF \_Ref69163054 \h  \\* MERGEFORMAT 4.

|tol=b - a2||` `SEQ Equação \\* ARABIC 4|
| - | -: | -: |
O algoritmo da bisseção é apresentado em sequência:

![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.004.png)***Algoritmo***

|**1**|ERRO = 100, TOL = 1E-2, [A, B]|
| - | - |
|**2**|**while** ERRO > TOL:|
|**3**||X = eq.  REF \_Ref69162594 \h  \\* MERGEFORMAT 1|
|**4**||Avalie f(a) e f(x)|
|**5**||**if** FA . FX < 0:|
|**6**|||A = A e B = X||
|**7**||**else:**||
|**8**|||A = X e B = B||
|**9**||ERRO = eq.  REF \_Ref69163054 \h  \\* MERGEFORMAT 4.||
|**10**|RAIZ = X||


|Figura  SEQ Figura \\* ARABIC 4 – Resultados do método da bisseção.|
| :-: |
|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.008.png)|![](Aspose.Words.e85b60cd-c16d-4fcc-9c35-f0bbb726f6f0.009.png)|
|Iterações|Convergência|
**REFERÊNCIAS**

` `ADDIN ZOTERO\_BIBL {"uncited":[],"omitted":[],"custom":[]} CSL\_BIBLIOGRAPHY [1]	Gilat A, Suramanian V. Métodos numéricos para engenheiros e cientistas: uma introdução com aplicações usando o MATLAB. 2008.






|**M. N. RABELO, W. M. PEREIRA JUNIOR** |**PAGE   \\* MERGEFORMAT2**||
| :- | :-: | -: |

