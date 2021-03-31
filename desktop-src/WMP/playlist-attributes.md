---
title: Atributos da lista de reprodução
description: Atributos da lista de reprodução
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, atributos
- listas de reprodução de metarquivo, atributos
- Listas de reprodução do metarquivo do Windows Media, atributos
- atributos, listas de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916142"
---
# <a name="playlist-attributes"></a><span data-ttu-id="27f2d-114">Atributos da lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="27f2d-114">Playlist Attributes</span></span>

<span data-ttu-id="27f2d-115">As listas de reprodução têm informações de metadados chamadas atributos, assim como os itens de mídia têm atributos.</span><span class="sxs-lookup"><span data-stu-id="27f2d-115">Playlists have metadata information called attributes, just as media items have attributes.</span></span> <span data-ttu-id="27f2d-116">Você pode recuperar os nomes e valores dos atributos da lista de reprodução e exibi-los em sua interface do usuário, ou o código pode executar ações com base no valor de um atributo.</span><span class="sxs-lookup"><span data-stu-id="27f2d-116">You can retrieve the names and values of playlist attributes and display them in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="27f2d-117">As listas de reprodução são definidas em arquivos organizados em um formato XML e determinados elementos no arquivo definem atributos de playlist.</span><span class="sxs-lookup"><span data-stu-id="27f2d-117">Playlists are defined in files organized in an XML format, and particular elements in the file define playlist attributes.</span></span> <span data-ttu-id="27f2d-118">Alguns elementos de atributo são bem conhecidos; o autor do metarquivo também pode definir atributos arbitrários.</span><span class="sxs-lookup"><span data-stu-id="27f2d-118">Some attribute elements are well-known; the author of the metafile can also define arbitrary attributes.</span></span> <span data-ttu-id="27f2d-119">Para obter mais informações sobre elementos de atributo em arquivos de playlist, consulte [Recuperando metadados](retrieving-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="27f2d-119">For more information about attribute elements in playlist files, see [Retrieving Metadata](retrieving-metadata.md).</span></span>

<span data-ttu-id="27f2d-120">A biblioteca pode fornecer atributos adicionais de playlist, como **SourceURL** ou **UserLastPlayedTime**.</span><span class="sxs-lookup"><span data-stu-id="27f2d-120">The library may provide additional playlist attributes, such as **SourceURL** or **UserLastPlayedTime**.</span></span> <span data-ttu-id="27f2d-121">Para obter mais informações sobre os atributos da lista de reprodução da biblioteca, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="27f2d-121">For more information about the library playlist attributes, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="27f2d-122">A *lista de reprodução*. a propriedade **attributeCount** recupera o número de atributos associados à playlist.</span><span class="sxs-lookup"><span data-stu-id="27f2d-122">The *Playlist*.**attributeCount** property retrieves the number of attributes associated with the playlist.</span></span> <span data-ttu-id="27f2d-123">A *lista de reprodução*. a propriedade **AttributeName** recupera o nome de um atributo com base em seu índice e na *lista de reprodução*. o método **getItemInfo** recupera o valor de um atributo com base em seu nome.</span><span class="sxs-lookup"><span data-stu-id="27f2d-123">The *Playlist*.**attributeName** property retrieves the name of an attribute based on its index, and the *Playlist*.**getItemInfo** method retrieves the value of an attribute based on its name.</span></span>

<span data-ttu-id="27f2d-124">Você pode modificar o valor de um atributo da playlist atual com a *lista de reprodução*. método **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="27f2d-124">You can modify the value of an attribute of the current playlist with the *Playlist*.**setItemInfo** method.</span></span>

<span data-ttu-id="27f2d-125">Um uso especial do método **setItemInfo** é classificar os itens na lista de reprodução, usando o atributo **SortAttribute** .</span><span class="sxs-lookup"><span data-stu-id="27f2d-125">A special use of the **setItemInfo** method is to sort the items in the playlist, using the **SortAttribute** attribute.</span></span> <span data-ttu-id="27f2d-126">O exemplo de C# a seguir classifica uma lista de reprodução pelos valores do atributo **UserLastPlayedTime** .</span><span class="sxs-lookup"><span data-stu-id="27f2d-126">The following C# example sorts a playlist by the values of the **UserLastPlayedTime** attribute.</span></span> <span data-ttu-id="27f2d-127">A *playlist* de variável é uma referência a um objeto de **playlist** .</span><span class="sxs-lookup"><span data-stu-id="27f2d-127">The variable *Playlist* is a reference to a **Playlist** object.</span></span>


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



<span data-ttu-id="27f2d-128">Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="27f2d-128">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="27f2d-129">O código de exemplo C# a seguir demonstra a recuperação de atributos de playlist.</span><span class="sxs-lookup"><span data-stu-id="27f2d-129">The following C# example code demonstrates retrieving playlist attributes.</span></span> <span data-ttu-id="27f2d-130">A primeira função, implaylists, popula um controle ListBox com os nomes das listas de reprodução disponíveis.</span><span class="sxs-lookup"><span data-stu-id="27f2d-130">The first function, ShowPlaylists, populates a ListBox control with the names of the available playlists.</span></span> <span data-ttu-id="27f2d-131">A segunda parte é o manipulador de eventos da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="27f2d-131">The second part is the list box event handler.</span></span> <span data-ttu-id="27f2d-132">Quando o usuário clica em um nome de playlist, esse código recupera os atributos dessa lista de reprodução e exibe esses atributos em uma segunda caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="27f2d-132">When the user clicks a playlist name, this code retrieves the attributes for that playlist and displays those attributes in a second list box.</span></span>


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



<span data-ttu-id="27f2d-133">O evento SelectedIndexchanged para o controle ListBox é chamado cada vez que o usuário seleciona um nome de lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="27f2d-133">The SelectedIndexChanged event for the ListBox control is called each time the user selects a playlist name.</span></span> <span data-ttu-id="27f2d-134">O manipulador de eventos a seguir preenche uma segunda caixa de listagem com os nomes e valores de atributo correspondentes à seleção do usuário.</span><span class="sxs-lookup"><span data-stu-id="27f2d-134">The following event handler fills a second list box with the attribute names and values corresponding to the user's selection.</span></span>


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="27f2d-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27f2d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f2d-136">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="27f2d-136">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="27f2d-137">**Atributos de item de mídia**</span><span class="sxs-lookup"><span data-stu-id="27f2d-137">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="27f2d-138">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="27f2d-138">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




