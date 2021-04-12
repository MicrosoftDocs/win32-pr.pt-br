---
title: Usando o script para controlar a inversão de URL
description: Usando o script para controlar a inversão de URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, apresentações baseadas na Web
- Modelo de objeto do Windows Media Player, apresentações baseadas na Web
- modelo de objeto, apresentações baseadas na Web
- Windows Media Player Mobile, apresentações baseadas na Web
- Controle ActiveX do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX móvel do Windows Media Player, apresentações baseadas na Web
- Controle ActiveX, apresentações baseadas na Web
- Windows Media Player, inversão de URL
- Modelo de objeto do Windows Media Player, inversão de URL
- modelo de objeto, inversão de URL
- Windows Media Player Mobile, inversão de URL
- Controle ActiveX do Windows Media Player, inversão de URL
- Controle ActiveX móvel do Windows Media Player, inversão de URL
- Controle ActiveX, inversão de URL
- Apresentações baseadas na Web, inversão de URL
- Criando apresentações baseadas na Web, inversão de URL
- Inversão de URL
- Windows Media Player, streaming de mídia avançada
- Modelo de objeto do Windows Media Player, streaming de mídia avançada
- modelo de objeto, streaming de mídia avançada
- Windows Media Player Mobile, streaming de mídia avançada
- Controle ActiveX do Windows Media Player, streaming de mídia avançada
- Controle ActiveX móvel do Windows Media Player, streaming de mídia avançada
- Controle ActiveX, streaming de mídia avançada
- Apresentações baseadas na Web, streaming de mídia avançada
- Criando apresentações baseadas na Web, streaming de mídia avançado
- streaming de mídia avançada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104364531"
---
# <a name="using-script-to-control-url-flipping"></a>Usando o script para controlar a inversão de URL

Quando um usuário se conecta a um fluxo de mídia avançado enquanto o fluxo já está em andamento, é possível que a página da Web transmitida seja exibida antes que todos os elementos sejam recebidos e armazenados em cache se o Windows Media Player invocar automaticamente a URL. Quando isso acontece, o usuário vê uma página da Web em branco ou incompleta até que o próximo conjunto de dados chegue no cache.

Você pode evitar a exibição de uma página da Web em branco ou incompleta invocando a URL usando o script em vez de permitir que o Windows Media Player faça isso automaticamente. Dessa forma, você pode ignorar a primeira URL inverter e, em seguida, invocar URLs subsequentes usando o código de script.

> [!Note]  
> Esta seção pressupõe que você esteja transmitindo HTML usando o SDK do Windows Media Encoder 9 Series e que você definiu o fluxo HTML para repetir.

 

Primeiro, você deve criar uma página da Web de conjunto de quadros para conter o quadro com o player incorporado e o quadro que exibe o HTML de streaming. Cada um desses dois quadros exibirá inicialmente uma página da Web separada, portanto, você criará um total de três páginas da Web. O código de exemplo a seguir demonstra a página da Web do conjunto de quadros:


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



O exemplo da página da Web anterior incorpora dois quadros. O primeiro quadro é exibido na metade esquerda da janela do navegador e exibe a página da Web chamada embed \_player.htm. O código de exemplo a seguir cria esta página da Web:


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



O segundo quadro no conjunto de quadros é exibido na metade direita da janela do navegador e exibe uma página da Web chamada "blank.htm". O código de exemplo a seguir cria esta página da Web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Quando a página conjunto de quadros é carregada no navegador, o quadro esquerdo mostra o player incorporado e o quadro direito mostra o texto "carregando..." para informar ao usuário que mais dados estão em breve. Quando o comando de script da primeira URL chega do fluxo HTML, o manipulador de eventos simplesmente altera o valor do sinalizador **booliano** . Quando cada comando de script de URL subsequente chega do fluxo HTML, o script no manipulador de eventos carrega a nova URL no quadro chamado "content" e a página da Web completa é exibida no quadro localizado na metade direita da janela do navegador.

Para obter mais informações sobre o streaming de HTML usando o Windows Media, consulte o SDK do Windows Media Encoder.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Streaming de mídia avançada**](rich-media-streaming.md)
</dt> <dt>

[**Inversão de URL**](url-flipping.md)
</dt> </dl>

 

 




