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
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="51079-122">Usando a propriedade invokeURLs em uma página da Web exibida pelo Firefox</span><span class="sxs-lookup"><span data-stu-id="51079-122">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="51079-123">Alguns arquivos de mídia contêm URLs inseridas para as quais o Windows Media Player exibe as páginas da Web em uma janela do navegador ou quadro à medida que o arquivo de mídia é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="51079-123">Some media files contain embedded URLs for which Windows Media Player displays webpages in a Web browser window or frame as the media file plays.</span></span> <span data-ttu-id="51079-124">No Windows Internet Explorer, você pode usar a propriedade [Settings. invokeURLs](settings-invokeurls.md) para especificar se as páginas são exibidas para URLs inseridas e pode usar a propriedade [Settings. DefaultFrame](settings-defaultframe.md) para especificar um quadro para exibir essas páginas.</span><span class="sxs-lookup"><span data-stu-id="51079-124">In Windows Internet Explorer, you can use the [Settings.invokeURLs](settings-invokeurls.md) property to specify whether pages are displayed for embedded URLs, and you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify a frame for displaying such pages.</span></span>

<span data-ttu-id="51079-125">No Firefox, algumas soluções alternativas são necessárias para definir a propriedade **invokeURLs** e especificar um quadro para exibir páginas para URLs inseridas.</span><span class="sxs-lookup"><span data-stu-id="51079-125">In Firefox, some workarounds are required to set the **invokeURLs** property and to specify a frame for displaying pages for embedded URLs.</span></span>

## <a name="setting-the-invokeurls-property"></a><span data-ttu-id="51079-126">Definindo a propriedade invokeURLs</span><span class="sxs-lookup"><span data-stu-id="51079-126">Setting the invokeURLs property</span></span>

<span data-ttu-id="51079-127">O valor padrão da propriedade **Settings. invokeURLs** é true, portanto, se você quiser que o valor seja false, deverá defini-lo explicitamente.</span><span class="sxs-lookup"><span data-stu-id="51079-127">The default value of the **Settings.invokeURLs** property is true, so if you want the value to be false, you must set it explicitly.</span></span> <span data-ttu-id="51079-128">No Internet Explorer, você pode definir **invokeURLs** como false em um elemento param dentro do elemento Object do controle Player.</span><span class="sxs-lookup"><span data-stu-id="51079-128">In Internet Explorer, you can set **invokeURLs** to false in a PARAM element inside the Player control's OBJECT element.</span></span>

<span data-ttu-id="51079-129">O plug-in do Firefox não oferece suporte à definição da propriedade **invokeURLs** em um elemento param.</span><span class="sxs-lookup"><span data-stu-id="51079-129">The Firefox plug-in does not support setting the **invokeURLs** property in a PARAM element.</span></span>

<span data-ttu-id="51079-130">Você pode contornar essa limitação definindo a propriedade **invokeURLs** no script.</span><span class="sxs-lookup"><span data-stu-id="51079-130">You can work around this limitation by setting the **invokeURLs** property in script.</span></span> <span data-ttu-id="51079-131">O código a seguir mostra como definir a propriedade **invokeURLs** como false em uma página da Web que pode ser exibida pelo Internet Explorer e pelo Firefox.</span><span class="sxs-lookup"><span data-stu-id="51079-131">The following code shows how to set the **invokeURLs** property to false in a webpage that can be displayed by both Internet Explorer and Firefox.</span></span>


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



## <a name="displaying-webpages-in-a-frame"></a><span data-ttu-id="51079-132">Exibindo páginas da Web em um quadro</span><span class="sxs-lookup"><span data-stu-id="51079-132">Displaying webpages in a frame</span></span>

<span data-ttu-id="51079-133">Um arquivo de mídia pode conter URLs que exibem páginas da Web em uma janela do navegador ou quadro à medida que o arquivo de mídia é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="51079-133">A media file can contain URLs that display webpages in a browser window or frame as the media file is played.</span></span> <span data-ttu-id="51079-134">No Internet Explorer, você pode usar a propriedade [Settings. DefaultFrame](settings-defaultframe.md) para especificar o quadro no qual essas páginas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="51079-134">In Internet Explorer, you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify the frame in which those pages are displayed.</span></span> <span data-ttu-id="51079-135">Se você não definir a propriedade **DefaultFrame** , as URLs serão exibidas em uma janela separada do navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="51079-135">If you do not set the **defaultFrame** property, URLs are displayed in a separate window of the default browser.</span></span> <span data-ttu-id="51079-136">No entanto, o plug-in do Firefox não oferece suporte à propriedade **Settings. DefaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="51079-136">However, the Firefox plug-in does not support the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="51079-137">Para contornar essa limitação, defina a propriedade **Settings. invokeURLs** como false e grave um manipulador de eventos [ScriptCommand](player-player-scriptcommand.md) que defina o local do quadro de destino.</span><span class="sxs-lookup"><span data-stu-id="51079-137">To work around this limitation, set the **Settings.invokeURLs** property to false and write a [ScriptCommand](player-player-scriptcommand.md) event handler that sets the location of the target frame.</span></span> <span data-ttu-id="51079-138">O exemplo a seguir, que funciona no Internet Explorer e no Firefox, ilustra essa técnica.</span><span class="sxs-lookup"><span data-stu-id="51079-138">The following example, which works in Internet Explorer and Firefox, illustrates this technique.</span></span> <span data-ttu-id="51079-139">Suponha que a página da Web mostrada no exemplo esteja nos quadros \[ 0 \] e você queira que a página da URL seja exibida nos quadros \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="51079-139">Assume that the webpage shown in the example is in frames\[0\] and you want the URL's page to be displayed in frames\[1\].</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="51079-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="51079-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51079-141">**Usando o controle do Windows Media Player com o Firefox**</span><span class="sxs-lookup"><span data-stu-id="51079-141">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




