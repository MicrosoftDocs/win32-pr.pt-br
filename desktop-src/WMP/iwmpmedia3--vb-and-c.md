---
title: Interface IWMPMedia3 (VB e C) (WMP. h)
description: Fornece métodos adicionais para acessar as propriedades de um item de mídia.
ms.assetid: e16aa5e2-ae44-41c2-8c61-fb688c2e89e2
keywords:
- IWMPMedia3 (VB e C) interface do Windows Media Player
- IWMPMedia3 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMedia3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb5438ad4d80031d5b45c738c6b6cc9335018af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779991"
---
# <a name="iwmpmedia3-vb-and-c-interface"></a><span data-ttu-id="e2649-105">Interface IWMPMedia3 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="e2649-105">IWMPMedia3 (VB and C#) interface</span></span>

<span data-ttu-id="e2649-106">Fornece métodos adicionais para acessar as propriedades de um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="e2649-106">Provides additional methods to access the properties of a media item.</span></span>

## <a name="members"></a><span data-ttu-id="e2649-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e2649-107">Members</span></span>

<span data-ttu-id="e2649-108">A interface **IWMPMedia3 (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e2649-108">The **IWMPMedia3 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="e2649-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2649-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e2649-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2649-110">Methods</span></span>

<span data-ttu-id="e2649-111">A interface **IWMPMedia3 (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e2649-111">The **IWMPMedia3 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="e2649-112">Método</span><span class="sxs-lookup"><span data-stu-id="e2649-112">Method</span></span>                                                                                           | <span data-ttu-id="e2649-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e2649-113">Description</span></span>                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2649-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="e2649-114">**getAttributeCountByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="e2649-115">Retorna o número de atributos associados ao tipo de atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="e2649-115">Returns the number of attributes associated with the specified attribute type.</span></span><br/>              |
| [<span data-ttu-id="e2649-116">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="e2649-116">**getItemInfoByType**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="e2649-117">Retorna o valor do atributo correspondente ao tipo de atributo e ao índice especificados.</span><span class="sxs-lookup"><span data-stu-id="e2649-117">Returns the value of the attribute corresponding to the specified attribute type and index.</span></span><br/> |



 

<span data-ttu-id="e2649-118">Obtenha uma interface **IWMPMedia3** convertendo o valor retornado por uma das propriedades ou métodos a seguir acessados por meio do objeto ou da interface a seguir.</span><span class="sxs-lookup"><span data-stu-id="e2649-118">Get an **IWMPMedia3** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="e2649-119">Objeto ou interface</span><span class="sxs-lookup"><span data-stu-id="e2649-119">Object or interface</span></span>                                               | <span data-ttu-id="e2649-120">Propriedade ou método</span><span class="sxs-lookup"><span data-stu-id="e2649-120">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2649-121">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="e2649-121">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="e2649-122">currentItem</span><span class="sxs-lookup"><span data-stu-id="e2649-122">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="e2649-123">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="e2649-123">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="e2649-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="e2649-124">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="e2649-125">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="e2649-125">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="e2649-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **obter \_ Item** em C#)</span><span class="sxs-lookup"><span data-stu-id="e2649-126">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="e2649-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2649-127">Requirements</span></span>



| <span data-ttu-id="e2649-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2649-128">Requirement</span></span> | <span data-ttu-id="e2649-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e2649-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e2649-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2649-130">Header</span></span><br/> | <dl> <span data-ttu-id="e2649-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2649-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2649-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2649-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2649-133">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="e2649-133">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2649-134">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e2649-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2649-135">**Interface IWMPMedia2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e2649-135">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





