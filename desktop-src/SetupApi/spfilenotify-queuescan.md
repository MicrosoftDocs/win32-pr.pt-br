---
description: A \_ notificação SPFILENOTIFY QUEUESCAN é enviada a uma rotina de retorno de chamada por SetupScanFileQueue para cada nó na subfila de cópia da fila de arquivos. Isso só ocorrerá se a função SetupScanFileQueue tiver sido chamada especificando o sinalizador SPQ da \_ verificação \_ usar o retorno de \_ chamada.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Mensagem de SPFILENOTIFY_QUEUESCAN (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755546"
---
# <a name="spfilenotify_queuescan-message"></a>\_Mensagem SPFILENOTIFY QUEUESCAN

A notificação **SPFILENOTIFY \_ QUEUESCAN** é enviada a uma rotina de retorno de chamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nó na subfila de cópia da fila de arquivos. Isso só ocorrerá se a função **SetupScanFileQueue** tiver sido chamada especificando o sinalizador SPQ da \_ verificação \_ usar o retorno de \_ chamada.


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Cadeia de caracteres terminada em nulo que especifica as informações de caminho de destino para o arquivo na fila no nó atual.

</dd> <dt>

*Param2* 
</dt> <dd>

Se o arquivo no nó atual da fila estiver em uso, *param2* usará a cópia atrasada do valor SPQ \_ \_ . Se o arquivo não estiver em uso, o valor será zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A rotina de retorno de chamada deve retornar um [código de erro do sistema](/windows/desktop/Debug/system-error-codes).

Se a rotina de retorno de chamada não retornar nenhum \_ erro, a verificação da fila continuará. Se a rotina retornar qualquer outro código de erro, a verificação de fila aborta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retorna **false**.

> [!Note]  
> Essa notificação não é tratada pela função [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

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

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

