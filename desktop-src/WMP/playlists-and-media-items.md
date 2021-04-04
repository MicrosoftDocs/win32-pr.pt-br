---
title: Listas de reprodução e itens de mídia
description: Listas de reprodução e itens de mídia
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, itens de mídia
- listas de reprodução de metarquivo, itens de mídia
- Playlists do metarquivo do Windows Media, itens de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916127"
---
# <a name="playlists-and-media-items"></a><span data-ttu-id="115cd-113">Listas de reprodução e itens de mídia</span><span class="sxs-lookup"><span data-stu-id="115cd-113">Playlists and Media Items</span></span>

<span data-ttu-id="115cd-114">Uma lista de reprodução é um conjunto de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="115cd-114">A playlist is a set of media items.</span></span> <span data-ttu-id="115cd-115">Um objeto **playlist** pode manipular os objetos de **mídia** que representam esses itens.</span><span class="sxs-lookup"><span data-stu-id="115cd-115">A **Playlist** object can manipulate the **Media** objects that represent those items.</span></span>

## <a name="retrieving-media-items"></a><span data-ttu-id="115cd-116">Recuperando itens de mídia</span><span class="sxs-lookup"><span data-stu-id="115cd-116">Retrieving Media Items</span></span>

<span data-ttu-id="115cd-117">Para uma lista de reprodução existente, você pode ler a *lista de reprodução*. **contagem** de propriedade para determinar quantos itens de mídia estão na playlist, e você pode obter uma referência ao objeto de **mídia** correspondente a um item específico usando a *lista de reprodução*. Propriedade do **Item** .</span><span class="sxs-lookup"><span data-stu-id="115cd-117">For an existing playlist, you can read the *Playlist*.**count** property to determine how many media items are in the playlist, and you can get a reference to the **Media** object corresponding to a specific item using the *Playlist*.**item** property.</span></span>

<span data-ttu-id="115cd-118">O exemplo de C# a seguir recupera uma referência de objeto para um item de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="115cd-118">The following C# example retrieves an object reference to a specific media item.</span></span> <span data-ttu-id="115cd-119">(Ao longo deste tópico, a variável *plist* é uma referência a um objeto **playlist** .)</span><span class="sxs-lookup"><span data-stu-id="115cd-119">(Throughout this topic, the variable *pList* is a reference to a **Playlist** object.)</span></span>


```C++
currMedia = pList.Item(0);

```



<span data-ttu-id="115cd-120">O exemplo de C# a seguir recupera os nomes de todos os itens de mídia em uma lista de reprodução e os coloca em uma caixa de listagem chamada lstOutput.</span><span class="sxs-lookup"><span data-stu-id="115cd-120">The following C# example retrieves the names of all the media items in a playlist and puts them in a ListBox named lstOutput.</span></span>


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a><span data-ttu-id="115cd-121">Adicionando itens a uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="115cd-121">Adding Items to a Playlist</span></span>

<span data-ttu-id="115cd-122">Você pode adicionar um item de mídia ao final de uma lista de reprodução ou a uma posição específica em uma lista de reprodução, usando a *lista de reprodução*. **appendItem** e *playlist*. métodos **insertItem** .</span><span class="sxs-lookup"><span data-stu-id="115cd-122">You can add a media item to the end of a playlist or at a specific position in a playlist, using the *Playlist*.**appendItem** and *Playlist*.**insertItem** methods.</span></span>

<span data-ttu-id="115cd-123">Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="115cd-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="115cd-124">O exemplo de C# a seguir demonstra as duas técnicas adicionando o item de mídia atual a uma lista de reprodução denominada "BluesTest", primeiro no final e, em seguida, no início da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="115cd-124">The following C# example demonstrates both techniques by adding the current media item to a playlist named "BluesTest", first at the end and then at the beginning of the playlist.</span></span>


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



<span data-ttu-id="115cd-125">Quando você cria uma nova lista de reprodução vazia usando a *playlistcollection*. método **newPlaylist** , você pode adicionar itens de mídia a ele chamando repetidamente a *lista de reprodução*. método **appendItem** .</span><span class="sxs-lookup"><span data-stu-id="115cd-125">When you create a new, empty playlist by using the *PlaylistCollection*.**newPlaylist** method, you can add media items to it by repeatedly calling the *Playlist*.**appendItem** method.</span></span>

## <a name="manipulating-media-items-in-a-playlist"></a><span data-ttu-id="115cd-126">Manipulando itens de mídia em uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="115cd-126">Manipulating Media Items in a Playlist</span></span>

<span data-ttu-id="115cd-127">Você pode alterar a posição de um item de mídia na lista de reprodução usando a *lista de reprodução*. método **moveItem** .</span><span class="sxs-lookup"><span data-stu-id="115cd-127">You can change the position of a media item in the playlist by using the *Playlist*.**moveItem** method.</span></span> <span data-ttu-id="115cd-128">Você especifica o item por seu índice atual e, em seguida, especifica o novo índice.</span><span class="sxs-lookup"><span data-stu-id="115cd-128">You specify the item by its current index, and then you specify the new index.</span></span> <span data-ttu-id="115cd-129">O exemplo C# a seguir move um item do índice 5 para o índice 0 em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="115cd-129">The following C# example moves an item from index 5 to index 0 within a playlist.</span></span>


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



<span data-ttu-id="115cd-130">Você pode remover um item de mídia da lista de reprodução usando a **lista de reprodução**. método **RemoveItem** .</span><span class="sxs-lookup"><span data-stu-id="115cd-130">You can remove a media item from the playlist by using the **Playlist**.**removeItem** method.</span></span> <span data-ttu-id="115cd-131">Observe que, se o item removido não for o item final na lista de reprodução, os valores de índice dos itens subsequentes mudarão.</span><span class="sxs-lookup"><span data-stu-id="115cd-131">Note that if the removed item was not the final item in the playlist, the index values of the subsequent items change.</span></span> <span data-ttu-id="115cd-132">O exemplo de C# a seguir remove o item especificado.</span><span class="sxs-lookup"><span data-stu-id="115cd-132">The following C# example removes the specified item.</span></span>


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> <span data-ttu-id="115cd-133">Os usuários podem alterar o conteúdo de uma lista de reprodução fora do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="115cd-133">Users can change the contents of a playlist outside of your application.</span></span> <span data-ttu-id="115cd-134">Sempre que você manipula os itens em uma lista de reprodução, deve monitorar e manipular os eventos relacionados à playlist do controle do Windows Media Player para garantir que seu código funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="115cd-134">Whenever you manipulate the items in a playlist, you should monitor and handle the playlist-related events of the Windows Media Player control to ensure that your code works correctly.</span></span> <span data-ttu-id="115cd-135">Esses eventos são *Player*. **CurrentPlaylistChange** e *Player*. **PlaylistChange**.</span><span class="sxs-lookup"><span data-stu-id="115cd-135">These events are *Player*.**CurrentPlaylistChange** and *Player*.**PlaylistChange**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="115cd-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="115cd-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="115cd-137">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="115cd-137">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="115cd-138">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="115cd-138">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="115cd-139">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="115cd-139">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




