---
description: Chamado pelo compilador para implementar extensões de manipulação de exceção estruturada.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: Função __C_specific_handler (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: c61d14b591f54ea44ba0f33a36a2ca5acecb129ba46b5f45fcc18185f5d9448c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017824"
---
# <a name="__c_specific_handler-function"></a>\_\_Função de manipulador de C \_ específico \_

Chamado pelo compilador para implementar extensões de manipulação de exceção estruturada.

O endereço relativo do manipulador específico de idioma está presente nas informações de desenrolamento, \_ sempre que sinalizadores UNW \_ Flag \_ EHANDLER ou UNW \_ Flag \_ UHANDLER estão definidos. O manipulador de idioma específico é chamado como parte da pesquisa de um manipulador de exceção ou como parte de um desenrolamento. Para obter mais informações, consulte [manipulador de linguagem específica](/cpp/build/language-specific-handler).

## <a name="syntax"></a>Sintaxe


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ExceptionRecord* \[ no\]
</dt> <dd>

Fornece um ponteiro para um registro de exceção que tem a definição padrão de Win64.

</dd> <dt>

*EstablisherFrame* \[ no\]
</dt> <dd>

O endereço da base da alocação de pilha fixa para esta função.

</dd> <dt>

*ContextRecord* \[ entrada, saída\]
</dt> <dd>

Aponta para o contexto de exceção no momento em que a exceção foi gerada (no caso do manipulador de exceção) ou no contexto "desenrolar" atual (no caso do manipulador de terminação).

</dd> <dt>

*DispatcherContext* \[ entrada, saída\]
</dt> <dd>

Aponta para o contexto do Dispatcher para esta função.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WDM. h</dt> </dl>        |
| Biblioteca<br/> | <dl> <dt>NtosKrnl. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

