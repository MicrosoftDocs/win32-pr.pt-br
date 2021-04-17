---
title: Inserindo o controle do jogador em uma página da Web exibida pelo Firefox
description: Inserindo o controle do jogador em uma página da Web exibida pelo Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
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
- Windows Media Player, Firefox
- Modelo de objeto do Windows Media Player, Firefox
- modelo de objeto, Firefox
- Windows Media Player Mobile, Firefox
- Controle ActiveX do Windows Media Player, Firefox
- Controle ActiveX móvel do Windows Media Player, Firefox
- Controle ActiveX, Firefox
- Firefox, sobre a incorporação de páginas da Web
- inserindo, páginas da Web
- Incorporação de página da Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "105783607"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Inserindo o controle do jogador em uma página da Web exibida pelo Firefox

Para inserir o controle do Windows Media Player em uma página da Web que pode ser exibida por um navegador Firefox, crie um elemento OBJECT ou um elemento EMBED que tenha um dos seguintes tipos MIME como seu atributo de **tipo** :

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



Os exemplos anteriores funcionam no Firefox, mas não no Internet Explorer. Para inserir o controle do jogador em uma página da Web que pode ser exibida pelo Internet Explorer, você deve criar um elemento OBJECT que tenha um atributo **ClassID** definido como a ID de classe do controle do Windows Media Player.

O exemplo a seguir mostra como inserir o controle do Windows Media Player em uma página da Web que pode ser exibida corretamente pelo Internet Explorer e pelo Firefox. O script na página detecta o tipo de navegador e gera a marca de objeto apropriada.


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

[**Usando o controle do Windows Media Player com o Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




