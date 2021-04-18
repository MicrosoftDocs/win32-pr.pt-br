---
description: A \_ notificação EndCopy do SPFILENOTIFY é passada para a função de retorno de chamada quando a fila conclui uma operação de cópia. Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Mensagem de SPFILENOTIFY_ENDCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756363"
---
# <a name="spfilenotify_endcopy-message"></a>\_Mensagem de ENDcopy do SPFILENOTIFY

A **notificação \_ EndCopy do SPFILENOTIFY** é passada para a função de retorno de chamada quando a fila conclui uma operação de cópia. Essa notificação é enviada mesmo que o usuário cancele ou se ocorrer um erro.


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . O membro **Win32Error** da estrutura **filePaths** indica o resultado da operação de cópia.

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O código de retorno é ignorado.

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

 

 




