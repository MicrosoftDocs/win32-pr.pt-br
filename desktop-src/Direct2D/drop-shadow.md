---
title: Efeito de sombra
description: Use o efeito de sombra para gerar uma sombra do canal alfa de uma imagem.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- efeito de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d88924140caac22b688a0ccb6948ee74312411c770bff99360847ef2cd1b4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833036"
---
# <a name="shadow-effect"></a>Efeito de sombra

Use o efeito de sombra para gerar uma sombra do canal alfa de uma imagem. A sombra é mais opaca para valores alfa mais altos e mais transparente para valores alfa inferiores. Você pode definir a quantidade de desfoque e a cor da sombra.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Modos de otimização](#optimization-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

O CLSID para esse efeito é CLSID \_ D2D1Shadow.

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra a saída do efeito de sombra traduzida para baixo e para a direita com a imagem de origem composta sobre ela no local original. O efeito de sombra só saída a sombra.



| Antes                                                  |
|---------------------------------------------------------|
| ![a imagem antes do efeito.](images/8-crop.png)      |
| Depois                                                   |
| ![a imagem após a transformação.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BlurStandardDeviation<br/> DESVIO PADRÃO DE DESFOQUE DE \_ \_ PROP DE SOMBRA \_ \_ \_ D2D1<br/> | A quantidade de desfoque a ser aplicada ao canal alfa da imagem. Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3. As unidades do desvio padrão e do raio de desfoque são DIPs.<br/> Essa propriedade é a mesma que a propriedade [Desfoque Gaussiano](gaussian-blur.md) desvio padrão. <br/> O tipo é FLOAT.<br/> O valor padrão é 3.0f.<br/> |
| Color<br/> COR DO PROP DE SOMBRA D2D1 \_ \_ \_<br/>                                     | A cor da sombra. Essa propriedade é um VECTOR 4F D2D1 \_ \_ definido como: (R, G, B, A). Você deve especificar essa cor em alfa reto.<br/> O tipo é D2D1 \_ VECTOR \_ 4F.<br/> O valor padrão é {0.0f, 0.0f, 0.0f, 1.0f}.<br/>                                                                                                                                                                     |
| Optimization<br/> OTIMIZAÇÃO DE PROP SOMBRA D2D1 \_ \_ \_<br/>                       | O nível de otimização de desempenho.<br/> O tipo é D2D1 \_ SHADOW \_ OPTIMIZATION.<br/> O valor padrão é D2D1 \_ SHADOW \_ OPTIMIZATION \_ BALANCED.<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>Modos de otimização



| Nome                                          | Descrição                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| VELOCIDADE DE OTIMIZAÇÃO D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica otimizações internas, como pré-dimensionamento em raios relativamente pequenos. Usa filtragem linear.                                  |
| OTIMIZAÇÃO D2D1 \_ DIRECTIONALBLUR \_ \_ EQUILIBRADA | Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem trilinear.                                                    |
| QUALIDADE DA \_ OTIMIZAÇÃO D2D1 DIRECTIONALBLUR \_ \_  | Usa apenas otimizações internas com raios de desfoque grandes, em que as aproximações têm menor probabilidade de serem visíveis. Usa filtragem trilinear. |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o tamanho da saída de desfoque. A quantidade de crescimento do bitmap de saída em relação ao bitmap original pode ser calculada usando a seguinte equação:

Crescimento de bitmap de saída (X e Y) = BlurStandardDeviation (DIPs (pixels independentes de dispositivo)) \* 6 \* (DPI do usuário)/96

A saída aumenta igualmente em todas as direções, portanto, por exemplo, se o tamanho aumentar em 10 pixels em cada direção, o canto superior esquerdo do bitmap está localizado em (-5, -5) e o canto inferior direito será em (105, 105) conforme mostrado no diagrama aqui.

![diagrama de crescimento do tamanho da saída do efeito sombra.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

