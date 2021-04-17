---
title: Interface IWMPControls (VB e C) (WMP. h)
description: Fornece uma maneira de manipular a reprodução de um item de mídia, representando os controles de transporte do Windows Media Player, como reproduzir, parar e pausar. a interface IWMPControls expõe as propriedades a seguir.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- IWMPControls (VB e C) interface do Windows Media Player
- IWMPControls (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762068"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a><span data-ttu-id="1c4b6-105">Interface IWMPControls (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="1c4b6-105">IWMPControls (VB and C#) interface</span></span>

<span data-ttu-id="1c4b6-106">Fornece uma maneira de manipular a reprodução de um item de mídia, representando os controles de transporte do Windows Media Player, como reproduzir, parar e pausar.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-106">Provides a way to manipulate the playback of a media item by representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>

<span data-ttu-id="1c4b6-107">A interface **IWMPControls** expõe as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-107">The **IWMPControls** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="1c4b6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1c4b6-108">Members</span></span>

<span data-ttu-id="1c4b6-109">A interface **IWMPControls (VB e C#)** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c4b6-109">The **IWMPControls (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="1c4b6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c4b6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c4b6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c4b6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c4b6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c4b6-112">Methods</span></span>

<span data-ttu-id="1c4b6-113">A interface **IWMPControls (VB e C#)** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-113">The **IWMPControls (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="1c4b6-114">Método</span><span class="sxs-lookup"><span data-stu-id="1c4b6-114">Method</span></span>                                                                       | <span data-ttu-id="1c4b6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c4b6-115">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c4b6-116">**fastForward**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-116">**fastForward**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | <span data-ttu-id="1c4b6-117">Inicia a reprodução rápida do item de mídia na direção de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-117">Starts fast play of the media item in the forward direction.</span></span><br/>                     |
| [<span data-ttu-id="1c4b6-118">**fastReverse**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-118">**fastReverse**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | <span data-ttu-id="1c4b6-119">Inicia a reprodução rápida do item de mídia na direção inversa.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-119">Starts fast play of the media item in the reverse direction.</span></span><br/>                     |
| [<span data-ttu-id="1c4b6-120">**última**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-120">**next**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | <span data-ttu-id="1c4b6-121">Define o próximo item na lista de reprodução como o item atual.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-121">Sets the next item in the playlist as the current item.</span></span><br/>                          |
| [<span data-ttu-id="1c4b6-122">**temporariamente**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-122">**pause**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | <span data-ttu-id="1c4b6-123">Pausa a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-123">Pauses playback of the media item.</span></span><br/>                                               |
| [<span data-ttu-id="1c4b6-124">**reproduzir**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-124">**play**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | <span data-ttu-id="1c4b6-125">Inicia a reprodução do item de mídia atual ou retoma a reprodução de um item pausado.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-125">Begins playback of the current media item, or resumes playback of a paused item.</span></span><br/> |
| [<span data-ttu-id="1c4b6-126">**playItem**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-126">**playItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | <span data-ttu-id="1c4b6-127">Reproduz o item de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-127">Plays the specified media item.</span></span><br/>                                                  |
| [<span data-ttu-id="1c4b6-128">**anterior**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-128">**previous**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | <span data-ttu-id="1c4b6-129">Define o item anterior na playlist como o item atual.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-129">Sets the previous item in the playlist as the current item.</span></span><br/>                      |
| [<span data-ttu-id="1c4b6-130">**deixar**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-130">**stop**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | <span data-ttu-id="1c4b6-131">Interrompe a reprodução do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-131">Stops playback of the media item.</span></span><br/>                                                |



 

### <a name="properties"></a><span data-ttu-id="1c4b6-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1c4b6-132">Properties</span></span>

<span data-ttu-id="1c4b6-133">A interface **IWMPControls (VB e C#)** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-133">The **IWMPControls (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="1c4b6-134">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1c4b6-134">Property</span></span>                                                                                                    | <span data-ttu-id="1c4b6-135">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="1c4b6-135">Access type</span></span>           | <span data-ttu-id="1c4b6-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c4b6-136">Description</span></span>                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c4b6-137">**currentItem**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-137">**currentItem**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | <span data-ttu-id="1c4b6-138">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1c4b6-138">Read/write</span></span><br/> | <span data-ttu-id="1c4b6-139">Obtém ou define o item de mídia atual em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-139">Gets or sets the current media item in a playlist.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="1c4b6-140">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-140">**currentMarker**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | <span data-ttu-id="1c4b6-141">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1c4b6-141">Read/write</span></span><br/> | <span data-ttu-id="1c4b6-142">Obtém ou define o número do marcador atual.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-142">Gets or sets the current marker number.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="1c4b6-143">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-143">**currentPosition**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | <span data-ttu-id="1c4b6-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1c4b6-144">Read/write</span></span><br/> | <span data-ttu-id="1c4b6-145">Obtém ou define a posição atual no item de mídia em segundos desde o início.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-145">Gets or sets the current position in the media item in seconds from the beginning.</span></span><br/>                                                                                    |
| [<span data-ttu-id="1c4b6-146">**currentPositionString**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-146">**currentPositionString**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | <span data-ttu-id="1c4b6-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c4b6-147">Read-only</span></span><br/>  | <span data-ttu-id="1c4b6-148">Obtém a posição atual no item de mídia como um **System. String**.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-148">Gets the current position in the media item as a **System.String**.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="1c4b6-149">**isAvailable**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-149">**isAvailable**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | <span data-ttu-id="1c4b6-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c4b6-150">Read-only</span></span><br/>  | <span data-ttu-id="1c4b6-151">Obtém um valor que indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-151">Gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span> <span data-ttu-id="1c4b6-152">No C#, esse é o método **Get \_ IsAvailable** .</span><span class="sxs-lookup"><span data-stu-id="1c4b6-152">In C#, this is the **get\_isAvailable** method.</span></span><br/> |



 

<span data-ttu-id="1c4b6-153">Obtenha uma interface **IWMPControls** usando a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c4b6-153">Get an **IWMPControls** interface by using the following property.</span></span>



| <span data-ttu-id="1c4b6-154">Objeto</span><span class="sxs-lookup"><span data-stu-id="1c4b6-154">Object</span></span>                                                                   | <span data-ttu-id="1c4b6-155">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1c4b6-155">Property</span></span>                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="1c4b6-156">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="1c4b6-156">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="1c4b6-157">**Ctlcontrols**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-157">**Ctlcontrols**</span></span>](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="1c4b6-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c4b6-158">Requirements</span></span>



| <span data-ttu-id="1c4b6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4b6-159">Requirement</span></span> | <span data-ttu-id="1c4b6-160">Valor</span><span class="sxs-lookup"><span data-stu-id="1c4b6-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1c4b6-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c4b6-161">Header</span></span><br/> | <dl> <span data-ttu-id="1c4b6-162"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c4b6-162"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c4b6-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c4b6-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c4b6-164">**Interfaces para Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-164">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="1c4b6-165">**Interface IWMPControls2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-165">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1c4b6-166">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1c4b6-166">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





