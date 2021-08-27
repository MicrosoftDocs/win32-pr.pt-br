---
title: Elemento Interval (repetitionType)
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
ms.openlocfilehash: ec6f2724f4374ed94fff47e6577a2887ca953cae0af66de9c64971cd80aa2050
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099996"
---
# <a name="interval-repetitiontype-element"></a>Elemento Interval (repetitionType)

Especifica a quantidade de tempo entre cada reinicialização da tarefa. O formato dessa cadeia de caracteres é `P<days>DT<hours>H<minutes>M<seconds>S` (por exemplo, "PT5M" é 5 minutos, "PT1H" é 1 hora e "PT20M" é 20 minutos). O tempo máximo permitido é de 31 dias e o tempo mínimo permitido é de 1 minuto.

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

O elemento é definido pelo tipo [**complexo repetitionType.**](taskschedulerschema-repetitiontype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                      | Derivado de                                                             | Descrição                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Especifica com que frequência a tarefa é executado e por quanto tempo o padrão de repetição é repetido após o início da tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o intervalo do padrão de repetição é especificado usando a [**propriedade RepetitionPattern.Interval.**](repetitionpattern-interval.md)

Para o desenvolvimento em C++, o intervalo do padrão de repetição é especificado usando a [**propriedade IRepetitionPattern::Interval.**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval)

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que usa um intervalo de repetição, consulte [Xml (Exemplo de Gatilho Diário).](daily-trigger-example--xml-.md)

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

 

 





