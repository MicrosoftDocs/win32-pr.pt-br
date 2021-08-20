---
title: Elemento Count (restartype)
description: Especifica o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Agendador de Tarefas de elemento de contagem
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 43d7c499d002e02f58390c28c3102a782ca7ad57ceff49650dd0279922b4fd6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943091"
---
# <a name="count-restarttype-element"></a>Elemento Count (restartype)

Especifica o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo tipo complexo [**Restart**](taskschedulerschema-restarttype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                               | Derivado de                                                       | Descrição                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**Restart**](taskschedulerschema-restarttype-complextype.md) | Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.<br/> |



## <a name="remarks"></a>Comentários

Se esse elemento for especificado, o elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) também deverá ser especificado para informar ao agendador de tarefas por quanto tempo tentar reiniciar a tarefa.

Para desenvolvimento em C++, consulte a [**Propriedade RestartCount de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).

Para desenvolvimento de script, consulte [**TaskSettings. RestartCount**](tasksettings-restartcount.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





