---
title: Interface IWMPMediaCollection (VB e C) (WMP. h)
description: Fornece métodos que podem ser usados para organizar uma grande coleção de itens de mídia.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- IWMPMediaCollection (VB e C) interface do Windows Media Player
- IWMPMediaCollection (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424fd45b1fd3d02000a9774ffe75ec87e52dd9c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811095"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a><span data-ttu-id="de47a-105">Interface IWMPMediaCollection (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="de47a-105">IWMPMediaCollection (VB and C#) interface</span></span>

<span data-ttu-id="de47a-106">Fornece métodos que podem ser usados para organizar uma grande coleção de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="de47a-106">Provides methods that can be used to organize a large collection of media items.</span></span>

## <a name="members"></a><span data-ttu-id="de47a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="de47a-107">Members</span></span>

<span data-ttu-id="de47a-108">A interface **IWMPMediaCollection (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de47a-108">The **IWMPMediaCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="de47a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="de47a-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="de47a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="de47a-110">Methods</span></span>

<span data-ttu-id="de47a-111">A interface **IWMPMediaCollection (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="de47a-111">The **IWMPMediaCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="de47a-112">Método</span><span class="sxs-lookup"><span data-stu-id="de47a-112">Method</span></span>                                                                                                                       | <span data-ttu-id="de47a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="de47a-113">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de47a-114">**add**</span><span class="sxs-lookup"><span data-stu-id="de47a-114">**add**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | <span data-ttu-id="de47a-115">Adiciona um novo item de mídia ou lista de reprodução à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="de47a-115">Adds a new media item or playlist to the library.</span></span><br/>                                                                                  |
| [<span data-ttu-id="de47a-116">**getAll**</span><span class="sxs-lookup"><span data-stu-id="de47a-116">**getAll**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | <span data-ttu-id="de47a-117">Retorna uma interface **IWMPPlaylist** que corresponde à playlist que contém todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="de47a-117">Returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span><br/>               |
| [<span data-ttu-id="de47a-118">**getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="de47a-118">**getAttributeStringCollection**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | <span data-ttu-id="de47a-119">Retorna uma interface **IWMPStringCollection** que representa o conjunto de todos os valores de um atributo especificado dentro de um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="de47a-119">Returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span><br/> |
| [<span data-ttu-id="de47a-120">**getByAlbum**</span><span class="sxs-lookup"><span data-stu-id="de47a-120">**getByAlbum**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | <span data-ttu-id="de47a-121">Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="de47a-121">Returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span><br/>                                |
| [<span data-ttu-id="de47a-122">**getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="de47a-122">**getByAttribute**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | <span data-ttu-id="de47a-123">Retorna uma interface **IWMPPlaylist** que corresponde ao atributo especificado com o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="de47a-123">Returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span><br/>                      |
| [<span data-ttu-id="de47a-124">**getByAuthor**</span><span class="sxs-lookup"><span data-stu-id="de47a-124">**getByAuthor**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | <span data-ttu-id="de47a-125">Retorna uma interface **IWMPPlaylist** que fornece acesso aos itens de mídia pelo autor especificado.</span><span class="sxs-lookup"><span data-stu-id="de47a-125">Returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span><br/>                             |
| [<span data-ttu-id="de47a-126">**getByGenre**</span><span class="sxs-lookup"><span data-stu-id="de47a-126">**getByGenre**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | <span data-ttu-id="de47a-127">Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia do gênero especificado.</span><span class="sxs-lookup"><span data-stu-id="de47a-127">Returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span><br/>                                  |
| [<span data-ttu-id="de47a-128">**getByName**</span><span class="sxs-lookup"><span data-stu-id="de47a-128">**getByName**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | <span data-ttu-id="de47a-129">Retorna uma interface **IWMPPlaylist** que fornece acesso a itens de mídia com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="de47a-129">Returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span><br/>                                 |
| [<span data-ttu-id="de47a-130">**getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="de47a-130">**getMediaAtom**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | <span data-ttu-id="de47a-131">Retorna o índice de um atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="de47a-131">Returns the index of a specified attribute.</span></span><br/>                                                                                        |
| <span data-ttu-id="de47a-132">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="de47a-132">**isDeleted**</span></span>                                                                                                                | <span data-ttu-id="de47a-133">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="de47a-133">No longer supported.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="de47a-134">**exclu**</span><span class="sxs-lookup"><span data-stu-id="de47a-134">**remove**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | <span data-ttu-id="de47a-135">Remove o item de mídia especificado da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="de47a-135">Removes the specified media item from the media collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="de47a-136">**setdeled**</span><span class="sxs-lookup"><span data-stu-id="de47a-136">**setDeleted**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | <span data-ttu-id="de47a-137">Move o item de mídia especificado para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="de47a-137">Moves the specified media item to the deleted items folder.</span></span><br/>                                                                        |



 

<span data-ttu-id="de47a-138">Obtenha uma interface **IWMPMediaCollection** usando as seguintes propriedades acessadas por meio do objeto ou da interface a seguir.</span><span class="sxs-lookup"><span data-stu-id="de47a-138">Get an **IWMPMediaCollection** interface by using the following properties accessed through the following object or interface.</span></span>



| <span data-ttu-id="de47a-139">Objeto ou interface</span><span class="sxs-lookup"><span data-stu-id="de47a-139">Object or interface</span></span>                                               | <span data-ttu-id="de47a-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de47a-140">Property</span></span>                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="de47a-141">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="de47a-141">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="de47a-142">**mediacollection**</span><span class="sxs-lookup"><span data-stu-id="de47a-142">**mediaCollection**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [<span data-ttu-id="de47a-143">**IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="de47a-143">**IWMPLibrary**</span></span>](iwmplibrary--vb-and-c.md)                      | [<span data-ttu-id="de47a-144">**mediacollection**</span><span class="sxs-lookup"><span data-stu-id="de47a-144">**mediaCollection**</span></span>](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="de47a-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de47a-145">Requirements</span></span>



| <span data-ttu-id="de47a-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="de47a-146">Requirement</span></span> | <span data-ttu-id="de47a-147">Valor</span><span class="sxs-lookup"><span data-stu-id="de47a-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="de47a-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de47a-148">Header</span></span><br/> | <dl> <span data-ttu-id="de47a-149"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="de47a-149"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de47a-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="de47a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de47a-151">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="de47a-151">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="de47a-152">**Interface IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="de47a-152">**IWMPMediaCollection2 Interface**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="de47a-153">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="de47a-153">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="de47a-154">**Interface IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="de47a-154">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





