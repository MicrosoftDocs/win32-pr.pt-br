---
title: Efeito de matiz-to-RGB
description: Converte uma imagem HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor) para o espaço de cores RGB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918379"
---
# <a name="hue-to-rgb-effect"></a>Efeito de matiz-to-RGB

Converte uma imagem HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor) para o espaço de cores RGB.

HSL e HSV são dois modelos diferentes para representar uma cor RGB em um espaço de cores cilíndrico. Eles são úteis porque permitem que você tenha uma razão de uma cor usando conceitos mais intuitivos, como matiz e intensidade versus combinar valores vermelho, verde e azul.

Esse efeito passa por quaisquer valores Alfa de entrada.

O CLSID para esse efeito é CLSID \_ D2D1HueToRgb.

Para inverter o comportamento desse efeito, use o [efeito de RGB para matiz](rgb-to-hue-effect.md).

-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="sample-code"></a>Código de exemplo

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriedades do efeito

As propriedades do efeito de contraste são definidas pela enumeração [**de \_ \_ prop d2d1 HUETORGB**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |



## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
