---
title: Método IMsRdpClipboard CanSyncRemoteClipboardToLocalSession
description: Indica se a Área de Transferência remota pode ser sincronizada com a sessão local.
ms.tgt_platform: multiple
keywords:
- Método CanSyncRemoteClipboardToLocalSession Serviços de Área de Trabalho Remota
- Método CanSyncRemoteClipboardToLocalSession Serviços de Área de Trabalho Remota, interface IMsRdpClipboard
- Interface IMsRdpClipboard Serviços de Área de Trabalho Remota, método CanSyncRemoteClipboardToLocalSession
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
ms.openlocfilehash: 40a9fc5d6dcdc2e96d9ce916bce0567cccc90adf10fcacc5d797f61ed292c116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000836"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>Método IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession

Indica se a Área de Transferência remota pode ser sincronizada com a sessão local.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parâmetros

**TRUE** se a Área de Transferência remota puder ser sincronizada com a sessão local; caso contrário, **FALSE.**

## <a name="return-value"></a>Valor retornado

Retornar **S \_ OK se** for bem-sucedido.

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