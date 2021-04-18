---
title: Métodos createellipsegeometry ID2D1Factory (D2d1. h)
description: Cria um ID2D1EllipseGeometry.
ms.assetid: 4c03bb0b-74fe-456a-aa26-5449d758c0ea
keywords:
- Métodos createellipsegeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ca991732b9a80fd93e3df3c2b72493f5195ea0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757334"
---
# <a name="id2d1factorycreateellipsegeometry-methods"></a><span data-ttu-id="ab6f0-104">Métodos ID2D1Factory:: createellipsegeometry</span><span class="sxs-lookup"><span data-stu-id="ab6f0-104">ID2D1Factory::CreateEllipseGeometry methods</span></span>

<span data-ttu-id="ab6f0-105">Cria um [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="ab6f0-105">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span>

### <a name="overload-list"></a><span data-ttu-id="ab6f0-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="ab6f0-106">Overload list</span></span>



| <span data-ttu-id="ab6f0-107">Método</span><span class="sxs-lookup"><span data-stu-id="ab6f0-107">Method</span></span>                                                                                                                                                      | <span data-ttu-id="ab6f0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab6f0-108">Description</span></span>                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="ab6f0-109">[**Createellipsegeometry (D2D1 \_ ELLIPSE&, ID2D1EllipseGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span><span class="sxs-lookup"><span data-stu-id="ab6f0-109">[**CreateEllipseGeometry(D2D1\_ELLIPSE&,ID2D1EllipseGeometry\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry))</span></span>  | <span data-ttu-id="ab6f0-110">Cria um [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="ab6f0-110">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |
| <span data-ttu-id="ab6f0-111">[**Createellipsegeometry ( \_ elipse d2d1 \* , ID2D1EllipseGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab6f0-111">[**CreateEllipseGeometry(D2D1\_ELLIPSE\*,ID2D1EllipseGeometry\*\*)**](/previous-versions/windows/desktop/legacy/dd371265(v=vs.85))</span></span> | <span data-ttu-id="ab6f0-112">Cria um [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span><span class="sxs-lookup"><span data-stu-id="ab6f0-112">Creates an [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry).</span></span> <br/> |



## <a name="examples"></a><span data-ttu-id="ab6f0-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab6f0-113">Examples</span></span>

<span data-ttu-id="ab6f0-114">O seguinte cria dois objetos [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e os combina usando os diferentes modos de combinação de geometria.</span><span class="sxs-lookup"><span data-stu-id="ab6f0-114">The following creates two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and combines them using the different geometry combine modes.</span></span>


```C++
HRESULT DemoApp::CreateGeometryResources()
{
    HRESULT hr = S_OK;
    ID2D1GeometrySink *pGeometrySink = NULL;

    // Create the first ellipse geometry to merge.
    const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
        D2D1::Point2F(75.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(
        circle1,
        &m_pCircleGeometry1
        );

    if (SUCCEEDED(hr))
    {
        // Create the second ellipse geometry to merge.
        const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
            D2D1::Point2F(125.0f, 75.0f),
            50.0f,
            50.0f
            );

        hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
    }


    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryUnion->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_UNION,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_INTERSECT to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryIntersect);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryIntersect->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_INTERSECT,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_XOR to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryXOR);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryXOR->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_XOR,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    if (SUCCEEDED(hr))
    {
        //
        // Use D2D1_COMBINE_MODE_EXCLUDE to combine the geometries.
        //
        hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryExclude);

        if (SUCCEEDED(hr))
        {
            hr = m_pPathGeometryExclude->Open(&pGeometrySink);

            if (SUCCEEDED(hr))
            {
                hr = m_pCircleGeometry1->CombineWithGeometry(
                    m_pCircleGeometry2,
                    D2D1_COMBINE_MODE_EXCLUDE,
                    NULL,
                    NULL,
                    pGeometrySink
                    );
            }

            if (SUCCEEDED(hr))
            {
                hr = pGeometrySink->Close();
            }

            SafeRelease(&pGeometrySink);
        }
    }

    return hr;
}
```



<span data-ttu-id="ab6f0-115">Esse código produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab6f0-115">This code produces the output shown in the following illustration.</span></span>

![ilustração de duas elipses combinadas usando quatro modos de combinação de geometria (Union, Intersect, Xor e Exclude)](images/combine-modes.png)

## <a name="requirements"></a><span data-ttu-id="ab6f0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab6f0-117">Requirements</span></span>



| <span data-ttu-id="ab6f0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab6f0-118">Requirement</span></span> | <span data-ttu-id="ab6f0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ab6f0-119">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6f0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab6f0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ab6f0-121"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab6f0-121"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab6f0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab6f0-122">Library</span></span><br/> | <dl> <span data-ttu-id="ab6f0-123"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab6f0-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="ab6f0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ab6f0-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="ab6f0-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab6f0-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6f0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab6f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab6f0-127">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="ab6f0-127">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
