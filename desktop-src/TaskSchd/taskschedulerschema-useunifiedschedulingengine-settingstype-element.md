---
title: Elemento UseUnifiedSchedulingEngine (settingstype)
description: Especifica que o mecanismo de agendamento unificado será usado para executar essa tarefa.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Agendador de Tarefas do elemento UseUnifiedSchedulingEngine
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a00798a46df3dfbb351dd8705b264192c38daff6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009152"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a>Elemento UseUnifiedSchedulingEngine (settingstype)

Especifica que o mecanismo de agendamento unificado será usado para executar essa tarefa.

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O elemento **UseUnifiedSchedulingEngine** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

A configuração padrão para esse elemento é false.

Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITaskSettings2:: UseUnifiedSchedulingEngine**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine) .

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que especifica que o mecanismo de agendamento unificado será usado para executar essa tarefa.


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





