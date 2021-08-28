---
title: Efeito de detecção de borda
description: Filtra o conteúdo de uma imagem, deixando linhas nas bordas das seções contrastadas da imagem.
ms.assetid: d22868cf-95fe-690e-66ac-268d7e116aee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7067243c19ed65bcdc23f1654999ff10ad3b80bafa641d0d3da940719db7bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967057"
---
# <a name="edge-detection-effect"></a>Efeito de detecção de borda

Filtra o conteúdo de uma imagem, deixando linhas nas bordas das seções contrastadas da imagem.

O CLSID para esse efeito é CLSID \_ D2D1EdgeDetection.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades de efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/edge-detection-effect.png)

## <a name="sample-code"></a>Código de exemplo

```cpp
ComPtr<ID2D1Effect> edgeDetectionEffect;
m_d2dContext->CreateEffect(CLSID_D2D1EdgeDetection, &edgeDetectionEffect);
 
edgeDetectionEffect->SetInput(0, bitmap);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_STRENGTH, 0.5f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_BLUR_RADIUS, 0.0f);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_MODE, D2D1_EDGEDETECTION_MODE_SOBEL);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_OVERLAY_EDGES, false);
edgeDetectionEffect->SetValue(D2D1_EDGEDETECTION_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(edgeDetectionEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriedades de efeito

As propriedades do efeito de detecção de borda são definidas pela enumeração [**D2D1 \_ EDGEDETECTION \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_edgedetection_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Servidor mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Cabeçalho                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
