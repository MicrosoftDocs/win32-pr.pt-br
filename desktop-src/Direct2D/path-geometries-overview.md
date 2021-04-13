---
title: Visão geral de geometrias de caminho
description: Descreve como usar geometrias de caminho para definir formas complexas.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104552100"
---
# <a name="path-geometries-overview"></a>Visão geral de geometrias de caminho

Este tópico descreve como usar geometrias de caminho Direct2D para criar desenhos complexos. Ele contém as seguintes seções:

-   [Pré-requisitos](#prerequisites)
-   [Geometrias de caminho em Direct2D](#path-geometries-in-direct2d)
-   [Usando um ID2D1GeometrySink para popular uma geometria de caminho](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Exemplo: criar um desenho complexo](#example-create-a-complex-drawing)
    -   [Criar uma geometria de caminho para as montanhas à esquerda](#create-a-path-geometry-for-the-left-mountain)
    -   [Criar uma geometria de caminho para as montanhas certas](#create-a-path-geometry-for-the-right-mountain)
    -   [Criar uma geometria de caminho para o Sun](#create-a-path-geometry-for-the-sun)
    -   [Criar uma geometria de caminho para o rio](#create-a-path-geometry-for-the-river)
    -   [Renderizar as geometrias de caminho na exibição](#render-the-path-geometries-onto-the-display)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Esta visão geral pressupõe que você esteja familiarizado com a criação de aplicativos Direct2D básicos, conforme descrito em [criando um aplicativo Direct2D simples](direct2d-quickstart.md). Ele também pressupõe que você esteja familiarizado com os recursos básicos das geometrias de Direct2D, conforme descrito na [visão geral de geometrias](direct2d-geometries-overview.md).

## <a name="path-geometries-in-direct2d"></a>Geometrias de caminho em Direct2D

As geometrias de caminho são representadas pela interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) . Para criar uma instância de uma geometria de caminho, chame o método [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) . Esses objetos podem ser usados para descrever valores geométricos complexos compostos de segmentos como arcos, curvas e linhas. Para preencher uma geometria de caminho com figuras e segmentos, chame o método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para recuperar um [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) e use os métodos do coletor de geometria para adicionar figuras e segmentos à geometria do caminho.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Usando um ID2D1GeometrySink para popular uma geometria de caminho

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) descreve um caminho geométrico que pode conter linhas, arcos, curvas Bézier cúbicas e curvas de Bézier quadráticas.

Um coletor de geometria consiste em uma ou mais figuras. Cada figura é composta por um ou mais segmentos de linha, curva ou arco. Para criar uma figura, chame o método [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , passando o ponto inicial da figura e, em seguida, use seus métodos Add (como [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) e [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para adicionar segmentos. Quando você terminar de adicionar segmentos, chame o método [**endfigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) . Você pode repetir essa sequência para criar figuras adicionais. Quando você terminar de criar figuras, chame o método [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .

## <a name="example-create-a-complex-drawing"></a>Exemplo: criar um desenho complexo

A ilustração a seguir mostra um desenho complexo com linhas, arcos e curvas de Bézier. O exemplo de código a seguir mostra como criar o desenho usando quatro objetos Geometry de caminho, um para a montanha esquerda, um para as montanhas corretas, um para o rio e outro para o sol com flares.

![ilustração de um rio, montanhas e sol, usando geometrias de caminho](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Criar uma geometria de caminho para as montanhas à esquerda

O exemplo primeiro cria uma geometria de caminho para as montanhas à esquerda, conforme mostrado na ilustração a seguir.

![Mostra um desenho complexo de um polígono que mostra uma montanha.](images/path-geo-leftmnt.png)

Para criar a montanha à esquerda, o exemplo chama o método [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para criar um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



Em seguida, o exemplo usa o método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para obter um coletor de geometria de um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e o armazena na variável *pSink* .


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



Em seguida, o exemplo chama [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passando a [**Figura d2d1 de \_ \_ início \_ preenchido**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) que indica que esta figura está preenchida e, em seguida, chama [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passando uma matriz de pontos de [**d2d1 do \_ ponto \_ 2F**](d2d1-point-2f.md) , (267, 177), (236, 192), (212, 160), (156, 255) e (346, 255).

O código a seguir mostra como fazer isso.


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Criar uma geometria de caminho para as montanhas certas

Em seguida, o exemplo cria outra geometria de caminho para a montanha correta com pontos (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) e (575, 263). A ilustração a seguir mostra como as montanhas certas são exibidas.

![ilustração de um polígono que mostra uma montanha](images/path-geo-rightmnt.png)

O código a seguir mostra como fazer isso.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a>Criar uma geometria de caminho para o Sun

Em seguida, o exemplo popula outra geometria de caminho para o sol, conforme mostrado na ilustração a seguir.

![ilustração de curvas de arco e Bézier que mostram o sol](images/path-geo-sun.png)

Para fazer isso, a geometria do caminho cria um coletor e adiciona uma figura para o arco e uma figura para cada clarão para o coletor. Repetindo a sequência de [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), seus métodos Add (como [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) e [**enddefinem**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), várias figuras são adicionadas ao coletor.

O código a seguir mostra como fazer isso.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a>Criar uma geometria de caminho para o rio

Em seguida, o exemplo cria outro caminho de geometria para o rio que contém curvas de Bézier. A ilustração a seguir mostra como o rio é exibido.

![ilustração de curvas de Bézier que mostram um rio](images/path-geo-river.png)

O código a seguir mostra como fazer isso.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a>Renderizar as geometrias de caminho na exibição

O código a seguir mostra como renderizar as geometrias de caminho populadas na exibição. Ele primeiro desenha e pinta a geometria Sun, a próxima da geometria da montanha esquerda, a geometria de rio e, por fim, a geometria de montanha correta.


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



O exemplo completo gera a ilustração a seguir.

![ilustração de um rio, montanhas e sol, usando geometrias de caminho](images/path-geo-mnts.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um aplicativo Direct2D simples](direct2d-quickstart.md)
</dt> <dt>

[Visão geral de geometrias](direct2d-geometries-overview.md)
</dt> </dl>

 

 