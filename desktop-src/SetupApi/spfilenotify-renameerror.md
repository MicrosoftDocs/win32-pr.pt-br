---
description: A \_ notificação SPFILENOTIFY RENAMEERROR será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de renomeação de arquivo.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Mensagem de SPFILENOTIFY_RENAMEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297098"
---
# <a name="spfilenotify_renameerror-message"></a>\_Mensagem SPFILENOTIFY RENAMEERROR

A notificação **SPFILENOTIFY \_ RENAMEERROR** será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de renomeação de arquivo.


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . O membro **Win32Error** da estrutura **filePaths** especifica o erro que ocorreu durante a operação de renomeação.

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A rotina de retorno de chamada deve retornar um dos seguintes.



| Código de retorno                                                                                  | Descrição                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**repetição de FILEOP \_**</dt> </dl> | O usuário optou por tentar a operação de renomeação novamente.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ ignorar**</dt> </dl>  | O usuário optou por ignorar a operação de renomeação de arquivo.<br/>                                                                                                                                                                                                      |
| <dl> <dt>**\_anular FILEOP**</dt> </dl> | Pare a confirmação da fila. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna **false**. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna informações de erro estendidas, como \_ o erro cancelado (se o usuário cancelou) ou o erro \_ não tem \_ memória suficiente \_ .<br/> |



 

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

