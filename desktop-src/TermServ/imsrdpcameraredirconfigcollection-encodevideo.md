---
title: Propriedade IMsRdpCameraRedirConfigCollection EncodeVideo
description: Especifica se o fluxo de vídeo é codificado em H.264 ou não.
ms.tgt_platform: multiple
keywords:
- Propriedade EncodeVideo Serviços de Área de Trabalho Remota
- A propriedade EncodeVideo Serviços de Área de Trabalho Remota , interface IMsRdpCameraRedirConfigCollection
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota , propriedade EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 9eda6fd63953425001906595b0cd8b594496e0f83974ba9d359ed43a639a4164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475956"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a>Propriedade IMsRdpCameraRedirConfigCollection::EncodeVideo

Especifica se o fluxo de vídeo é codificado em H.264 ou não.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a>Valor da propriedade

Um valor que indica se o fluxo de vídeo é codificado em H.264 ou não.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>