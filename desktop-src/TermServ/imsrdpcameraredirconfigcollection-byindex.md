---
title: Propriedade IMsRdpCameraRedirConfigCollection ByIndex
description: Retorna um objeto IMsRdpCameraRedirConfig por seu índice na coleção.
ms.tgt_platform: multiple
keywords:
- Propriedade ByIndex Serviços de Área de Trabalho Remota
- A propriedade ByIndex Serviços de Área de Trabalho Remota , interface IMsRdpCameraRedirConfigCollection
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota propriedade , ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 375c0b110975c6ca791bbbe1f61a5b597b00316242484cd68ef018b7ef4ea88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138959"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a>Propriedade IMsRdpCameraRedirConfigCollection::ByIndex

Retorna um [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por seu índice na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>Valor da propriedade

O [objeto IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde ao índice especificado.

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