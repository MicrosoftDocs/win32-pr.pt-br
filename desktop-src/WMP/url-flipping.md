---
title: Inversão de URL
description: Inversão de URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "103637309"
---
# <a name="url-flipping"></a><span data-ttu-id="1a1b1-120">Inversão de URL</span><span class="sxs-lookup"><span data-stu-id="1a1b1-120">URL Flipping</span></span>

<span data-ttu-id="1a1b1-121">O uso de páginas da Web para apresentações de slides é chamado de inversão de URL e é manipulado automaticamente pelo Windows Media Player quando ele encontra comandos de script de URL inseridos no fluxo de mídia digital que está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-121">Using webpages for slide shows is called URL flipping, and is handled automatically by Windows Media Player when it encounters URL script commands embedded in the digital media stream it is playing.</span></span> <span data-ttu-id="1a1b1-122">Você pode especificar um quadro de destino para suas páginas em cada comando de script ou pode especificá-lo definindo a propriedade **Settings. DefaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="1a1b1-122">You can specify a target frame for your pages in each script command, or you can specify it by setting the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="1a1b1-123">Você pode definir essa propriedade no código do script ou usando um elemento PARAM dentro do elemento OBJECT que incorpora o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-123">You can set this property in script code or by using a PARAM element within the OBJECT element that embeds the Windows Media Player control.</span></span>

<span data-ttu-id="1a1b1-124">Você está livre para lidar com os comandos de script de URL no código JScript, assim como faria com os comandos de script personalizados.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-124">You are free to handle the URL script commands in your JScript code just as you would handle custom script commands.</span></span> <span data-ttu-id="1a1b1-125">Se você quiser que o controle do Windows Media Player ignore comandos de script de URL para que você possa tratá-los inteiramente por conta própria, defina as *configurações*. Propriedade **invokeURLs** como false no código de script ou usando um elemento param como descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-125">If you want the Windows Media Player control to ignore URL script commands so that you can handle them entirely by yourself, set the *Settings*.**invokeURLs** property to false either in script code or using a PARAM element as previously described.</span></span>

<span data-ttu-id="1a1b1-126">O exemplo a seguir ilustra um conjunto de quadros típico para inversão de URL.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-126">The following example illustrates a typical frameset for URL flipping.</span></span> <span data-ttu-id="1a1b1-127">Primeiro, crie uma página que descreva o conjunto de quadros:</span><span class="sxs-lookup"><span data-stu-id="1a1b1-127">First, create a page that describes the frameset:</span></span>


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



<span data-ttu-id="1a1b1-128">Em seguida, crie o arquivo player.html referenciado no conjunto de quadros usando o seguinte código (o arquivo video. wmv deve existir no mesmo diretório que os arquivos HTML):</span><span class="sxs-lookup"><span data-stu-id="1a1b1-128">Next, create the player.html file referenced in the frameset by using the following code (the video.wmv file is assumed to exist in the same directory as the HTML files):</span></span>


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



<span data-ttu-id="1a1b1-129">Se suas páginas da Web forem pequenas o suficiente para serem carregadas rapidamente, essa configuração poderá ser suficiente para suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-129">If your webpages are small enough to load rapidly, this setup may be sufficient for your needs.</span></span> <span data-ttu-id="1a1b1-130">Se, por outro lado, suas páginas da Web forem complexas, o streaming de mídia avançado poderá ser mais eficaz, dependendo da velocidade de conexão de seu público.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-130">If, on the other hand, your webpages are complex, rich media streaming may be more effective depending on the connection speed of your audience.</span></span>

> [!Note]  
> <span data-ttu-id="1a1b1-131">A inversão de URL não funciona corretamente com páginas exibidas no Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-131">URL flipping does not work correctly with pages viewed in Netscape Navigator.</span></span> <span data-ttu-id="1a1b1-132">Em vez de aparecer no quadro especificado por **DefaultFrame**, cada comando de script de URL recebido no navegador EXIBE a URL em uma nova janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="1a1b1-132">Instead of appearing in the frame specified by **defaultFrame**, each URL script command received in Navigator displays the URL in a new browser window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1a1b1-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a1b1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a1b1-134">**Criando Web-Based apresentações**</span><span class="sxs-lookup"><span data-stu-id="1a1b1-134">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="1a1b1-135">**Usando o script para controlar a inversão de URL**</span><span class="sxs-lookup"><span data-stu-id="1a1b1-135">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




