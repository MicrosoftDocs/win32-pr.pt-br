---
description: A notificação SPFILENOTIFY \_ STARTQUEUE é enviada para a rotina de retorno de chamada quando o processo de compromisso da fila é iniciado.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: SPFILENOTIFY_STARTQUEUE mensagem (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40d4fedde850d975edd697423339c686fe697911b9bef2fdc252baffda0158f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073206"
---
# <a name="spfilenotify_startqueue-message"></a>Mensagem SPFILENOTIFY \_ STARTQUEUE

A **notificação SPFILENOTIFY \_ STARTQUEUE** é enviada para a rotina de retorno de chamada quando o processo de compromisso da fila é iniciado.


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Lidar com a janela que deve ter as caixas de diálogo que a rotina de retorno de chamada gera.

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, a rotina de retorno de chamada deverá chamar [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), especificando o erro e retornar zero. A [**função SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retornará **FALSE** e uma chamada subsequente para [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o código de erro definido pela rotina de retorno de chamada.

Se nenhum erro ocorrer, a rotina de retorno de chamada deverá retornar um valor não zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



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

 

