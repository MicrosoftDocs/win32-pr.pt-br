---
title: Como desenhar e preencher uma forma básica
description: Este tópico descreve como desenhar uma forma básica.
ms.assetid: 8a68fc3f-118c-447b-856c-05417ae4ef29
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d072d6f43467aab9230796bfb24139630995e3f525c7e86a0c5e179ddd82048e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003711"
---
# <a name="how-to-draw-and-fill-a-basic-shape"></a>Como desenhar e preencher uma forma básica

Este tópico descreve como desenhar uma forma básica. A interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) fornece métodos para delinear e preencher re elipses, retângulos e linhas. Os exemplos a seguir mostram como criar e desenhar uma elipse.

Este tópico contém as seguintes seções:

-   [Desenhar o contorno de uma elipse com um traço sólido](#draw-the-outline-of-an-ellipse-with-a-solid-stroke)
-   [Desenhar uma elipse com um traço tracejado](#draw-an-ellipse-with-a-dashed-stroke)
-   [Desenhar e preencher uma elipse](#draw-and-fill-an-ellipse)
-   [Desenhando formas mais complexas](#drawing-more-complex-shapes)
-   [Tópicos relacionados](#related-topics)

## <a name="draw-the-outline-of-an-ellipse-with-a-solid-stroke"></a>Desenhar o contorno de uma elipse com um traço sólido

Para desenhar o contorno de uma elipse, defina um pincel (como [**uma ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ou [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)) para pintar o contorno e uma [**\_ ELLIPSE D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) para descrever a posição e as dimensões da elipse e, em seguida, passar esses objetos para o método [**ID2D1RenderTarget::D rawEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) O exemplo a seguir cria um pincel de cor sólida preta e o armazena no membro da classe m \_ spBlackBrush.


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black),
    &m_pBlackBrush
    );
```



O exemplo a seguir define uma [**\_ ELLIPSE D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) e a usa com o pincel definido no exemplo anterior para desenhar o contorno de uma elipse. Este exemplo produz a saída mostrada na ilustração a seguir.

![ilustração de uma elipse com um traço sólido](images/drawandfillellipseexample-1.png)


```C++
D2D1_ELLIPSE ellipse = D2D1::Ellipse(
    D2D1::Point2F(100.f, 100.f),
    75.f,
    50.f
    );

m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f);
```



## <a name="draw-an-ellipse-with-a-dashed-stroke"></a>Desenhar uma elipse com um traço tracejado

O exemplo anterior usou um traço simples. Você pode modificar a aparência de um traço de várias maneiras criando [**um ID2D1StroseStyle.**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) O **ID2D1StrkeStyle** permite especificar a forma no início e no final de um traço, se ele tem um padrão de traço e assim por diante. O exemplo a seguir cria **um ID2D1 CadakeStyle** que descreve um traço tracejado. Este exemplo usa um padrão de traço predefinido, [**D2D1 \_ DASH STYLE DASH DOT \_ \_ \_ \_ DOT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_dash_style), mas você também pode especificar seu próprio.


```C++
D2D1_STROKE_STYLE_PROPERTIES strokeStyleProperties = D2D1::StrokeStyleProperties(
    D2D1_CAP_STYLE_FLAT,  // The start cap.
    D2D1_CAP_STYLE_FLAT,  // The end cap.
    D2D1_CAP_STYLE_TRIANGLE, // The dash cap.
    D2D1_LINE_JOIN_MITER, // The line join.
    10.0f, // The miter limit.
    D2D1_DASH_STYLE_DASH_DOT_DOT, // The dash style.
    0.0f // The dash offset.
    );

hr = m_pDirect2dFactory->CreateStrokeStyle(strokeStyleProperties, NULL, 0, &m_pStrokeStyle);

```



O exemplo a seguir usa o estilo de traço com o [**método DrawEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) Este exemplo produz a saída mostrada na ilustração a seguir.

![ilustração de uma elipse com um traço tracejado](images/drawandfillellipseexample-2.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



## <a name="draw-and-fill-an-ellipse"></a>Desenhar e preencher uma elipse

Para pintar o interior de uma elipse, use o [**método FillEllipse.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) O exemplo a seguir usa o [**método DrawEllipse**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) para delinear a elipse e, em seguida, usa o **método FillEllipse** para pintar seu interior. Este exemplo produz a saída mostrada na ilustração a seguir.

![ilustração de uma elipse com um traço tracejado e, em seguida, preenchida com uma cor cinza sólida](images/drawandfillellipseexample-3.png)


```C++
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
```



O exemplo a seguir preenche a elipse primeiro e, em seguida, desenha seu contorno. Este exemplo produz a saída mostrada na ilustração a seguir.

![ilustração de uma elipse preenchida com uma cor cinza sólida e, em seguida, descrita com um traço tracejado](images/drawandfillellipseexample-4.png)


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pSilverBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 10.f, m_pStrokeStyle);
```



O código foi omitido desses exemplos.

## <a name="drawing-more-complex-shapes"></a>Desenhando formas mais complexas

Para desenhar formas mais complexas, defina objetos ID2D1Geometry e use-os com os métodos [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) e [**FillGeometry.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) Para obter mais informações, consulte a [Visão geral de geometrias.](direct2d-geometries-overview.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral de geometrias](direct2d-geometries-overview.md)
</dt> <dt>

[Visão geral de pincéis](direct2d-brushes-overview.md)
</dt> </dl>

 

 
