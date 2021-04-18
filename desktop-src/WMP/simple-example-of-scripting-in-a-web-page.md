---
title: Exemplo simples de script em uma página da Web
description: Exemplo simples de script em uma página da Web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- Controle ActiveX do Windows Media Player, exemplo de script
- Controle ActiveX móvel do Windows Media Player, exemplo de script
- Controle ActiveX, exemplo de script
- inserindo, páginas da Web
- Inserção de página da Web, exemplo de script
- exemplo de script para inserção de página da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "105763290"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a>Exemplo simples de script em uma página da Web

Você pode facilmente inserir o controle do Windows Media Player em um arquivo HTML usando qualquer linguagem de script que seu navegador reconhece. O exemplo simples a seguir usa o Microsoft JScript para criar uma página que irá reproduzir um arquivo quando você clicar em um botão e parar de executar o arquivo quando você clicar em outro botão.

Você pode inserir o controle ActiveX do Windows Media Player em uma página da Web usando as quatro etapas a seguir:

1.  Crie a página da Web.
2.  Adicione a marca do objeto.
3.  Adicione uma interface do usuário. Nesse caso, dois botões.
4.  Adicione algumas linhas de código para responder quando o usuário clicar em um dos botões que você criou.

## <a name="creating-the-web-page"></a>Criando a página da Web

A primeira etapa é criar uma página da Web HTML válida. O código a seguir é o mínimo necessário para criar uma página HTML em branco, mas válida:


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a>Adicionando a marca do objeto

Depois de criar uma página da Web, você precisa adicionar uma marca de objeto. Isso identifica o controle ActiveX para o navegador e configura todas as definições iniciais. Você deve posicionar a marca de objeto no corpo do código. Se você colocá-lo no corpo, a interface do usuário padrão do Windows Media Player será visível. Se você quiser criar sua própria interface de usuário, defina os atributos de altura e largura como 0 (zero). Você também pode definir o *Player*. Propriedade **UIMODE** como "invisível" quando você deseja ocultar o controle, mas ainda reservar espaço para ele na página. O código a seguir é recomendado quando você fornece uma interface do usuário personalizada:


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



Os seguintes atributos de marca de objeto são necessários:

ID

O nome que será usado por outras partes do código para identificar e usar o controle ActiveX. Você pode escolher qualquer nome desejado, desde que ele seja um nome que ainda não esteja sendo usado por HTML, por extensões HTML ou pela linguagem de script que você está usando. Neste exemplo, o nome "Player" é usado, mas você também pode chamá-lo de "myplayr" ou algo mais. Basta escolher um nome que seja exclusivo para essa página da Web.

CLASSID

Um número hexadecimal muito grande que é exclusivo para o controle. Apenas um controle tem esse número e é o controle ActiveX do Windows Media Player. Para evitar erros tipográficos, você pode copiar e colar esse número da documentação. As versões do controle do Windows Media Player anteriores à versão 7,0 tinham um ClassID diferente.

## <a name="adding-a-user-interface"></a>Adicionando uma interface do usuário

O HTML permite uma vasta gama de elementos da interface do usuário, permitindo que o usuário interaja com sua página da Web clicando, pressionando chaves e outras ações do usuário. Adicionar alguns botões de entrada é a maneira mais fácil de fornecer uma interface de usuário rápida. O código a seguir cria dois botões que podem responder ao usuário. Clicar em um botão inicia o fluxo de mídia em execução e o outro botão o interrompe:


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



O nome do botão é usado para identificar o botão para seu código; o valor é o rótulo que será exibido no botão e o atributo OnClick identificará qual parte do seu código de script será chamada quando o botão for clicado.

## <a name="adding-scripting-code"></a>Adicionando código de script

O código de script adiciona interatividade à sua página. O código de script pode responder a eventos, chamar métodos e alterar as propriedades de tempo de execução. Os scripts estendidos são colocados em um conjunto de marcas de SCRIPT. A marca de SCRIPT informa ao navegador onde está o código de script e identifica a linguagem de script. Se você não identificar um idioma, o idioma padrão será Microsoft JScript.

É uma boa prática de criação colocar o script em marcas de comentário HTML para que os navegadores que não dão suporte a scripts não processem seu código como texto. Coloque a marca de SCRIPT em qualquer lugar dentro do corpo do arquivo HTML e insira o código de comentário entre as marcas de SCRIPT de abertura e fechamento.

O exemplo de código do Microsoft JScript a seguir chama o controle do Windows Media Player e executa uma ação apropriada em resposta ao clique no botão correspondente.


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



A função de exemplo, StartMeUp, é chamada quando o botão marcado como executar é clicado e a função ShutMeDown é chamada quando o botão parar é clicado.

O código dentro de StartMeUp usa a propriedade URL para definir um caminho para a mídia. A mídia começará a ser reproduzida imediatamente.

O código ShutMeDown chama o método **Stop** do objeto **Controls** . Observe que o objeto **Controls** é chamado por meio da propriedade **Controls** do objeto **Player** , que tem o valor de ID de "Player".

O código a seguir mostra um exemplo completo.


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



Observe que você deve fornecer uma URL válida para um nome de arquivo válido na propriedade URL. Nesse caso, a suposição é que o arquivo Laure. WMA esteja no mesmo diretório que o arquivo HTML.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o controle do Windows Media Player em uma página da Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




