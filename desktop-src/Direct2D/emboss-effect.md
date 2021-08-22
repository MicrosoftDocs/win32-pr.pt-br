---
title: Efeito de entalhe
description: Cria uma versão em tons de cinza da imagem que aparece como se ela estivesse carimbada em papel.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0fe9b779cbad2b73b877338871f7adff3a36fb4bfb1c291be6de94f736088f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586956"
---
# <a name="emboss-effect"></a>Efeito de entalhe

Cria uma versão em tons de cinza da imagem que aparece como se ela estivesse carimbada em papel.

O CLSID para esse efeito é CLSID \_ D2D1Emboss.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/emboss-effect.png)

## <a name="sample-code"></a>Código de exemplo

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriedades do efeito

As propriedades do efeito de entalhe são definidas pela enumeração [**\_ \_ prop d2d1 relevo**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
