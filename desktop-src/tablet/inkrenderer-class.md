---
description: Representa o gerenciamento de mapeamentos da tinta para a janela de exibição. Use o objeto InkRenderer para exibir a tinta em uma janela. Você também pode usá-lo para reposicionar e redimensionar o traço.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Classe InkRenderer (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172065"
---
# <a name="inkrenderer-class"></a><span data-ttu-id="7cf54-105">Classe InkRenderer</span><span class="sxs-lookup"><span data-stu-id="7cf54-105">InkRenderer class</span></span>

<span data-ttu-id="7cf54-106">Representa o gerenciamento de mapeamentos da tinta para a janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="7cf54-106">Represents the management of mappings from ink to the display window.</span></span> <span data-ttu-id="7cf54-107">Use o objeto **InkRenderer** para exibir a tinta em uma janela.</span><span class="sxs-lookup"><span data-stu-id="7cf54-107">Use the **InkRenderer** object to display ink in a window.</span></span> <span data-ttu-id="7cf54-108">Você também pode usá-lo para reposicionar e redimensionar o traço.</span><span class="sxs-lookup"><span data-stu-id="7cf54-108">You can also use it to reposition and resize stroke.</span></span>

<span data-ttu-id="7cf54-109">**InkRenderer** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7cf54-109">**InkRenderer** has these types of members:</span></span>

-   [<span data-ttu-id="7cf54-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="7cf54-110">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="7cf54-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7cf54-111">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="7cf54-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="7cf54-112">Interfaces</span></span>

<span data-ttu-id="7cf54-113">A classe **InkRenderer** define essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="7cf54-113">The **InkRenderer** class defines these interfaces.</span></span>



| <span data-ttu-id="7cf54-114">Interface</span><span class="sxs-lookup"><span data-stu-id="7cf54-114">Interface</span></span>        | <span data-ttu-id="7cf54-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cf54-115">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="7cf54-116">**IInkRenderer**</span><span class="sxs-lookup"><span data-stu-id="7cf54-116">**IInkRenderer**</span></span> | <span data-ttu-id="7cf54-117">Esse objeto implementa a interface com do **IInkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="7cf54-117">This object implements the **IInkRenderer** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="7cf54-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="7cf54-118">Methods</span></span>

<span data-ttu-id="7cf54-119">A classe **InkRenderer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7cf54-119">The **InkRenderer** class has these methods.</span></span>



| <span data-ttu-id="7cf54-120">Método</span><span class="sxs-lookup"><span data-stu-id="7cf54-120">Method</span></span>                                                                     | <span data-ttu-id="7cf54-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cf54-121">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cf54-122">**Draw**</span><span class="sxs-lookup"><span data-stu-id="7cf54-122">**Draw**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | <span data-ttu-id="7cf54-123">Desenha traços em um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7cf54-123">Draws strokes on a device context.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="7cf54-124">**DrawStroke**</span><span class="sxs-lookup"><span data-stu-id="7cf54-124">**DrawStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | <span data-ttu-id="7cf54-125">Desenha um traço no contexto de dispositivo do Windows especificado.</span><span class="sxs-lookup"><span data-stu-id="7cf54-125">Draws a stroke on the specified windows device context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="7cf54-126">**GetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="7cf54-126">**GetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | <span data-ttu-id="7cf54-127">Recupera a transformação de objeto que foi usada para renderizar a tinta.</span><span class="sxs-lookup"><span data-stu-id="7cf54-127">Retrieves the object transform that was used to render ink.</span></span><br/>                                                                                   |
| [<span data-ttu-id="7cf54-128">**GetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="7cf54-128">**GetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | <span data-ttu-id="7cf54-129">Recupera a transformação de exibição usada para renderizar a tinta.</span><span class="sxs-lookup"><span data-stu-id="7cf54-129">Retrieves the view transform that is used to render ink.</span></span><br/>                                                                                      |
| [<span data-ttu-id="7cf54-130">**InkSpaceToPixel**</span><span class="sxs-lookup"><span data-stu-id="7cf54-130">**InkSpaceToPixel**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | <span data-ttu-id="7cf54-131">Converte um local em coordenadas de espaço de tinta para estar no espaço de pixel.</span><span class="sxs-lookup"><span data-stu-id="7cf54-131">Converts a location in ink space coordinates to be in pixel space.</span></span><br/>                                                                            |
| [<span data-ttu-id="7cf54-132">**InkSpaceToPixelFromPoints**</span><span class="sxs-lookup"><span data-stu-id="7cf54-132">**InkSpaceToPixelFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | <span data-ttu-id="7cf54-133">Converte uma matriz de pontos em coordenadas de espaço de tinta para o espaço de pixel.</span><span class="sxs-lookup"><span data-stu-id="7cf54-133">Converts an array of points in ink space coordinates to pixel space.</span></span><br/>                                                                          |
| [<span data-ttu-id="7cf54-134">**Medida**</span><span class="sxs-lookup"><span data-stu-id="7cf54-134">**Measure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | <span data-ttu-id="7cf54-135">Calcula o retângulo no contexto do dispositivo que conteria uma coleção de traços se eles foram desenhados com o objeto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="7cf54-135">Calculates the rectangle on the device context that would contain a collection of strokes if they were drawn with the **InkRenderer** object.</span></span><br/> |
| [<span data-ttu-id="7cf54-136">**MeasureStroke**</span><span class="sxs-lookup"><span data-stu-id="7cf54-136">**MeasureStroke**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | <span data-ttu-id="7cf54-137">Calcula o retângulo no contexto do dispositivo que conteria um traço se eles fossem desenhados com o objeto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="7cf54-137">Calculates the rectangle on the device context that would contain a stroke if they were drawn with the **InkRenderer** object.</span></span><br/>                |
| [<span data-ttu-id="7cf54-138">**Mover**</span><span class="sxs-lookup"><span data-stu-id="7cf54-138">**Move**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | <span data-ttu-id="7cf54-139">Aplica uma tradução à transformação exibir em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="7cf54-139">Applies a translation to the view transform in ink space coordinates.</span></span><br/>                                                                         |
| [<span data-ttu-id="7cf54-140">**PixelToInkSpace**</span><span class="sxs-lookup"><span data-stu-id="7cf54-140">**PixelToInkSpace**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | <span data-ttu-id="7cf54-141">Converte um local em coordenadas de pixel para estar no espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="7cf54-141">Converts a location in pixel coordinates to be in ink space.</span></span><br/>                                                                                  |
| [<span data-ttu-id="7cf54-142">**PixelToInkSpaceFromPoints**</span><span class="sxs-lookup"><span data-stu-id="7cf54-142">**PixelToInkSpaceFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | <span data-ttu-id="7cf54-143">Converte uma matriz de pontos em coordenadas de espaço em pixel para o espaço à tinta.</span><span class="sxs-lookup"><span data-stu-id="7cf54-143">Converts an array of points in pixel space coordinates to ink space.</span></span><br/>                                                                          |
| [<span data-ttu-id="7cf54-144">**Girar**</span><span class="sxs-lookup"><span data-stu-id="7cf54-144">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | <span data-ttu-id="7cf54-145">Aplica uma rotação à transformação de exibição.</span><span class="sxs-lookup"><span data-stu-id="7cf54-145">Applies a rotation to the view transform.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="7cf54-146">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="7cf54-146">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | <span data-ttu-id="7cf54-147">Dimensiona a transformação da exibição na dimensão X e Y.</span><span class="sxs-lookup"><span data-stu-id="7cf54-147">Scales the view transform in the X and Y dimension.</span></span><br/>                                                                                           |
| [<span data-ttu-id="7cf54-148">**SetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="7cf54-148">**SetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | <span data-ttu-id="7cf54-149">Define a transformação do objeto que é usada para renderizar a tinta.</span><span class="sxs-lookup"><span data-stu-id="7cf54-149">Sets the object transform that is used to render ink.</span></span><br/>                                                                                         |
| [<span data-ttu-id="7cf54-150">**SetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="7cf54-150">**SetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | <span data-ttu-id="7cf54-151">Define a transformação de exibição usada para renderizar a tinta.</span><span class="sxs-lookup"><span data-stu-id="7cf54-151">Sets the view transform that is used to render ink.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="7cf54-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cf54-152">Remarks</span></span>

<span data-ttu-id="7cf54-153">A impressão também é feita por meio do objeto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="7cf54-153">Printing is also done through the **InkRenderer** object.</span></span>

<span data-ttu-id="7cf54-154">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="7cf54-154">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cf54-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cf54-155">Requirements</span></span>



| <span data-ttu-id="7cf54-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cf54-156">Requirement</span></span> | <span data-ttu-id="7cf54-157">Valor</span><span class="sxs-lookup"><span data-stu-id="7cf54-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf54-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cf54-158">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf54-159">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7cf54-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7cf54-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cf54-160">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf54-161">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7cf54-161">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7cf54-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cf54-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cf54-163"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7cf54-163"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7cf54-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7cf54-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cf54-165"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cf54-165"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7cf54-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cf54-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf54-167">**Propriedade do renderizador**</span><span class="sxs-lookup"><span data-stu-id="7cf54-167">**Renderer Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[<span data-ttu-id="7cf54-168">**Classe InkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="7cf54-168">**InkDrawingAttributes Class**</span></span>](inkdrawingattributes-class.md)
</dt> <dt>

[<span data-ttu-id="7cf54-169">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="7cf54-169">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="7cf54-170">[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cf54-170">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

