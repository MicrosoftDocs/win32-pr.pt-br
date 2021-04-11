---
title: Uma lista de reprodução de estação de rádio de exemplo
description: Uma lista de reprodução de estação de rádio de exemplo
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Listas de reprodução do metarquivo do Windows Media, exemplos de playlist
- listas de reprodução, exemplos de playlist
- listas de reprodução de metarquivo, exemplos de playlist
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, exemplos de listas de reprodução
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, listas de reprodução de exemplo
- listas de reprodução, listas de reprodução de exemplo
- listas de reprodução de metarquivo, listas de reprodução de exemplo
- Playlists do metarquivo do Windows Media, exemplo de código
- listas de reprodução, exemplo de código
- listas de reprodução de metarquivo, exemplo de código
- Playlists do metarquivo do Windows Media, exemplo de playlist de estação de rádio
- listas de reprodução, exemplo de playlist de estação de rádio
- listas de reprodução de metarquivo, exemplo de playlist de estação de rádio
- Exemplos do Windows Media Player, playlist
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, listas de reprodução de exemplo
- Windows Media Player, exemplo de playlist de estação de rádio
- exemplos de playlist
- exemplos de playlist
- listas de reprodução de exemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363878"
---
# <a name="an-example-radio-station-playlist"></a><span data-ttu-id="64344-125">Uma lista de reprodução de estação de rádio de exemplo</span><span class="sxs-lookup"><span data-stu-id="64344-125">An Example Radio Station Playlist</span></span>

<span data-ttu-id="64344-126">O código de exemplo a seguir ilustra como criar uma lista de reprodução para digitalizar três estações de rádio de rock.</span><span class="sxs-lookup"><span data-stu-id="64344-126">The following example code illustrates how to create a playlist to scan three rock radio stations.</span></span> <span data-ttu-id="64344-127">A marca de rádio da empresa fictícia Adventure Works está na lista de reprodução e em todos os fluxos individuais na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="64344-127">The fictitious company Adventure Works Radio brand is on the playlist and on all of the individual streams within the playlist.</span></span> <span data-ttu-id="64344-128">Ao escrever seu código, altere todas as URLs e nomes de arquivo para nomes de arquivo válidos que sejam acessíveis ao seu Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="64344-128">When you write your code, change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="64344-129">Uma playlist é criada para cada uma das estações.</span><span class="sxs-lookup"><span data-stu-id="64344-129">A playlist is created for each of the stations.</span></span> <span data-ttu-id="64344-130">Uma quarta lista de reprodução examina as três primeiras.</span><span class="sxs-lookup"><span data-stu-id="64344-130">A fourth playlist scans through the first three.</span></span> <span data-ttu-id="64344-131">As listas de reprodução são criadas para referenciar anúncios gerados dinamicamente e ter a identidade visual de rádio da Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="64344-131">The playlists are created to reference dynamically generated advertisements and have Adventure Works Radio branding.</span></span>

<span data-ttu-id="64344-132">Uma das listas de reprodução que representam uma estação de rádio pode ser parecida com esta.</span><span class="sxs-lookup"><span data-stu-id="64344-132">One of the playlists representing a radio station might look like this.</span></span>


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="64344-133">A lista de reprodução pode ser construída de referências para as listas de reprodução individuais.</span><span class="sxs-lookup"><span data-stu-id="64344-133">The playlist can then be constructed of references to the individual playlists.</span></span>

<span data-ttu-id="64344-134">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="64344-134">Example Code</span></span>


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



<span data-ttu-id="64344-135">Este exemplo deve reproduzir um anúncio seguido de 30 segundos de cada uma das três estações referenciadas, uma após a outra.</span><span class="sxs-lookup"><span data-stu-id="64344-135">This example would play an ad followed by 30 seconds of each of the three stations referenced, one after the other.</span></span> <span data-ttu-id="64344-136">Este ciclo será repetido indefinidamente porque o atributo **Count** do elemento **REPEAT** não está definido.</span><span class="sxs-lookup"><span data-stu-id="64344-136">This cycle will repeat indefinitely because the **COUNT** attribute of the **REPEAT** element is not defined.</span></span>

-   <span data-ttu-id="64344-137">Os exemplos de empresas, organizações, produtos, pessoas e eventos aqui descritos são fictícios.</span><span class="sxs-lookup"><span data-stu-id="64344-137">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="64344-138">Nenhuma associação com qualquer empresa, organização, produto, pessoa ou evento real é intencional nem deve ser presumida.</span><span class="sxs-lookup"><span data-stu-id="64344-138">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64344-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64344-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64344-140">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="64344-140">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="64344-141">**Exemplos de playlist**</span><span class="sxs-lookup"><span data-stu-id="64344-141">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="64344-142">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="64344-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="64344-143">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="64344-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="64344-144">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="64344-144">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




