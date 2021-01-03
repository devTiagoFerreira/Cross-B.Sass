# Cross-B.Sass


### Cross-B.Sass - Uma biblioteca Sass para Cross-browser.


#### Importante!

Para um bom entendimento de como Cross-B.Sass funciona é importante que você tenha alguma familiaridade com [Sass](https://sass-lang.com/guide). Caso contrário, antes de botar a mão na massa, tire um tempinho para ler esse [guia](https://sass-lang.com/guide)!


#### Como funciona?

Quando se trata de folhas de estilo (style sheets), definir apenas uma linha de comando para alterar um atributo, muitas vezes, não é o suficiente. Isso acontece pois, além de cada navegador (browser) interpretar os arquivos .css a sua maneira, existem várias versões do mesmo browser, ou seja, quanto mais antigo é o browser, menor a probabilidade de haver suporte a novos recursos. 


##### Utilizando apenas Css

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

Cross-B.Sass tem como objetivo facilitar todo esse processo utilizando [Sass](https://sass-lang.com/guide).


#### Utilizando Cross-B.Sass

```
    //Arquivo style.scss

    @import '_lib'

   .box {
        @include transform(translate(100px));
    }

```

#### Cross-B.Sass fazendo o trabalho pesado para você!

````
    //Arquivo _cross-b.scss

    @mixin transform($prop) {
        transform: $prop;
        -moz-transform: $prop; //Firefox 3
        -ms-transform: $prop; //Internet Explorer 9
        -o-transform: $prop; //Opera 10
        -webkit-transform: $prop; //Chrome, Opera 12, Safari 3
    }

````




