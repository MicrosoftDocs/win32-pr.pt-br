---
title: Interface IWMPPlaylistCollection (VB e C) (WMP. h)
description: Fornece métodos para manipular interfaces IWMPPlaylist e IWMPPlaylistArray em uma coleção.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- IWMPPlaylistCollection (VB e C) interface do Windows Media Player
- IWMPPlaylistCollection (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc97f9e98838fedc3bd5441d6bfda2da5319dd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811450"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a><span data-ttu-id="49e1c-105">Interface IWMPPlaylistCollection (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="49e1c-105">IWMPPlaylistCollection (VB and C#) interface</span></span>

<span data-ttu-id="49e1c-106">Fornece métodos para manipular interfaces **IWMPPlaylist** e **IWMPPlaylistArray** em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="49e1c-106">Provides methods for manipulating **IWMPPlaylist** and **IWMPPlaylistArray** interfaces in a collection.</span></span>

## <a name="members"></a><span data-ttu-id="49e1c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="49e1c-107">Members</span></span>

<span data-ttu-id="49e1c-108">A interface **IWMPPlaylistCollection (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="49e1c-108">The **IWMPPlaylistCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="49e1c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="49e1c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="49e1c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="49e1c-110">Methods</span></span>

<span data-ttu-id="49e1c-111">A interface **IWMPPlaylistCollection (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="49e1c-111">The **IWMPPlaylistCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="49e1c-112">Método</span><span class="sxs-lookup"><span data-stu-id="49e1c-112">Method</span></span>                                                                                                 | <span data-ttu-id="49e1c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="49e1c-113">Description</span></span>                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49e1c-114">**getAll**</span><span class="sxs-lookup"><span data-stu-id="49e1c-114">**getAll**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | <span data-ttu-id="49e1c-115">Retorna uma interface **IWMPPlaylistArray** que fornece acesso a todas as listas de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="49e1c-115">Returns an **IWMPPlaylistArray** interface that provides access to all of the playlists in the library.</span></span><br/>             |
| [<span data-ttu-id="49e1c-116">**getByName**</span><span class="sxs-lookup"><span data-stu-id="49e1c-116">**getByName**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | <span data-ttu-id="49e1c-117">Retorna uma interface **IWMPPlaylistArray** que fornece acesso a listas de reprodução com o nome especificado, se existir.</span><span class="sxs-lookup"><span data-stu-id="49e1c-117">Returns an **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span><br/> |
| [<span data-ttu-id="49e1c-118">**importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="49e1c-118">**importPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | <span data-ttu-id="49e1c-119">Adiciona uma lista de reprodução estática à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="49e1c-119">Adds a static playlist to the library.</span></span><br/>                                                                              |
| [<span data-ttu-id="49e1c-120">**isDeleted**</span><span class="sxs-lookup"><span data-stu-id="49e1c-120">**isDeleted**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | <span data-ttu-id="49e1c-121">Retorna um valor que indica se a playlist especificada está na pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="49e1c-121">Returns a value indicating whether the specified playlist is in the deleted items folder.</span></span><br/>                           |
| [<span data-ttu-id="49e1c-122">**newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="49e1c-122">**newPlaylist**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | <span data-ttu-id="49e1c-123">Retorna uma interface **IWMPPlaylist** para uma lista de reprodução nova e vazia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="49e1c-123">Returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span><br/>                                     |
| [<span data-ttu-id="49e1c-124">**exclu**</span><span class="sxs-lookup"><span data-stu-id="49e1c-124">**remove**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | <span data-ttu-id="49e1c-125">Remove uma lista de reprodução da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="49e1c-125">Removes a playlist from the library.</span></span><br/>                                                                                |
| <span data-ttu-id="49e1c-126">**setdeled**</span><span class="sxs-lookup"><span data-stu-id="49e1c-126">**setDeleted**</span></span>                                                                                         | <span data-ttu-id="49e1c-127">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="49e1c-127">No longer supported.</span></span><br/>                                                                                                |



 

<span data-ttu-id="49e1c-128">Obtenha uma interface **IWMPPlaylistCollection** usando a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="49e1c-128">Get an **IWMPPlaylistCollection** interface by using the following property.</span></span>



| <span data-ttu-id="49e1c-129">Objeto</span><span class="sxs-lookup"><span data-stu-id="49e1c-129">Object</span></span>                                                                   | <span data-ttu-id="49e1c-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="49e1c-130">Property</span></span>                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49e1c-131">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="49e1c-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="49e1c-132">**playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="49e1c-132">**playlistCollection**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="49e1c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49e1c-133">Requirements</span></span>



| <span data-ttu-id="49e1c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="49e1c-134">Requirement</span></span> | <span data-ttu-id="49e1c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="49e1c-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="49e1c-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49e1c-136">Header</span></span><br/> | <dl> <span data-ttu-id="49e1c-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="49e1c-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e1c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="49e1c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e1c-139">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="49e1c-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="49e1c-140">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49e1c-140">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="49e1c-141">**Interface IWMPPlaylistArray (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="49e1c-141">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





