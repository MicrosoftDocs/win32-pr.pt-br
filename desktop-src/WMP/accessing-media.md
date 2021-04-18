---
title: Acessando mídia
description: Acessando mídia
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Playlists do metarquivo do Windows Media, acessando mídia
- listas de reprodução, acessando mídia
- listas de reprodução de metarquivo, acesso à mídia
- Playlists do metarquivo do Windows Media, acesso à mídia
- listas de reprodução, acesso à mídia
- listas de reprodução de metarquivo, acesso à mídia
- Playlists do metarquivo do Windows Media, controlando a reprodução
- listas de reprodução, controlando a reprodução
- listas de reprodução de metarquivo, controlando a reprodução
- Playlists do metarquivo do Windows Media, definindo a duração
- listas de reprodução, definindo a duração
- listas de reprodução de metarquivo, definindo duração
- Windows Media Player, acessando mídia
- Windows Media Player, acesso à mídia
- Windows Media Player, controlando a reprodução
- Windows Media Player, definindo a duração
- Acessando mídia
- acesso à mídia
- controlando a reprodução
- definindo a duração
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105794532"
---
# <a name="accessing-media"></a><span data-ttu-id="8e857-123">Acessando mídia</span><span class="sxs-lookup"><span data-stu-id="8e857-123">Accessing Media</span></span>

<span data-ttu-id="8e857-124">Use as listas de reprodução para especificar e controlar a mídia de streaming ou os arquivos de mídia que o Windows Media Player reproduz.</span><span class="sxs-lookup"><span data-stu-id="8e857-124">Use playlists to specify and to control the streaming media or media files that Windows Media Player plays.</span></span>

<span data-ttu-id="8e857-125">Use o elemento **entry** para especificar um único elemento de mídia (um arquivo de mídia ou uma transmissão ao vivo) e quaisquer elementos filho (como imagens, links **moreinfo** e texto **abstrato** ).</span><span class="sxs-lookup"><span data-stu-id="8e857-125">Use the **ENTRY** element to specify a single media element (a media file or a live stream) and any child elements (such as images, **MOREINFO** links, and **ABSTRACT** text).</span></span> <span data-ttu-id="8e857-126">Use um elemento **ENTRYREF** para especificar uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="8e857-126">Use an **ENTRYREF** element to specify a playlist.</span></span> <span data-ttu-id="8e857-127">Uma lista de reprodução pode conter um ou mais elementos de **entrada** ou **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="8e857-127">A playlist can contain one or more **ENTRY** or **ENTRYREF** elements.</span></span> <span data-ttu-id="8e857-128">O Windows Media Player executa uma lista de reprodução iniciando com a primeira entrada e, em seguida, executando cada entrada por vez até que a lista seja concluída.</span><span class="sxs-lookup"><span data-stu-id="8e857-128">Windows Media Player executes a playlist by starting with the first entry and then playing each entry in turn until the list is finished.</span></span>

<span data-ttu-id="8e857-129">Um elemento de **entrada** pode apontar para qualquer tipo de mídia que o Windows Media Player possa reproduzir.</span><span class="sxs-lookup"><span data-stu-id="8e857-129">An **ENTRY** element can point to any type of media that Windows Media Player can play.</span></span> <span data-ttu-id="8e857-130">Isso inclui não apenas arquivos. WMA,. wmv,. ASF e. avi, para citar alguns, mas também fluxos ao vivo.</span><span class="sxs-lookup"><span data-stu-id="8e857-130">This includes not only .wma, .wmv, .asf, and .avi files, to name a few, but live streams as well.</span></span> <span data-ttu-id="8e857-131">Usando uma série de elementos **entry** ou **ENTRYREF** para fazer referência ao conteúdo de mídia, você pode usar uma lista de reprodução para enviar um único fluxo que consiste em várias fontes.</span><span class="sxs-lookup"><span data-stu-id="8e857-131">By using a series of **ENTRY** or **ENTRYREF** elements to reference media content, you can use a playlist to send a single stream that consists of multiple sources.</span></span> <span data-ttu-id="8e857-132">Os fluxos referenciados serão executados em sequência e vistos como um fluxo contínuo pelo Visualizador.</span><span class="sxs-lookup"><span data-stu-id="8e857-132">The referenced streams will play sequentially and be seen as one continuous stream by the viewer.</span></span> <span data-ttu-id="8e857-133">Por exemplo, a lista de reprodução pode conter dois elementos de **entrada** : uma introdução padrão de um arquivo de mídia do Windows com uma extensão. WMA e um fluxo do Windows Media ao vivo.</span><span class="sxs-lookup"><span data-stu-id="8e857-133">For example, the playlist can contain two **ENTRY** elements: a standard introduction from a Windows Media file with a .wma extension, and a live Windows Media stream.</span></span>

> [!Note]  
> <span data-ttu-id="8e857-134">Uma lista de reprodução não deve conter links para arquivos de mídia que tenham conteúdo criado com versões diferentes do DRM (Rights Management digital).</span><span class="sxs-lookup"><span data-stu-id="8e857-134">A playlist must not contain links to media files that have content created with different versions of Digital Rights Management (DRM).</span></span> <span data-ttu-id="8e857-135">Em uma lista de reprodução de metarquivo, se houver links para arquivos de mídia com conteúdo DRM versão 1 e para arquivos de mídia criados com versões posteriores do DRM, o Windows Media Player só executará o conteúdo do DRM versão 1.</span><span class="sxs-lookup"><span data-stu-id="8e857-135">In a metafile playlist, if there are links for media files with DRM version 1 content and for media files created with later DRM versions, Windows Media Player will only play the DRM version 1 content.</span></span>

 

## <a name="controlling-playback"></a><span data-ttu-id="8e857-136">Controlando a reprodução</span><span class="sxs-lookup"><span data-stu-id="8e857-136">Controlling Playback</span></span>

<span data-ttu-id="8e857-137">Use as listas de reprodução para controlar não apenas quais clipes de mídia são reproduzidos, mas também quais partes do clipe são reproduzidas e como.</span><span class="sxs-lookup"><span data-stu-id="8e857-137">Use playlists to control not only which media clip is played, but also which portions of the clip are played and how.</span></span> <span data-ttu-id="8e857-138">Você pode usar as listas de reprodução para definir um conjunto de clipes a serem em loop ou repetidos, para definir a duração da reprodução e para atribuir horários de início e marcadores de início e término para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="8e857-138">You can use playlists to define a set of clips to be looped or repeated, to set the duration of play, and to assign start times, and start and end markers for each entry.</span></span> <span data-ttu-id="8e857-139">Os elementos **StartTime**, **STARTMARKER** e **endmarcer** funcionam em conjunto com marcadores no arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8e857-139">The **STARTTIME**, **STARTMARKER**, and **ENDMARKER** elements work in conjunction with markers in the media file.</span></span>

<span data-ttu-id="8e857-140">Por exemplo, a lista de reprodução a seguir usa uma faixa de anúncio e o link **moreinfo** associado em uma **entrada** e faz referência a um **STARTMARKER** e um **endmarcer**.</span><span class="sxs-lookup"><span data-stu-id="8e857-140">For example, the following playlist uses an ad banner and the associated **MOREINFO** link in one **ENTRY**, and references a **STARTMARKER** and **ENDMARKER**.</span></span>


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a><span data-ttu-id="8e857-141">Definindo a duração</span><span class="sxs-lookup"><span data-stu-id="8e857-141">Setting Duration</span></span>

<span data-ttu-id="8e857-142">Use o elemento **Duration** para especificar por quanto tempo reproduzir um clipe ou conjunto de clipes.</span><span class="sxs-lookup"><span data-stu-id="8e857-142">Use the **DURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="8e857-143">Você também pode usar o atributo **PREviewmode** do elemento **ASX** em conjunto com o elemento **PREVIEWDURATION** para especificar por quanto tempo um clipe ou conjunto de clipes deve ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="8e857-143">You can also use the **PREVIEWMODE** attribute of the **ASX** element in conjunction with the **PREVIEWDURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="8e857-144">Defina o atributo **PREviewmode** como Sim para usar o elemento **PREVIEWDURATION** para especificar por quanto tempo o clipe associado será reproduzido.</span><span class="sxs-lookup"><span data-stu-id="8e857-144">Set the **PREVIEWMODE** attribute to YES to use the **PREVIEWDURATION** element to specify how long to play the associated clip.</span></span> <span data-ttu-id="8e857-145">Os elementos **PREVIEWDURATION** e **Duration** têm o mesmo comportamento.</span><span class="sxs-lookup"><span data-stu-id="8e857-145">The **PREVIEWDURATION** and **DURATION** elements have the same behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e857-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e857-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e857-147">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="8e857-147">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="8e857-148">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="8e857-148">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="8e857-149">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8e857-149">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8e857-150">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8e857-150">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




