---
title: Croma-efeito de chave
description: Converte uma determinada cor mais ou menos uma tolerância para alfa. Por exemplo, croma-Key pode remover o plano de fundo de uma imagem para um efeito de sobreposição de tela verde.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824326"
---
# <a name="chroma-key-effect"></a>Croma-efeito de chave

Converte uma determinada cor mais ou menos uma tolerância para alfa. Por exemplo, croma-Key pode remover o plano de fundo de uma imagem para um efeito de sobreposição de tela verde.

O CLSID para esse efeito é CLSID \_ D2D1ChromaKey.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/chromakey-effect.png)

> [!Note]  
> Neste exemplo, a saída do efeito croma é a segunda imagem com o plano de fundo transparente do xadrez. A terceira imagem combina isso com uma imagem de plano de fundo para a sobreposição de tela verde final.

## <a name="sample-code"></a>Código de exemplo

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriedades do efeito

As propriedades para o efeito croma-Key são definidas pela enumeração [**d2d1 \_ Chromakey \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
