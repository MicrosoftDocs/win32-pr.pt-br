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
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454897"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





