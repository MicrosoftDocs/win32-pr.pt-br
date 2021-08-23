---
description: A notificação SPFILENOTIFY ENDRENAME é enviada para a rotina de retorno de chamada quando a fila \_ conclui uma operação de renomeação. Essa notificação será enviada mesmo se o usuário cancelar ou se ocorrer um erro.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: SPFILENOTIFY_ENDRENAME mensagem (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f34ad30cc103e8a13277d3383bad8c2e46409eaabe6f957ace27aebc9759990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683116"
---
# <a name="spfilenotify_endrename-message"></a>Mensagem SPFILENOTIFY \_ ENDRENAME

A **notificação SPFILENOTIFY \_ ENDRENAME** é enviada para a rotina de retorno de chamada quando a fila conclui uma operação de renomeação. Essa notificação será enviada mesmo se o usuário cancelar ou se ocorrer um erro.


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma [**estrutura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) O **membro Win32Error** da estrutura **FILEPATHS** indica o resultado da operação de cópia.

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

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

[**Filepaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




