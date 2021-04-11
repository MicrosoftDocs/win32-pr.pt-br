---
title: Propriedade IMsRdpCameraRedirConfig InstanceId
description: Obtém a ID da instância da câmera.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade InstanceId
- Serviços de Área de Trabalho Remota da propriedade InstanceId, interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig, Propriedade InstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 42654e84f64b25a051a78963339ca95d4ebf760f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104163674"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>Propriedade IMsRdpCameraRedirConfig:: InstanceId

Obtém a ID da instância da câmera.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>Valor da propriedade

A ID da instância da câmera.

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