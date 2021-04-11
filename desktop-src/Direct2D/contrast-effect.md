---
title: Efeito de contraste
description: Aumenta ou reduz o contraste de uma imagem.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009476"
---
# <a name="contrast-effect"></a>Efeito de contraste

Aumenta ou reduz o contraste de uma imagem.

O CLSID para esse efeito é CLSID \_ D2D1Contrast.

A função Contrast modifica cada valor de canal de cor usando dois, piecewises quadráticas de semipolinomiais que atendem à continuidade da inclinação no ponto (0,5, 0,5).

![polinomiais quadráticas piecewise que atendem à continuidade da inclinação no ponto (0,5, 0,5)](images/contrast-effect-slope.png)

-   [Imagens de exemplo](#example-images)
-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-images"></a>Imagens de exemplo

Este exemplo mostra a saída do efeito com o contraste máximo aplicado (Contrast = 1,0).

Antes

![imagem antes da aplicação do efeito](images/contrast-effect-before.png)

After (após)

![imagem após o efeito ser aplicado](images/contrast-effect-after.png)

## <a name="sample-code"></a>Código de exemplo

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriedades do efeito

As propriedades do efeito de contraste são definidas pela enumeração [**de \_ \_ prop Contrast d2d1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
