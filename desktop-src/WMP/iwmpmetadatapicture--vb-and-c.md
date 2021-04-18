---
title: Interface IWMPMetadataPicture (VB e C) (WMP. h)
description: Fornece propriedades para obter informações sobre a imagem contida em um arquivo de mídia digital representado por um atributo WM/Picturemetadata.
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB e C) interface do Windows Media Player
- IWMPMetadataPicture (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3b462c431a136745974dcde5716c3bd81226f15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810545"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a><span data-ttu-id="35d57-105">Interface IWMPMetadataPicture (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="35d57-105">IWMPMetadataPicture (VB and C#) interface</span></span>

<span data-ttu-id="35d57-106">Fornece propriedades para obter informações sobre a imagem contida em um arquivo de mídia digital representado por um atributo de metadados do [**WM/Picture**](/windows/desktop/wmformat/wmpicture).</span><span class="sxs-lookup"><span data-stu-id="35d57-106">Provides properties for getting information about the image contained in a digital media file that is represented by a [**WM/Picture**](/windows/desktop/wmformat/wmpicture)metadata attribute.</span></span> <span data-ttu-id="35d57-107">Esse atributo corresponde a imagens de arte do álbum contidas em um arquivo de mídia digital, não à arte do álbum baixada pela Internet.</span><span class="sxs-lookup"><span data-stu-id="35d57-107">This attribute corresponds to album art images contained in a digital media file, not to album art downloaded over the Internet.</span></span>

<span data-ttu-id="35d57-108">A interface **IWMPMetadataPicture** expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="35d57-108">The **IWMPMetadataPicture** interface exposes the following properties.</span></span>



| <span data-ttu-id="35d57-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="35d57-109">Property</span></span>                                                                                   | <span data-ttu-id="35d57-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="35d57-110">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="35d57-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="35d57-111">**Description**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | <span data-ttu-id="35d57-112">Obtém a descrição da imagem representada pelo atributo de metadados.</span><span class="sxs-lookup"><span data-stu-id="35d57-112">Gets the description of the image represented by the metadata attribute.</span></span>  |
| [<span data-ttu-id="35d57-113">**MIME**</span><span class="sxs-lookup"><span data-stu-id="35d57-113">**mimeType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | <span data-ttu-id="35d57-114">Obtém o tipo MIME da imagem representada pelo atributo de metadados.</span><span class="sxs-lookup"><span data-stu-id="35d57-114">Gets the MIME type of the image represented by the metadata attribute.</span></span>    |
| [<span data-ttu-id="35d57-115">**TipoDeFigura**</span><span class="sxs-lookup"><span data-stu-id="35d57-115">**pictureType**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | <span data-ttu-id="35d57-116">Obtém o tipo de imagem da imagem representada pelo atributo de metadados.</span><span class="sxs-lookup"><span data-stu-id="35d57-116">Gets the picture type of the image represented by the metadata attribute.</span></span> |
| [<span data-ttu-id="35d57-117">**URL**</span><span class="sxs-lookup"><span data-stu-id="35d57-117">**URL**</span></span>](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | <span data-ttu-id="35d57-118">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="35d57-118">Internal use only.</span></span>                                                        |



 

<span data-ttu-id="35d57-119">Obtenha uma interface **IWMPMetadataPicture** passando o nome do atributo [**WM/Picture**](/windows/desktop/wmformat/wmpicture) para o método a seguir e convertendo o objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="35d57-119">Get an **IWMPMetadataPicture** interface by passing in the attribute name [**WM/Picture**](/windows/desktop/wmformat/wmpicture) to the following method and casting the object that is returned.</span></span>



| <span data-ttu-id="35d57-120">Interface</span><span class="sxs-lookup"><span data-stu-id="35d57-120">Interface</span></span>                                  | <span data-ttu-id="35d57-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="35d57-121">Property</span></span>                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="35d57-122">**IWMPMedia3**</span><span class="sxs-lookup"><span data-stu-id="35d57-122">**IWMPMedia3**</span></span>](iwmpmedia3--vb-and-c.md) | [<span data-ttu-id="35d57-123">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="35d57-123">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a><span data-ttu-id="35d57-124">Membros</span><span class="sxs-lookup"><span data-stu-id="35d57-124">Members</span></span>

<span data-ttu-id="35d57-125">A interface **IWMPMetadataPicture (VB e C#)** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="35d57-125">The **IWMPMetadataPicture (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="35d57-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35d57-126">Requirements</span></span>



| <span data-ttu-id="35d57-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="35d57-127">Requirement</span></span> | <span data-ttu-id="35d57-128">Valor</span><span class="sxs-lookup"><span data-stu-id="35d57-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="35d57-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35d57-129">Header</span></span><br/> | <dl> <span data-ttu-id="35d57-130"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d57-130"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35d57-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="35d57-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35d57-132">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="35d57-132">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

