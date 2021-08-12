---
title: Método IMsRdpClipboard CanSyncLocalClipboardToRemoteSession
description: Indica se a área de transferência local pode ser sincronizada com a sessão remota.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CanSyncLocalClipboardToRemoteSession
- Método CanSyncLocalClipboardToRemoteSession Serviços de Área de Trabalho Remota, interface IMsRdpClipboard
- Serviços de Área de Trabalho Remota de interface IMsRdpClipboard, método CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: dabc12064ff43a2bb64a562d1aa3050681f46c31dd2698154beb1dafe3cfd85e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606911"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>Método IMsRdpClipboard:: CanSyncLocalClipboardToRemoteSession

Indica se a área de transferência local pode ser sincronizada com a sessão remota.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>Parâmetros

**True** se a área de transferência local puder ser sincronizada com a sessão remota; caso contrário, **false**.

## <a name="return-value"></a>Valor retornado

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