---
title: Métodos ID2D1Factory CreateTransformedGeometry (D2d1. h)
description: Transforma a geometria especificada e armazena o resultado como um objeto ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Métodos CreateTransformedGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757710"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a><span data-ttu-id="bada0-104">Métodos ID2D1Factory:: CreateTransformedGeometry</span><span class="sxs-lookup"><span data-stu-id="bada0-104">ID2D1Factory::CreateTransformedGeometry methods</span></span>

<span data-ttu-id="bada0-105">Transforma a geometria especificada e armazena o resultado como um objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bada0-105">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bada0-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="bada0-106">Overload list</span></span>



| <span data-ttu-id="bada0-107">Método</span><span class="sxs-lookup"><span data-stu-id="bada0-107">Method</span></span>                                                                                                                                                                                                                  | <span data-ttu-id="bada0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bada0-108">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bada0-109">[**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bada0-109">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F\*,ID2D1TransformedGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))</span></span> | <span data-ttu-id="bada0-110">Transforma a geometria especificada e armazena o resultado como um objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bada0-110">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |
| <span data-ttu-id="bada0-111">[**CreateTransformedGeometry (ID2D1Geometry \* , D2D \_ Matrix \_ 3x2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span><span class="sxs-lookup"><span data-stu-id="bada0-111">[**CreateTransformedGeometry(ID2D1Geometry\*,D2D\_MATRIX\_3X2\_F&,ID2D1TransformedGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))</span></span>  | <span data-ttu-id="bada0-112">Transforma a geometria especificada e armazena o resultado como um objeto [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bada0-112">Transforms the specified geometry and stores the result as an [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) object.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="bada0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bada0-113">Remarks</span></span>

<span data-ttu-id="bada0-114">Assim como outros recursos, uma geometria transformada herda o espaço de recursos e a política de Threading da fábrica que o criou.</span><span class="sxs-lookup"><span data-stu-id="bada0-114">Like other resources, a transformed geometry inherits the resource space and threading policy of the factory that created it.</span></span> <span data-ttu-id="bada0-115">Esse objeto é imutável.</span><span class="sxs-lookup"><span data-stu-id="bada0-115">This object is immutable.</span></span>

<span data-ttu-id="bada0-116">Ao traçar uma geometria transformada com o método [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) , a largura do traço não é afetada pela transformação aplicada à geometria.</span><span class="sxs-lookup"><span data-stu-id="bada0-116">When stroking a transformed geometry with the [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) method, the stroke width is not affected by the transform applied to the geometry.</span></span> <span data-ttu-id="bada0-117">A largura do traço só é afetada pela transformação do mundo.</span><span class="sxs-lookup"><span data-stu-id="bada0-117">The stroke width is only affected by the world transform.</span></span>

## <a name="examples"></a><span data-ttu-id="bada0-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bada0-118">Examples</span></span>

<span data-ttu-id="bada0-119">O exemplo a seguir cria um [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))e, em seguida, o Desenha sem transformá-lo.</span><span class="sxs-lookup"><span data-stu-id="bada0-119">The following example creates an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), then draws it without transforming it.</span></span> <span data-ttu-id="bada0-120">Ele produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="bada0-120">It produces the output shown in the following illustration.</span></span>

![ilustração de um retângulo](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



<span data-ttu-id="bada0-122">O exemplo a seguir usa o destino render para dimensionar a geometria por um fator de 3 e, em seguida, a desenha.</span><span class="sxs-lookup"><span data-stu-id="bada0-122">The next example uses the render target to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="bada0-123">A ilustração a seguir mostra o resultado do desenho do retângulo sem a transformação e com a transformação; observa que o traço é mais espesso após a transformação, embora a espessura do traço seja 1.</span><span class="sxs-lookup"><span data-stu-id="bada0-123">The following illustration shows the result of drawing the rectangle without the transform and with the transform; notices that the stroke is thicker after the transform, even though the stroke thickness is 1.</span></span>

![ilustração de um retângulo menor dentro de um retângulo maior com um traço mais espesso](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



<span data-ttu-id="bada0-125">O exemplo a seguir usa o método **CreateTransformedGeometry** para dimensionar a geometria por um fator de 3 e, em seguida, a desenha.</span><span class="sxs-lookup"><span data-stu-id="bada0-125">The next example uses the **CreateTransformedGeometry** method to scale the geometry by a factor of 3, then draws it.</span></span> <span data-ttu-id="bada0-126">Ele produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="bada0-126">It produces the output shown in the following illustration.</span></span> <span data-ttu-id="bada0-127">Observe que, embora o retângulo seja maior, seu traço ainda não aumentou.</span><span class="sxs-lookup"><span data-stu-id="bada0-127">Notice that, although the rectangle is larger, its stroke hasn't increased.</span></span>

![ilustração de um retângulo menor dentro de um retângulo maior com o mesmo traço](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a><span data-ttu-id="bada0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bada0-129">Requirements</span></span>



| <span data-ttu-id="bada0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bada0-130">Requirement</span></span> | <span data-ttu-id="bada0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bada0-131">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bada0-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bada0-132">Header</span></span><br/>  | <dl> <span data-ttu-id="bada0-133"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="bada0-133"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="bada0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bada0-134">Library</span></span><br/> | <dl> <span data-ttu-id="bada0-135"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bada0-135"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="bada0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bada0-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="bada0-137"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bada0-137"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bada0-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bada0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bada0-139">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="bada0-139">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
