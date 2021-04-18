---
title: Interface IWMPMediaCollection2 (VB e C) (WMP. h)
description: Fornece métodos que complementam a interface IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB e C) interface do Windows Media Player
- IWMPMediaCollection2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789536"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a><span data-ttu-id="e5ee6-105">Interface IWMPMediaCollection2 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="e5ee6-105">IWMPMediaCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="e5ee6-106">Fornece métodos que complementam a interface **IWMPMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="e5ee6-106">Provides methods that supplement the **IWMPMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="e5ee6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="e5ee6-107">Members</span></span>

<span data-ttu-id="e5ee6-108">A interface **IWMPMediaCollection2 (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e5ee6-108">The **IWMPMediaCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="e5ee6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5ee6-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e5ee6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5ee6-110">Methods</span></span>

<span data-ttu-id="e5ee6-111">A interface **IWMPMediaCollection2 (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e5ee6-111">The **IWMPMediaCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="e5ee6-112">Método</span><span class="sxs-lookup"><span data-stu-id="e5ee6-112">Method</span></span>                                                                                                                     | <span data-ttu-id="e5ee6-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5ee6-113">Description</span></span>                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5ee6-114">**createQuery**</span><span class="sxs-lookup"><span data-stu-id="e5ee6-114">**createQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | <span data-ttu-id="e5ee6-115">Retorna uma interface **IWMPQuery** que representa uma nova consulta.</span><span class="sxs-lookup"><span data-stu-id="e5ee6-115">Returns an **IWMPQuery** interface that represents a new query.</span></span><br/>                                                                                               |
| [<span data-ttu-id="e5ee6-116">**getByAttributeAndMediaType**</span><span class="sxs-lookup"><span data-stu-id="e5ee6-116">**getByAttributeAndMediaType**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | <span data-ttu-id="e5ee6-117">Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que têm um tipo de mídia e um atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="e5ee6-117">Returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span><br/>                                     |
| [<span data-ttu-id="e5ee6-118">**getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="e5ee6-118">**getPlaylistByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | <span data-ttu-id="e5ee6-119">Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia que correspondem às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="e5ee6-119">Returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span><br/>                                                    |
| [<span data-ttu-id="e5ee6-120">**getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="e5ee6-120">**getStringCollectionByQuery**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | <span data-ttu-id="e5ee6-121">Retorna uma interface **IWMPStringCollection** que fornece acesso ao conjunto de todos os valores de cadeia de caracteres para um atributo especificado que corresponde às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="e5ee6-121">Returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span><br/> |



 

<span data-ttu-id="e5ee6-122">Obtenha uma interface **IWMPMediaCollection2** convertendo o valor retornado pela propriedade [**AxWindowsMediaPlayer. mediacollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) ou o valor retornado pela propriedade [**IWMPLibrary. mediacollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ee6-122">Get an **IWMPMediaCollection2** interface by casting the value returned by the [**AxWindowsMediaPlayer.mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) property or the value returned by the [**IWMPLibrary.mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ee6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5ee6-123">Requirements</span></span>



| <span data-ttu-id="e5ee6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5ee6-124">Requirement</span></span> | <span data-ttu-id="e5ee6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e5ee6-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e5ee6-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5ee6-126">Header</span></span><br/> | <dl> <span data-ttu-id="e5ee6-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ee6-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ee6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5ee6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ee6-129">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="e5ee6-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="e5ee6-130">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e5ee6-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





