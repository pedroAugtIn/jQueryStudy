# Minhas anotações sobre jQuery

jQuery é uma biblioteca Javascript que simplifica a interação com documentos HTML, manipulação de eventos, animações, AJAX. Ela fornece uma maneira fácil de selecionar elementos do DOM.
Todas as funções jQuery começam com $.
jQuery geralmente seleciona um elemento HTML através de um selector e faz algo com este elemento.
No curso do freecodecamp iniciamos criando um script de uma “document ready function”, a qual, segundo o chatgpt, é uma função em jquery que é executada assim que o DOM HTML da página está totalmente carregado e pronto para ser manipulado. A sintaxe básica é:
  <script>
    $(document).ready(function() {
      // Seu código jQuery aqui
    });
  </script>

Neste caso, por exemplo, selecionamos todos os nossos elementos button e criamos uma animação de “bounce”:
<script>
  $(document).ready(function() {
$("button").addClass("animated bounce");
  });
</script>


.addClass() permite adicionarmos, através de jQuery, classes a elementos.
Da mesma forma, podemos utilizar o $() do jQuery para selecionar classes, seguindo o mesmo padrão do CSS, bastando adicionar ‘.’ Antes da classe, por exemplo:
$(".well").addClass("animated shake")

Podemos também selecionar elementos pelo seu ID, bastando seguir o padrão do CSS e adicionar ‘#’ antes do ID do elemento:
$("#target3").addClass("animated fadeOut")

Da mesma forma que podemos adicionar classes com o .addClass(), podemos remover classes com o .removeClass(). Ex:
$("#target2").removeClass("btn-default");

jQuery tem uma função chamada .css() que nos permite mudar o CSS de um elemento.
Por exemplo, mudando a cor de um elemento para azul:
$("#target1").css("color", "blue");

jQuery tem uma função chamada .prop() que nos permite ajustar as propriedades de um elemento.
Por exemplo, podemos desabilitar todos os botões de nosso html:
$("button").prop("disabled", true);

Usando jQuery é possível mudar o texto entre o começo e o fim de uma tag. jQuery possui uma função chamada .html() que permite adicionar tag HTML e taxto dentro de um elemento. Qualquer conteúdo anteriormente adicionado ao html será completamente substituído pelo conteúdo fornecido à função.
Logo, com essa função podemos alterar texto adicionando tags, como por exemplo <i> para itálico de texto, <em> para trazer ênfase, etc. ex:
$("h3").html("<em>jQuery Playground</em>");
Existe também uma função semelhante chamada .text(), que apenas permite alteração de texto, sem adicionar novas tags ao nosso elemento.
jQuery possui uma função chamada .remove(), capaz de remover elementos HTML completos. Ex: 
$("#target4").remove();

jQuery tem uma função chamada appendTo(), que permite movermos um elemento html a outro elemento. Por exemplo, digamos que nós temos 6 botões, 3 no div de id=”left-well” e 3 no div de id=”right-well”. Se quiséssemos passar nosso button de id =”target4”, do div right-well para o div left-well, seria só fazer:
$("#target4").appendTo("#left-well");

Com jQuery não só mover é possível, também é possível copiar o elemento para outro local através da função clone():
$("#target2").clone().appendTo("#right-well");

jQuery também possui uma função chamada parent(), que nos permite acessar o elemento “pai” daquele elemento que selecionamos.
Por exemplo, digamos que queremos acessar o elemento pai de nosso “left-well” e concedê-lo uma background-color azul:
$("#left-well").parent().css("background-color", "blue")
Da mesma forma, podemos acessar os elementos filhos daquele elemento que selecionamos através da função .children().
Por exemplo, podemos acessar todos os elementos filhos de nosso “left-well” e atribuir a eles uma color blue:
$("#left-well").children().css("color", "blue")

jQuery também utiliza CSS Selectors para selecionar elementos específicos. O “target:nth-child(n)” CSS selector permite selecionar todos os “nth elements” com a classe selecionada ou tipo de elemento. Vejamos como poderíamos selecionar o terceiro elemento de cada “well” e adicionar a class “bounce” a eles:
$(".target:nth-child(3)").addClass("animated bounce");

Também é possível selecionar elementos baseando-se em sua posição, através de :odd e :even
:odd: Este seletor seleciona todos os elementos de índice ímpar dentro de um conjunto de elementos.
:even: Este seletor seleciona todos os elementos de índice par dentro de um conjunto de elementos.
Vejamos como poderíamos selecionar todos os “odd elements” com a class “target” e dar a eles classes:
$(".target:odd").addClass("animated shake");


