---
title: Métodos ID2D1RenderTarget CreateRadialGradientBrush (D2d1. h)
description: Cria um objeto ID2D1RadialGradientBrush que pode ser usado para pintar áreas com um gradiente radial.
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- Métodos CreateRadialGradientBrush Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 680cc981943e45eb32834e48151f391f6249cc1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758702"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a><span data-ttu-id="00cf6-104">Métodos ID2D1RenderTarget:: CreateRadialGradientBrush</span><span class="sxs-lookup"><span data-stu-id="00cf6-104">ID2D1RenderTarget::CreateRadialGradientBrush methods</span></span>

<span data-ttu-id="00cf6-105">Cria um objeto [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que pode ser usado para pintar áreas com um gradiente radial.</span><span class="sxs-lookup"><span data-stu-id="00cf6-105">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) object that can be used to paint areas with a radial gradient.</span></span>

### <a name="overload-list"></a><span data-ttu-id="00cf6-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="00cf6-106">Overload list</span></span>



| <span data-ttu-id="00cf6-107">Método</span><span class="sxs-lookup"><span data-stu-id="00cf6-107">Method</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="00cf6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="00cf6-108">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00cf6-109">[**CreateRadialGradientBrush ( \_ Propriedades de \_ pincel de gradiente d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="00cf6-109">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>                            | <span data-ttu-id="00cf6-110">Cria um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contém as interrupções de gradiente especificadas, não tem transformação e tem uma opacidade base de 1,0.</span><span class="sxs-lookup"><span data-stu-id="00cf6-110">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops, has no transform, and has a base opacity of 1.0.</span></span> <br/> |
| <span data-ttu-id="00cf6-111">[**CreateRadialGradientBrush ( \_ Propriedades de \_ pincel de gradiente d2d1 \_ \_&, propriedades de pincel de d2d1 \_ \_&, ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="00cf6-111">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES&,D2D1\_BRUSH\_PROPERTIES&,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span>   | <span data-ttu-id="00cf6-112">Cria um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contém as interrupções de gradiente especificadas e tem a transformação especificada e a opacidade base.</span><span class="sxs-lookup"><span data-stu-id="00cf6-112">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |
| <span data-ttu-id="00cf6-113">[**CreateRadialGradientBrush ( \_ Propriedades de \_ pincel de gradiente d2d1 \_ \_ \* , \_ Propriedades de pincel d2d1 \_ \* , ID2D1GradientStopCollection \* , ID2D1RadialGradientBrush \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span><span class="sxs-lookup"><span data-stu-id="00cf6-113">[**CreateRadialGradientBrush(D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES\*,D2D1\_BRUSH\_PROPERTIES\*,ID2D1GradientStopCollection\*,ID2D1RadialGradientBrush\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))</span></span> | <span data-ttu-id="00cf6-114">Cria um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que contém as interrupções de gradiente especificadas e tem a transformação especificada e a opacidade base.</span><span class="sxs-lookup"><span data-stu-id="00cf6-114">Creates an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that contains the specified gradient stops and has the specified transform and base opacity.</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="00cf6-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="00cf6-115">Examples</span></span>

<span data-ttu-id="00cf6-116">Para obter um exemplo, consulte [como criar um pincel de gradiente radial](how-to-create-a-radial-gradient-brush.md).</span><span class="sxs-lookup"><span data-stu-id="00cf6-116">For an example, see [How to Create a Radial Gradient Brush](how-to-create-a-radial-gradient-brush.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00cf6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00cf6-117">Requirements</span></span>



| <span data-ttu-id="00cf6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="00cf6-118">Requirement</span></span> | <span data-ttu-id="00cf6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="00cf6-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00cf6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00cf6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="00cf6-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="00cf6-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="00cf6-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00cf6-122">Library</span></span><br/> | <dl> <span data-ttu-id="00cf6-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00cf6-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="00cf6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="00cf6-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="00cf6-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00cf6-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00cf6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="00cf6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00cf6-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="00cf6-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="00cf6-128">Como criar um pincel gradiente radial</span><span class="sxs-lookup"><span data-stu-id="00cf6-128">How to Create a Radial Gradient Brush</span></span>](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[<span data-ttu-id="00cf6-129">Visão geral de pincéis</span><span class="sxs-lookup"><span data-stu-id="00cf6-129">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> </dl>

<span data-ttu-id="00cf6-130">�</span><span class="sxs-lookup"><span data-stu-id="00cf6-130">�</span></span>

<span data-ttu-id="00cf6-131">�</span><span class="sxs-lookup"><span data-stu-id="00cf6-131">�</span></span>
