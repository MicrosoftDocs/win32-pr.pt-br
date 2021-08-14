---
title: Elemento URI (registrationInfoType)
description: Especifica o URI da tarefa.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- Elemento URI Agendador de Tarefas
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b9a2d9b8faf327f7b64be2cdd4273f2252405767004dc6e0d58b0c95b5f1910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355599"
---
# <a name="uri-registrationinfotype-element"></a>Elemento URI (registrationInfoType)

Especifica o URI da tarefa. Esse elemento é usado para especificar onde a tarefa registrada é colocada na hierarquia de pastas de tarefas.

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

O **elemento URI** é definido pelo [**tipo complexo registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                           | Derivado de                                                                         | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o URI da tarefa é especificado usando a [**propriedade RegistrationInfo.URI.**](registrationinfo-uri.md)

Para desenvolvimento em C++, o URI da tarefa é especificado usando a [**propriedade IRegistrationInfo::URI.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri)

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

 

 





