---
title: Usando parâmetros e comandos personalizados
description: Usando parâmetros e comandos personalizados
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Playlists do metarquivo do Windows Media, parâmetros personalizados
- listas de reprodução, parâmetros personalizados
- listas de reprodução de metarquivo, parâmetros personalizados
- Playlists do metarquivo do Windows Media, comandos personalizados
- listas de reprodução, comandos personalizados
- listas de reprodução de metarquivo, comandos personalizados
- Listas de reprodução do metarquivo do Windows Media, parâmetros
- listas de reprodução, parâmetros
- listas de reprodução de metarquivo, parâmetros
- parâmetros personalizados
- comandos personalizados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822723"
---
# <a name="using-custom-parameters-and-commands"></a><span data-ttu-id="18d72-114">Usando parâmetros e comandos personalizados</span><span class="sxs-lookup"><span data-stu-id="18d72-114">Using Custom Parameters and Commands</span></span>

<span data-ttu-id="18d72-115">Você pode criar parâmetros personalizados para passar metadados adicionais em uma lista de reprodução de metarquivo usando o elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="18d72-115">You can create custom parameters to pass additional metadata in a metafile playlist by using the **PARAM** element.</span></span> <span data-ttu-id="18d72-116">Use o atributo **Name** do elemento **param** para definir o nome do parâmetro personalizado.</span><span class="sxs-lookup"><span data-stu-id="18d72-116">Use the **NAME** attribute of the **PARAM** element to define the custom parameter name.</span></span> <span data-ttu-id="18d72-117">Use o atributo **Value** para definir o valor para o parâmetro personalizado nomeado.</span><span class="sxs-lookup"><span data-stu-id="18d72-117">Use the **VALUE** attribute to define the value for the named custom parameter.</span></span>

<span data-ttu-id="18d72-118">Recupere metadados de **parâmetro** usando os métodos **getItemInfo** dos objetos de **mídia** e de lista de **reprodução** .</span><span class="sxs-lookup"><span data-stu-id="18d72-118">Retrieve **PARAM** metadata by using the **getItemInfo** methods of the **Media** and **Playlist** objects.</span></span> <span data-ttu-id="18d72-119">Para obter um exemplo de como usar esses métodos para recuperar metadados, consulte o método [attributeCount](playlist-attributecount.md) do objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="18d72-119">For an example using these methods to retrieve metadata, see the [attributeCount](playlist-attributecount.md) method of the **Playlist** object.</span></span>

<span data-ttu-id="18d72-120">O exemplo de playlist de metarquivo a seguir mostra o uso do elemento **param** para definir parâmetros personalizados.</span><span class="sxs-lookup"><span data-stu-id="18d72-120">The following example metafile playlist shows the use of the **PARAM** element to define custom parameters.</span></span>


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="18d72-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18d72-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18d72-122">**Usando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="18d72-122">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




