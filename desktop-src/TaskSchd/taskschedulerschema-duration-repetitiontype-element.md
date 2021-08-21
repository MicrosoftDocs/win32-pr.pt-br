---
title: Elemento Duration (repetiçãotype)
description: Especifica por quanto tempo o padrão é repetido.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Elemento Duration Agendador de Tarefas
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d2194f573f4592c6388d1640b2525ecbf69e8e8d6121c7c345caa20698a3a482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857214"
---
# <a name="duration-repetitiontype-element"></a>Elemento Duration (repetiçãotype)

Especifica por quanto tempo o padrão é repetido. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> . Se nenhum valor for especificado para a duração, o padrão será repetido indefinidamente. O valor mínimo é um minuto.

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
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

Para aplicativos de script, a duração do padrão é especificada usando a propriedade [**RepetitionPattern. Duration**](repetitionpattern-duration.md) .

Para aplicativos C++, a duração do padrão é especificada usando a propriedade [**IRepetitionPattern::D uração**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .

## <a name="examples"></a>Exemplos

O XML a seguir define um padrão de repetição para um gatilho.


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





