---
title: Propriedade IMsRdpCameraRedirConfig InstanceId
description: Obtém a ID da instância da câmera.
ms.tgt_platform: multiple
keywords:
- Propriedade InstanceId Serviços de Área de Trabalho Remota
- A propriedade InstanceId Serviços de Área de Trabalho Remota , interface IMsRdpCameraRedirConfig
- Interface IMsRdpCameraRedirConfig Serviços de Área de Trabalho Remota , propriedade InstanceId
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
ms.openlocfilehash: 621c865f9727cf484430d00609dcfcfac2431a514cf2bade714fdd4d81b0408c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400996"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>Propriedade IMsRdpCameraRedirConfig::InstanceId

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