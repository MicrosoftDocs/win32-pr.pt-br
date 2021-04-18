---
title: Interface IWMPMedia (VB e C) (WMP. h)
description: Fornece uma maneira de definir e recuperar as propriedades de um item de mídia. A interface IWMPMedia expõe as propriedades a seguir.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB e C) interface do Windows Media Player
- IWMPMedia (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760252"
---
# <a name="iwmpmedia-vb-and-c-interface"></a><span data-ttu-id="48690-105">Interface IWMPMedia (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="48690-105">IWMPMedia (VB and C#) interface</span></span>

<span data-ttu-id="48690-106">Fornece uma maneira de definir e recuperar as propriedades de um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="48690-106">Provides a way to set and retrieve the properties of a media item.</span></span>

<span data-ttu-id="48690-107">A interface **IWMPMedia** expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="48690-107">The **IWMPMedia** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="48690-108">Membros</span><span class="sxs-lookup"><span data-stu-id="48690-108">Members</span></span>

<span data-ttu-id="48690-109">A interface **IWMPMedia (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="48690-109">The **IWMPMedia (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="48690-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="48690-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="48690-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48690-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48690-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="48690-112">Methods</span></span>

<span data-ttu-id="48690-113">A interface **IWMPMedia (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="48690-113">The **IWMPMedia (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="48690-114">Método</span><span class="sxs-lookup"><span data-stu-id="48690-114">Method</span></span>                                                                             | <span data-ttu-id="48690-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="48690-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48690-116">**GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="48690-116">**getAttributeName**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | <span data-ttu-id="48690-117">Retorna o nome do atributo correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="48690-117">Returns the name of the attribute corresponding to the specified index.</span></span><br/>                            |
| [<span data-ttu-id="48690-118">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="48690-118">**getItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | <span data-ttu-id="48690-119">Retorna o valor do atributo especificado para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="48690-119">Returns the value of the specified attribute for the media item.</span></span><br/>                                   |
| [<span data-ttu-id="48690-120">**getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="48690-120">**getItemInfoByAtom**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | <span data-ttu-id="48690-121">Retorna o valor do atributo com o número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="48690-121">Returns the value of the attribute with the specified index number.</span></span><br/>                                |
| [<span data-ttu-id="48690-122">**Getmarkname**</span><span class="sxs-lookup"><span data-stu-id="48690-122">**getMarkerName**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | <span data-ttu-id="48690-123">Retorna o nome do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="48690-123">Returns the name of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="48690-124">**getmarcadortime**</span><span class="sxs-lookup"><span data-stu-id="48690-124">**getMarkerTime**</span></span>](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | <span data-ttu-id="48690-125">Retorna a hora do marcador no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="48690-125">Returns the time of the marker at the specified index.</span></span><br/>                                             |
| [<span data-ttu-id="48690-126">**isMemberOf**</span><span class="sxs-lookup"><span data-stu-id="48690-126">**isMemberOf**</span></span>](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | <span data-ttu-id="48690-127">Retorna um valor que indica se o item de mídia especificado é um membro da playlist especificada.</span><span class="sxs-lookup"><span data-stu-id="48690-127">Returns a value indicating whether the specified media item is a member of the specified playlist.</span></span><br/> |
| [<span data-ttu-id="48690-128">**isReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="48690-128">**isReadOnlyItem**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | <span data-ttu-id="48690-129">Retorna um valor que indica se os atributos do item de mídia especificado podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="48690-129">Returns a value indicating whether the attributes of the specified media item can be edited.</span></span><br/>       |
| [<span data-ttu-id="48690-130">**setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="48690-130">**setItemInfo**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | <span data-ttu-id="48690-131">Define o valor do atributo especificado para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="48690-131">Sets the value of the specified attribute for the media item.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="48690-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="48690-132">Properties</span></span>

<span data-ttu-id="48690-133">A interface **IWMPMedia (VB e C#)** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48690-133">The **IWMPMedia (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="48690-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="48690-134">Property</span></span>                                                                                      | <span data-ttu-id="48690-135">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="48690-135">Access type</span></span>          | <span data-ttu-id="48690-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="48690-136">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48690-137">**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="48690-137">**attributeCount**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | <span data-ttu-id="48690-138">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-138">Read-only</span></span><br/> | <span data-ttu-id="48690-139">Obtém o número de atributos que podem ser consultados e/ou definidos para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="48690-139">Gets the number of attributes that can be queried and/or set for the media item.</span></span><br/>                                                          |
| [<span data-ttu-id="48690-140">**permanência**</span><span class="sxs-lookup"><span data-stu-id="48690-140">**duration**</span></span>](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | <span data-ttu-id="48690-141">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-141">Read-only</span></span><br/> | <span data-ttu-id="48690-142">Obtém a duração em segundos do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="48690-142">Gets the duration in seconds of the current media item.</span></span><br/>                                                                                   |
| [<span data-ttu-id="48690-143">**duraçãostring**</span><span class="sxs-lookup"><span data-stu-id="48690-143">**durationString**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | <span data-ttu-id="48690-144">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-144">Read-only</span></span><br/> | <span data-ttu-id="48690-145">Obtém um valor que indica a duração do item de mídia atual no formato HH: MM: SS.</span><span class="sxs-lookup"><span data-stu-id="48690-145">Gets a value indicating the duration of the current media item in HH:MM:SS format.</span></span><br/>                                                        |
| [<span data-ttu-id="48690-146">**imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="48690-146">**imageSourceHeight**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | <span data-ttu-id="48690-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-147">Read-only</span></span><br/> | <span data-ttu-id="48690-148">Obtém a altura do item de mídia atual em pixels.</span><span class="sxs-lookup"><span data-stu-id="48690-148">Gets the height of the current media item in pixels.</span></span><br/>                                                                                      |
| [<span data-ttu-id="48690-149">**imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="48690-149">**imageSourceWidth**</span></span>](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | <span data-ttu-id="48690-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-150">Read-only</span></span><br/> | <span data-ttu-id="48690-151">Obtém a largura do item de mídia atual em pixels.</span><span class="sxs-lookup"><span data-stu-id="48690-151">Gets the width of the current media item in pixels.</span></span><br/>                                                                                       |
| [<span data-ttu-id="48690-152">**isidêntico**</span><span class="sxs-lookup"><span data-stu-id="48690-152">**isIdentical**</span></span>](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | <span data-ttu-id="48690-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-153">Read-only</span></span><br/> | <span data-ttu-id="48690-154">Obtém um valor que indica se o item de mídia especificado é o mesmo que o atual.</span><span class="sxs-lookup"><span data-stu-id="48690-154">Gets a value indicating whether the specified media item is the same as the current one.</span></span> <span data-ttu-id="48690-155">No C#, esse é o método **Get \_ isidêntico** .</span><span class="sxs-lookup"><span data-stu-id="48690-155">In C#, this is the **get\_isIdentical** method.</span></span><br/> |
| [<span data-ttu-id="48690-156">**markerCount**</span><span class="sxs-lookup"><span data-stu-id="48690-156">**markerCount**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | <span data-ttu-id="48690-157">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-157">Read-only</span></span><br/> | <span data-ttu-id="48690-158">Obtém o número de marcadores no item de mídia.</span><span class="sxs-lookup"><span data-stu-id="48690-158">Gets the number of markers in the media item.</span></span><br/>                                                                                             |
| [<span data-ttu-id="48690-159">**nomes**</span><span class="sxs-lookup"><span data-stu-id="48690-159">**name**</span></span>](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | <span data-ttu-id="48690-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-160">Read-only</span></span><br/> | <span data-ttu-id="48690-161">Obtém ou define o nome do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="48690-161">Gets or sets the name of the media item.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="48690-162">**sourceURL**</span><span class="sxs-lookup"><span data-stu-id="48690-162">**sourceURL**</span></span>](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | <span data-ttu-id="48690-163">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="48690-163">Read-only</span></span><br/> | <span data-ttu-id="48690-164">Obtém a URL do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="48690-164">Gets the URL of the media item.</span></span><br/>                                                                                                           |



 

<span data-ttu-id="48690-165">Obtenha uma interface **IWMPMedia** usando as propriedades ou métodos a seguir acessados por meio do objeto ou da interface a seguir.</span><span class="sxs-lookup"><span data-stu-id="48690-165">Get an **IWMPMedia** interface by using the following properties or methods accessed through the following object or interface.</span></span>



| <span data-ttu-id="48690-166">Objeto ou interface</span><span class="sxs-lookup"><span data-stu-id="48690-166">Object or interface</span></span>                                               | <span data-ttu-id="48690-167">Propriedade ou método</span><span class="sxs-lookup"><span data-stu-id="48690-167">Property or method</span></span>                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48690-168">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="48690-168">**IWMPControls**</span></span>](iwmpcontrols--vb-and-c.md)                    | [<span data-ttu-id="48690-169">**CurrentItem**</span><span class="sxs-lookup"><span data-stu-id="48690-169">**currentitem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [<span data-ttu-id="48690-170">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="48690-170">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | <span data-ttu-id="48690-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="48690-171">[**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [**newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md)</span></span> |
| [<span data-ttu-id="48690-172">**IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="48690-172">**IWMPPlaylist**</span></span>](iwmpplaylist--vb-and-c.md)                    | <span data-ttu-id="48690-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (obter \_ item em C#)</span><span class="sxs-lookup"><span data-stu-id="48690-173">[**Item**](iwmpplaylist-item--vb-and-c.md) (get\_Item in C#)</span></span>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="48690-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48690-174">Requirements</span></span>



| <span data-ttu-id="48690-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="48690-175">Requirement</span></span> | <span data-ttu-id="48690-176">Valor</span><span class="sxs-lookup"><span data-stu-id="48690-176">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="48690-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48690-177">Header</span></span><br/> | <dl> <span data-ttu-id="48690-178"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="48690-178"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48690-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="48690-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48690-180">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="48690-180">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="48690-181">**Interface IWMPMedia2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="48690-181">**IWMPMedia2 Interface (VB and C#)**</span></span>](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="48690-182">**Interface IWMPMedia3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="48690-182">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





