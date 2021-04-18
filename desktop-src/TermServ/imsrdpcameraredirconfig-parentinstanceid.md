---
title: Propriedade IMsRdpCameraRedirConfig ParentInstanceId
description: Obtém a ID da instância do dispositivo pai da câmera.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ParentInstanceId
- Propriedade ParentInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig, Propriedade ParentInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105793773"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a>IMsRdpCameraRedirConfig: Propriedade arentInstanceId de:P

Obtém a ID da instância do dispositivo pai da câmera.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a>Valor da propriedade

A ID da instância do dispositivo pai da câmera.

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