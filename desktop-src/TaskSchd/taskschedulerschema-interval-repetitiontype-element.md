---
title: Elemento Interval (repetiçãotype)
description: Especifica a quantidade de tempo entre cada reinicialização da tarefa.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Elemento Interval Agendador de Tarefas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734191"
---
# <a name="interval-repetitiontype-element"></a>Elemento Interval (repetiçãotype)

Especifica a quantidade de tempo entre cada reinicialização da tarefa. O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, "PT5M" é de 5 minutos, "PT1H" é de 1 hora e "PT20M" é de 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo tipo complexo de [**repetição**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                      | Derivado de                                                             | Descrição                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetição**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o intervalo do padrão de repetição é especificado usando a propriedade [**RepetitionPattern. Interval**](repetitionpattern-interval.md) .

Para desenvolvimento em C++, o intervalo do padrão de repetição é especificado usando a propriedade [**IRepetitionPattern:: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que usa um intervalo de repetição, consulte [exemplo de gatilho diário (XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





