---
title: Interface IOrpcDebugNotify
description: Fornece a funcionalidade de depuração remota.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- IOrpcDebugNotify interface COM
- Interface COM de IOrpcDebugNotify, descrita
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
ms.openlocfilehash: e3dd051819b70ae93b7c615d803e12134221d55ffbd464c60d5b9c41d983eb9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678576"
---
# <a name="iorpcdebugnotify-interface"></a>Interface IOrpcDebugNotify

Fornece a funcionalidade de depuração remota.

## <a name="when-to-implement"></a>Quando implementar

Implemente essa interface para habilitar a depuração remota por RPC.

## <a name="when-to-use"></a>Quando usar

Essa interface deve ser usada para depuração remota em processo quando exceções de software não devem ser usadas para as notificações do depurador COM. Ele permite que os depurador em processo sejam notificados por chamadas diretas usando esses métodos.

## <a name="members"></a>Membros

A interface **IOrpcDebugNotify** herda da interface [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) **IOrpcDebugNotify** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IOrpcDebugNotify** tem esses métodos.



| Método                                                              | Descrição                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Envia dados do depurador de cliente para o depurador de servidor.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Recupera o tamanho do buffer RPC do depurador do lado do cliente.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informa o cliente de uma solicitação de depurador de saída para o servidor.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Envia dados do depurador de servidor para o depurador do cliente.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Recupera o tamanho do buffer RPC do depurador do lado do servidor.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informa o servidor de uma solicitação de depurador de entrada do cliente.<br/> |



 

## <a name="remarks"></a>Comentários

Uma biblioteca de importação que contém a interface **IOrpcDebugNotify** não está incluída no SDK (Software Development Kit) do Microsoft Windows. Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) do oleaut.dll e fornecer esses métodos por meio da interface **IOrpcDebugNotify.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ DBG \_ BUFFER**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

