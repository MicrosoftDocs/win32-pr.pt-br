---
title: Efeito de sombra
description: Use o efeito de sombra para gerar uma sombra do canal alfa de uma imagem.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- efeito de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294766"
---
# <a name="shadow-effect"></a>Efeito de sombra

Use o efeito de sombra para gerar uma sombra do canal alfa de uma imagem. A sombra é mais opaca para valores Alfa mais altos e mais transparente para valores Alfa inferiores. Você pode definir a quantidade de desfoque e a cor da sombra.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de otimização](#optimization-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

O CLSID para esse efeito é CLSID \_ D2D1Shadow.

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra a saída do efeito de sombra traduzida para baixo e para a direita com a imagem de origem composta por ela no local original. O efeito de sombra só gera a sombra.



| Antes                                                  |
|---------------------------------------------------------|
| ![a imagem antes do efeito.](images/8-crop.png)      |
| After (após)                                                   |
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



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BlurStandardDeviation<br/> \_ \_ \_ Desvio padrão de desfoque da d2d1 Shadow prop \_ \_<br/> | A quantidade de desfoque a ser aplicada ao canal alfa da imagem. Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3. As unidades do desvio padrão e do raio de desfoque são DIPs.<br/> Essa propriedade é igual à propriedade de desvio padrão de [Desfoque Gaussiano](gaussian-blur.md) . <br/> O tipo é FLOAT.<br/> O valor padrão é 3.0 f.<br/> |
| Cor<br/> \_Cor de \_ prop d2d1 Shadow \_<br/>                                     | A cor da sombra. Essa propriedade é um \_ vetor d2d1 \_ 4F definido como: (R, G, B, a). Você deve especificar essa cor em alfa linear.<br/> O tipo é \_ 4F de vetor d2d1 \_ .<br/> O valor padrão é {0,0 f, 0,0 f, 0,0 f, 1,0 f}.<br/>                                                                                                                                                                     |
| Optimization<br/> \_Otimização da \_ prop d2d1 Shadow \_<br/>                       | O nível de otimização de desempenho.<br/> O tipo é \_ otimização de sombra d2d1 \_ .<br/> O valor padrão é D2D1 \_ de \_ otimização de sombra \_ .<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>Modos de otimização



| Nome                                          | Descrição                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Velocidade de otimização do D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica otimizações internas, como o dimensionamento prévio em raios relativamente pequenos. Usa filtragem linear.                                  |
| D2D1 \_ DIRECTIONALBLUR de \_ otimização \_ balanceada | Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem triline.                                                    |
| \_Qualidade de \_ otimização de DIRECTIONALBLUR d2d1 \_  | Usa apenas otimizações internas com raios grandes de desfoque, em que as aproximações são menos prováveis de serem visíveis. Usa a filtragem triline. |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o tamanho da saída de desfoque. A quantidade de crescimento do bitmap de saída em relação ao bitmap original pode ser calculada usando a seguinte equação:

Crescimento do bitmap de saída (X e Y) = BlurStandardDeviation (pixels independentes do dispositivo (DIPs)) \* 6 \* (DPI do usuário)/96

A saída aumenta igualmente em todas as direções, por exemplo, se o tamanho aumenta por 10 pixels em cada direção, o canto superior esquerdo do bitmap está localizado em (-5,-5) e o direito inferior estará em (105, 105), conforme mostrado no diagrama aqui.

![diagrama de crescimento do tamanho de saída do efeito de sombra.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

