---
title: Propriedade IMsRdpCameraRedirConfig DeviceExists
description: Especifica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).
ms.tgt_platform: multiple
keywords:
- Propriedade DeviceExists Serviços de Área de Trabalho Remota
- A propriedade DeviceExists Serviços de Área de Trabalho Remota , interface IMsRdpCameraRedirConfig
- Interface IMsRdpCameraRedirConfig Serviços de Área de Trabalho Remota , propriedade DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 617c91491d88736ca60218d71f9dd5aa02ad0f9faeefdda6b872ba9262cec587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990656"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>Propriedade IMsRdpCameraRedirConfig::D eviceExists

Especifica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>Valor da propriedade

Um valor que indica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig é definido como 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>