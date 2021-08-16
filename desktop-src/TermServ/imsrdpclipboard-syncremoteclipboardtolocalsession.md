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
ms.openlocfilehash: e1e56a67504ab3182ed6ccaba97591e8259d6e46b6ebdd3bdc06fbaf63c170f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000816"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>Método IMsRdpClipboard:: SyncRemoteClipboardToLocalSession

Sincroniza a área de transferência remota para a sessão local.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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