---
title: Efeito de brilho
description: Use o efeito de brilho para controlar o brilho da imagem.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- efeito de brilho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88b67615948cbea74333605e900de194c0eeeb3d747d83af5eae8a750e6f135
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119215359"
---
# <a name="brightness-effect"></a>Efeito de brilho

Use o efeito de brilho para controlar o brilho da imagem.

O CLSID para esse efeito é CLSID \_ D2D1Brightness.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo



| Antes                                                      |
|-------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)  |
| Depois                                                       |
| ![a imagem após a transformação.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição da propriedade                                                 | Tipo e valor padrão                              | Descrição                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WhitePoint<br/> PONTO EM BRANCO DO \_ \_ PROP DE BRILHO \_ D2D1 \_<br/> | D2D1 \_ VECTOR \_ 2F<br/> {1.0f, 1.0f}<br/> | A parte superior da curva de transferência de brilho. O ponto em branco ajusta a aparência das partes mais interessantes da imagem. Essa propriedade é para o valor x e o valor y, nessa ordem. Cada um dos valores dessa propriedade está entre 0 e 1, inclusive. |
| BlackPoint<br/> PONTO PRETO DO \_ \_ PROP DE BRILHO \_ D2D1 \_<br/> | D2D1 \_ VECTOR \_ 2F<br/> {0.0f, 0.0f}<br/> | A parte inferior da curva de transferência de brilho. O ponto preto ajusta a aparência das partes mais escuras da imagem. Essa propriedade é para o valor x e o valor y, nessa ordem. Cada um dos valores dessa propriedade está entre 0 e 1, inclusive.   |



 

Esse efeito usa os pontos branco e preto especificados para gerar uma função de transferência usada para ajustar o bitmap. A próxima equação descreve a função de transferência. As intensidades de entrada são definidas entre 0 e 1.

![algoritmo de brilho](images/brightness-formula1.png)

O algoritmo de efeito implementa uma equação que cria a função de transferência. Usamos essa função para ajustar os pixels da imagem. Os valores x e y do ponto preto e do ponto em branco são as coordenadas em duas dimensões conectadas para formar a transformação. Cada parte da equação de saída final:

1.  Converte os dados de imagem de espaço linear em espaço não linear usando esta equação:![função auxiliar 1](images/brightness-formula2.png)

2.  Ajusta a imagem de acordo com estes valores:
    -   *input* são os valores de intensidade de pixel da imagem de entrada de 0 a 1.

    -   *White Pt. (x, y) o* local da curva de transformação para intenções de pixel mais brilhante.

    -   *Black Pt. (x, y) é* o local da curva de transformação para intensidades de pixel de imersão.

3.  Converte os dados de imagem de volta em espaço linear usando esta equação: ![função auxiliar 2](images/brightness-formula3.png)

A equação de saída final e as partes do componente são mostradas aqui.

![os cálculos completos para ajuste de brilho](images/brightness-formula4.png)

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é o mesmo que o tamanho do bitmap de entrada.

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

 

