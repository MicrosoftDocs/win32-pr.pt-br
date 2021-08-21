---
title: Tipo complexo triggerBaseType
description: Define o atributo, elementos filho base e informações de sequenciamento para todos os tipos complexos de gatilho.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- tipo complexo triggerBaseType Agendador de Tarefas
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21eed68ff260d199a46adabc0e560533658c6cc1398d00f9507b80b40fb69955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611007"
---
# <a name="triggerbasetype-complex-type"></a>Tipo complexo triggerBaseType

Define o atributo, elementos filho base e informações de sequenciamento para todos os tipos complexos de gatilho.

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                      | Type                                                                     | Descrição                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**habilitado**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | booleano                                                                  | Especifica que o gatilho está habilitado.<br/>                                                                      |
| [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | A data e a hora em que o gatilho é desativado.<br/>                                                          |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Especifica o intervalo quando o gatilho pode iniciar a tarefa.<br/>                                                 |
| [**Repetição**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido depois que o gatilho é acionado.<br/> |
| [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | A data e a hora em que o gatilho é ativado.<br/>                                                            |



## <a name="attributes"></a>Atributos



| Nome | Tipo | Descrição                           |
|------|------|---------------------------------------|
| id   | ID   | Identificador do gatilho.<br/> |



## <a name="remarks"></a>Comentários

Tipos complexos de gatilho incluem o seguinte.

-   [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)
-   [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)
-   [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)
-   [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)
-   [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)
-   [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)
-   [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas complexos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





