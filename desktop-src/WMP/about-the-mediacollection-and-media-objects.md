---
title: Sobre o Mediacollection e os objetos de mídia
description: Sobre o Mediacollection e os objetos de mídia
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player, objeto Mediacollection
- Modelo de objeto do Windows Media Player, objeto Mediacollection
- modelo de objeto, objeto Mediacollection
- Controle ActiveX do Windows Media Player, objeto Mediacollection
- Controle ActiveX, objeto Mediacollection
- Controle ActiveX móvel do Windows Media Player, objeto Mediacollection
- Windows Media Player Mobile, objeto Mediacollection
- Objeto mediacollection
- Windows Media Player, objeto de mídia
- Modelo de objeto do Windows Media Player, objeto de mídia
- modelo de objeto, objeto de mídia
- Controle ActiveX do Windows Media Player, objeto de mídia
- Controle ActiveX, objeto de mídia
- Controle ActiveX móvel do Windows Media Player, objeto de mídia
- Windows Media Player Mobile, objeto de mídia
- Objeto de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763389"
---
# <a name="about-the-mediacollection-and-media-objects"></a><span data-ttu-id="b4c59-119">Sobre o Mediacollection e os objetos de mídia</span><span class="sxs-lookup"><span data-stu-id="b4c59-119">About the MediaCollection and Media Objects</span></span>

<span data-ttu-id="b4c59-120">O **mediacollection** e os objetos de **mídia** regem a coleção de mídias, que define os locais de arquivos de mídia digital que o Windows Media Player pode acessar.</span><span class="sxs-lookup"><span data-stu-id="b4c59-120">The **MediaCollection** and **Media** objects govern the media collection, which defines the locations of digital media files that Windows Media Player can access.</span></span> <span data-ttu-id="b4c59-121">Você Obtém o objeto **mediacollection** da propriedade **mediacollection** do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="b4c59-121">You get the **MediaCollection** object from the **mediaCollection** property of the **Player** object.</span></span> <span data-ttu-id="b4c59-122">A propriedade **mediacollection** retorna o objeto **mediacollection** .</span><span class="sxs-lookup"><span data-stu-id="b4c59-122">The **mediaCollection** property returns the **MediaCollection** object.</span></span> <span data-ttu-id="b4c59-123">Você só pode acessar as propriedades do objeto **mediacollection** depois de criá-lo.</span><span class="sxs-lookup"><span data-stu-id="b4c59-123">You can only access the properties of the **MediaCollection** object after you have created it.</span></span> <span data-ttu-id="b4c59-124">Por exemplo, para adicionar um objeto de **mídia** (uma música), use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="b4c59-124">For example, to add a **Media** object (a song), use the following code:</span></span>


```C++
player.mediacollection.add('laure.wma');

```



<span data-ttu-id="b4c59-125">Você adicionou o arquivo Laure. WMA à coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="b4c59-125">You have added the file laure.wma to the media collection.</span></span>

<span data-ttu-id="b4c59-126">Você pode obter o objeto de **mídia** atual usando a propriedade **currentMedia** do **Player**.</span><span class="sxs-lookup"><span data-stu-id="b4c59-126">You can get the current **Media** object by using the **currentMedia** property of the **Player**.</span></span> <span data-ttu-id="b4c59-127">Por exemplo, esse código obtém a propriedade **Duration** do objeto de **mídia** atual:</span><span class="sxs-lookup"><span data-stu-id="b4c59-127">For example, this code gets the **duration** property of the current **Media** object:</span></span>


```C++
myduration = player.currentmedia.duration;

```



<span data-ttu-id="b4c59-128">Há várias maneiras de obter um objeto de **mídia** para que você possa acessar suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b4c59-128">There are many ways to get a **Media** object so that you can access its properties.</span></span> <span data-ttu-id="b4c59-129">Por exemplo, se você quiser acessar a propriedade **Duration** da mídia atual, cada uma das linhas de código a seguir poderá ser usada.</span><span class="sxs-lookup"><span data-stu-id="b4c59-129">For example, if you want to access the **duration** property of the current media, each of the following lines of code could be used.</span></span>

<span data-ttu-id="b4c59-130">Para obter a duração da mídia em execução no momento:</span><span class="sxs-lookup"><span data-stu-id="b4c59-130">To get the duration of the currently playing media:</span></span>


```C++
player.currentMedia.duration;

```



<span data-ttu-id="b4c59-131">Para obter a duração da mídia atual em uma lista de reprodução:</span><span class="sxs-lookup"><span data-stu-id="b4c59-131">To get the duration of the current media in a playlist:</span></span>


```C++
player.controls.currentItem.duration;

```



<span data-ttu-id="b4c59-132">Para obter a duração do terceiro item de mídia em uma lista de reprodução:</span><span class="sxs-lookup"><span data-stu-id="b4c59-132">To get the duration of the third media item in a playlist:</span></span>


```C++
player.currentPlaylist.item(2).duration;

```



<span data-ttu-id="b4c59-133">Para obter a duração do terceiro item de mídia em um gênero "Jazz":</span><span class="sxs-lookup"><span data-stu-id="b4c59-133">To get the duration of the third media item in a "Jazz" genre:</span></span>


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



<span data-ttu-id="b4c59-134">Para obter a duração do terceiro item de mídia na segunda Playlist:</span><span class="sxs-lookup"><span data-stu-id="b4c59-134">To get the duration of the third media item in the second playlist:</span></span>


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a><span data-ttu-id="b4c59-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4c59-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4c59-136">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="b4c59-136">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b4c59-137">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="b4c59-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="b4c59-138">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="b4c59-138">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




