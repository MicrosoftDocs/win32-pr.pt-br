---
description: A \_ notificação SPFILENOTIFY ENDSUBQUEUE é enviada para a função de retorno de chamada quando a fila conclui todas as operações na subfila excluir, renomear ou copiar.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Mensagem de SPFILENOTIFY_ENDSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72645aafbe94e3f90d11f8ccf65ed8c6006301db811bccd80936cadbf0478dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964545"
---
# <a name="spfilenotify_endsubqueue-message"></a>\_Mensagem SPFILENOTIFY ENDSUBQUEUE

A notificação **SPFILENOTIFY \_ ENDSUBQUEUE** é enviada para a função de retorno de chamada quando a fila conclui todas as operações na subfila excluir, renomear ou copiar.


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Subfila que foi concluída. Esse parâmetro pode ser um dos valores a seguir FILEOP \_ excluir, FILEOP \_ Rename ou FILEOP \_ Copy.

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



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

 

 




