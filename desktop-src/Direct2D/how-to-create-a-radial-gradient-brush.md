---
title: Como criar um pincel gradiente radial
description: Mostra como criar um pincel de gradiente radial usando Direct2D.
ms.assetid: 663743c9-16e9-4e3a-90b2-883ef0b8d5cf
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe3509a80f80132f4a5e5d65f62476be1cac61d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162322"
---
# <a name="how-to-create-a-radial-gradient-brush"></a>Como criar um pincel gradiente radial

Para criar um pincel de gradiente radial, use o método [**ID2DRenderTarget:: CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) e especifique as propriedades do pincel de gradiente radial e a coleção de parada de gradiente. Algumas sobrecargas permitem que você especifique as propriedades do pincel. O código a seguir mostra como criar um pincel de gradiente radial para preencher um círculo e um pincel preto sólido para desenhar o contorno do círculo.

O código produz a saída mostrada na ilustração a seguir.

![ilustração de um círculo preenchido com um pincel de gradiente radial](images/brushes-ovw-radials.png)

1.  Declare uma variável do tipo [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).
    ```C++
        ID2D1RadialGradientBrush *m_pRadialGradientBrush;
    ```

    

2.  Crie uma matriz de estruturas de [**\_ \_ parada de gradiente d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) para colocar na coleção de parada de gradiente. A estrutura de **\_ \_ parada de gradiente d2d1** contém a posição e a cor de uma parada de gradiente. A posição indica a posição relativa da parada do gradiente no pincel. O valor está no intervalo \[ 0,0 f, 1,0 f \] , conforme mostrado no código a seguir.

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

    

3.  Use o método [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para criar a coleção [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) de uma matriz declarada anteriormente de estruturas de [**\_ \_ parada de gradiente d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Em seguida, use o [**CreateRadialGradientBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) para criar um pincel de gradiente radial.

    > [!Note]  
    > A partir do Windows 8, você pode usar o método [**ID2D1DeviceContext:: CreateGradientStopCollection**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-creategradientstopcollection) para criar uma coleção [**ID2D1GradientStopCollection1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1gradientstopcollection1) em vez do método [**ID2D1RenderTarget:: CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) . Essa interface adiciona gradientes de alta cor e a interpolação de gradientes em cores retas ou prmultiplieds. Consulte a página **ID2DDeviceContext:: CreateGradientStopCollection** para obter mais informações.

     

    ```C++
    // The center of the gradient is in the center of the box.
    // The gradient origin offset was set to zero(0, 0) or center in this case.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateRadialGradientBrush(
            D2D1::RadialGradientBrushProperties(
                D2D1::Point2F(75, 75),
                D2D1::Point2F(0, 0),
                75,
                75),
            pGradientStops,
            &m_pRadialGradientBrush
            );
    }
    ```

    

    ```C++
    m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
    m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Direct2D](reference.md)
</dt> </dl>

 

 