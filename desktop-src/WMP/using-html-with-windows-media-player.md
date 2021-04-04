---
title: Usando HTML com o Windows Media Player
description: Usando HTML com o Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Windows Media Player, HTML
- Modelo de objeto do Windows Media Player, HTML
- modelo de objeto, HTML
- Controle ActiveX do Windows Media Player, HTML para modelo de objeto
- Controle ActiveX, HTML para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, HTML para modelo de objeto
- Windows Media Player Mobile, HTML para modelo de objeto
- HTML com o Windows Media Player
- Inserção de página da Web, HTML
- inserindo, páginas da Web
- comandos de script
- Inversão de URL
- streaming de mídia avançada
- suporte a navegador
- exibindo páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822691"
---
# <a name="using-html-with-windows-media-player"></a><span data-ttu-id="02bbb-118">Usando HTML com o Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="02bbb-118">Using HTML with Windows Media Player</span></span>

## <a name="overview"></a><span data-ttu-id="02bbb-119">Visão geral</span><span class="sxs-lookup"><span data-stu-id="02bbb-119">Overview</span></span>

<span data-ttu-id="02bbb-120">O uso de HTML com o Windows Media Player é uma excelente maneira de combinar áudio e vídeo com texto e gráficos.</span><span class="sxs-lookup"><span data-stu-id="02bbb-120">Using HTML with Windows Media Player is an excellent way to combine audio and video with text and graphics.</span></span> <span data-ttu-id="02bbb-121">Você pode inserir o controle do Windows Media Player em uma página da Web quando desejar complementar seu conteúdo estático ou criar aplicativos da Internet com mídia digital.</span><span class="sxs-lookup"><span data-stu-id="02bbb-121">You can embed the Windows Media Player control in a webpage when you want to supplement your static content or create Web applications with digital media.</span></span> <span data-ttu-id="02bbb-122">Quando você deseja complementar sua mídia digital com HTML, por outro lado, você pode exibir páginas da Web no modo completo do Player referenciando-as nas listas de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02bbb-122">When you want to supplement your digital media with HTML, on the other hand, you can display webpages in the full mode of the Player by referencing them in Windows Media metafile playlists.</span></span>

<span data-ttu-id="02bbb-123">Se você escrever programas personalizados que incorporam o controle do Windows Media Player no modo remoto, também poderá controlar as páginas da Web exibidas nos vários painéis do modo completo do Player quando os usuários desencaixam o controle.</span><span class="sxs-lookup"><span data-stu-id="02bbb-123">If you write custom programs that embed the Windows Media Player control in remote mode, you can also control the webpages displayed in the various panes of the full mode of the Player when your users undock the control.</span></span> <span data-ttu-id="02bbb-124">Isso permite preservar a continuidade entre os Estados encaixados e desencaixados.</span><span class="sxs-lookup"><span data-stu-id="02bbb-124">This lets you preserve continuity between the docked and undocked states.</span></span>

## <a name="web-embedding"></a><span data-ttu-id="02bbb-125">Inserção na Web</span><span class="sxs-lookup"><span data-stu-id="02bbb-125">Web Embedding</span></span>

<span data-ttu-id="02bbb-126">Você pode usar o controle do Windows Media Player como parte de uma página da Web criada por você.</span><span class="sxs-lookup"><span data-stu-id="02bbb-126">You can use the Windows Media Player control as part of a webpage you create.</span></span> <span data-ttu-id="02bbb-127">Consulte [inserindo o controle do Windows Media Player em uma página da Web](embedding-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="02bbb-127">See [Embedding the Windows Media Player Control in a Web Page](embedding-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="script-commands-and-url-flipping"></a><span data-ttu-id="02bbb-128">Comandos de script e inversão de URL</span><span class="sxs-lookup"><span data-stu-id="02bbb-128">Script Commands and URL Flipping</span></span>

<span data-ttu-id="02bbb-129">Comandos de script são pares de texto/valor que você pode inserir em seus arquivos de mídia digital ou fluxos.</span><span class="sxs-lookup"><span data-stu-id="02bbb-129">Script commands are text/value pairs you can embed in your digital media files or streams.</span></span> <span data-ttu-id="02bbb-130">Você pode usar comandos de script personalizados exclusivamente para disparar código de script, enquanto permite que o Windows Media Player manipule outros comandos de script automaticamente.</span><span class="sxs-lookup"><span data-stu-id="02bbb-130">You might use custom script commands solely to trigger script code, while letting Windows Media Player handle other script commands automatically.</span></span>

<span data-ttu-id="02bbb-131">Quando você tem várias páginas da Web que acompanham uma apresentação de mídia digital, os comandos de script de URL podem alterar automaticamente a página em um quadro enquanto o controle do Windows Media Player continua a reproduzir mídia digital em outro quadro.</span><span class="sxs-lookup"><span data-stu-id="02bbb-131">When you have several webpages that accompany a digital media presentation, URL script commands can automatically change the page in one frame while the Windows Media Player control continues playing digital media in another frame.</span></span> <span data-ttu-id="02bbb-132">Isso é chamado de inversão de URL e é uma maneira excelente de criar uma apresentação de slides multimídia.</span><span class="sxs-lookup"><span data-stu-id="02bbb-132">This is called URL flipping, and is an excellent way to create a multimedia slide show.</span></span> <span data-ttu-id="02bbb-133">Outros comandos de script manipulados automaticamente permitem alternar a reprodução para um arquivo de mídia ou fluxo diferente, exibir texto de legenda ou disparar eventos como inserções de anúncios definidas em uma lista de reprodução do metarquivo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02bbb-133">Other automatically handled script commands let you switch playback to a different media file or stream, display captioning text, or trigger events such as ad insertions defined in a Windows Media metafile playlist.</span></span>

<span data-ttu-id="02bbb-134">Para obter mais informações sobre a inversão de URL, consulte [Creating Web-Based Presentations](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="02bbb-134">For more information about URL flipping, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="rich-media-streaming"></a><span data-ttu-id="02bbb-135">Streaming de mídia avançada</span><span class="sxs-lookup"><span data-stu-id="02bbb-135">Rich Media Streaming</span></span>

<span data-ttu-id="02bbb-136">A inversão de URL funciona melhor com páginas simples que são carregadas rapidamente.</span><span class="sxs-lookup"><span data-stu-id="02bbb-136">URL flipping works best with simple pages that load rapidly.</span></span> <span data-ttu-id="02bbb-137">Com páginas mais complexas, vários componentes são transferidos individualmente, dificultando a sincronização da exibição de página com mídia digital.</span><span class="sxs-lookup"><span data-stu-id="02bbb-137">With more complex pages, multiple components are transferred individually, making it difficult to synchronize page display with digital media.</span></span> <span data-ttu-id="02bbb-138">Para permitir apresentações de mídia sofisticadas complexas, as páginas da Web podem ser adicionadas a um fluxo de mídia e entregues ao Player da mesma maneira que áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="02bbb-138">To allow complex rich media presentations, webpages can be added to a media stream and delivered to the Player in the same way as audio and video.</span></span> <span data-ttu-id="02bbb-139">Isso permite que você sincronize os componentes da sua apresentação com muito mais facilidade, especialmente em conexões de baixa velocidade.</span><span class="sxs-lookup"><span data-stu-id="02bbb-139">This lets you synchronize the components of your presentation much more easily, especially over low-speed connections.</span></span>

<span data-ttu-id="02bbb-140">Para obter mais informações sobre streaming de mídia avançada, consulte [criando Web-Based apresentações](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="02bbb-140">For more information about rich media streaming, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="browser-support"></a><span data-ttu-id="02bbb-141">Suporte do navegador</span><span class="sxs-lookup"><span data-stu-id="02bbb-141">Browser Support</span></span>

<span data-ttu-id="02bbb-142">Você pode inserir o controle do Windows Media Player no Microsoft Internet Explorer, no Firefox e no Netscape Navigator, embora o processo seja um pouco diferente para cada um.</span><span class="sxs-lookup"><span data-stu-id="02bbb-142">You can embed the Windows Media Player control in Microsoft Internet Explorer, Firefox, and Netscape Navigator, although the process is slightly different for each.</span></span> <span data-ttu-id="02bbb-143">Você também pode criar páginas da Web projetadas para funcionar com todos os três navegadores.</span><span class="sxs-lookup"><span data-stu-id="02bbb-143">You can also create webpages designed to work with all three browsers.</span></span>

<span data-ttu-id="02bbb-144">Com o Internet Explorer e o Firefox, você insere o controle usando o elemento de objeto HTML.</span><span class="sxs-lookup"><span data-stu-id="02bbb-144">With Internet Explorer and Firefox, you embed the control using the HTML OBJECT element.</span></span> <span data-ttu-id="02bbb-145">O navegador requer uma abordagem diferente, no entanto, porque ele não oferece suporte diretamente a controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="02bbb-145">Navigator requires a different approach, however, because it doesn't directly support ActiveX controls.</span></span> <span data-ttu-id="02bbb-146">Com o navegador, você usa o elemento APPLET para inserir um miniaplicativo Java especial na página.</span><span class="sxs-lookup"><span data-stu-id="02bbb-146">With Navigator, you use the APPLET element to embed a special Java applet into the page.</span></span> <span data-ttu-id="02bbb-147">Este applet manipula a comunicação com o controle ActiveX do Player.</span><span class="sxs-lookup"><span data-stu-id="02bbb-147">This applet handles communication with the Player ActiveX control.</span></span>

<span data-ttu-id="02bbb-148">Para obter mais informações sobre o suporte do Firefox, consulte [usando o controle do Windows Media Player com o Firefox](using-the-windows-media-player-control-with-firefox.md).</span><span class="sxs-lookup"><span data-stu-id="02bbb-148">For more information about Firefox support, see [Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).</span></span>

<span data-ttu-id="02bbb-149">Para obter mais informações sobre o suporte ao Netscape Navigator, consulte [usando o Windows Media Player com o Netscape 7,1](using-windows-media-player-with-netscape-7-1.md).</span><span class="sxs-lookup"><span data-stu-id="02bbb-149">For more information about Netscape Navigator support, see [Using Windows Media Player with Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).</span></span>

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a><span data-ttu-id="02bbb-150">Exibindo páginas da Web no modo completo do Player</span><span class="sxs-lookup"><span data-stu-id="02bbb-150">Displaying Web Pages in the Full Mode of the Player</span></span>

<span data-ttu-id="02bbb-151">Você pode estender a funcionalidade do Windows Media Player ou fornecer uma exibição personalizada das informações que acompanham a mídia digital exibindo páginas da Web no modo completo do Player.</span><span class="sxs-lookup"><span data-stu-id="02bbb-151">You can extend the functionality of Windows Media Player or provide a custom view of information that accompanies your digital media by displaying webpages in the full mode of the Player.</span></span> <span data-ttu-id="02bbb-152">Esse é o recurso HTMLView de metaarquivos do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02bbb-152">This is the HTMLView feature of Windows Media metafiles.</span></span> <span data-ttu-id="02bbb-153">Os metaarquivos oferecem um grande controle sobre o conteúdo da lista de reprodução, permitindo que você faça a transição diretamente entre os clipes, insira anúncios e exiba imagens ainda no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="02bbb-153">Metafiles give you great control over playlist content, allowing you to seamlessly transition between clips, insert advertisements, and display still images in Windows Media Player.</span></span> <span data-ttu-id="02bbb-154">Para exibir as páginas da Web no modo completo do Player, use o elemento PARAM para adicionar referências de URL às suas entradas de playlist ou a listas de reprodução inteiras.</span><span class="sxs-lookup"><span data-stu-id="02bbb-154">To display webpages in the full mode of the Player, you use the PARAM element to add URL references to your playlist entries or to entire playlists.</span></span>

<span data-ttu-id="02bbb-155">Para obter mais informações sobre o uso de páginas da Web em metaarquivos, consulte [exibindo páginas da Web no Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="02bbb-155">For more information about using webpages in metafiles, see [Displaying Web Pages in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02bbb-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02bbb-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02bbb-157">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="02bbb-157">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




