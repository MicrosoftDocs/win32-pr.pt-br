---
title: Interface IWMPMedia2 (VB e C) (WMP. h)
description: Fornece acesso a uma propriedade de item de mídia adicional.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB e C) interface do Windows Media Player
- IWMPMedia2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810546"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a><span data-ttu-id="cb0d8-105">Interface IWMPMedia2 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="cb0d8-105">IWMPMedia2 (VB and C#) interface</span></span>

<span data-ttu-id="cb0d8-106">Fornece acesso a uma propriedade de item de mídia adicional.</span><span class="sxs-lookup"><span data-stu-id="cb0d8-106">Provides access to an additional media item property.</span></span>

<span data-ttu-id="cb0d8-107">Além das propriedades e métodos herdados de **IWMPMedia**, a interface **IWMPMedia2** expõe a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="cb0d8-107">In addition to the properties and methods inherited from **IWMPMedia**, the **IWMPMedia2** interface exposes the following property.</span></span>



| <span data-ttu-id="cb0d8-108">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cb0d8-108">Property</span></span>                                                 | <span data-ttu-id="cb0d8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb0d8-109">Description</span></span>                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="cb0d8-110">Erro</span><span class="sxs-lookup"><span data-stu-id="cb0d8-110">Error</span></span>](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | <span data-ttu-id="cb0d8-111">Obtém uma interface **IWMPErrorItem** se o item de mídia tiver uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="cb0d8-111">Gets an **IWMPErrorItem** interface if the media item has an error condition.</span></span> |



 

<span data-ttu-id="cb0d8-112">Obtenha uma interface **IWMPMedia2** convertendo o valor retornado por uma das propriedades ou métodos a seguir acessados por meio do objeto ou da interface a seguir.</span><span class="sxs-lookup"><span data-stu-id="cb0d8-112">Get an **IWMPMedia2** interface by casting the value returned by one of the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="cb0d8-113">Objeto ou interface</span><span class="sxs-lookup"><span data-stu-id="cb0d8-113">Object or interface</span></span>                                               | <span data-ttu-id="cb0d8-114">Propriedade ou método</span><span class="sxs-lookup"><span data-stu-id="cb0d8-114">Property or method</span></span>                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb0d8-115">IWMPControls</span><span class="sxs-lookup"><span data-stu-id="cb0d8-115">IWMPControls</span></span>](iwmpcontrols--vb-and-c.md)                        | [<span data-ttu-id="cb0d8-116">currentItem</span><span class="sxs-lookup"><span data-stu-id="cb0d8-116">currentItem</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [<span data-ttu-id="cb0d8-117">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="cb0d8-117">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="cb0d8-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="cb0d8-118">[currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="cb0d8-119">IWMPPlaylist</span><span class="sxs-lookup"><span data-stu-id="cb0d8-119">IWMPPlaylist</span></span>](iwmpplaylist--vb-and-c.md)                        | <span data-ttu-id="cb0d8-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **obter \_ Item** em C#)</span><span class="sxs-lookup"><span data-stu-id="cb0d8-120">[Item](iwmpplaylist-item--vb-and-c.md) ( **get\_Item** in C#)</span></span>                                                                   |



 

## <a name="members"></a><span data-ttu-id="cb0d8-121">Membros</span><span class="sxs-lookup"><span data-stu-id="cb0d8-121">Members</span></span>

<span data-ttu-id="cb0d8-122">A interface **IWMPMedia2 (VB e C#)** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="cb0d8-122">The **IWMPMedia2 (VB and C#)** interface does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb0d8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb0d8-123">Requirements</span></span>



| <span data-ttu-id="cb0d8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb0d8-124">Requirement</span></span> | <span data-ttu-id="cb0d8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cb0d8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cb0d8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb0d8-126">Header</span></span><br/> | <dl> <span data-ttu-id="cb0d8-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb0d8-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb0d8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb0d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0d8-129">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="cb0d8-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb0d8-130">**IWMPErrorItem (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cb0d8-130">**IWMPErrorItem (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb0d8-131">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cb0d8-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cb0d8-132">**Interface IWMPMedia3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="cb0d8-132">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





