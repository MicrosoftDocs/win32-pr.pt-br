---
title: Usando a propriedade invokeURLs em uma página da Web exibida pelo Firefox
description: Usando a propriedade invokeURLs em uma página da Web exibida pelo Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX do Windows Media Player, Propriedade invokeURLs
- Controle ActiveX móvel do Windows Media Player, Propriedade invokeURLs
- inserindo, páginas da Web
- Incorporação de página da Web, Propriedade invokeURLs
- Windows Media Player, Firefox
- Modelo de objeto do Windows Media Player, Firefox
- modelo de objeto, Firefox
- Controle ActiveX do Windows Media Player, Firefox
- Controle ActiveX, Firefox
- Firefox, Propriedade invokeURLs
- Incorporação de página da Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "105782676"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Usando a propriedade invokeURLs em uma página da Web exibida pelo Firefox

Alguns arquivos de mídia contêm URLs inseridas para as quais o Windows Media Player exibe as páginas da Web em uma janela do navegador ou quadro à medida que o arquivo de mídia é reproduzido. No Windows Internet Explorer, você pode usar a propriedade [Settings. invokeURLs](settings-invokeurls.md) para especificar se as páginas são exibidas para URLs inseridas e pode usar a propriedade [Settings. DefaultFrame](settings-defaultframe.md) para especificar um quadro para exibir essas páginas.

No Firefox, algumas soluções alternativas são necessárias para definir a propriedade **invokeURLs** e especificar um quadro para exibir páginas para URLs inseridas.

## <a name="setting-the-invokeurls-property"></a>Definindo a propriedade invokeURLs

O valor padrão da propriedade **Settings. invokeURLs** é true, portanto, se você quiser que o valor seja false, deverá defini-lo explicitamente. No Internet Explorer, você pode definir **invokeURLs** como false em um elemento param dentro do elemento Object do controle Player.

O plug-in do Firefox não oferece suporte à definição da propriedade **invokeURLs** em um elemento param.

Você pode contornar essa limitação definindo a propriedade **invokeURLs** no script. O código a seguir mostra como definir a propriedade **invokeURLs** como false em uma página da Web que pode ser exibida pelo Internet Explorer e pelo Firefox.


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a>Exibindo páginas da Web em um quadro

Um arquivo de mídia pode conter URLs que exibem páginas da Web em uma janela do navegador ou quadro à medida que o arquivo de mídia é reproduzido. No Internet Explorer, você pode usar a propriedade [Settings. DefaultFrame](settings-defaultframe.md) para especificar o quadro no qual essas páginas são exibidas. Se você não definir a propriedade **DefaultFrame** , as URLs serão exibidas em uma janela separada do navegador padrão. No entanto, o plug-in do Firefox não oferece suporte à propriedade **Settings. DefaultFrame** . Para contornar essa limitação, defina a propriedade **Settings. invokeURLs** como false e grave um manipulador de eventos [ScriptCommand](player-player-scriptcommand.md) que defina o local do quadro de destino. O exemplo a seguir, que funciona no Internet Explorer e no Firefox, ilustra essa técnica. Suponha que a página da Web mostrada no exemplo esteja nos quadros \[ 0 \] e você queira que a página da URL seja exibida nos quadros \[ 1 \] .


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o controle do Windows Media Player com o Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




