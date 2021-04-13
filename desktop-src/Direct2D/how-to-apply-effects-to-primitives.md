---
title: Como aplicar efeitos a primitivos
description: Este tópico mostra como aplicar uma série de efeitos a primitivos Direct2D e DirectWrite.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366433"
---
# <a name="how-to-apply-effects-to-primitives"></a>Como aplicar efeitos a primitivos

Este tópico mostra como aplicar uma série de efeitos a primitivos [Direct2D](./direct2d-portal.md) e [DirectWrite](direct2d-and-directwrite.md) .

Você pode usar a [API de efeitos Direct2D](effects-overview.md) para aplicar grafos de efeito a primitivos renderizados pelo [Direct2D](./direct2d-portal.md) para uma imagem. O exemplo aqui tem dois retângulos arredondados e o texto "Direct2D". Use Direct2D para desenhar os retângulos e [DirectWrite](direct2d-and-directwrite.md) para desenhar o texto.

![retângulos com o texto "Direct2D" em.](images/direct2d-rounded.png)

Usando [efeitos de Direct2D](effects-overview.md), você pode fazer com que essa imagem fique parecida com a próxima imagem. Aplique o [Desfoque Gaussiano](gaussian-blur.md), a [Iluminação especular ponto](specular-lighting.md), a [composição aritmética](arithmetic-composite.md)e os efeitos [compostos](composite.md) para os primitivos 2D para criar a imagem aqui.

![retângulos com o texto "Direct2D" dentro de depois que vários efeitos são aplicados.](images/direct2d-svg.png)

Depois de renderizar os retângulos e o texto em uma superfície intermediária, você pode usá-los como entrada para objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) no grafo de imagem.

Neste exemplo, defina a imagem original como a entrada para o [efeito de desfoque gaussiano](gaussian-blur.md) e, em seguida, defina a saída do Desfoque como a entrada para o [efeito de iluminação especular de ponto](specular-lighting.md). O resultado desse efeito é então composto com a imagem original duas vezes para obter a imagem final que é processada para a janela.

Aqui está um diagrama do gráfico de imagem.

![diagrama de gráfico de efeito.](images/effect-graph.png)

Esse grafo de efeito consiste em quatro objetos [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , cada um representando um efeito interno diferente. Você pode criar e conectar efeitos personalizados da mesma maneira, depois de registrá-los usando [**ID1D1Factory1:: RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). O código aqui cria os efeitos, define as propriedades e conecta o gráfico de efeito mostrado anteriormente.

1.  Crie o efeito de [Desfoque Gaussiano](gaussian-blur.md) usando o método [**ID2D1DeviceContext:: createeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) e especificando o CLSID apropriado. Os CLSIDs para os efeitos internos são definidos em d2d1effects. h. Em seguida, você define o desvio padrão do Desfoque usando o método [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

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

    

    O efeito de [Desfoque Gaussiano](gaussian-blur.md) desfoca todos os canais da imagem, incluindo o canal alfa.

2.  Crie o efeito de [Iluminação especular](point-specular.md) e defina as propriedades. A posição da luz é um vetor de 3 valores de ponto flutuante, portanto, você deve declará-lo como uma variável separada e passá-lo para o método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

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

    

    O efeito de [Iluminação especular](point-specular.md) usa o canal alfa da entrada para criar um mapa de altura para a iluminação.

3.  Há dois efeitos compostos diferentes que você pode usar o efeito [composto](composite.md) e a [composição aritmética](arithmetic-composite.md). Esse grafo de efeito usa ambos.

    Crie o efeito [composto](composite.md) e defina o modo como d2d1 de \_ origem do modo composto \_ \_ \_ em, que gera a interseção entre as imagens de origem e de destino.

    O efeito [composto aritmético](arithmetic-composite.md) compõe as duas imagens de entrada com base em uma fórmula definida pelo World Wide Web CONSORTIUM (W3C) para o padrão SVG (gráfico de vetor escalonável). Crie uma composição aritmética e defina os coeficientes para a fórmula.

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

    

    Nesse gráfico de efeito, os dois efeitos compostos levam a saída dos outros efeitos e da superfície intermediária como entradas e os compõe.

4.  Por fim, você conecta os efeitos para formar o grafo definindo as entradas para as imagens e os bitmaps apropriados.

    O primeiro efeito, [Desfoque Gaussiano](gaussian-blur.md), recebe sua entrada da superfície intermediária para a qual você renderiza os primitivos. Você define a entrada usando o método [**ID2D1Effect:: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) e especifica o índice de um objeto [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) . O desfoque gaussiano e os efeitos de [Iluminação especular](point-specular.md) têm apenas uma única entrada. O efeito de iluminação especular usa o canal alfa desfocado do Desfoque Gaussiano

    Os [efeitos compostos composto e](composite.md) [aritmético](arithmetic-composite.md) têm várias entradas. Para garantir que as imagens sejam colocadas juntas na ordem correta, você deve especificar o índice correto para cada imagem de entrada.

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

    

5.  Passe o objeto de efeito de [composição aritmético](arithmetic-composite.md) para o método [**ID2DDeviceContext::D RawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) e ele processa e desenha a saída do grafo.

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

    

 

 