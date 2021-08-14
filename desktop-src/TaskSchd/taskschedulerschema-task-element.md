---
title: Elemento Task
description: Define a tarefa que é executada pelo serviço de Agendador de Tarefas.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Elemento de tarefa Agendador de Tarefas
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3be36d0799e98b99a6d5ebe6430220b29fe2192935f67e9df5e189bc0f970a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356229"
---
# <a name="task-element"></a>Elemento Task

Define a tarefa que é executada pelo serviço de Agendador de Tarefas.

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type                                                                                 | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md)                   | [**ActionType**](taskschedulerschema-actionstype-complextype.md)                   | Especifica as ações executadas pela tarefa.<br/>                                                                             |
| [**Dados**](taskschedulerschema-data-tasktype-element.md)                         | [**Tipo de dados**](taskschedulerschema-datatype-complextype.md)                         | Especifica os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Especifica os contextos de segurança que podem ser usados para executar a tarefa.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingstype**](taskschedulerschema-settingstype-complextype.md)                 | Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/>                                                 |
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md)                 | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md)                 | Especifica os gatilhos que iniciam a tarefa.<br/>                                                                              |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).

Para o desenvolvimento de scripts, consulte [**TaskDefinition**](taskdefinition.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





