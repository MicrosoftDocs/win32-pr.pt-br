---
title: Como transformar uma geometria
description: Mostra como transformar uma geometria usando Direct2D.
ms.assetid: de434615-14b1-4b66-b09b-e90468e03d58
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ae15d0b1da304f9dfe24ff5de33a9f1582e2ca05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105748241"
---
# <a name="how-to-transform-a-geometry"></a>Como transformar uma geometria

Para transformar uma geometria, você pode aplicar a transformação ao destino de renderização chamando [**SetTransform**](id2d1rendertarget-settransform.md) ou aplicar a transformação à geometria chamando [**CreateTransformedGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)). Embora ambas as abordagens transformem uma geometria, elas têm algumas diferenças fundamentais. **CreateTransformedGeometry** afeta o preenchimento, mas não afeta a largura do traço. Além disso, o **CreateTransformedGeometry** transforma a geometria sozinha sem afetar outras formas no destino de renderização, enquanto [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) aplica a transformação a todas as formas no destino de renderização.

Este tópico de instruções descreve como transformar uma geometria chamando [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)).

**Para transformar uma geometria**

1.  Declare uma variável [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) .
2.  Chame o método [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) para criar uma geometria transformada.

O código a seguir mostra como criar um vidro de hora, transformar o vidro de hora e desenhar os óculos de hora original e resultante.


```C++
// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}

if (SUCCEEDED(hr))
{
    // Create a transformed geometry which is tilted at an angle to the previous geometry
    hr = m_pD2DFactory->CreateTransformedGeometry(
        m_pPathGeometry,
        D2D1::Matrix3x2F::Rotation(
            45.f,
            D2D1::Point2F(100, 100)),
        &m_pTransformedGeometry
        );
}
```



 

 