---
title: Como aplicar efeitos a primitivos
description: Este tópico mostra como aplicar uma série de efeitos a Direct2D e DirectWrite primitivos.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17cbf1efe17d1c23c90382f3b95fb41e33946a93935b0be02fc5b41f314a8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569568"
---
# <a name="how-to-apply-effects-to-primitives"></a>Como aplicar efeitos a primitivos

Este tópico mostra como aplicar uma série de efeitos a Direct2D [e](./direct2d-portal.md) [DirectWrite](direct2d-and-directwrite.md) primitivos.

Você pode usar a [API Direct2D efeitos para](effects-overview.md) aplicar grafos de efeito a primitivos renderizados por Direct2D a uma imagem. [](./direct2d-portal.md) O exemplo aqui tem dois retângulos arredondados e o texto "Direct2D". Use Direct2D para desenhar os retângulos [e](direct2d-and-directwrite.md) DirectWrite desenhar o texto.

![retângulos com o texto "direct2d" dentro.](images/direct2d-rounded.png)

Usando [Direct2D efeitos](effects-overview.md), você pode fazer com que essa imagem se pareça com a próxima imagem. Aplique os Desfoque Gaussiano , [](composite.md) [a](gaussian-blur.md)iluminação [especular](specular-lighting.md)de ponto, a composição aritmética e os efeitos compostos aos primitivos 2D para criar a imagem aqui. [](arithmetic-composite.md)

![retângulos com o texto "direct2d" dentro depois que vários efeitos são aplicados.](images/direct2d-svg.png)

Depois de renderizar os retângulos e o texto em uma superfície intermediária, você pode usá-lo como entrada para [**objetos ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) no grafo de imagem.

Neste exemplo, de definir a imagem original como a entrada para o efeito Desfoque Gaussiano e, em seguida, definir [a](gaussian-blur.md) saída do desfoque como a entrada para o efeito de Iluminação [Especular de Ponto](specular-lighting.md). O resultado desse efeito é composto com a imagem original duas vezes para obter a imagem final renderizada na janela.

Aqui está um diagrama do grafo de imagem.

![diagrama de grafo de efeito.](images/effect-graph.png)

Esse grafo de efeito consiste em quatro [**objetos ID2D1Effect,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) cada um representando um efeito integrado diferente. Você pode criar e conectar efeitos personalizados da mesma maneira, depois de registrá-los usando [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). O código aqui cria os efeitos, define as propriedades e conecta o grafo de efeito mostrado anteriormente.

1.  Crie o [efeito de desfoque gaussiano](gaussian-blur.md) usando o [**método ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) e especificando o CLSID adequado. As CLSIDs para os efeitos integrados são definidas em d2d1effects.h. Em seguida, você definirá o desvio padrão do desfoque usando o [**método ID2D1Effect::SetValue.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    O [efeito de desfoque gaussiano](gaussian-blur.md) desfoque todos os canais da imagem, incluindo o canal alfa.

2.  Crie o [efeito de iluminação](point-specular.md) especular e de definir as propriedades. A posição da luz é um vetor de 3 valores de ponto flutuante, portanto, você deve declare-o como uma variável separada e passá-la para o [**método SetValue.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    O [efeito de iluminação especular](point-specular.md) usa o canal alfa da entrada para criar um mapa de altura para a iluminação.

3.  Há dois efeitos compostos diferentes que você pode usar o [efeito](composite.md) composto e a composição [aritmética](arithmetic-composite.md). Esse grafo de efeito usa ambos.

    Criar o [efeito composto](composite.md) e definir o modo como D2D1 COMPOSITE MODE SOURCE IN, que gera a interseção das imagens de \_ \_ \_ \_ origem e de destino.

    O [efeito composto](arithmetic-composite.md) aritmético compõe as duas imagens de entrada com base em uma fórmula definida pelo W3C (World Wide Web Consortium) para o padrão SVG (Gráficos Vetoriais Escalonáveis). Criar composição aritmética e definir os coeficientes para a fórmula.

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    Os coeficientes para o efeito [composto aritmético](arithmetic-composite.md) são mostrados aqui.

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    Nesse grafo de efeito, ambos os efeitos compostos levam a saída dos outros efeitos e da superfície intermediária como entradas e os composição.

4.  Por fim, você conecta os efeitos para formar o grafo definindo as entradas para as imagens e bitmaps adequados.

    O primeiro efeito, [desfoque gaussiano,](gaussian-blur.md)recebe sua entrada da superfície intermediária para a que você renderizado os primitivos. Você pode definir a entrada usando o método [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) e especificar o índice de [**um objeto ID2D1Image.**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) O desfoque gaussiano [e efeitos de iluminação especular](point-specular.md) têm apenas uma única entrada. O efeito de iluminação especular usa o canal alfa desfocado do desfoque gaussiano

    Os [efeitos compostos e](composite.md) [aritméticos](arithmetic-composite.md) têm várias entradas. Para garantir que as imagens sejam reunidas na ordem correta, você deve especificar o índice correto para cada imagem de entrada.

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  Passe o [objeto de efeito](arithmetic-composite.md) composto aritmético para o método [**ID2DDeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) e ele processa e desenha a saída do grafo.

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 