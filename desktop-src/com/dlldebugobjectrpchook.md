---
title: Função DllDebugObjectRPCHook
description: Exportado por DLLs COM para habilitar a depuração remota.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- COM função DllDebugObjectRPCHook
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812261"
---
# <a name="dlldebugobjectrpchook-function"></a>Função DllDebugObjectRPCHook

Exportado por DLLs COM para habilitar a depuração remota.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fTrace* 
</dt> <dd>

Se for **true**, a depuração remota será habilitada. Se for **false**, a depuração remota não estará habilitada.

</dd> <dt>

*lpOrpcInitArgs* 
</dt> <dd>

Um ponteiro para uma estrutura [**ORPC \_ init \_ args**](orpc-init-args.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**True** se for bem-sucedido; caso contrário, **false**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ole32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORPC \_ DBG \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_buffer de DBG ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_argumentos de inicialização ORPC \_**](orpc-init-args.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





