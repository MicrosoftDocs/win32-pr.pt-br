---
title: Efeito de brilho
description: Use o efeito de brilho para controlar o brilho da imagem.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- efeito de brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104563971"
---
# <a name="brightness-effect"></a>Efeito de brilho

Use o efeito de brilho para controlar o brilho da imagem.

O CLSID para esse efeito é CLSID \_ D2D1Brightness.

-   [Imagem de exemplo](#example-image)
-   [Propriedades do efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                      |
|-------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)  |
| After (após)                                                       |
| ![a imagem após a transformação.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição da propriedade                                                 | Tipo e valor padrão                              | Descrição                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WhitePoint<br/> \_ \_ \_ Ponto branco de prop \_ d2d1 de brilho<br/> | \_Vetor d2d1 \_ 2F<br/> {1,0 f, 1,0 f}<br/> | A parte superior da curva de transferência de brilho. O ponto branco ajusta a aparência das partes mais brilhantes da imagem. Essa propriedade é para o valor x e o valor y, nessa ordem. Cada um dos valores dessa propriedade está entre 0 e 1, inclusive. |
| BlackPoint<br/> \_ \_ \_ Ponto preto de prop \_ d2d1 de brilho<br/> | \_Vetor d2d1 \_ 2F<br/> {0,0 f, 0,0 f}<br/> | A parte inferior da curva de transferência de brilho. O ponto preto ajusta a aparência das partes mais escuras da imagem. Essa propriedade é para o valor x e o valor y, nessa ordem. Cada um dos valores dessa propriedade está entre 0 e 1, inclusive.   |



 

Esse efeito usa os pontos branco e preto especificados para gerar uma função de transferência usada para ajustar o bitmap. A próxima equação descreve a função de transferência. As intensidades de entrada são definidas entre 0 e 1.

![algoritmo de brilho](images/brightness-formula1.png)

O algoritmo de efeito implementa uma equação que cria a função de transferência. Usamos essa função para ajustar os pixels da imagem. Os valores x e y do ponto preto e do ponto branco são as coordenadas em duas dimensões que estão conectadas para formar a transformação. Cada parte da equação de saída final:

1.  Converte os dados de imagem do espaço linear em espaço não linear usando esta equação:![função auxiliar 1](images/brightness-formula2.png)

2.  Ajusta a imagem de acordo com estes valores:
    -   *entrada* são os valores de intensidade de pixel da imagem de entrada de 0 a 1.

    -   *Pt branca. (x, y)* o local da curva de transformação para intensidades de pixel mais brilhantes.

    -   *Black pt. (x, y)* é o local da curva de transformação para intensidades de pixel do DIMM.

3.  Converte os dados da imagem de volta em espaço linear usando esta equação: ![função auxiliar 2](images/brightness-formula3.png)

A equação de saída final e as partes do componente são mostradas aqui.

![os cálculos completos para o ajuste de brilho](images/brightness-formula4.png)

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.

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

 

