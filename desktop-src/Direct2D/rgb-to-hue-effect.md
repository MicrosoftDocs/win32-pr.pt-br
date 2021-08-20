---
title: Efeito RGB para matiz
description: Converte uma imagem RGB nos espaços de cores HSL (Matiz, Saturação, Luz) ou HSV (Matiz, Saturação, Valor).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c474705d050c2ef2eff9050a759c60c5d8f1098440e06601ec1e3981e349aaff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160382"
---
# <a name="rgb-to-hue-effect"></a>Efeito RGB para matiz

Converte uma imagem RGB nos espaços de cores HSL (Matiz, Saturação, Luz) ou HSV (Matiz, Saturação, Valor).

HSL e HSV são dois modelos diferentes para representar uma cor RGB em um espaço de cores cilíndrica. Eles são úteis porque permitem que você adoece uma cor usando conceitos mais intuitivos, como matiz e intensidade, em vez de combinar valores vermelhos, verdes e azuis.

Esse efeito normaliza os dados de saída (matiz, valor de saturação para HSV ou matiz, saturação, leveza para HSL) para o intervalo \[ 0, 1 \] .

O CLSID para esse efeito é CLSID \_ D2D1RgbTo Ltda.

Para reverter o comportamento desse efeito, use o [efeito Hue para RGB](hue-to-rgb-effect.md).

-   [Código de exemplo](#sample-code)
-   [Propriedades de efeito](#effect-properties)
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



## <a name="effect-properties"></a>Propriedades de efeito

As propriedades para o efeito de contraste são definidas pela [**enumeração D2D1 \_ RGBTO \_ LTDA.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Servidor mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Cabeçalho                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
