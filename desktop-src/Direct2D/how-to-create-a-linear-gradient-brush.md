---
title: Como criar um pincel de gradiente linear
description: Mostra como criar um pincel de gradiente linear usando Direct2D.
ms.assetid: 3cf5acc6-2f17-49d4-aca5-a84a846d1749
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 3a50a6e3ab421e2275644051ed647d5c4501f8e0
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824134"
---
# <a name="how-to-create-a-linear-gradient-brush"></a>Como criar um pincel de gradiente linear

Para criar um pincel de gradiente linear, use o método [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) e especifique as propriedades de pincel de gradiente linear e a coleção de parada de gradiente. Algumas sobrecargas permitem que você especifique as propriedades do pincel. O código a seguir mostra como criar um pincel de gradiente linear para preencher um quadrado e um pincel preto sólido para desenhar a estrutura de tópicos do quadrado.

O código produz a saída mostrada na ilustração a seguir.

![ilustração de um quadrado preenchido com um pincel de gradiente linear](images/brushes-ovw-lineargradient.png)

1.  Declare uma variável do tipo [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).
    ```C++
        ID2D1LinearGradientBrush *m_pLinearGradientBrush;
    ```

    

2.  Use o método [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_id2d1gradientstopcollection)) para criar a coleção [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) com uma matriz declarada de estruturas de [**\_ \_ parada de gradiente d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) , conforme mostrado no código a seguir.
    > [!Note]  
    > A partir do Windows 8, você pode usar o método [**ID2D1DeviceContext:: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) para criar uma coleção [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) em vez disso. Essa interface adiciona gradientes de alta cor e a interpolação de gradientes em cores retas ou prmultiplieds. Consulte a página **ID2DDeviceContext:: CreateGradientStopCollection** para obter mais informações.

     

    ```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
    ```

    

3.  Use o [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) para criar um pincel de gradiente linear, preencha o quadrado com o pincel e desenhe o quadrado com o pincel de cor preta.
    ```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Direct2D](reference.md)
</dt> </dl>

 

 
