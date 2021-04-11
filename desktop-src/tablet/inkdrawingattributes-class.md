---
description: Representa os atributos aplicados à tinta quando ele é desenhado.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Classe InkDrawingAttributes (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297230"
---
# <a name="inkdrawingattributes-class"></a><span data-ttu-id="07d59-103">Classe InkDrawingAttributes</span><span class="sxs-lookup"><span data-stu-id="07d59-103">InkDrawingAttributes class</span></span>

<span data-ttu-id="07d59-104">Representa os atributos aplicados à tinta quando ele é desenhado.</span><span class="sxs-lookup"><span data-stu-id="07d59-104">Represents the attributes that are applied to ink when it is drawn.</span></span>

<span data-ttu-id="07d59-105">**InkDrawingAttributes** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="07d59-105">**InkDrawingAttributes** has these types of members:</span></span>

-   [<span data-ttu-id="07d59-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="07d59-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="07d59-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="07d59-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="07d59-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07d59-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="07d59-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="07d59-109">Interfaces</span></span>

<span data-ttu-id="07d59-110">A classe **InkDrawingAttributes** define essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="07d59-110">The **InkDrawingAttributes** class defines these interfaces.</span></span>



| <span data-ttu-id="07d59-111">Interface</span><span class="sxs-lookup"><span data-stu-id="07d59-111">Interface</span></span>                 | <span data-ttu-id="07d59-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="07d59-112">Description</span></span>                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="07d59-113">**IInkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-113">**IInkDrawingAttributes**</span></span> | <span data-ttu-id="07d59-114">Esse objeto implementa a interface com do **IInkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="07d59-114">This object implements the **IInkDrawingAttributes** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="07d59-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="07d59-115">Methods</span></span>

<span data-ttu-id="07d59-116">A classe **InkDrawingAttributes** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="07d59-116">The **InkDrawingAttributes** class has these methods.</span></span>



| <span data-ttu-id="07d59-117">Método</span><span class="sxs-lookup"><span data-stu-id="07d59-117">Method</span></span>                         | <span data-ttu-id="07d59-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="07d59-118">Description</span></span>                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07d59-119">**8i**</span><span class="sxs-lookup"><span data-stu-id="07d59-119">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | <span data-ttu-id="07d59-120">Cria um objeto [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** ou [**InkRecognizerContext**](inkrecognizercontext-class.md) duplicado.</span><span class="sxs-lookup"><span data-stu-id="07d59-120">Creates a duplicate [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes**, or [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="07d59-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07d59-121">Properties</span></span>

<span data-ttu-id="07d59-122">A classe **InkDrawingAttributes** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="07d59-122">The **InkDrawingAttributes** class has these properties.</span></span>



| <span data-ttu-id="07d59-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="07d59-123">Property</span></span>                                                                           | <span data-ttu-id="07d59-124">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="07d59-124">Access type</span></span>           | <span data-ttu-id="07d59-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="07d59-125">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07d59-126">**Suavizado**</span><span class="sxs-lookup"><span data-stu-id="07d59-126">**AntiAliased**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | <span data-ttu-id="07d59-127">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-127">Read/write</span></span><br/> | <span data-ttu-id="07d59-128">Obtém ou define o valor que especifica se as cores de primeiro plano e de plano de fundo ao longo da borda da tinta são mescladas para aumentar a suavidade de um traço de tinta.</span><span class="sxs-lookup"><span data-stu-id="07d59-128">Gets or sets the value that specifies whether the foreground and background colors along the edge of the ink are blended to increase the smoothness of an ink stroke.</span></span><br/> |
| [<span data-ttu-id="07d59-129">**Cor**</span><span class="sxs-lookup"><span data-stu-id="07d59-129">**Color**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | <span data-ttu-id="07d59-130">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-130">Read/write</span></span><br/> | <span data-ttu-id="07d59-131">Obtém ou define a cor da tinta desenhada com esse objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="07d59-131">Gets or sets the color of the ink drawn with this **InkDrawingAttributes** object.</span></span><br/>                                                                                    |
| [<span data-ttu-id="07d59-132">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="07d59-132">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="07d59-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07d59-133">Read-only</span></span><br/>  | <span data-ttu-id="07d59-134">Obtém a coleção de dados definidos pelo aplicativo que são armazenados no objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="07d59-134">Gets the collection of application-defined data that is stored in the **InkDrawingAttributes** object.</span></span><br/>                                                                |
| [<span data-ttu-id="07d59-135">**FitToCurve**</span><span class="sxs-lookup"><span data-stu-id="07d59-135">**FitToCurve**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | <span data-ttu-id="07d59-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-136">Read/write</span></span><br/> | <span data-ttu-id="07d59-137">Obtém ou define o valor que especifica se a tinta é renderizada como uma série de curvas, em vez de linhas entre pontos de exemplo de caneta.</span><span class="sxs-lookup"><span data-stu-id="07d59-137">Gets or sets the value that specifies whether ink is rendered as a series of curves instead of as lines between pen sample points.</span></span><br/>                                    |
| [<span data-ttu-id="07d59-138">**Altura**</span><span class="sxs-lookup"><span data-stu-id="07d59-138">**Height**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | <span data-ttu-id="07d59-139">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-139">Read/write</span></span><br/> | <span data-ttu-id="07d59-140">Obtém ou define a altura da caneta ao desenhar tinta com este objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="07d59-140">Gets or sets the height of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                        |
| [<span data-ttu-id="07d59-141">**IgnorePressure**</span><span class="sxs-lookup"><span data-stu-id="07d59-141">**IgnorePressure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | <span data-ttu-id="07d59-142">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-142">Read/write</span></span><br/> | <span data-ttu-id="07d59-143">Obtém ou define o valor que especifica se a tinta desenhada se torna automaticamente mais larga com uma pressão maior da dica de caneta na superfície do Tablet.</span><span class="sxs-lookup"><span data-stu-id="07d59-143">Gets or sets the value that specifies whether drawn ink automatically becomes wider with increased pressure of the pen tip on the tablet surface.</span></span><br/>                     |
| [<span data-ttu-id="07d59-144">**PenTip**</span><span class="sxs-lookup"><span data-stu-id="07d59-144">**PenTip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | <span data-ttu-id="07d59-145">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-145">Read/write</span></span><br/> | <span data-ttu-id="07d59-146">Obtém ou define a dica de caneta a ser usada (bola ou retângulo) ao desenhar tinta com este objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="07d59-146">Gets or sets the pen tip to use (ball or rectangle) when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                       |
| [<span data-ttu-id="07d59-147">**RasterOperation**</span><span class="sxs-lookup"><span data-stu-id="07d59-147">**RasterOperation**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | <span data-ttu-id="07d59-148">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-148">Read/write</span></span><br/> | <span data-ttu-id="07d59-149">Obtém ou define como a cor da caneta interage com as cores de plano de fundo existentes na exibição quando a tinta é desenhada.</span><span class="sxs-lookup"><span data-stu-id="07d59-149">Gets or sets how the pen color interacts with the existing background colors on the display when the ink is drawn.</span></span><br/>                                                    |
| [<span data-ttu-id="07d59-150">**Transparência**</span><span class="sxs-lookup"><span data-stu-id="07d59-150">**Transparency**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | <span data-ttu-id="07d59-151">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-151">Read/write</span></span><br/> | <span data-ttu-id="07d59-152">Obtém ou define o valor de transparência da tinta desenhada.</span><span class="sxs-lookup"><span data-stu-id="07d59-152">Gets or sets the transparency value of drawn ink.</span></span> <span data-ttu-id="07d59-153">Os valores variam de zero (totalmente opaco) a 255 (totalmente transparente).</span><span class="sxs-lookup"><span data-stu-id="07d59-153">Values range from zero (totally opaque) to 255 (totally transparent).</span></span><br/>                                               |
| [<span data-ttu-id="07d59-154">**Largura**</span><span class="sxs-lookup"><span data-stu-id="07d59-154">**Width**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | <span data-ttu-id="07d59-155">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07d59-155">Read/write</span></span><br/> | <span data-ttu-id="07d59-156">Obtém ou define a largura da caneta ao desenhar tinta com este objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="07d59-156">Gets or sets the width of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="07d59-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="07d59-157">Remarks</span></span>

<span data-ttu-id="07d59-158">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="07d59-158">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="07d59-159">Esses atributos de desenho podem ser associados a um traço ou cursor e especificar configurações como cor, largura e transparência.</span><span class="sxs-lookup"><span data-stu-id="07d59-159">These drawing attributes can be associated with a stroke or a cursor and specify settings such as color, width, and transparency.</span></span>

<span data-ttu-id="07d59-160">Para especificar os atributos de desenho de um traço, use a propriedade [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) do objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="07d59-160">To specify the drawing attributes of a stroke, use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span> <span data-ttu-id="07d59-161">Para especificar os atributos de desenho de todos os traços dentro de uma coleção de traços, chame o método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) da coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="07d59-161">To specify the drawing attributes of all of the strokes within a collection of strokes, call the [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) method of the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

<span data-ttu-id="07d59-162">Cada objeto [**InkCollector**](inkcollector-class.md) , objeto [**InkOverlay**](inkoverlay-class.md) e controle [InkPicture](inkpicture-control-reference.md) pode especificar um conjunto diferente de atributos de desenho para o mesmo cursor.</span><span class="sxs-lookup"><span data-stu-id="07d59-162">Each [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control can specify a different set of drawing attributes for the same cursor.</span></span> <span data-ttu-id="07d59-163">Use a propriedade [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) para obter ou definir os atributos de desenho de um cursor.</span><span class="sxs-lookup"><span data-stu-id="07d59-163">Use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object to get or set the drawing attributes of a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d59-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07d59-164">Requirements</span></span>



| <span data-ttu-id="07d59-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d59-165">Requirement</span></span> | <span data-ttu-id="07d59-166">Valor</span><span class="sxs-lookup"><span data-stu-id="07d59-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d59-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07d59-167">Minimum supported client</span></span><br/> | <span data-ttu-id="07d59-168">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="07d59-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="07d59-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07d59-169">Minimum supported server</span></span><br/> | <span data-ttu-id="07d59-170">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="07d59-170">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="07d59-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07d59-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="07d59-172"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="07d59-172"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="07d59-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07d59-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="07d59-174"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d59-174"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="07d59-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="07d59-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d59-176">**Propriedade DrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-176">**DrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

<span data-ttu-id="07d59-177">**Propriedade DrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-177">**DrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="07d59-178">**Propriedade DrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-178">**DrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="07d59-179">**Propriedade DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-179">**DefaultDrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

<span data-ttu-id="07d59-180">**Propriedade DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-180">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="07d59-181">**Propriedade DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-181">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="07d59-182">**Método ModifyDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="07d59-182">**ModifyDrawingAttributes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[<span data-ttu-id="07d59-183">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="07d59-183">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="07d59-184">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="07d59-184">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

[<span data-ttu-id="07d59-185">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="07d59-185">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

