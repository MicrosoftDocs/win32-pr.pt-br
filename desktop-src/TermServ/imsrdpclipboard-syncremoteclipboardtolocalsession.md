---
title: Método IMsRdpClipboard SyncRemoteClipboardToLocalSession
description: Sincroniza a área de transferência remota para a sessão local.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SyncRemoteClipboardToLocalSession
- Método SyncRemoteClipboardToLocalSession Serviços de Área de Trabalho Remota, interface IMsRdpClipboard
- Serviços de Área de Trabalho Remota de interface IMsRdpClipboard, método SyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d397d7c1ca4407a5125877721be9aa022f8132a7
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104500118"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>Método IMsRdpClipboard:: SyncRemoteClipboardToLocalSession

Sincroniza a área de transferência remota para a sessão local.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT SyncRemoteClipboardToLocalSession();
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
| IID                      | IID \_ IMsRdpClipboard é definido como 2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>