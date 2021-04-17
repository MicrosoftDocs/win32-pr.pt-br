---
title: Propriedade IMsRdpCameraRedirConfig FriendlyName
description: Obtém o nome amigável da câmera.
ms.tgt_platform: multiple
keywords:
- Propriedade FriendlyName Serviços de Área de Trabalho Remota
- Propriedade FriendlyName Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfig
- Interface IMsRdpCameraRedirConfig Serviços de Área de Trabalho Remota, Propriedade FriendlyName
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.FriendlyName
- IMsRdpCameraRedirConfig.get_FriendlyName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 2ffded502f64426392e89c2d18831770133e352d
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105798331"
---
# <a name="imsrdpcameraredirconfigfriendlyname-property"></a>Propriedade IMsRdpCameraRedirConfig:: FriendlyName

Obtém o nome amigável da câmera.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_FriendlyName(
    [out, retval] BSTR* pFriendlyName
);
```

## <a name="property-value"></a>Valor da propriedade

O nome amigável da câmera.

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