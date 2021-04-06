---
title: Recuperando metadados
description: Recuperando metadados
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Playlists do metarquivo do Windows Media, Recuperando metadados
- listas de reprodução, Recuperando metadados
- listas de reprodução de metarquivo, Recuperando metadados
- Playlists do metarquivo do Windows Media, recuperação de metadados
- listas de reprodução, recuperação de metadados
- listas de reprodução de metarquivo, recuperação de metadados
- metadados, recuperando
- recuperando metadados
- Windows Media Player, Recuperando metadados
- Windows Media Player, recuperação de metadados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916412"
---
# <a name="retrieving-metadata"></a><span data-ttu-id="89fc5-113">Recuperando metadados</span><span class="sxs-lookup"><span data-stu-id="89fc5-113">Retrieving Metadata</span></span>

<span data-ttu-id="89fc5-114">Enquanto um show ou um clipe está sendo reproduzido, o script pode recuperar metadados, como título e autor, usando os métodos **getItemInfo** dos objetos de **mídia** e **playlist** do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="89fc5-114">While a show or clip is playing, your script can retrieve metadata, such as title and author, by using the **getItemInfo** methods of the Windows Media Player **Media** and **Playlist** objects.</span></span> <span data-ttu-id="89fc5-115">Você pode recuperar metadados do escopo ASX usando métodos de objeto de **lista de reprodução** e do escopo de entrada usando métodos de objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="89fc5-115">You can retrieve metadata from the ASX scope using **Playlist** object methods and from the ENTRY scope using **Media** object methods.</span></span>

<span data-ttu-id="89fc5-116">Por exemplo, para recuperar os valores de autor, resumo e PARAM no arquivo a seguir, use o método **getItemInfo** do objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="89fc5-116">For example, to retrieve the values for AUTHOR, ABSTRACT and PARAM in the following file, use the **getItemInfo** method of the **Playlist** object.</span></span> <span data-ttu-id="89fc5-117">O nome do atributo é necessário para este método.</span><span class="sxs-lookup"><span data-stu-id="89fc5-117">The attribute name is required for this method.</span></span> <span data-ttu-id="89fc5-118">Os nomes de atributo podem ser obtidos fornecendo o número de índice para a propriedade **AttributeName** .</span><span class="sxs-lookup"><span data-stu-id="89fc5-118">Attribute names can be obtained by providing the index number to the **attributeName** property.</span></span> <span data-ttu-id="89fc5-119">Os índices disponíveis para um objeto **playlist** podem ser obtidos usando a propriedade **attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="89fc5-119">The available indexes for a **Playlist** object can be obtained using the **attributeCount** property.</span></span>

## <a name="example-code"></a><span data-ttu-id="89fc5-120">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="89fc5-120">Example Code</span></span>


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



<span data-ttu-id="89fc5-121">Para recuperar os valores do objeto de **mídia** atual no escopo de entrada para ref, title, Copyright e param ("três"), use a propriedade **CurrentMedia** do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="89fc5-121">To retrieve the values of the current **Media** object in the ENTRY scope for REF,TITLE,COPYRIGHT, and PARAM ("three"), use the **currentMedia** property of the **Player** object.</span></span> <span data-ttu-id="89fc5-122">Use a propriedade **attributeCount** do objeto de **mídia** para determinar o número de atributos disponíveis para o objeto de **mídia** especificado.</span><span class="sxs-lookup"><span data-stu-id="89fc5-122">Use the **attributeCount** property of the **Media** object to determine the number of attributes available for the specified **Media** object.</span></span> <span data-ttu-id="89fc5-123">Use números de índice com o método **getItemInfoByAtom** para recuperar valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="89fc5-123">Use index numbers with the **getItemInfoByAtom** method to retrieve attribute values.</span></span> <span data-ttu-id="89fc5-124">Use números de índice com o método **GetAttributeName** do objeto de **mídia** para determinar os nomes dos atributos disponíveis e, em seguida, use os resultados com o método **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="89fc5-124">Use index numbers with the **getAttributeName** method of the **Media** object to determine the names of the available attributes, and then use the results with the **getItemInfo** method.</span></span>

<span data-ttu-id="89fc5-125">Para obter um exemplo de como usar métodos de objeto do Windows Media Player para recuperar metadados, consulte [playlist. attributeCount](playlist-attributecount.md).</span><span class="sxs-lookup"><span data-stu-id="89fc5-125">For an example of using Windows Media Player object methods to retrieve metadata, see [Playlist.attributeCount](playlist-attributecount.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89fc5-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89fc5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89fc5-127">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="89fc5-127">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="89fc5-128">**Playlists de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="89fc5-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="89fc5-129">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="89fc5-129">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




