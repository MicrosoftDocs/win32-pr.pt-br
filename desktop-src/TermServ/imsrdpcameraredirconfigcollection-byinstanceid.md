---
title: Propriedade IMsRdpCameraRedirConfigCollection ByInstanceId
description: Retorna um objeto IMsRdpCameraRedirConfig da coleção que corresponde à ID de instância especificada.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ByInstanceId
- Propriedade ByInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456326"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>Propriedade IMsRdpCameraRedirConfigCollection:: ByInstanceId

Retorna um objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde à ID de instância especificada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valor da propriedade

O objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde à ID de instância especificada.

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