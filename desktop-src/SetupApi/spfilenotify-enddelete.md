---
description: A \_ notificação EndDelete do SPFILENOTIFY é retornada para a rotina de retorno de chamada quando uma fila conclui uma operação de exclusão. Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: Mensagem de SPFILENOTIFY_ENDDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 638bf333c034ececd5a22536805b2adab970df9f15e70d9f4a9f161229937aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964599"
---
# <a name="spfilenotify_enddelete-message"></a>SPFILENOTIFY mensagem de fim de \_ exclusão

A **notificação \_ EndDelete do SPFILENOTIFY** é retornada para a rotina de retorno de chamada quando uma fila conclui uma operação de exclusão. Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . O membro **Win32Error** da estrutura **filePaths** indica o resultado de uma operação de cópia.

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O código de retorno é ignorado.

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




