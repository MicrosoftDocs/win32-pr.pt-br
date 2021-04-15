---
title: Usando listas de reprodução automáticas para organizar o conteúdo na biblioteca
description: Usando listas de reprodução automáticas para organizar o conteúdo na biblioteca
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Lojas online do Windows Media Player, listas de reprodução automáticas
- lojas online, listas de reprodução automáticas
- Digite 1 lojas online, listas de reprodução automáticas
- tipo 2 lojas online, listas de reprodução automáticas
- Lojas online do Windows Media Player, organizando o conteúdo da biblioteca
- lojas online, organizando o conteúdo da biblioteca
- Digite 1 lojas online, organizando o conteúdo da biblioteca
- Digite 2 lojas online, organizando o conteúdo da biblioteca
- Lojas online do Windows Media Player, organização de conteúdo de biblioteca
- lojas online, organização de conteúdo de biblioteca
- Digite 1 lojas online, organização de conteúdo de biblioteca
- Digite 2 lojas online, organização de conteúdo de biblioteca
- biblioteca, organizando conteúdo
- organizando o conteúdo da biblioteca
- playlists automáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498736"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a><span data-ttu-id="2873a-118">Usando listas de reprodução automáticas para organizar o conteúdo na biblioteca</span><span class="sxs-lookup"><span data-stu-id="2873a-118">Using Auto Playlists to Organize Content in the Library</span></span>

<span data-ttu-id="2873a-119">Você pode usar listas de reprodução automáticas para organizar o conteúdo premium fornecido por você.</span><span class="sxs-lookup"><span data-stu-id="2873a-119">You can use auto playlists to organize premium content you provide.</span></span> <span data-ttu-id="2873a-120">Por exemplo, você pode usar o Windows Media Player para criar uma lista de reprodução automática que contém apenas o conteúdo que você forneceu tendo uma classificação de usuário de pelo menos quatro estrelas.</span><span class="sxs-lookup"><span data-stu-id="2873a-120">For example, you could use Windows Media Player to create an auto playlist that contains only content you provided having a user rating of at least four stars.</span></span> <span data-ttu-id="2873a-121">Em seguida, você pode adicionar a lista de reprodução automática à biblioteca no Windows Media Player para que ela seja exibida no nó músicas adquiridas no nó distribuidor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2873a-121">You can then add the auto playlist to the library in Windows Media Player so that it displays in the Purchased Music node under your content distributor node.</span></span>

<span data-ttu-id="2873a-122">Para fazer isso, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="2873a-122">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="2873a-123">Crie a lista de reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="2873a-123">Create the auto playlist.</span></span>
2.  <span data-ttu-id="2873a-124">Usando o Windows Explorer, navegue até a lista de reprodução automática e recupere o arquivo. wpl.</span><span class="sxs-lookup"><span data-stu-id="2873a-124">Using Windows Explorer, browse to the auto playlist and retrieve the .wpl file.</span></span>
3.  <span data-ttu-id="2873a-125">Usando o modelo de objeto do Windows Media Player, adicione a lista de reprodução automática à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2873a-125">Using the Windows Media Player object model, add the auto playlist to the library.</span></span>
4.  <span data-ttu-id="2873a-126">Defina o atributo **WM/ContentDistributor** da lista de reprodução para o nome da chave do distribuidor de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2873a-126">Set the **WM/ContentDistributor** attribute for the playlist to your content distributor key name.</span></span>
5.  <span data-ttu-id="2873a-127">Defina o atributo **SyncOnly** para a lista de reprodução como true.</span><span class="sxs-lookup"><span data-stu-id="2873a-127">Set the **SyncOnly** attribute for the playlist to true.</span></span>

<span data-ttu-id="2873a-128">O código de exemplo do JScript a seguir mostra uma função que adiciona uma lista de reprodução automática chamada "visitas favoritas" ao nó da Proseware na biblioteca:</span><span class="sxs-lookup"><span data-stu-id="2873a-128">The following JScript example code shows a function that adds an auto playlist named "Favorite Hits" to the Proseware node in the library:</span></span>


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a><span data-ttu-id="2873a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2873a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2873a-130">Sobre a integração de biblioteca</span><span class="sxs-lookup"><span data-stu-id="2873a-130">About Library Integration</span></span>](download-manager-overview.md)
</dt> <dt>

[<span data-ttu-id="2873a-131">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="2873a-131">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2873a-132">**Mediacollection. adicionar**</span><span class="sxs-lookup"><span data-stu-id="2873a-132">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="2873a-133">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="2873a-133">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="2873a-134">**Listas de reprodução estáticas e automáticas**</span><span class="sxs-lookup"><span data-stu-id="2873a-134">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> <dt>

[<span data-ttu-id="2873a-135">**Atributo SyncOnly**</span><span class="sxs-lookup"><span data-stu-id="2873a-135">**SyncOnly Attribute**</span></span>](synconly-attribute.md)
</dt> <dt>

[<span data-ttu-id="2873a-136">**Atributo WM/ContentDistributor**</span><span class="sxs-lookup"><span data-stu-id="2873a-136">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="2873a-137">**Trabalhando com a biblioteca**</span><span class="sxs-lookup"><span data-stu-id="2873a-137">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




