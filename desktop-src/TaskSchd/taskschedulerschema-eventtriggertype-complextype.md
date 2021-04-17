---
title: Tipo complexo eventTriggertype
description: Define os elementos filho e as informações de sequenciamento para o elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- tipo complexo de eventTriggertype Agendador de Tarefas
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813038"
---
# <a name="eventtriggertype-complex-type"></a>Tipo complexo eventTriggertype

Define os elementos filho e as informações de sequenciamento para o elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retardo**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                | Especifica a quantidade de tempo entre o momento em que o evento ocorre e quando a tarefa é iniciada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md) | Especifica a consulta XPath que identifica o evento que dispara o gatilho.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Especifica uma sequência de elementos que cada um contém um nome e um valor de consulta XPath. As consultas são aplicadas a um evento retornado da assinatura de evento especificada no elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . O nome para o valor de consulta XPath pode ser usado como uma variável no elemento [**Body**](taskschedulerschema-body-showmessagetype-element.md) na seção de ação de " [**exmessage**](taskschedulerschema-showmessage-actiongroup-element.md) " de uma tarefa. <br/> |



## <a name="remarks"></a>Comentários

Além do elemento filho definido aqui, o elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) também usa elementos filho definidos pelo tipo complexo [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





