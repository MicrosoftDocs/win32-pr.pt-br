---
title: Estrutura de ORPC_INIT_ARGS
description: A \_ estrutura ORPC Init \_ args contém informações usadas para inicializar a depuração remota usando a interface IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- COM ORPC_INIT_ARGS estrutura COM
- COM ponteiro de estrutura de LPORPC_INIT_ARGS COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085351"
---
# <a name="orpc_init_args-structure"></a>\_Estrutura de \_ argumentos init ORPC

A estrutura **ORPC \_ init \_ args** contém informações usadas para inicializar a depuração remota usando a interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a>Membros

<dl> <dt>

**lpIntfOrpcDebug**
</dt> <dd>

Um ponteiro para a interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) para uso por depuradores em processo. Se o depurador não estiver em processo ou for um sistema Macintosh, esse campo deverá ser **nulo**.

</dd> <dt>

**pvPSN**
</dt> <dd>

Um ponteiro para o número de série do processo do Macintosh do processo do depurador. Se o depurado não for um sistema Macintosh, esse campo deverá ser **nulo**.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Reservado. Deve ser 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reservado. Deve ser 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ORPC \_ DBG \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_buffer de DBG ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





