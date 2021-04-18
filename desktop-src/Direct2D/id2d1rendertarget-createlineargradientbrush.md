---
title: Métodos CreateLinearGradientBrush ID2D1RenderTarget (D2d1. h)
description: Cria um objeto ID2D1LinearGradientBrush para áreas de pintura com um gradiente linear.
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- Métodos CreateLinearGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813002"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a><span data-ttu-id="5f7ea-104">Métodos ID2D1RenderTarget:: CreateLinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="5f7ea-104">ID2D1RenderTarget::CreateLinearGradientBrush methods</span></span>

<span data-ttu-id="5f7ea-105">Cria um objeto [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para áreas de pintura com um gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="5f7ea-105">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) object for painting areas with a linear gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="5f7ea-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="5f7ea-106">Overload list</span></span>



| <span data-ttu-id="5f7ea-107">Método</span><span class="sxs-lookup"><span data-stu-id="5f7ea-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="5f7ea-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f7ea-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7ea-109">[**CreateLinearGradientBrush ( \_ Propriedades de \_ pincel de gradiente LINEAR d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="5f7ea-109">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>                            | <span data-ttu-id="5f7ea-110">Cria um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contém as interrupções de gradiente especificadas, não tem transformação e tem uma opacidade base de 1,0.</span><span class="sxs-lookup"><span data-stu-id="5f7ea-110">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="5f7ea-111">[**CreateLinearGradientBrush (D2D1 \_ , \_ Propriedades de pincel de gradiente linear \_ \_&, \_ Propriedades de pincel d2d1 \_&, ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="5f7ea-111">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span>   | <span data-ttu-id="5f7ea-112">Cria um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contém as interrupções de gradiente especificadas e tem a transformação especificada e a opacidade base.</span><span class="sxs-lookup"><span data-stu-id="5f7ea-112">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="5f7ea-113">[**CreateLinearGradientBrush ( \_ Propriedades de \_ pincel de gradiente linear d2d1 \_ \_ \* , \_ Propriedades de pincel d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1LinearGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span><span class="sxs-lookup"><span data-stu-id="5f7ea-113">[**CreateLinearGradientBrush(D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1LinearGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))</span></span> | <span data-ttu-id="5f7ea-114">Cria um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que contém as interrupções de gradiente especificadas e tem a transformação especificada e a opacidade base.</span><span class="sxs-lookup"><span data-stu-id="5f7ea-114">Creates an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="5f7ea-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f7ea-115">Examples</span></span>

<span data-ttu-id="5f7ea-116">Para obter um exemplo que mostra como criar uma coleção de parada de gradiente e usá-la para definir um gradiente linear, consulte [como criar um pincel de gradiente linear](how-to-create-a-linear-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="5f7ea-116">For an example showing how to create a gradient stop collection and use it to define a linear gradient, see [How to Create a Linear Gradient Brush](how-to-create-a-linear-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f7ea-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f7ea-117">Requirements</span></span>



| <span data-ttu-id="5f7ea-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f7ea-118">Requirement</span></span> | <span data-ttu-id="5f7ea-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5f7ea-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7ea-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f7ea-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5f7ea-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f7ea-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f7ea-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f7ea-122">Library</span></span><br/> | <dl> <span data-ttu-id="5f7ea-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f7ea-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f7ea-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5f7ea-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f7ea-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f7ea-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f7ea-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f7ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f7ea-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="5f7ea-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="5f7ea-128">**CreateGradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="5f7ea-128">**CreateGradientStopCollection**</span></span>](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[<span data-ttu-id="5f7ea-129">**ID2D1GradientStopCollection**</span><span class="sxs-lookup"><span data-stu-id="5f7ea-129">**ID2D1GradientStopCollection**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[<span data-ttu-id="5f7ea-130">**ID2D1LinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="5f7ea-130">**ID2D1LinearGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[<span data-ttu-id="5f7ea-131">**ID2D1RadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="5f7ea-131">**ID2D1RadialGradientBrush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[<span data-ttu-id="5f7ea-132">Como criar um pincel de gradiente linear</span><span class="sxs-lookup"><span data-stu-id="5f7ea-132">How to Create a Linear Gradient Brush</span></span>](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="5f7ea-133">Visão geral de pincéis</span><span class="sxs-lookup"><span data-stu-id="5f7ea-133">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="5f7ea-134">�</span><span class="sxs-lookup"><span data-stu-id="5f7ea-134">�</span></span>

<span data-ttu-id="5f7ea-135">�</span><span class="sxs-lookup"><span data-stu-id="5f7ea-135">�</span></span>
