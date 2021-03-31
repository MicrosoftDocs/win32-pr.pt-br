---
title: Efeito de sépia
description: Converte uma imagem em tons de sépia.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6ead1d439e86cbd35be14d1f0ae32923de408d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918331"
---
# <a name="sepia-effect"></a>Efeito de sépia

Converte uma imagem em tons de sépia.

O CLSID para esse efeito é CLSID \_ D2D1Sepia.

-   [Imagem de exemplo](#example-image)
-   [Código de exemplo](#sample-code)
-   [Propriedades do efeito](#effect-properties)
-   [Requisitos](#requirements)
-   [Tópicos relacionados](#related-topics)

## <a name="example-image"></a>Imagem de exemplo

![exemplo de saída de efeito](images/sepia-effect.png)

## <a name="sample-code"></a>Código de exemplo


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propriedades do efeito

As propriedades do efeito de sépia são definidas pela enumeração [**de \_ \_ prop d2d1 sépia**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------|
| Cliente mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| Servidor mínimo com suporte | Aplicativos do Windows 10 \[ Desktop aplicativos da \| Windows Store\] |
| parâmetro                   | d2d1effects \_ 2. h                                  |
| Biblioteca                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Tópicos relacionados

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




