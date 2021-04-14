---
title: Método IOrpcDebugNotify ClientNotify
description: Informa ao cliente uma solicitação de depuração de saída para o servidor.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Método COM de ClientNotify
- Método ClientNotify COM, interface IOrpcDebugNotify
- IOrpcDebugNotify interface COM, método ClientNotify
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
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455971"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a>Método IOrpcDebugNotify:: ClientNotify

Informa ao cliente uma solicitação de depuração de saída para o servidor.

> [!Note]  
> Uma biblioteca de importação que contém a função **ClientNotify** não está incluída no SDK (Software Development Kit) do Microsoft Windows. Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll e fornecer essa função por meio da interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

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

Um ponteiro para uma estrutura [**ORPC \_ DBG \_ All**](orpc-dbg-all.md) que contém informações específicas de notificação que o sistema RPC com passa para o depurador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_argumentos de inicialização ORPC \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

