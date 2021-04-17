---
title: Efeito de desfoque gaussiano
description: Use o efeito de desfoque gaussiano para criar um desfoque com base na função gaussiana em toda a imagem de entrada.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Desfoque Gaussiano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562327"
---
# <a name="gaussian-blur-effect"></a>Efeito de desfoque gaussiano

Use o efeito de desfoque gaussiano para criar um desfoque com base na função gaussiana em toda a imagem de entrada.

Você pode usar esse efeito para criar brilhos e soltar sombras e usar o efeito [composto](composite.md) para aplicar o resultado à imagem original. Ele é útil no processamento de fotos para filtros como realces e sombras. Você pode usar a saída desse efeito para entrada em efeitos de iluminação, como os efeitos de iluminação [especular](specular-lighting.md) ou de [iluminação difusa](diffuse-lighting.md) , porque o canal alfa está indefinido e efeitos de iluminação usam o canal alfa para determinar a geometria da superfície como um mapa de altura.

Esse efeito é usado pelo efeito de [sombra](drop-shadow.md) interna.

O CLSID para esse efeito é CLSID \_ D2D1GaussianBlur.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Modos de otimização](#optimization-modes)
-   [Modos de borda](#border-modes)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| After (após)                                                        |
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



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                    | Descrição                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| I<br/> \_ \_ Desvio padrão da prop d2d1 GAUSSIANBLUR \_ \_<br/> | A quantidade de desfoque a ser aplicada à imagem. Você pode calcular o raio de desfoque do kernel multiplicando o desvio padrão por 3. As unidades do desvio padrão e do raio de desfoque são DIPs. Um valor de DIPs zero desabilita totalmente esse efeito. O tipo é FLOAT.<br/> O valor padrão é 3.0 f.<br/> |
| Optimization<br/> \_Otimização de \_ prop d2d1 GAUSSIANBLUR \_<br/>             | O modo de otimização. Consulte [modos de otimização](#optimization-modes) para obter mais informações. O tipo é D2D1 \_ GAUSSIANBLUR \_ Optimization.<br/> O valor padrão é D2D1 \_ GAUSSIANBLUR \_ Optimization \_ baequilibrada.<br/>                                                                                                            |
| Bordermode<br/> \_Modo de \_ borda de prop d2d1 GAUSSIANBLUR \_ \_<br/>               | O modo usado para calcular a borda da imagem, suave ou difícil. Consulte [modos de borda](#border-modes) para obter mais informações. <br/> O tipo é o \_ modo de borda d2d1 GAUSSIANBLUR \_ \_ .<br/> O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Modos de otimização



| Nome                                          | Descrição                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Velocidade de otimização do D2D1 \_ DIRECTIONALBLUR \_ \_    | Aplica otimizações internas, como o dimensionamento prévio em raios relativamente pequenos. Usa filtragem linear.                                  |
| D2D1 \_ DIRECTIONALBLUR de \_ otimização \_ balanceada | Usa os mesmos limites de otimização que o modo de velocidade, mas usa filtragem triline.                                                    |
| \_Qualidade de \_ otimização de DIRECTIONALBLUR d2d1 \_  | Usa apenas otimizações internas com raios grandes de desfoque, em que as aproximações são menos prováveis de serem visíveis. Usa a filtragem triline. |



 

## <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | O efeito preenche a imagem com pixels pretos transparentes à medida que aplica o kernel de desfoque, resultando em uma borda suave. <br/>                                                                                             |
| \_Modo de borda d2d1 \_ \_ Hard | O efeito coloca a saída para o tamanho da imagem de entrada. Quando o efeito aplica o kernel de desfoque, ele estende a imagem de entrada com uma transformação de borda de tipo espelho para exemplos fora dos limites de entrada.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de saída

A saída desse efeito pode ser maior do que o bitmap de entrada com base no raio de desfoque e no modo de borda. Se o modo de borda for definido como \_ d2d1 \_ modo de borda \_ suave, os s imensionar do bitmap de saída aumentará pelo tamanho do kernel de desfoque, representado em pixels. Esta tabela fornece uma equação que você pode usar para calcular o bitmap de saída.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Portanto, se o tamanho da imagem aumentar por 10 pixels em cada direção, o canto superior esquerdo da imagem estará localizado em (-5,-5), enquanto o direito inferior estará em (105, 105).

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

 

