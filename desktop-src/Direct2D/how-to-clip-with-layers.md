---
title: Como cortar em uma máscara geométrica
description: Mostra como cortar uma região com camadas.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c2258938020593014b5b6f5ea77516e7770f8589601cf4139971b3532b22fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569337"
---
# <a name="how-to-clip-to-a-geometric-mask"></a>Como cortar em uma máscara geométrica

Este tópico descreve como usar uma máscara geométrica para cortar uma região de uma camada.

**Para cortar uma região com uma máscara geométrica**

1.  Crie a [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) que será usada para cortar a região.
2.  Chame [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para criar uma camada.
3.  Chame [**ID2D1RenderTarget::P layer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e passe a máscara geométrica definida na etapa 1.
4.  Desenhe o conteúdo a ser clipe.
5.  Chame [**ID2D1RenderTarget::P opLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para remover a camada do destino de renderização.

O exemplo a seguir usa uma máscara geométrica para cortar uma imagem e vários retângulos. A ilustração a seguir mostra o bitmap original à esquerda e o bitmap recortado para a máscara geométrica à direita.

![ilustração de um bitmap goldfish antes e depois que o bitmap é recortado para uma máscara em forma de estrela](images/cliparegion-layers.png)

Para cortar o desenho, conforme mostrado na ilustração anterior, crie um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e use-o para definir uma estrela. O código a seguir mostra como fazer isso.


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



Chame [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para criar uma camada.

> [!Note]  
> Começando com Windows 8, você não precisa chamar [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)). Na maioria das situações, o desempenho será melhor se você não chamar esse método e Direct2D gerenciar os recursos de camada.

 

Chame [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) com a máscara de geometria para efetuar push da camada. Desenhe o conteúdo a ser clipe e chame [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para abrir a camada. Isso produz o desenho em forma de estrela. O código a seguir mostra como fazer isso.


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral das camadas](direct2d-layers-overview.md)
</dt> <dt>

[Direct2D Referência](reference.md)
</dt> </dl>

 

 