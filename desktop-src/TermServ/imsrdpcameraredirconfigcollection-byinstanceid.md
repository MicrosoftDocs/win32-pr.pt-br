---
title: Propriedade IMsRdpCameraRedirConfigCollection ByInstanceId
description: Retorna um objeto IMsRdpCameraRedirConfig da coleção que corresponde à ID de instância especificada.
ms.tgt_platform: multiple
keywords:
- Propriedade ByInstanceId Serviços de Área de Trabalho Remota
- Propriedade ByInstanceId Serviços de Área de Trabalho Remota , interface IMsRdpCameraRedirConfigCollection
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota , propriedade ByInstanceId
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
ms.openlocfilehash: e621efa61c6e033a9066da30fc6a2a97c76ebec94e9bfe848743f8b031b08d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080066"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>Propriedade IMsRdpCameraRedirConfigCollection::ByInstanceId

Retorna um [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) da coleção que corresponde à ID de instância especificada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valor da propriedade

O [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde à ID de instância especificada.

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