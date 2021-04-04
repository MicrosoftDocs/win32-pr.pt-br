---
title: Elemento Date (registrationInfoType)
description: Especifica a data e a hora em que a tarefa é registrada.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Agendador de Tarefas de elemento de data
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085874"
---
# <a name="date-registrationinfotype-element"></a>Elemento Date (registrationInfoType)

Especifica a data e a hora em que a tarefa é registrada.

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

O elemento **Date** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                           | Derivado de                                                                         | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, a data de registro de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Date**](registrationinfo-date.md) .

Para o desenvolvimento em C++, a data de registro de uma tarefa é especificada usando a propriedade [**IRegistrationInfo::D ATA**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





