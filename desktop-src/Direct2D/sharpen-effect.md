---
title: Efeito de nitidez
description: Ajusta a imagem.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74d95f7305dd6d44eb4dfbe2707f9e636e2ce704af2dc02fcf55477dbf2222d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873756"
---
# <a name="sharpen-effect"></a>Efeito de nitidez

Ajusta a imagem.

O CLSID para esse efeito é CLSID \_ D2D1Sharpen.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/sharpen-effect.png)

## <a name="sample-code"></a>Código de exemplo


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propriedades do efeito

As propriedades para o efeito de nitidez são definidas pela enumeração de [**\_ \_ prop d2d1 nitidez**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



