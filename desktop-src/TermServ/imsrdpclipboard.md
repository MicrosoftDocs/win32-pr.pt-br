---
title: Interface do IMsRdpClipboard
description: Representa o controlador da área de transferência usado para sincronizar as áreas de transferência local e remota se a sincronização da área de transferência manual estiver habilitada.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClipboard
- Serviços de Área de Trabalho Remota da interface IMsRdpClipboard, descrita
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104087199"
---
# <a name="imsrdpclipboard-interface"></a>Interface do IMsRdpClipboard

Representa o controlador da área de transferência usado para sincronizar as áreas de transferência locais e remotas se a sincronização da área de transferência manual estiver habilitada (ou seja, o valor da propriedade [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) for definido como **true**).

## <a name="members"></a>Membros

A interface **IMsRdpClipboard** herda de **IUnknown**. **IMsRdpClipboard** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMsRdpClipboard** tem esses métodos.


| Método        | Descrição      |
|:---------------|:----------------|
| [**CanSyncLocalClipboardToRemoteSession**](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  Indica se a área de transferência local pode ser sincronizada com a sessão remota.                   |
| [**CanSyncRemoteClipboardToLocalSession**](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  Indica se a área de transferência remota pode ser sincronizada com a sessão local.                   |
| [**SyncLocalClipboardToRemoteSession**](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  Sincroniza a área de transferência local com a sessão remota.                   |
| [**SyncRemoteClipboardToLocalSession**](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   Sincroniza a área de transferência remota para a sessão local.                      |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard é definido como 2E769EE8-00C7-43DC-AFD9-235D75B72A40            |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable7:: Clipboard**](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
