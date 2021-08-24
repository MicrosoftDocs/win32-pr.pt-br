---
title: Efeito de exposição
description: Aumente ou diminua a exposição da imagem.
ms.assetid: d384f539-5c19-53c7-e52b-bf833e221449
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdcd99e125251c3144d96ffd6054897e6801eb3299c1d1ae90e37494620faea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652916"
---
# <a name="exposure-effect"></a>Efeito de exposição

Aumente ou diminua a exposição da imagem.

O CLSID para esse efeito é CLSID \_ D2D1Exposure.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requirements](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/exposure-effect.png)

## <a name="sample-code"></a>Código de exemplo


```C++
ComPtr<ID2D1Effect> exposureEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Exposure, &exposureEffect);
 
exposureEffect->SetInput(0, bitmap);
exposureEffect->SetValue(D2D1_EXPOSURE_PROP_EXPOSURE_VALUE, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(exposureEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propriedades do efeito

As propriedades do efeito de exposição são definidas pela enumeração [**de \_ \_ prop d2d1 Exposure**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_exposure_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 10 \[ aplicativos da área de trabalho \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




