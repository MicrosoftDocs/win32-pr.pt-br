---
title: Método IOrpcDebugNotify ClientNotify
description: Informa o cliente de uma solicitação de depurador de saída para o servidor.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Método CLIENTNotify COM
- Método CLIENTNotify COM, interface IOrpcDebugNotify
- IOrpcDebugNotify interface COM , método ClientNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc80262b75bb170f14fa191f5a60e658cd371765714860f09a7bbcadcbcc369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854276"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a>Método IOrpcDebugNotify::ClientNotify

Informa o cliente de uma solicitação de depurador de saída para o servidor.

> [!Note]  
> Uma biblioteca de importação que contém **a função ClientNotify** não está incluída no SDK (Software Development Kit) do Microsoft Windows. Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) do oleaut.dll e fornecer essa função por meio da interface [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

## <a name="syntax"></a>Sintaxe


```C++
void ClientNotify(
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

 

