---
title: Valores de atributo para conteúdo de TV
description: Valores de atributo para conteúdo de TV
ms.assetid: 70afb0fc-9eb0-4b94-a32a-f9202db94270
keywords:
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, conteúdo de TV
- Valores de atributo de conteúdo de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb63e872edd80944772a320da5f2094e6d8f5757
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006155"
---
# <a name="attribute-values-for-tv-content"></a><span data-ttu-id="1d177-114">Valores de atributo para conteúdo de TV</span><span class="sxs-lookup"><span data-stu-id="1d177-114">Attribute Values for TV Content</span></span>

<span data-ttu-id="1d177-115">Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1d177-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="1d177-116">O Windows Media Player 10 ou posterior pode organizar o conteúdo de TV na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1d177-116">Windows Media Player 10 or later can organize TV content in the library.</span></span> <span data-ttu-id="1d177-117">O Windows Media Player trata o conteúdo de TV como uma subcategoria de conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1d177-117">Windows Media Player treats TV content as a subcategory of video content.</span></span> <span data-ttu-id="1d177-118">Para fazer com que o conteúdo de vídeo apareça nos nós de TV na biblioteca, defina o **WM/MediaClassPrimaryID** e os atributos **WM/MediaClassSecondaryID** para os valores na tabela a seguir usando a *mídia*. método **setItemInfo** :</span><span class="sxs-lookup"><span data-stu-id="1d177-118">To make video content appear in the TV nodes in the library, set the **WM/MediaClassPrimaryID** and the **WM/MediaClassSecondaryID** attributes to the values in the following table by using the *media*.**setItemInfo** method:</span></span>



| <span data-ttu-id="1d177-119">Atributo</span><span class="sxs-lookup"><span data-stu-id="1d177-119">Attribute</span></span>                    | <span data-ttu-id="1d177-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1d177-120">Value</span></span>                                |
|------------------------------|--------------------------------------|
| <span data-ttu-id="1d177-121">**WM/MediaClassPrimaryID**</span><span class="sxs-lookup"><span data-stu-id="1d177-121">**WM/MediaClassPrimaryID**</span></span>   | <span data-ttu-id="1d177-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span><span class="sxs-lookup"><span data-stu-id="1d177-122">DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B</span></span> |
| <span data-ttu-id="1d177-123">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="1d177-123">**WM/MediaClassSecondaryID**</span></span> | <span data-ttu-id="1d177-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span><span class="sxs-lookup"><span data-stu-id="1d177-124">BA7F258A-62F7-47A9-B21F-4651C42A000E</span></span> |



 

<span data-ttu-id="1d177-125">Você também pode usar esses valores para determinar se um determinado item de mídia digital contém conteúdo de TV usando a *mídia*. **getItemInfo** ou *mídia*. métodos **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="1d177-125">You can also use these values to determine whether a particular digital media item contains TV content by using the *media*.**getItemInfo** or *media*.**getItemInfoByType** methods.</span></span>

<span data-ttu-id="1d177-126">Lembre-se de usar os valores de **GUID** como valores de **cadeia de caracteres** ao especificar ou recuperar esses valores.</span><span class="sxs-lookup"><span data-stu-id="1d177-126">Remember to use the **GUID** values as **string** values when specifying or retrieving these values.</span></span>

<span data-ttu-id="1d177-127">O código de exemplo C# a seguir define os atributos de classe de mídia de forma que um item de mídia seja identificado como conteúdo de TV.</span><span class="sxs-lookup"><span data-stu-id="1d177-127">The following C# example code sets the media class attributes so that a media item will be identified as TV content.</span></span>


```C++
// Initialize the media object.
// This code assumes only 1 item named MyFile.
IWMPMedia3 media = (IWMPMedia3)Player.mediaCollection.getByName("MyFile").item(0);

// Set the primary media-class identifier.
media.setItemInfo("WM/MediaClassPrimaryID", "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B");

// Set the secondary media-class identifier.
media.setItemInfo("WM/MediaClassSecondaryID", "BA7F258A-62F7-47A9-B21F-4651C42A000E");

```



<span data-ttu-id="1d177-128">Para obter mais informações sobre os valores possíveis para os atributos de classe de mídia, consulte as [diretrizes de uso de metadados do Windows Media](/previous-versions/ms867702(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="1d177-128">For more info about the possible values for the media class attributes, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d177-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d177-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d177-130">**Atributos de item de mídia**</span><span class="sxs-lookup"><span data-stu-id="1d177-130">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d177-131">**Acesso à biblioteca**</span><span class="sxs-lookup"><span data-stu-id="1d177-131">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="1d177-132">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="1d177-132">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




