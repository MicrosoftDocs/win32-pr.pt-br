---
description: A \_ notificação SPFILENOTIFY DELETEERROR será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de exclusão de arquivo.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Mensagem de SPFILENOTIFY_DELETEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011760"
---
# <a name="spfilenotify_deleteerror-message"></a>\_Mensagem SPFILENOTIFY DELETEERROR

A notificação **SPFILENOTIFY \_ DELETEERROR** será enviada para a rotina de retorno de chamada se ocorrer um erro durante uma operação de exclusão de arquivo.


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A rotina de retorno de chamada deve retornar um dos valores a seguir.



| Código de retorno                                                                                  | Descrição                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_anular FILEOP**</dt> </dl> | O processamento da fila deve ser cancelado. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retorna zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna informações de erro ESTENDIdas, como erro \_ cancelado (se o usuário cancelou) ou erro \_ não \_ há \_ memória suficiente.<br/> |
| <dl> <dt>**repetição de FILEOP \_**</dt> </dl> | O usuário está tentando a operação de exclusão novamente.<br/>                                                                                                                                                                                                                 |
| <dl> <dt>**FILEOP \_ ignorar**</dt> </dl>  | O usuário está ignorando a operação de exclusão de arquivo.<br/>                                                                                                                                                                                                                    |



 

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

 

