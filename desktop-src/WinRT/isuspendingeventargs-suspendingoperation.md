---
description: Obtém a operação de suspensão do aplicativo.
ms.assetid: 33FCAED5-7568-4483-A643-A536B53F7003
title: 'Propriedade ISuspendingEventArgs:: SuspendingOperation (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs.SuspendingOperation
- ISuspendingEventArgs.get_SuspendingOperation
- ISuspendingEventArgs.put_SuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e12ccbb372d7c712585766bba8d7921fae57a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827136"
---
# <a name="isuspendingeventargssuspendingoperation-property"></a>Propriedade ISuspendingEventArgs:: SuspendingOperation

Obtém a operação de suspensão do aplicativo.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SuspendingOperation();

HRESULT get_SuspendingOperation(
  [out, retval] ISuspendingOperation **value
);
```



## <a name="property-value"></a>Valor da propriedade

A operação de suspensão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| parâmetro<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 




