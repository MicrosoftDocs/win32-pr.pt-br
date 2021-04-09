---
title: Modificando a exibição
description: Modificando a exibição
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Playlists do metarquivo do Windows Media, modificando exibições
- listas de reprodução, modificando exibições
- listas de reprodução de metarquivo, modificando exibições
- Playlists do metarquivo do Windows Media, exibir modificação
- listas de reprodução, modificação de exibição
- listas de reprodução de metarquivo, modificação de exibição
- Windows Media Player, exibir modificação
- Windows Media Player, modificando vídeos
- Windows Media Player, propriedades de texto
- Windows Media Player, propriedades da imagem
- Windows Media Player, propriedades de MOREINFO
- Windows Media Player, texto ABSTRATO
- Propriedades de MOREINFO
- Texto ABSTRATO
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005304"
---
# <a name="modifying-the-display"></a><span data-ttu-id="61f5a-117">Modificando a exibição</span><span class="sxs-lookup"><span data-stu-id="61f5a-117">Modifying the Display</span></span>

<span data-ttu-id="61f5a-118">As listas de reprodução podem alterar a interface do usuário do Windows Media Player de quatro maneiras principais:</span><span class="sxs-lookup"><span data-stu-id="61f5a-118">Playlists can alter the Windows Media Player user interface in four main ways:</span></span>

-   <span data-ttu-id="61f5a-119">Propriedades de texto</span><span class="sxs-lookup"><span data-stu-id="61f5a-119">Text properties</span></span>
-   <span data-ttu-id="61f5a-120">Propriedades da imagem</span><span class="sxs-lookup"><span data-stu-id="61f5a-120">Image properties</span></span>
-   <span data-ttu-id="61f5a-121">Propriedades de MOREINFO</span><span class="sxs-lookup"><span data-stu-id="61f5a-121">MOREINFO properties</span></span>
-   <span data-ttu-id="61f5a-122">Texto ABSTRATO</span><span class="sxs-lookup"><span data-stu-id="61f5a-122">ABSTRACT text</span></span>

## <a name="text-properties"></a><span data-ttu-id="61f5a-123">Propriedades de texto</span><span class="sxs-lookup"><span data-stu-id="61f5a-123">Text properties</span></span>

<span data-ttu-id="61f5a-124">O Windows Media Player permite a exibição de texto de metadados de título, autor, direitos autorais e descrição.</span><span class="sxs-lookup"><span data-stu-id="61f5a-124">Windows Media Player enables the display of Title, Author, Copyright, and Description metadata text.</span></span> <span data-ttu-id="61f5a-125">Os metadados do clipe podem vir do fluxo ou do arquivo de mídia, ou podem vir de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="61f5a-125">Clip metadata can come from the stream or media file, or it can come from a playlist.</span></span> <span data-ttu-id="61f5a-126">Mostrar metadados vem da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="61f5a-126">Show metadata comes from the playlist.</span></span> <span data-ttu-id="61f5a-127">Em geral, as listas de reprodução são um método melhor de passar Propriedades de texto para o Windows Media Player, especialmente se os elementos de texto provavelmente forem alterados.</span><span class="sxs-lookup"><span data-stu-id="61f5a-127">In general, playlists are a better method of passing text properties to Windows Media Player, especially if text elements are likely to change.</span></span> <span data-ttu-id="61f5a-128">É mais fácil editar texto em uma lista de reprodução do que criar novamente um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="61f5a-128">It is easier to edit text in a playlist than to re-author a media file.</span></span> <span data-ttu-id="61f5a-129">E como as propriedades lidas de uma playlist substituem aquelas contidas no arquivo de mídia, você pode atualizar facilmente o texto de exibição adicionando o novo texto à propriedade correspondente em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="61f5a-129">And because properties read from a playlist override those contained in the media file, you can easily update display text by adding the new text to the corresponding property in a playlist.</span></span> <span data-ttu-id="61f5a-130">No exemplo a seguir, o texto dos metadados título e autor na playlist substitui o título e o texto do autor contidos no arquivo de mídia, Sample. WMA.</span><span class="sxs-lookup"><span data-stu-id="61f5a-130">In the following example, the text of the Title and Author metadata in the playlist overrides the Title and Author text contained in the media file, sample.wma.</span></span>

<span data-ttu-id="61f5a-131">O texto de **Descrição** é recuperado de um arquivo de mídia do Windows referenciado em um elemento de **entrada** , a menos que haja um elemento **abstract** em uma lista de reprodução de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="61f5a-131">**DESCRIPTION** text is retrieved from a Windows Media file referenced in an **ENTRY** element unless there is an **ABSTRACT** element in a metafile playlist.</span></span> <span data-ttu-id="61f5a-132">Se houver texto **abstrato** , ele será exibido, substituindo o texto de **Descrição** .</span><span class="sxs-lookup"><span data-stu-id="61f5a-132">If there is **ABSTRACT** text, it will be displayed, overriding the **DESCRIPTION** text.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a><span data-ttu-id="61f5a-133">Propriedades da imagem</span><span class="sxs-lookup"><span data-stu-id="61f5a-133">Image properties</span></span>

<span data-ttu-id="61f5a-134">Imagens de faixa podem ser adicionadas à interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="61f5a-134">Banner images can be added to the user interface of Windows Media Player.</span></span> <span data-ttu-id="61f5a-135">O elemento gráfico pode ser usado para anunciar, fornecer informações e fornecer acesso a sites, para citar algumas possibilidades.</span><span class="sxs-lookup"><span data-stu-id="61f5a-135">The graphic can be used for advertising, providing information, and providing access to websites, to name a few possibilities.</span></span>

<span data-ttu-id="61f5a-136">Use o elemento **banner** para especificar uma imagem gráfica (32 pixels de altura por 194 pixels de largura) para exibição pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="61f5a-136">Use the **BANNER** element to specify a graphic image (32 pixels high by 194 pixels wide) for display by Windows Media Player.</span></span> <span data-ttu-id="61f5a-137">O gráfico é exibido abaixo de qualquer conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="61f5a-137">The graphic is displayed below any video content.</span></span> <span data-ttu-id="61f5a-138">Um hiperlink pode ser adicionado à faixa usando o elemento filho **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="61f5a-138">A hyperlink can be added to the banner using the **MOREINFO** child element.</span></span>

<span data-ttu-id="61f5a-139">Uma dica de ferramenta pode ser definida por um elemento **abstrato** dentro do escopo do elemento de **faixa** .</span><span class="sxs-lookup"><span data-stu-id="61f5a-139">A ToolTip can be defined by an **ABSTRACT** element within the scope of the **BANNER** element.</span></span> <span data-ttu-id="61f5a-140">Qualquer texto de dica de ferramenta definido pode ser exibido pausando o ponteiro do mouse sobre o gráfico de faixa.</span><span class="sxs-lookup"><span data-stu-id="61f5a-140">Any defined ToolTip text can be displayed by pausing the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="61f5a-141">Selecionar o gráfico de faixa com o ponteiro do mouse ativará qualquer hiperlink definido com o elemento **moreinfo** .</span><span class="sxs-lookup"><span data-stu-id="61f5a-141">Selecting the banner graphic with the mouse pointer will activate any hyperlink defined with the **MOREINFO** element.</span></span>

<span data-ttu-id="61f5a-142">O formato de gráfico de **banner** preferencial é o formato GIF.</span><span class="sxs-lookup"><span data-stu-id="61f5a-142">The preferred **BANNER** graphics format is the GIF format.</span></span> <span data-ttu-id="61f5a-143">O formato JPG pode ser usado se o gráfico for dimensionado corretamente.</span><span class="sxs-lookup"><span data-stu-id="61f5a-143">The JPG format can be used if the graphic is properly sized.</span></span>

<span data-ttu-id="61f5a-144">O exemplo anterior ilustra o uso do elemento **banner** .</span><span class="sxs-lookup"><span data-stu-id="61f5a-144">The previous example illustrates use of the **BANNER** element.</span></span>

> [!Note]  
> <span data-ttu-id="61f5a-145">Não há suporte para imagens de **banner** com arquivos DRM ou quando o Windows Media Player está inserido em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="61f5a-145">**BANNER** images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

 

<span data-ttu-id="61f5a-146">Para obter mais informações sobre faixas, consulte [gráficos personalizados no Windows Media Player](custom-graphics-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="61f5a-146">For more information about banners, see [Custom Graphics in Windows Media Player](custom-graphics-in-windows-media-player.md).</span></span>

## <a name="moreinfo-properties"></a><span data-ttu-id="61f5a-147">Propriedades de MOREINFO</span><span class="sxs-lookup"><span data-stu-id="61f5a-147">MOREINFO properties</span></span>

<span data-ttu-id="61f5a-148">As áreas de texto e imagem da interface do usuário podem ser associadas a URLs.</span><span class="sxs-lookup"><span data-stu-id="61f5a-148">Text and image areas of the user interface can be associated with URLs.</span></span> <span data-ttu-id="61f5a-149">Durante a reprodução, os usuários podem selecionar uma dessas seções para se conectar à URL associada a ela no navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="61f5a-149">During playback, users can select one of these sections to connect to the URL associated with it in their Web browser.</span></span> <span data-ttu-id="61f5a-150">Por exemplo, você pode associar o site de um anunciante a uma imagem de faixa do AD, conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="61f5a-150">For example, you can associate an advertiser's website with an ad banner image as shown in the following code snippet.</span></span>


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a><span data-ttu-id="61f5a-151">Texto ABSTRATO</span><span class="sxs-lookup"><span data-stu-id="61f5a-151">ABSTRACT text</span></span>

<span data-ttu-id="61f5a-152">O texto **abstrato** é usado para exibir uma breve descrição de pop-up das áreas de texto ou imagem da interface do usuário à qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="61f5a-152">**ABSTRACT** text is used to display a short pop-up description of the text or image areas of the user interface it is associated with.</span></span> <span data-ttu-id="61f5a-153">Durante a reprodução, se o ponteiro do mouse focalizar uma dessas áreas, uma dica de ferramenta aparecerá ao lado do ponteiro do mouse exibindo o texto **abstrato** associado à área.</span><span class="sxs-lookup"><span data-stu-id="61f5a-153">During playback, if the mouse pointer hovers over one of these areas, a ToolTip appears beside the mouse pointer displaying the **ABSTRACT** text associated with the area.</span></span> <span data-ttu-id="61f5a-154">O texto **abstrato** é recuperado de um metarquivo e é definido com o elemento **abstract** .</span><span class="sxs-lookup"><span data-stu-id="61f5a-154">**ABSTRACT** text is retrieved from a metafile and is defined with the **ABSTRACT** element.</span></span> <span data-ttu-id="61f5a-155">O elemento **abstract** pode ser um elemento filho de uma **entrada** ou um elemento de **faixa** .</span><span class="sxs-lookup"><span data-stu-id="61f5a-155">The **ABSTRACT** element can be a child element of either an **ENTRY** or a **BANNER** element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61f5a-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61f5a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f5a-157">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="61f5a-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="61f5a-158">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="61f5a-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="61f5a-159">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="61f5a-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="61f5a-160">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="61f5a-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




