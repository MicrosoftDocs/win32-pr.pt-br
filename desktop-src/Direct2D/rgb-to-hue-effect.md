---
title: Efeito de RGB para matiz
description: Converte uma imagem RGB nos espaços de cores HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369532"
---
# <a name="rgb-to-hue-effect"></a>Efeito de RGB para matiz

Converte uma imagem RGB nos espaços de cores HSL (Matiz, saturação, claridade) ou HSV (Matiz, saturação, valor).

HSL e HSV são dois modelos diferentes para representar uma cor RGB em um espaço de cores cilíndrico. Eles são úteis porque permitem que você tenha uma razão de uma cor usando conceitos mais intuitivos, como matiz e intensidade versus combinar valores vermelho, verde e azul.

Esse efeito normaliza os dados de saída (Matiz, valor de saturação para HSV ou matiz, saturação, claridade para HSL) para o intervalo de \[ 0, 1 \] .

O CLSID para esse efeito é CLSID \_ D2D1RgbToHue.

Para inverter o comportamento desse efeito, use o [efeito de matiz para RGB](hue-to-rgb-effect.md).

-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="sample-code"></a>Código de exemplo


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a>Propriedades do efeito

As propriedades do efeito de contraste são definidas pela enumeração [**de \_ \_ prop d2d1 RGBTOHUE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
