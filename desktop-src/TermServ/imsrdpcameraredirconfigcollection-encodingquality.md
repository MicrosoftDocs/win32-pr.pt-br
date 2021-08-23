---
title: Propriedade IMsRdpCameraRedirConfigCollection EncodingQuality
description: Especifica a qualidade de codificação (taxa de bits).
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade EncodingQuality
- Propriedade EncodingQuality Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 94537773a54ddeb9bceb2483b7f8db6766f7b3f32f9a8a7fe2d9a24659209870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574426"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a>Propriedade IMsRdpCameraRedirConfigCollection:: EncodingQuality

Especifica a qualidade de codificação (taxa de bits).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a>Valor da propriedade

Um dos seguintes valores de enumeração **CameraRedirEncodingQuality** que especifica a qualidade de codificação (taxa de bits).

| Nome do membro de enumeração | Valor |
|-----------------|--------|
| encodingQualityLow | 0x0000 |
| encodingQualityMedium | 0x0001 |
| encodingQualityHigh | 0x0002 |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>