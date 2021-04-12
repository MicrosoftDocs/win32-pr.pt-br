---
title: Listas de reprodução estáticas e automáticas
description: Listas de reprodução estáticas e automáticas
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, estáticas
- listas de reprodução de metarquivo, estáticos
- Playlists do metarquivo do Windows Media, estáticos
- listas de reprodução estáticas
- playlists automáticas
- listas de reprodução, automática
- listas de reprodução de metarquivo, automática
- Playlists do metarquivo do Windows Media, automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363745"
---
# <a name="static-and-auto-playlists"></a><span data-ttu-id="6db73-118">Listas de reprodução estáticas e automáticas</span><span class="sxs-lookup"><span data-stu-id="6db73-118">Static and Auto Playlists</span></span>

<span data-ttu-id="6db73-119">Há dois tipos de listas de reprodução:</span><span class="sxs-lookup"><span data-stu-id="6db73-119">There are two types of playlists:</span></span>

-   <span data-ttu-id="6db73-120">Listas de reprodução estáticas, que incluem itens de mídia específicos</span><span class="sxs-lookup"><span data-stu-id="6db73-120">Static playlists, which include specific media items</span></span>
-   <span data-ttu-id="6db73-121">Listas de reprodução automáticas, que pesquisam a biblioteca toda vez que são abertas e podem conter itens de mídia diferentes em momentos diferentes.</span><span class="sxs-lookup"><span data-stu-id="6db73-121">Auto playlists, which search the library every time they are opened and may contain different media items at different times.</span></span> <span data-ttu-id="6db73-122">Uma lista de reprodução automática é o resultado de uma consulta de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6db73-122">An auto playlist is the result of a database query.</span></span>

<span data-ttu-id="6db73-123">Para importar uma lista de reprodução estática de um metarquivo, primeiro chame *Player*. **newPlaylist** para criar um objeto de **lista de reprodução** com base nos dados no metarquivo e, em seguida, passar esse objeto para *playlistcollection*. **importPlaylist** para adicionar a lista de reprodução à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6db73-123">To import a static playlist from a metafile, first call *Player*.**newPlaylist** to create a **Playlist** object based on the data in the metafile, and then pass that object to *PlaylistCollection*.**importPlaylist** to add the playlist to the library.</span></span>

<span data-ttu-id="6db73-124">Para importar uma lista de reprodução automática de um metarquivo, use *mediacollection*. **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="6db73-124">To import an auto playlist from a metafile, use *MediaCollection*.**add**.</span></span> <span data-ttu-id="6db73-125">Para obter mais informações, consulte [playlists e o objeto mediacollection](playlists-and-the-mediacollection-object.md).</span><span class="sxs-lookup"><span data-stu-id="6db73-125">For more information, see [Playlists and the MediaCollection Object](playlists-and-the-mediacollection-object.md).</span></span>

<span data-ttu-id="6db73-126">Para importar uma lista de reprodução estática de um metarquivo de playlist automática, use o *Player*. **newPlaylist** e *playlistcollection*. **importPlaylist** conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6db73-126">To import a static playlist from an auto playlist metafile, use *Player*.**newPlaylist** and *PlaylistCollection*.**importPlaylist** as described earlier.</span></span> <span data-ttu-id="6db73-127">A lista de reprodução automática será executada uma vez e uma lista de reprodução estática será criada com base no resultado dessa execução.</span><span class="sxs-lookup"><span data-stu-id="6db73-127">The auto playlist will be executed once and a static playlist will be created based on the result of that execution.</span></span>

<span data-ttu-id="6db73-128">O uso de uma lista de reprodução automática para consultar a biblioteca do usuário não tem suporte para páginas da Web que os usuários acessam pela Internet.</span><span class="sxs-lookup"><span data-stu-id="6db73-128">Using an auto playlist to query the user's library is not supported for webpages that users access over the Internet.</span></span>

<span data-ttu-id="6db73-129">O código de exemplo C# a seguir demonstra a importação de um metarquivo de playlist automática como uma lista de reprodução estática.</span><span class="sxs-lookup"><span data-stu-id="6db73-129">The following C# example code demonstrates importing an auto playlist metafile as a static playlist.</span></span> <span data-ttu-id="6db73-130">Para executar este exemplo, crie uma lista de reprodução automática usando a interface do usuário da biblioteca e, em seguida, inclua o caminho correto para o metarquivo de playlist automática neste código.</span><span class="sxs-lookup"><span data-stu-id="6db73-130">To run this sample, create an auto playlist by using the library user interface, and then include the correct path to the auto playlist metafile in this code.</span></span>


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a><span data-ttu-id="6db73-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6db73-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db73-132">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="6db73-132">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> </dl>

 

 




