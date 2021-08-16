---
title: Elemento UserId (logonTriggerType)
description: Identificador do usuário. A tarefa é iniciada quando esse usuário faz logona no computador.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
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
ms.openlocfilehash: 33a1e0f82a3005bfec8e689d088a8d8e28ebbf0a949e4288338d27e68c3a0314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355562"
---
# <a name="userid-logontriggertype-element"></a>Elemento UserId (logonTriggerType)

Identificador do usuário. A tarefa é iniciada quando esse usuário faz logona no computador.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

O **elemento UserId** é definido pelo [**tipo complexo logonTriggerType.**](taskschedulerschema-logontriggertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Especifica um gatilho que inicia uma tarefa quando um usuário faz login.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento de scripts, o identificador de usuário para o gatilho de logon é especificado usando a [**propriedade LogonTrigger.UserId.**](logontrigger-userid.md)

Para desenvolvimento em C++, o identificador de usuário para o gatilho de logon é especificado usando a [**propriedade ILogonTrigger::UserId.**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid)

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que especifica um gatilho de [logon, consulte Xml (Exemplo de Gatilho de Logon).](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





