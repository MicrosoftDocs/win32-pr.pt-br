---
title: Método IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Indica se a área de transferência remota pode ser sincronizada com a sessão local.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CanSyncRemoteClipboardToLocalSession
- Método CanSyncRemoteClipboardToLocalSession Serviços de Área de Trabalho Remota, interface IMsRdpClipboard
- Serviços de Área de Trabalho Remota de interface IMsRdpClipboard, método CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "105793774"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>Método IMsRdpClipboard:: CanSyncRemoteClipboardToLocalSession

Indica se a área de transferência remota pode ser sincronizada com a sessão local.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parâmetros

**True** se a área de transferência remota puder ser sincronizada com a sessão local; caso contrário, **false**.

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