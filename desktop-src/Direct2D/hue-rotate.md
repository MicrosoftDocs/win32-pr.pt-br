---
title: Efeito de rotação de matiz
description: Use o efeito de rotação de matiz para alterar o matiz de uma imagem aplicando uma matriz de cores com base no ângulo de rotação.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- efeito de rotação de matiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ab9b1649db96bc5ee100df98ed10b4021b506e3ad71bb426778655348b2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569117"
---
# <a name="hue-rotatation-effect"></a>Efeito de rotação de matiz

Use o efeito de rotação de matiz para alterar o matiz de uma imagem aplicando uma matriz de cores com base no ângulo de rotação.

O CLSID para esse efeito é CLSID \_ D2D1Rotation.

-   [Imagem de exemplo](#example-image)
-   [Propriedades de efeito](#effect-properties)
-   [Bitmap de saída](#output-bitmap)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

O exemplo aqui mostra as imagens de entrada e saída do efeito de rotação de matiz com um ângulo de rotação de 270 graus.



| Antes                                                       |
|--------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg)   |
| Depois                                                        |
| ![a imagem após a transformação.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



O efeito calcula uma matriz de cores com base no ângulo de rotação (*?*) especificado com a propriedade D2D1 \_ HUEROTATION \_ PROP \_ ANGLE. Aqui estão as equações de matriz.

![cálculos de rotação de matiz](images/hue-formula.png)

A matriz criada depende apenas do ângulo de rotação. Você poderá usar o efeito [da matriz](color-matrix.md) de cores se precisar de uma matriz específica.

## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                         | Tipo e valor padrão           | Descrição                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| Ângulo<br/> D2D1 \_ HUEROTATION \_ PROP \_ ANGLE<br/> | FLOAT<br/> 0.0f<br/> | O ângulo para girar o matiz, em graus. |



 

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

 

