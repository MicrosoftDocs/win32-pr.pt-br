---
title: Método IOrpcDebugNotify ClientGetBufferSize
description: Recupera o tamanho do buffer RPC do depurador do lado do cliente.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- Método COM ClientGetBufferSize
- Interface COM do método ClientGetBufferSize, IOrpcDebugNotify
- IOrpcDebugNotify interface COM , método ClientGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 038273dfd93264d483bacb314b78e33f3e8f16cef4f120be27bd48901ef5b060
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859466"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a>Método IOrpcDebugNotify::ClientGetBufferSize

Recupera o tamanho do buffer RPC do depurador do lado do cliente.

> [!Note]  
> Uma biblioteca de importação que **contém a função ClientGetBufferSize** não está incluída no SDK (Software Development Kit) do Microsoft Windows. Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) do oleaut.dll e fornecer essa função por meio da interface [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

## <a name="syntax"></a>Sintaxe


```C++
void ClientGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Um ponteiro para uma estrutura [**\_ DBG \_ ALL ORPC**](orpc-dbg-all.md) que contém informações específicas de notificação que o sistema RPC COM passa para o depurador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

