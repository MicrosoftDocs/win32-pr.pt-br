---
title: Atributos de item de mídia
description: Atributos de item de mídia
ms.assetid: d43addec-e06c-4ef3-9012-3ecf589b105c
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac8595cc07504c9cd3e195431513a1f8565e87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005484"
---
# <a name="media-item-attributes"></a><span data-ttu-id="128c1-120">Atributos de item de mídia</span><span class="sxs-lookup"><span data-stu-id="128c1-120">Media Item Attributes</span></span>

<span data-ttu-id="128c1-121">Ao examinar a biblioteca no Windows Media Player, você normalmente vê uma grande quantidade de informações sobre um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="128c1-121">When you look at the library in Windows Media Player, you typically see a great deal of information about a media item.</span></span> <span data-ttu-id="128c1-122">Além do nome de uma faixa de áudio, por exemplo, você provavelmente verá o nome do álbum no qual a faixa está, os nomes do artista e do Composer, o gênero da música e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="128c1-122">In addition to the name of an audio track, for example, you will likely see the name of the album the track is on, the names of the artist and composer, the genre of the music, and so on.</span></span>

<span data-ttu-id="128c1-123">No modelo de objeto do Windows Media Player, esses itens de metadados são chamados de atributos.</span><span class="sxs-lookup"><span data-stu-id="128c1-123">In the Windows Media Player object model, these metadata items are called attributes.</span></span> <span data-ttu-id="128c1-124">O modelo de objeto inclui propriedades e métodos que você pode usar para consultar itens de mídia e listas de reprodução para atributos.</span><span class="sxs-lookup"><span data-stu-id="128c1-124">The object model includes properties and methods you can use to query media items and playlists for attributes.</span></span> <span data-ttu-id="128c1-125">Você pode exibir valores de atributo em sua interface do usuário ou o seu código pode executar ações com base no valor de um atributo.</span><span class="sxs-lookup"><span data-stu-id="128c1-125">You can then display attribute values in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="128c1-126">Os tópicos a seguir descrevem como trabalhar com atributos de item de mídia.</span><span class="sxs-lookup"><span data-stu-id="128c1-126">The following topics describe working with media item attributes.</span></span>



| <span data-ttu-id="128c1-127">Tópico</span><span class="sxs-lookup"><span data-stu-id="128c1-127">Topic</span></span>                                                                                      | <span data-ttu-id="128c1-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="128c1-128">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="128c1-129">Noções básicas sobre fontes de atributo</span><span class="sxs-lookup"><span data-stu-id="128c1-129">Understanding Attribute Sources</span></span>](understanding-attribute-sources.md)                     | <span data-ttu-id="128c1-130">Descreve como a origem de um item de mídia afeta os atributos que podem ser associados a ele.</span><span class="sxs-lookup"><span data-stu-id="128c1-130">Describes how the source of a media item affects the attributes that may be associated with it.</span></span> |
| [<span data-ttu-id="128c1-131">Lendo valores de atributo</span><span class="sxs-lookup"><span data-stu-id="128c1-131">Reading Attribute Values</span></span>](reading-attribute-values.md)                                   | <span data-ttu-id="128c1-132">Mostra os métodos para recuperar o valor de um atributo.</span><span class="sxs-lookup"><span data-stu-id="128c1-132">Shows the methods for retrieving the value of an attribute.</span></span>                                     |
| [<span data-ttu-id="128c1-133">Atributos com vários valores</span><span class="sxs-lookup"><span data-stu-id="128c1-133">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md)                     | <span data-ttu-id="128c1-134">Mostra os métodos para recuperar o valor de um atributo de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="128c1-134">Shows the methods for retrieving the value of a multi-valued attribute.</span></span>                         |
| [<span data-ttu-id="128c1-135">Lendo valores de atributo de um CD ou DVD</span><span class="sxs-lookup"><span data-stu-id="128c1-135">Reading Attribute Values from a CD or DVD</span></span>](reading-attribute-values-from-a-cd-or-dvd.md) | <span data-ttu-id="128c1-136">Fornece um aplicativo de exemplo que lê todos os atributos de um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="128c1-136">Provides a sample application that reads all of the attributes of a media item.</span></span>                 |
| [<span data-ttu-id="128c1-137">Alterando valores de atributo</span><span class="sxs-lookup"><span data-stu-id="128c1-137">Changing Attribute Values</span></span>](changing-attribute-values.md)                                 | <span data-ttu-id="128c1-138">Mostra o método para alterar o valor de um atributo.</span><span class="sxs-lookup"><span data-stu-id="128c1-138">Shows the method for changing the value of an attribute.</span></span>                                        |
| [<span data-ttu-id="128c1-139">Valores de atributo para conteúdo de TV</span><span class="sxs-lookup"><span data-stu-id="128c1-139">Attribute Values for TV Content</span></span>](attribute-values-for-tv-content.md)                     | <span data-ttu-id="128c1-140">Mostra como especificar atributos para conteúdo de vídeo digital que contém programas de TV.</span><span class="sxs-lookup"><span data-stu-id="128c1-140">Shows how to specify attributes for digital video content that contains TV shows.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="128c1-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="128c1-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="128c1-142">**Atributos da lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="128c1-142">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> <dt>

[<span data-ttu-id="128c1-143">**Trabalhando com a biblioteca**</span><span class="sxs-lookup"><span data-stu-id="128c1-143">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




