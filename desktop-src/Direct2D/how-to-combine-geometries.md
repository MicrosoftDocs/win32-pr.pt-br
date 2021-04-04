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
# <a name="how-to-combine-geometries"></a>Como combinar geometrias

Este tópico descreve como combinar duas geometrias. O Direct2D dá suporte a quatro modos para combinar geometrias: Union, Intersect, XOR e exclude. Esses modos são especificados no tipo de enumeração [**\_ \_ modo de combinação d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) .

**Para combinar duas geometrias usando qualquer um dos quatro modos**

1.  Declare uma geometria de caminho: uma variável do tipo [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) que armazenará o resultado da combinação de geometria.
2.  Declare um coletor de geometria: uma variável do tipo [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) que armazenará a geometria do caminho.
3.  Crie o objeto de geometria de caminho chamando o método [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .
4.  Abra o objeto de coletor de geometria chamando o método [**ID2D1PathGeometry:: Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) .
5.  Use um dos quatro modos para combinar as duas geometrias chamando o método [**ID2D1EllipseGeometry:: CombineWithGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) .
6.  Feche o objeto de coletor de geometria.

O código a seguir declara as variáveis do tipo [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e **ID2D1GeometrySink**.


```C++
    ID2D1PathGeometry *m_pPathGeometryUnion;
    ID2D1PathGeometry *m_pPathGeometryIntersect;
    ID2D1PathGeometry *m_pPathGeometryXOR;
    ID2D1PathGeometry *m_pPathGeometryExclude;
```



O código a seguir usa cada um dos quatro modos para combinar os dois objetos [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) e executa as seguintes ações:

-   Cria duas reticências, m \_ spEllipseGeometryOne e m \_ spEllipseGeometryTwo.
-   Cria um objeto de geometria de caminho.
-   Abre um objeto de coletor de geometria.
-   Combina as duas reticências.
-   Fecha o objeto de coletor de geometria.


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



Esse código produz a saída mostrada na ilustração a seguir.

![ilustração de duas geometrias e quatro modos para combinar as geometrias (Union, interseção, Xor e Exclude)](images/combine-modes.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**\_Modo de combinação de d2d1 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)
</dt> <dt>

[**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)
</dt> <dt>

[**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)
</dt> <dt>

**ID2D1GeometrySink**
</dt> </dl>

 

 