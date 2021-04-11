---
title: Método IMsRdpClientNonScriptable7 DisableDpiCursorScalingForProcess
description: Desabilita o dimensionamento local do cursor do mouse recebido do servidor, garantindo que a forma do cursor seja renderizada corretamente sem modificação.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DisableDpiCursorScalingForProcess
- Método DisableDpiCursorScalingForProcess Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable7, método DisableDpiCursorScalingForProcess
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.DisableDpiCursorScalingForProcess
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a0de989fb0b1c3c644c73f214d368f2cab2ba5d5
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104295930"
---
# <a name="imsrdpclientnonscriptable7disabledpicursorscalingforprocess-method"></a>IMsRdpClientNonScriptable7: método isableDpiCursorScalingForProcess de:D

Desabilita o dimensionamento local do cursor do mouse recebido do servidor, garantindo que a forma do cursor seja renderizada corretamente sem modificação.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT DisableDpiCursorScalingForProcess();
```

## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retornar **S \_ OK** se for bem-sucedido.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 é definido como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>
