---
description: A \_ notificação SPFILENOTIFY STARTSUBQUEUE é enviada para a função de retorno de chamada quando a fila começa a processar as operações na subfila excluir, renomear ou copiar.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Mensagem de SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755305"
---
# <a name="spfilenotify_startsubqueue-message"></a>\_Mensagem SPFILENOTIFY STARTSUBQUEUE

A notificação **SPFILENOTIFY \_ STARTSUBQUEUE** é enviada para a função de retorno de chamada quando a fila começa a processar as operações na subfila excluir, renomear ou copiar.


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Subfila que foi iniciada. Esse parâmetro pode ser qualquer um dos valores FILEOP \_ excluir, FILEOP \_ Rename ou FILEOP \_ Copy.

</dd> <dt>

*Param2* 
</dt> <dd>

Número de operações de cópia, renomeação ou exclusão de arquivo na subfila.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, a rotina de retorno de chamada deverá chamar [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), especificando o erro e, em seguida, retornará zero. A função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retornará **false** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro definido pela rotina de retorno de chamada.

Se nenhum erro ocorrer, a rotina de retorno de chamada deverá retornar um valor diferente de zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral](overview.md)
</dt> <dt>

[Notificações](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

