# Cross-B.Sass
 
 
### Cross-B.Sass - Uma biblioteca Sass para Cross-browser.
 
 
#### Importante!
 
Para um bom entendimento de como Cross-B.Sass funciona é importante que você tenha alguma familiaridade com [Sass](https://sass-lang.com/guide). Caso contrário, antes de botar a mão na massa, tire um tempinho para ler esse [guia](https://sass-lang.com/guide)!
 
#### Como funciona?
 
Quando se trata de folhas de estilo (style sheets), definir apenas uma linha de comando para alterar um atributo, muitas vezes, não é o suficiente. Isso acontece pois, além de cada navegador (browser) interpretar os arquivos .css a sua maneira, existem várias versões do mesmo browser, ou seja, quanto mais antigo é o browser, menor a probabilidade de haver suporte a novos recursos. 
 
Para oferecer suporte a um maior número de browsers/versões temos que definir várias linhas com o mesma propriedade. Veja o exemplo a seguir utilizando apenas Css!
 
##### Propriedade transform apenas com Css
 
```
    //Arquivo style.css
 
   .box {
       transform: translate(100px);
       -moz-transform: translate(100px); //Firefox 3
       -ms-transform: translate(100px); //Internet Explorer 9
       -o-transform: translate(100px); //Opera 10
       -webkit-transform: translate(100px); //Chrome, Opera 12, Safari 3
    }
 
```

Acabamos de ver um exemplo de Cross-browser. 
 
Cross-browser traduzido do inglês - Compatibilidade entre navegadores é a capacidade de um site ou aplicativo da web funcionar em diferentes navegadores e se degradar normalmente quando os recursos do navegador estão ausentes. 
[Wikipedia](https://en.wikipedia.org/wiki/Cross-browser_compatibility)
 
Obviamente a técnica se estende muito além das style sheets, já que para oferecer suporte a tanta diversidade se faz necessário muitas vezes, o uso de Javascript, jQuery e várias outras bibliotecas e técnicas.
 
Cross-B.Sass tem como objetivo facilitar todo esse processo utilizando [Sass](https://sass-lang.com/guide). Com Cross-B.Sass você faz todo o processo do exemplo anterior apenas declarando uma única linha. 
 
#### Propriedade transform com Cross-B.Sass
 
```
    //Arquivo style.scss
 
    @import 'cross-b' //Importação da biblioteca Cross-B.Sass.
 
   .box {
        @include transform(translate(100px)); //
    }
 
```

Muito mais simples, certo?
 
Veja agora como o Cross-B.Sass trata a propriedade internamente.
 
#### Cross-B.Sass fazendo o trabalho pesado para você!
 
```
    //Arquivo _cross-b.scss
 
    @mixin transform($prop) {
        transform: $prop;
        -moz-transform: $prop; //Firefox 3
        -ms-transform: $prop; //Internet Explorer 9
        -o-transform: $prop; //Opera 10
        -webkit-transform: $prop; //Chrome, Opera 12, Safari 3
    }

```