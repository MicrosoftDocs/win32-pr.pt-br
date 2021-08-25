---
title: Efeito de cartaz
description: O efeito de cartaz reduz o número de cores exclusivas em uma imagem.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21372ee43935441168609cc81ef053ac96fd3fdbbd7cd3c16578f13d1a47fda1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636096"
---
# <a name="posterize-effect"></a>Efeito de cartaz

O efeito de cartaz reduz o número de cores exclusivas em uma imagem.

O CLSID para esse efeito é CLSID \_ D2D1Posterize.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades de efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/posterize-effect.png)

## <a name="sample-code"></a>Código de exemplo


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propriedades de efeito

As propriedades para o efeito de posterização são definidas pela enumeração [**D2D1 \_ POSTERIZE \_ PROP.**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Servidor mínimo com suporte | \[Windows 10 aplicativos da \| área Windows Aplicativos da Store\] |
| Cabeçalho                   | d2d1effects \_ 2.h                                  |
| Biblioteca                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


