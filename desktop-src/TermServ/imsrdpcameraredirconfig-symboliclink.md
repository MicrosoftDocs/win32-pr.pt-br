---
title: Propriedade IMsRdpCameraRedirConfig SymbolicLink
description: Obtém o link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SymbolicLink
- Propriedade SymbolicLink Serviços de Área de Trabalho Remota, interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig, Propriedade SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103825451"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a>Propriedade IMsRdpCameraRedirConfig:: SymbolicLink

Obtém o link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a>Valor da propriedade

O link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.

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