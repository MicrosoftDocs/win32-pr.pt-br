---
title: Usando script para controlar a invertia de URL
description: Usando script para controlar a invertia de URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player apresentações baseadas na Web
- Windows Media Player de objeto, apresentações baseadas na Web
- modelo de objeto, apresentações baseadas na Web
- Windows Media Player Apresentações móveis baseadas na Web
- Windows Media Player ActiveX controle, apresentações baseadas na Web
- Windows Media Player Controle ActiveX dispositivo móvel, apresentações baseadas na Web
- ActiveX controle, apresentações baseadas na Web
- Windows Media Player, invertindo URL
- Windows Media Player de objeto, inverter URL
- modelo de objeto, inverter URL
- Windows Media Player Móvel, invertindo URL
- Windows Media Player ActiveX controle, invertia de URL
- Windows Media Player Controle de ActiveX móvel, invertindo URL
- ActiveX controle, invertindo URL
- Apresentações baseadas na Web, invertia de URL
- criando apresentações baseadas na Web, invertindo URL
- Invertia de URL
- Windows Media Player streaming de mídias rich
- Windows Media Player de objeto, streaming de mídias rich
- modelo de objeto, streaming de mídias rich
- Windows Media Player Streaming de mídia móvel e rich
- Windows Media Player ActiveX controle, streaming de mídia rico
- Windows Media Player Controle de ActiveX móvel, streaming de mídias rich
- ActiveX controle, streaming de mídia rico
- Apresentações baseadas na Web, streaming de mídias rich
- criando apresentações baseadas na Web, streaming de mídias rich
- streaming de mídia rica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9470bf2b812d36bceb6159ab089e3b08c49bc84515320872b125ed6519568141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507126"
---
# <a name="using-script-to-control-url-flipping"></a>Usando script para controlar a invertia de URL

Quando um usuário se conecta a um fluxo de mídia rico enquanto o fluxo já está em andamento, é possível que a página da Web transmitida seja exibida antes de todos os elementos chegarem e tenham sido armazenados em cache se Windows Media Player invocar automaticamente a URL. Quando isso acontece, o usuário vê uma página da Web em branco ou incompleta até que o próximo conjunto de dados chegue ao cache.

Você pode evitar exibir uma página da Web em branco ou incompleta invocando a URL usando o script em vez de Windows Media Player fazer isso automaticamente. Dessa forma, você pode ignorar a primeira invasão de URL e, em seguida, invocar URLs subsequentes usando o código de script.

> [!Note]  
> Esta seção presume que você está transmitindo HTML usando o SDK Windows Media Encoder 9 Series e que você definiu o fluxo HTML para repetir.

 

Primeiro, você deve criar uma página da Web do quadro para conter o quadro com o Player inserido e o quadro que exibe o HTML de streaming. Cada um desses dois quadros exibirá uma página da Web separada inicialmente, portanto, você criará um total de três páginas da Web. O código de exemplo a seguir demonstra a página da Web do frameset:


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



O exemplo de página da Web anterior incorpora dois quadros. O primeiro quadro é exibido na metade esquerda da janela do navegador e exibe a página da Web chamada inserir \_player.htm. O código de exemplo a seguir cria esta página da Web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



O segundo quadro no quadro é exibido na metade direita da janela do navegador e exibe uma página da Web chamada "blank.htm". O código de exemplo a seguir cria esta página da Web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Quando a página de conjuntos de quadros é carregada no navegador, o quadro esquerdo mostra o Player inserido e o quadro direito mostra o texto "Carregando..." para informar ao usuário que mais dados serão futuros. Quando o primeiro comando de script de URL chega do fluxo HTML, o manipulador de eventos simplesmente altera o valor do **sinalizador booliana.** Quando cada comando de script de URL subsequente chega do fluxo HTML, o script no manipulador de eventos carrega a nova URL no quadro chamado "conteúdo", e a página da Web completa é exibida no quadro localizado na metade direita da janela do navegador.

Para obter mais informações sobre como transmitir HTML usando Windows Media, consulte o SDK Windows Media Encoder.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Rich Media Streaming**](rich-media-streaming.md)
</dt> <dt>

[**Invertia de URL**](url-flipping.md)
</dt> </dl>

 

 




