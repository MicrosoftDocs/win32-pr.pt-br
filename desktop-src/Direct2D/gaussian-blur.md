---
title: Efeito de desfoque gaussiano
description: Use o efeito de desfoque gaussiano para criar um desfoque com base na função gaussiana em toda a imagem de entrada.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Desfoque gaussiano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b759ed0f5f70c4fc11ad902c7a45db3b3059847ce6895d25c3dbb9c9eee8330
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967076"
---
# <a name="gaussian-blur-effect"></a>Efeito de desfoque gaussiano

Use o efeito de desfoque gaussiano para criar um desfoque com base na função gaussiana em toda a imagem de entrada.

Você pode usar esse efeito para criar brilhos e soltar sombras e usar o efeito composto para aplicar o resultado à imagem original. [](composite.md) Ele é útil no processamento de fotos para filtros como realçamentos e sombras. Você pode usar a saída desse efeito para [](specular-lighting.md) entrada em [](diffuse-lighting.md) efeitos de iluminação, como os efeitos iluminação especular ou iluminação difusa, porque o canal alfa também está desfocado e efeitos de iluminação usam o canal alfa para determinar a geometria da superfície como um mapa de altura.

Esse efeito é usado pelo efeito [sombra](drop-shadow.md) integrado.

O CLSID para esse efeito é CLSID \_ D2D1GaussianBlur.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Modos de otimização](#optimization-modes)
-   [Modos de borda](#border-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| Depois                                                        |
| ![a imagem após a transformação.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                                    | Descrição                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> D2D1 \_ DESVIO PADRÃO DE PROP DE GAUSSIANBLUR \_ \_ \_<br/> | A quantidade de desfoque a ser aplicada à imagem. Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3. As unidades do desvio padrão e do raio de desfoque são DIPs. Um valor de zero DIPs desabilita totalmente esse efeito. O tipo é FLOAT.<br/> O valor padrão é 3.0f.<br/> |
| Optimization<br/> OTIMIZAÇÃO DE PROP D2D1 \_ GAUSSIANBLUR \_ \_<br/>             | O modo de otimização. Confira [Modos de otimização](#optimization-modes) para obter mais informações. O tipo é OTIMIZAÇÃO \_ DE GAUSSIANBLUR D2D1. \_<br/> O valor padrão é D2D1 \_ GAUSSIANBLUR \_ OPTIMIZATION \_ BALANCED.<br/>                                                                                                            |
| BorderMode<br/> D2D1 \_ MODO DE BORDA DE PROP GAUSSIANBLUR \_ \_ \_<br/>               | O modo usado para calcular a borda da imagem, suave ou rígido. Confira [Modos de borda para](#border-modes) obter mais informações. <br/> O tipo é D2D1 \_ GAUSSIANBLUR \_ BORDER \_ MODE.<br/> O valor padrão é D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Modos de otimização



| Nome                                          | Descrição                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| VELOCIDADE DE OTIMIZAÇÃO D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica otimizações internas, como pré-dimensionamento em raios relativamente pequenos. Usa filtragem linear.                                  |
| OTIMIZAÇÃO D2D1 \_ DIRECTIONALBLUR \_ \_ EQUILIBRADA | Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem trilinear.                                                    |
| QUALIDADE DA OTIMIZAÇÃO D2D1 \_ DIRECTIONALBLUR \_ \_  | Usa apenas otimizações internas com raios de desfoque grandes, em que as aproximações têm menor probabilidade de serem visíveis. Usa filtragem trilinear. |



 

## <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ MODO DE BORDA \_ \_ SUAVE | O efeito padra a imagem com pixels pretos transparentes, pois aplica o kernel de desfoque, resultando em uma borda suave. <br/>                                                                                             |
| D2D1 \_ MODO DE BORDA \_ \_ RÍGIDO | O efeito fixa a saída ao tamanho da imagem de entrada. Quando o efeito aplica o kernel de desfoque, ele estende a imagem de entrada com uma transformação de borda do tipo espelho para exemplos fora dos limites de entrada.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

A saída desse efeito pode ser maior que o bitmap de entrada com base no raio de desfoque e no modo de borda. Se o modo de borda estiver definido como D2D1 BORDER MODE SOFT, o tamanho do bitmap de saída aumentará pelo tamanho do kernel de \_ \_ \_ desfoque, representado em pixels. Esta tabela fornece uma equação que você pode usar para calcular o bitmap de saída.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Portanto, se o tamanho da imagem aumentar em 10 pixels em cada direção, o canto superior esquerdo da imagem estará localizado em (-5, -5), enquanto o canto inferior direito estará em (105, 105).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

