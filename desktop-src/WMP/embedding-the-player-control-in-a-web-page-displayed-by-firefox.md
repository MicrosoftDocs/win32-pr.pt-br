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
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="9fb03-123">Inserindo o controle do jogador em uma página da Web exibida pelo Firefox</span><span class="sxs-lookup"><span data-stu-id="9fb03-123">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="9fb03-124">Para inserir o controle do Windows Media Player em uma página da Web que pode ser exibida por um navegador Firefox, crie um elemento OBJECT ou um elemento EMBED que tenha um dos seguintes tipos MIME como seu atributo de **tipo** :</span><span class="sxs-lookup"><span data-stu-id="9fb03-124">To embed the Windows Media Player control in a webpage that can be displayed by a Firefox browser, create an OBJECT element or an EMBED element that has one of the following mime types as its **type** attribute:</span></span>

-   <span data-ttu-id="9fb03-125">aplicativo/x-MS-WMP</span><span class="sxs-lookup"><span data-stu-id="9fb03-125">application/x-ms-wmp</span></span>
-   <span data-ttu-id="9fb03-126">aplicativo/ASX</span><span class="sxs-lookup"><span data-stu-id="9fb03-126">application/asx</span></span>
-   <span data-ttu-id="9fb03-127">vídeo/x-ms-asf-plugin</span><span class="sxs-lookup"><span data-stu-id="9fb03-127">video/x-ms-asf-plugin</span></span>
-   <span data-ttu-id="9fb03-128">aplicativo/x-mplayer2</span><span class="sxs-lookup"><span data-stu-id="9fb03-128">application/x-mplayer2</span></span>
-   <span data-ttu-id="9fb03-129">vídeo/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="9fb03-129">video/x-ms-asf</span></span>
-   <span data-ttu-id="9fb03-130">vídeo/x-MS-WM</span><span class="sxs-lookup"><span data-stu-id="9fb03-130">video/x-ms-wm</span></span>
-   <span data-ttu-id="9fb03-131">áudio/x-MS-WMA</span><span class="sxs-lookup"><span data-stu-id="9fb03-131">audio/x-ms-wma</span></span>
-   <span data-ttu-id="9fb03-132">áudio/x-MS-Wax</span><span class="sxs-lookup"><span data-stu-id="9fb03-132">audio/x-ms-wax</span></span>
-   <span data-ttu-id="9fb03-133">vídeo/x-MS-WMV</span><span class="sxs-lookup"><span data-stu-id="9fb03-133">video/x-ms-wmv</span></span>
-   <span data-ttu-id="9fb03-134">vídeo/x-MS-wvx</span><span class="sxs-lookup"><span data-stu-id="9fb03-134">video/x-ms-wvx</span></span>

<span data-ttu-id="9fb03-135">O tipo MIME preferencial é application/x-MS-WMP.</span><span class="sxs-lookup"><span data-stu-id="9fb03-135">The preferred mime type is application/x-ms-wmp.</span></span>

<span data-ttu-id="9fb03-136">Os exemplos a seguir mostram como inserir o controle Player usando um elemento OBJECT ou um elemento EMBED.</span><span class="sxs-lookup"><span data-stu-id="9fb03-136">The following examples show how to embed the Player control using an OBJECT element or an EMBED element.</span></span>


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



<span data-ttu-id="9fb03-137">Os exemplos anteriores funcionam no Firefox, mas não no Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9fb03-137">The preceeding examples work in Firefox but not in Internet Explorer.</span></span> <span data-ttu-id="9fb03-138">Para inserir o controle do jogador em uma página da Web que pode ser exibida pelo Internet Explorer, você deve criar um elemento OBJECT que tenha um atributo **ClassID** definido como a ID de classe do controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9fb03-138">To embed the Player control in a webpage that can be displayed by Internet Explorer, you must create an OBJECT element that has a **classid** attribute set to the class ID of the Windows Media Player control.</span></span>

<span data-ttu-id="9fb03-139">O exemplo a seguir mostra como inserir o controle do Windows Media Player em uma página da Web que pode ser exibida corretamente pelo Internet Explorer e pelo Firefox.</span><span class="sxs-lookup"><span data-stu-id="9fb03-139">The following example shows how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span> <span data-ttu-id="9fb03-140">O script na página detecta o tipo de navegador e gera a marca de objeto apropriada.</span><span class="sxs-lookup"><span data-stu-id="9fb03-140">Script on the page detects the browser type and generates the appropriate OBJECT tag.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9fb03-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9fb03-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fb03-142">**Usando o controle do Windows Media Player com o Firefox**</span><span class="sxs-lookup"><span data-stu-id="9fb03-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




