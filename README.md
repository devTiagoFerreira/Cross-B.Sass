# Cross-B.Sass

### Cross-B.Sass - Uma biblioteca Sass para Cross-browser.

#### Como funciona?

Quando se trata de folhas de estilo (style sheets), definir apenas uma linha de comomando para alterar um atributo, muitas vezes, não é o sulficiente. Isso acontece pois, além de cada navegador (browser) interpretar os arquivos .css a sua maneira, existem várias versões do mesmo browser, ou seja, quanto mais antigo é o browser, menor a probabilidade de haver suporte a novos recursos.

##### Veja esse exemplo

```
   .box {
       transform: translate(100px);
       -moz-transform: translate(100px); //Firefox 3
       -ms-transform: translate(100px); //Internet Explorer 9
       -o-transform: translate(100px); //Opera 10
       -webkit-transform: translate(100px); //Chrome, Opera 12, Safari 3
    }

```
