---
title: Como desenhar e preencher uma forma complexa
description: Direct2D fornece a interface ID2D1PathGeometry para descrever formas complexas que podem conter curvas, arcos e linhas. Este tópico descreve como definir e renderizar uma geometria de caminho.
ms.assetid: d7aad487-04e0-448d-bedf-b8dfadc7bbe9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222d3d94eb1f9e944a1c5113baf938a7c3da6e86751a7be748798ace12a9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569197"
---
# <a name="how-to-draw-and-fill-a-complex-shape"></a>Como desenhar e preencher uma forma complexa

Direct2D fornece a interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) para descrever formas complexas que podem conter curvas, arcos e linhas. Este tópico descreve como definir e renderizar uma geometria de caminho.

Para definir uma geometria de caminho, primeiro use o método [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para criar a geometria do caminho e, em seguida, use o método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) de geometry do caminho para recuperar um [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Em seguida, você pode adicionar linhas, curvas e arcos chamando os vários métodos Add do coletor.

O exemplo a seguir cria um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), recupera um coletor e o usa para definir uma forma de ampulheta.


```C++
ID2D1GeometrySink *pSink = NULL;

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
```

Observe que um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) é um recurso independente de dispositivo e pode, portanto, ser criado uma vez e mantido durante a vida útil do aplicativo. (Para obter mais informações sobre diferentes tipos de recursos, consulte a [visão geral de recursos](resources-and-resource-domains.md).)

O exemplo a seguir cria dois pincéis que serão usados para pintar a estrutura de tópicos e o preenchimento da geometria de caminho.


```C++
if (SUCCEEDED(hr))
{
    // Create a black brush.
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &m_pBlackBrush
        );
}

if (SUCCEEDED(hr))
{
    // Create a linear gradient.
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 0.25f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = m_pRenderTarget->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(100, 0),
                D2D1::Point2F(100, 200)),
            D2D1::BrushProperties(),
            pGradientStops,
            &m_pLGBrush
            );
    }

    SafeRelease(&pGradientStops);
}
```



O exemplo final usa os métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) para pintar a estrutura de tópicos e o interior da geometria. Este exemplo produz a saída mostrada na ilustração a seguir.

![ilustração de uma geometria em forma de ampulheta](images/transformgeometryexample-1.png)


```C++
void DemoApp::RenderGeometryExample()
{
    // Translate subsequent drawings by 20 device-independent pixels.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Translation(20.f, 20.f)
        );

    // Draw the hour glass geometry at the upper left corner of the client area.
    m_pRenderTarget->DrawGeometry(m_pPathGeometry, m_pBlackBrush, 10.f);
    m_pRenderTarget->FillGeometry(m_pPathGeometry, m_pLGBrush);
}
```

O código foi omitido neste exemplo. Para obter mais informações sobre geometrias, consulte a [visão geral de geometrias](direct2d-geometries-overview.md).
