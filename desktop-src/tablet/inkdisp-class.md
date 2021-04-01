---
description: Representa os traços de tinta coletados em um espaço de tinta.
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Classe InkDisp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 429cbf85bdc92753cda1e58a0e89086b4b5b8b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646827"
---
# <a name="inkdisp-class"></a><span data-ttu-id="e1ac2-103">Classe InkDisp</span><span class="sxs-lookup"><span data-stu-id="e1ac2-103">InkDisp class</span></span>

<span data-ttu-id="e1ac2-104">Representa os traços de tinta coletados em um espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="e1ac2-105">**InkDisp** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e1ac2-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="e1ac2-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="e1ac2-106">Events</span></span>](#events)
-   [<span data-ttu-id="e1ac2-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="e1ac2-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="e1ac2-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1ac2-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="e1ac2-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1ac2-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="e1ac2-110">Eventos</span><span class="sxs-lookup"><span data-stu-id="e1ac2-110">Events</span></span>

<span data-ttu-id="e1ac2-111">A classe **InkDisp** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="e1ac2-112">Evento</span><span class="sxs-lookup"><span data-stu-id="e1ac2-112">Event</span></span>                                    | <span data-ttu-id="e1ac2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ac2-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="e1ac2-114">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="e1ac2-115">Ocorre quando um traço é adicionado ao objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="e1ac2-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="e1ac2-117">Ocorre quando um traço é excluído do objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="e1ac2-118">Interfaces</span><span class="sxs-lookup"><span data-stu-id="e1ac2-118">Interfaces</span></span>

<span data-ttu-id="e1ac2-119">A classe **InkDisp** define essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="e1ac2-120">Interface</span><span class="sxs-lookup"><span data-stu-id="e1ac2-120">Interface</span></span>    | <span data-ttu-id="e1ac2-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ac2-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="e1ac2-122">**IInkDisp**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-122">**IInkDisp**</span></span> | <span data-ttu-id="e1ac2-123">Esse objeto implementa a interface com do **IInkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="e1ac2-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1ac2-124">Methods</span></span>

<span data-ttu-id="e1ac2-125">A classe **InkDisp** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="e1ac2-126">Método</span><span class="sxs-lookup"><span data-stu-id="e1ac2-126">Method</span></span>                                                                   | <span data-ttu-id="e1ac2-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ac2-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1ac2-128">**AddStrokesAtRectangle**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="e1ac2-129">Insere uma coleção Stroke no objeto **InkDisp** no retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="e1ac2-130">**CanPaste**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="e1ac2-131">Indica se o [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) pode ser convertido em um objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="e1ac2-132">**Clipe**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="e1ac2-133">Remove partes de um traço ou coleção de traços que estão fora de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="e1ac2-134">**ClipboardCopy**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="e1ac2-135">Copia a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="e1ac2-136">**ClipboardCopyWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="e1ac2-137">Copia os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contidos no retângulo conhecido para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="e1ac2-138">**ClipboardPaste**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="e1ac2-139">Copia o [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) da área de transferência para o objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="e1ac2-140">**8i**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="e1ac2-141">Cria um objeto **InkDisp** duplicado.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="e1ac2-142">**CreateStroke**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="e1ac2-143">Cria um traço a partir de pontos ou dados de pacote.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="e1ac2-144">**Hipertraços**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="e1ac2-145">Cria uma coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) para este objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="e1ac2-146">**DeleteStroke**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="e1ac2-147">Exclui um traço do objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="e1ac2-148">**DeleteStrokes**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="e1ac2-149">Exclui os traços do objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="e1ac2-150">**Método ExtractStrokes**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="e1ac2-151">Extrai traços do objeto **InkDisp** e retorna um novo objeto **InkDisp** contendo os traços extraídos.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="e1ac2-152">**Método ExtractWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="e1ac2-153">Recorta ou copia traços de um objeto de **classe InkDisp** existente e os cola em um novo objeto de **classe InkDisp** , usando o retângulo conhecido para determinar quais traços extrair.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="e1ac2-154">**GetBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="e1ac2-155">Recupera a caixa delimitadora de todos os traços no objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="e1ac2-156">**HitTestCircle**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="e1ac2-157">Recupera a coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que está completamente dentro ou interseccionada por um círculo conhecido.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="e1ac2-158">**HitTestWithLasso**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="e1ac2-159">Recupera os traços dentro de uma área de seleção de polilinha.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="e1ac2-160">**HitTestWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="e1ac2-161">Recupera os traços contidos em um retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e1ac2-162">**Carregar**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="e1ac2-163">Popula um novo objeto **InkDisp** com dados binários conhecidos.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="e1ac2-164">**NearestPoint**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="e1ac2-165">Recupera o [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dentro do objeto **InkDisp** que é mais próximo de um ponto conhecido, fornecendo, opcionalmente, informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="e1ac2-166">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="e1ac2-167">Converte a tinta em um formato especificado e retorna os dados binários.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="e1ac2-168">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1ac2-168">Properties</span></span>

<span data-ttu-id="e1ac2-169">A classe **InkDisp** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="e1ac2-170">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e1ac2-170">Property</span></span>                                                                           | <span data-ttu-id="e1ac2-171">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="e1ac2-171">Access type</span></span>           | <span data-ttu-id="e1ac2-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1ac2-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1ac2-173">**CustomStrokes**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="e1ac2-174">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1ac2-174">Read-only</span></span><br/>  | <span data-ttu-id="e1ac2-175">Obtém a coleção [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) a ser persistida com a tinta.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="e1ac2-176">**Bit**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="e1ac2-177">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e1ac2-177">Read/write</span></span><br/> | <span data-ttu-id="e1ac2-178">Obtém ou define o valor que indica se um objeto **InkDisp** foi modificado desde a última vez em que a tinta foi salva.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="e1ac2-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="e1ac2-180">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1ac2-180">Read-only</span></span><br/>  | <span data-ttu-id="e1ac2-181">Obtém a coleção de dados definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="e1ac2-182">**Traços**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="e1ac2-183">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1ac2-183">Read-only</span></span><br/>  | <span data-ttu-id="e1ac2-184">Obtém a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contida no objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="e1ac2-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1ac2-185">Remarks</span></span>

<span data-ttu-id="e1ac2-186">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="e1ac2-187">A primeira instanciação desse objeto faz com que o GDI+ seja instanciado também.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="e1ac2-188">Um efeito colateral é que, se você estiver usando um único objeto de tinta em um loop e criar e destruí-lo no loop, fará com que o GDI+ seja instanciado repetidamente.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="e1ac2-189">Isso pode causar uma degradação do desempenho em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="e1ac2-190">Para evitar isso, mantenha uma única instância de um objeto de tinta em todos os momentos enquanto seu aplicativo estiver usando a tinta.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="e1ac2-191">Um objeto **InkDisp** é um contêiner de dados de traço (ponto).</span><span class="sxs-lookup"><span data-stu-id="e1ac2-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="e1ac2-192">Os dados de traço, ou os pontos coletados pela caneta, são colocados em um objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="e1ac2-193">A propriedade [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contém os dados para todos os traços dentro do objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="e1ac2-194">O objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) e o controle [InkPicture](inkpicture-control-reference.md) coleta pontos do dispositivo de entrada e os coloca em um objeto **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="e1ac2-195">Esses objetos, essencialmente, agem como a origem que distribui a tinta em um ou vários objetos **InkDisp** diferentes, que atuam como contêineres que mantêm a tinta distribuída.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="e1ac2-196">O espaço de tinta é um espaço de coordenadas virtual para o qual as coordenadas do contexto do Tablet são mapeadas.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="e1ac2-197">Esse espaço é fixado em um sistema de coordenadas HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="e1ac2-198">Em coordenadas de espaço de tinta, uma mudança de 0 para 1 é igual a 1 unidade de HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="e1ac2-199">Esse mapeamento torna mais fácil relacionar vários objetos **InkDisp** .</span><span class="sxs-lookup"><span data-stu-id="e1ac2-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="e1ac2-200">O objeto [**InkRenderer**](inkrenderer-class.md) gerencia os mapeamentos entre a tinta e a janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e1ac2-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ac2-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1ac2-201">Requirements</span></span>



| <span data-ttu-id="e1ac2-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1ac2-202">Requirement</span></span> | <span data-ttu-id="e1ac2-203">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ac2-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ac2-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1ac2-204">Minimum supported client</span></span><br/> | <span data-ttu-id="e1ac2-205">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e1ac2-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e1ac2-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1ac2-206">Minimum supported server</span></span><br/> | <span data-ttu-id="e1ac2-207">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e1ac2-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e1ac2-208">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1ac2-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1ac2-209"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e1ac2-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e1ac2-210">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1ac2-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1ac2-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1ac2-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e1ac2-212">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1ac2-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ac2-213">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="e1ac2-214">[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e1ac2-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e1ac2-215">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="e1ac2-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

