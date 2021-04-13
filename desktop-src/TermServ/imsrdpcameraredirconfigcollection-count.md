---
title: Propriedade IMsRdpCameraRedirConfigCollection Count
description: Retorna o número de objetos IMsRdpCameraRedirConfig na coleção.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de contagem
- Serviços de Área de Trabalho Remota da propriedade Count, interface IMsRdpCameraRedirConfigCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfigCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.Count
- IMsRdpCameraRedirConfigCollection.get_Count
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31927428b709136de87f436ad92cc6a78fa9795a
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104456331"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a>Propriedade IMsRdpCameraRedirConfigCollection:: Count

Retorna o número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a>Valor da propriedade

O número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) na coleção.

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