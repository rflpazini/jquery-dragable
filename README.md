jquery-dragable
===============
__obs:__ este repo. está totalmento em [pt-Br](http://pt.wikipedia.org/wiki/Portugu%C3%AAs_brasileiro), já que as vezes encontro com alguns desenvolvedores que dizem ser um pouco difícil encontrar conteúdo em nosso idioma.<br />

<br  />Crie um objeto que possa ser arrastando e soltando em uma outra parte do site de uma forma simples. Foi uma das formas mais simples que eu encontrei de fazer, então espero ajudar.

Arquivos
========

Para a construção do projeto, foram utilizadas as bibliotecas [Jquery](http://jquery.com/) e [Jquery-UI](http://jqueryui.com/). Como framework front-end utilizei a [Bootstrap](http://getbootstrap.com/) para agilizar no desenvolvimento. <br />
Você vai encontrar os seguintes arquivos no projeto:<br />

* index.html
* js
  * jquery-1.11.1.min.js
  * jquery-ui.js
* css
  * bootstrap.css
  * style.css

Setup
====

Para que você entenda o que acontece, tudo é comandado por esta função, ela está dentro do arquivo html:

```javascript
			$(document).ready(function(){
                $(".item").draggable({
                    helper: 'clone'
                });
                
                $("#carrinho").droppable({
                    accept:".item",
                    drop:function(event, ui){
                        var itemComprado = $(ui.draggable.clone);
                        $(this).append(itemComprado), 
                        alert('Mensagem....');
                    } 
                });
            });
```

O resto é feito pelos arquivos Js que foram adicionados no Html.
Esta função habilita o carrinho para receber os itens e assim que o evento de clique é efetuado, ela clona o item que foi clicado e libera para que o mesmo seja adicionado dentro do carrinho. Assim que o item é soltado dentro do carrinho, o mesmo é desabilitado para ser arrastado. <br />

### Quer contribuir? Alguma dica para melhorar o código? ###

* De um fork
* Faça um Pull Request

Por enquanto é isso. [@RafaelPazini](http://twitter.com/RafaelPazini)

