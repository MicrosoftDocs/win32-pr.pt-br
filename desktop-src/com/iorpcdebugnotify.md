---
title: Interface IOrpcDebugNotify
description: Fornece a funcionalidade de depuração remota.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- COM interface IOrpcDebugNotify
- COM interface IOrpcDebugNotify, descrita
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499800"
---
# <a name="iorpcdebugnotify-interface"></a>Interface IOrpcDebugNotify

Fornece a funcionalidade de depuração remota.

## <a name="when-to-implement"></a>Quando implementar

Implemente essa interface para habilitar a depuração remota via RPC.

## <a name="when-to-use"></a>Quando usar

Essa interface deve ser usada para depuração remota em processo quando exceções de software não devem ser usadas para as notificações do depurador COM. Ele permite que os depuradores em processo sejam notificados por chamadas diretas usando esses métodos.

## <a name="members"></a>Membros

A interface **IOrpcDebugNotify** herda da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . **IOrpcDebugNotify** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IOrpcDebugNotify** tem esses métodos.



| Método                                                              | Descrição                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Envia dados do depurador do cliente para o depurador do servidor.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Recupera o tamanho do buffer RPC do depurador do lado do cliente.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informa ao cliente uma solicitação de depuração de saída para o servidor.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Envia dados do depurador do servidor para o depurador do cliente.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Recupera o tamanho do buffer RPC do depurador do lado do servidor.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informa ao servidor de uma solicitação de entrada do depurador do cliente.<br/> |



 

## <a name="remarks"></a>Comentários

Uma biblioteca de importação que contém a interface **IOrpcDebugNotify** não está incluída no SDK (Software Development Kit) do Microsoft Windows. Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll e fornecer esses métodos por meio da interface **IOrpcDebugNotify** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ DBG \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_buffer de DBG ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_argumentos de inicialização ORPC \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

