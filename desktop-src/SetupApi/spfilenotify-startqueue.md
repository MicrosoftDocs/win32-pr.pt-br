---
description: A \_ notificação SPFILENOTIFY STARTQUEUE é enviada para a rotina de retorno de chamada quando o processo de compromisso de fila é iniciado.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Mensagem de SPFILENOTIFY_STARTQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756137"
---
# <a name="spfilenotify_startqueue-message"></a>\_Mensagem SPFILENOTIFY STARTQUEUE

A notificação **SPFILENOTIFY \_ STARTQUEUE** é enviada para a rotina de retorno de chamada quando o processo de compromisso de fila é iniciado.


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Manipule a janela que é proprietária das caixas de diálogo geradas pela rotina de retorno de chamada.

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

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

 

