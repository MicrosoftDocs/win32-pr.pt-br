---
title: Inserindo o controle do jogador em uma página da Web exibida pelo Firefox
description: Inserindo o controle do jogador em uma página da Web exibida pelo Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Windows Media Player, inserindo controle de ActiveX
- modelo de objeto Windows Media Player, inserindo ActiveX controle
- modelo de objeto, inserindo ActiveX controle
- Windows Media Player controle de ActiveX móvel, incorporando
- Windows Media Player controle de ActiveX, inserindo
- Windows Media Player controle de ActiveX móvel, incorporando
- controle de ActiveX, inserindo
- controle de ActiveX de Windows Media Player, páginas da Web
- Windows Media Player controle de ActiveX móvel, páginas da Web
- controle de ActiveX, páginas da Web
- Windows Media Player, Firefox
- modelo de objeto Windows Media Player, Firefox
- modelo de objeto, Firefox
- Windows Media Player Móvel, Firefox
- controle de ActiveX de Windows Media Player, Firefox
- Windows Media Player controle de ActiveX móvel, Firefox
- controle de ActiveX, Firefox
- Firefox, sobre a incorporação de páginas da Web
- inserindo, páginas da Web
- Incorporação de página da Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c1db799df78cb6c62516798f4bbd196c093f02225386f0c1009bfa11d9a668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578583"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Inserindo o controle do jogador em uma página da Web exibida pelo Firefox

para inserir o controle de Windows Media Player em uma página da web que pode ser exibida por um navegador Firefox, crie um elemento OBJECT ou um elemento embed que tenha um dos seguintes tipos mime como seu atributo de **tipo** :

-   aplicativo/x-MS-WMP
-   aplicativo/ASX
-   vídeo/x-ms-asf-plugin
-   aplicativo/x-mplayer2
-   vídeo/x-ms-asf
-   vídeo/x-MS-WM
-   áudio/x-MS-WMA
-   áudio/x-MS-Wax
-   vídeo/x-MS-WMV
-   vídeo/x-MS-wvx

O tipo MIME preferencial é application/x-MS-WMP.

Os exemplos a seguir mostram como inserir o controle Player usando um elemento OBJECT ou um elemento EMBED.


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



Os exemplos anteriores funcionam no Firefox, mas não no Internet Explorer. para inserir o controle Player em uma página da web que pode ser exibida pelo Internet Explorer, você deve criar um elemento OBJECT que tenha um atributo **classid** definido como a ID de classe do controle de Windows Media Player.

o exemplo a seguir mostra como inserir o controle de Windows Media Player em uma página da web que pode ser exibida corretamente pelo Internet Explorer e pelo Firefox. O script na página detecta o tipo de navegador e gera a marca de objeto apropriada.


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**usando o controle de Windows Media Player com o Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




