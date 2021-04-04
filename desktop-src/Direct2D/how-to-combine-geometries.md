---
title: Como combinar geometrias
description: Mostra como combinar duas geometrias usando Direct2D.
ms.assetid: c5413e59-ae73-4797-b4ad-3a78ad700634
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8332421c62f49b60bb2186118ac7f741922fdc7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007874"
---
# <a name="how-to-combine-geometries"></a><span data-ttu-id="31a7d-103">Como combinar geometrias</span><span class="sxs-lookup"><span data-stu-id="31a7d-103">How to Combine Geometries</span></span>

<span data-ttu-id="31a7d-104">Este tópico descreve como combinar duas geometrias.</span><span class="sxs-lookup"><span data-stu-id="31a7d-104">This topic describes how to combine two geometries.</span></span> <span data-ttu-id="31a7d-105">O Direct2D dá suporte a quatro modos para combinar geometrias: Union, Intersect, XOR e exclude.</span><span class="sxs-lookup"><span data-stu-id="31a7d-105">Direct2D supports four modes for combining geometries: Union, Intersect, XOR, and Exclude.</span></span> <span data-ttu-id="31a7d-106">Esses modos são especificados no tipo de enumeração [**\_ \_ modo de combinação d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) .</span><span class="sxs-lookup"><span data-stu-id="31a7d-106">These modes are specified in the [**D2D1\_COMBINE\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) enum type.</span></span>

<span data-ttu-id="31a7d-107">**Para combinar duas geometrias usando qualquer um dos quatro modos**</span><span class="sxs-lookup"><span data-stu-id="31a7d-107">**To combine two geometries by using any of the four modes**</span></span>

1.  <span data-ttu-id="31a7d-108">Declare uma geometria de caminho: uma variável do tipo [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) que armazenará o resultado da combinação de geometria.</span><span class="sxs-lookup"><span data-stu-id="31a7d-108">Declare a path geometry: a variable of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) that will store the result of geometry combination.</span></span>
2.  <span data-ttu-id="31a7d-109">Declare um coletor de geometria: uma variável do tipo [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) que armazenará a geometria do caminho.</span><span class="sxs-lookup"><span data-stu-id="31a7d-109">Declare a geometry sink: a variable of type [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) that will store the path geometry.</span></span>
3.  <span data-ttu-id="31a7d-110">Crie o objeto de geometria de caminho chamando o método [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="31a7d-110">Create the path geometry object by calling the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span>
4.  <span data-ttu-id="31a7d-111">Abra o objeto de coletor de geometria chamando o método [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .</span><span class="sxs-lookup"><span data-stu-id="31a7d-111">Open the geometry sink object by calling the [**ID2D1PathGeometry::Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method.</span></span>
5.  <span data-ttu-id="31a7d-112">Use um dos quatro modos para combinar as duas geometrias chamando o método [**ID2D1EllipseGeometry:: CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) .</span><span class="sxs-lookup"><span data-stu-id="31a7d-112">Use one of the four modes to combine the two geometries by calling the [**ID2D1EllipseGeometry::CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) method.</span></span>
6.  <span data-ttu-id="31a7d-113">Feche o objeto de coletor de geometria.</span><span class="sxs-lookup"><span data-stu-id="31a7d-113">Close the geometry sink object.</span></span>

<span data-ttu-id="31a7d-114">O código a seguir declara as variáveis do tipo [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e **ID2D1GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="31a7d-114">The following code declares the variables of type [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and **ID2D1GeometrySink**.</span></span>


```C++
    ID2D1PathGeometry *m_pPathGeometryUnion;
    ID2D1PathGeometry *m_pPathGeometryIntersect;
    ID2D1PathGeometry *m_pPathGeometryXOR;
    ID2D1PathGeometry *m_pPathGeometryExclude;
```



<span data-ttu-id="31a7d-115">O código a seguir usa cada um dos quatro modos para combinar os dois objetos [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="31a7d-115">The following code uses each of the four modes to combine the two [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) objects and performs the following actions:</span></span>

-   <span data-ttu-id="31a7d-116">Cria duas reticências, m \_ spEllipseGeometryOne e m \_ spEllipseGeometryTwo.</span><span class="sxs-lookup"><span data-stu-id="31a7d-116">Creates two ellipses, m\_spEllipseGeometryOne and m\_spEllipseGeometryTwo.</span></span>
-   <span data-ttu-id="31a7d-117">Cria um objeto de geometria de caminho.</span><span class="sxs-lookup"><span data-stu-id="31a7d-117">Creates a path geometry object.</span></span>
-   <span data-ttu-id="31a7d-118">Abre um objeto de coletor de geometria.</span><span class="sxs-lookup"><span data-stu-id="31a7d-118">Opens a geometry sink object.</span></span>
-   <span data-ttu-id="31a7d-119">Combina as duas reticências.</span><span class="sxs-lookup"><span data-stu-id="31a7d-119">Combines the two ellipses.</span></span>
-   <span data-ttu-id="31a7d-120">Fecha o objeto de coletor de geometria.</span><span class="sxs-lookup"><span data-stu-id="31a7d-120">Closes the geometry sink object.</span></span>


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



<span data-ttu-id="31a7d-121">Esse código produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="31a7d-121">This code produces the output shown in the following illustration.</span></span>

![ilustração de duas geometrias e quatro modos para combinar as geometrias (Union, interseção, Xor e Exclude)](images/combine-modes.png)

## <a name="related-topics"></a><span data-ttu-id="31a7d-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31a7d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31a7d-124">**\_Modo de combinação de d2d1 \_**</span><span class="sxs-lookup"><span data-stu-id="31a7d-124">**D2D1\_COMBINE\_MODE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)
</dt> <dt>

[<span data-ttu-id="31a7d-125">**ID2D1EllipseGeometry**</span><span class="sxs-lookup"><span data-stu-id="31a7d-125">**ID2D1EllipseGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)
</dt> <dt>

[<span data-ttu-id="31a7d-126">**ID2D1PathGeometry**</span><span class="sxs-lookup"><span data-stu-id="31a7d-126">**ID2D1PathGeometry**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)
</dt> <dt>

<span data-ttu-id="31a7d-127">**ID2D1GeometrySink**</span><span class="sxs-lookup"><span data-stu-id="31a7d-127">**ID2D1GeometrySink**</span></span>
</dt> </dl>

 

 