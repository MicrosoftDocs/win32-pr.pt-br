---
title: Elemento UserId (sessionStateChangeTriggerType)
description: Contém o usuário para a sessão de Terminal Server. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- Elemento UserId Agendador de Tarefas
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6f6ddaf196f83d727e4641df6e59375033eb60c076451d70866d9d227ca457d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355571"
---
# <a name="userid-sessionstatechangetriggertype-element"></a>Elemento UserId (sessionStateChangeTriggerType)

Contém o usuário para a sessão de Terminal Server. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

O elemento **userid** é definido pelo tipo complexo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                       | Derivado de                                                                                           | Descrição                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando uma sessão de Terminal Server muda de estado.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade UserID de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).

Para desenvolvimento de script, consulte [**SessionStateChangeTrigger. UserID**](sessionstatechangetrigger-userid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





