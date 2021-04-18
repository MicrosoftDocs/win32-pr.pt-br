---
title: Métodos SetTransform de ID2D1Brush (D2d1 \_ 1. h)
description: Define a transformação aplicada ao pincel.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- Métodos SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766332"
---
# <a name="id2d1brushsettransform-methods"></a><span data-ttu-id="1452e-104">Métodos ID2D1Brush:: SetTransform</span><span class="sxs-lookup"><span data-stu-id="1452e-104">ID2D1Brush::SetTransform methods</span></span>

<span data-ttu-id="1452e-105">Define a transformação aplicada ao pincel.</span><span class="sxs-lookup"><span data-stu-id="1452e-105">Sets the transformation applied to the brush.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1452e-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="1452e-106">Overload list</span></span>



| <span data-ttu-id="1452e-107">Método</span><span class="sxs-lookup"><span data-stu-id="1452e-107">Method</span></span>                                                                                       | <span data-ttu-id="1452e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1452e-108">Description</span></span>                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span data-ttu-id="1452e-109">[**SetTransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="1452e-109">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="1452e-110">Define a transformação aplicada ao pincel.</span><span class="sxs-lookup"><span data-stu-id="1452e-110">Sets the transformation applied to the brush.</span></span><br/> |
| <span data-ttu-id="1452e-111">[**SetTransform ( \_ matriz d2d1 \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="1452e-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="1452e-112">Define a transformação aplicada ao pincel.</span><span class="sxs-lookup"><span data-stu-id="1452e-112">Sets the transformation applied to the brush.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1452e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1452e-113">Remarks</span></span>

<span data-ttu-id="1452e-114">Quando você pinta com um pincel, ele pinta no espaço de coordenadas do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1452e-114">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="1452e-115">Os pincéis não se posicionam automaticamente para se alinharem com o objeto que está sendo pintado; Por padrão, eles começam a pintar na origem (0, 0) do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1452e-115">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="1452e-116">Você pode "mover" o gradiente definido por um [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) para uma área de destino definindo seu ponto de partida e ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="1452e-116">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="1452e-117">Da mesma forma, você pode mover o gradiente definido por um [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) alterando seu centro e raios.</span><span class="sxs-lookup"><span data-stu-id="1452e-117">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="1452e-118">Para alinhar o conteúdo de um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) à área que está sendo pintada, você pode usar o método **SetTransform** para converter o bitmap no local desejado.</span><span class="sxs-lookup"><span data-stu-id="1452e-118">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the **SetTransform** method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="1452e-119">Essa transformação afeta apenas o pincel; Ele não afeta nenhum outro conteúdo desenhado pelo destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="1452e-119">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="1452e-120">As ilustrações a seguir mostram o efeito de usar um [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para preencher um retângulo localizado em (100, 100).</span><span class="sxs-lookup"><span data-stu-id="1452e-120">The following illustrations show the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="1452e-121">A ilustração na ilustração à esquerda mostra o resultado do preenchimento do retângulo sem transformar o pincel: o bitmap é desenhado na origem do destino do processamento.</span><span class="sxs-lookup"><span data-stu-id="1452e-121">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="1452e-122">Como resultado, apenas uma parte do bitmap é exibida no retângulo.</span><span class="sxs-lookup"><span data-stu-id="1452e-122">As a result, only a portion of the bitmap appears in the rectangle.</span></span>

<span data-ttu-id="1452e-123">A ilustração à direita mostra o resultado da transformação do [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para que seu conteúdo seja deslocado 50 pixels para a direita e 50 pixels para baixo.</span><span class="sxs-lookup"><span data-stu-id="1452e-123">The illustration on the right shows the result of transforming the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="1452e-124">O bitmap agora preenche o retângulo.</span><span class="sxs-lookup"><span data-stu-id="1452e-124">The bitmap now fills the rectangle.</span></span>

![ilustração de dois quadrados, um pintado com um bitmap sem um pincel transformado e um pintado com um pincel transformado](images/brushes-ovw-transform.png)

## <a name="examples"></a><span data-ttu-id="1452e-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1452e-126">Examples</span></span>

<span data-ttu-id="1452e-127">Os exemplos de código a seguir mostram como criar a transformação mostrada no diagrama à direita na ilustração anterior.</span><span class="sxs-lookup"><span data-stu-id="1452e-127">The following code examples show how to create the transformation shown in the right diagram in the preceding illustration.</span></span> <span data-ttu-id="1452e-128">Primeiro, aplique uma tradução ao [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), movendo o pincel 50 pixels para o eixo x e 50 pixels para baixo ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="1452e-128">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="1452e-129">Em seguida, use o **ID2D1BitmapBrush** para preencher o retângulo que tem o canto superior esquerdo em (100, 100) e no canto inferior direito em (200, 200).</span><span class="sxs-lookup"><span data-stu-id="1452e-129">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a><span data-ttu-id="1452e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1452e-130">Requirements</span></span>



| <span data-ttu-id="1452e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1452e-131">Requirement</span></span> | <span data-ttu-id="1452e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1452e-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1452e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1452e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1452e-134"><dt>D2d1 \_ 1. h (inclui D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1452e-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="1452e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1452e-135">Library</span></span><br/> | <dl> <span data-ttu-id="1452e-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1452e-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1452e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1452e-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="1452e-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1452e-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="1452e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="1452e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1452e-140">Visão geral de pincéis</span><span class="sxs-lookup"><span data-stu-id="1452e-140">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="1452e-141">**ID2D1Brush**</span><span class="sxs-lookup"><span data-stu-id="1452e-141">**ID2D1Brush**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

<span data-ttu-id="1452e-142">�</span><span class="sxs-lookup"><span data-stu-id="1452e-142">�</span></span>

<span data-ttu-id="1452e-143">�</span><span class="sxs-lookup"><span data-stu-id="1452e-143">�</span></span>
