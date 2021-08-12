---
title: Elemento UseUnifiedSchedulingEngine (settingsType)
description: Especifica que o Mecanismo de Agendamento Unificado será usado para executar essa tarefa.
ms.assetid: 93436f14-1caf-4ec8-bf74-a198b7dcb27c
keywords:
- Elemento UseUnifiedSchedulingEngine Agendador de Tarefas
topic_type:
- apiref
api_name:
- UseUnifiedSchedulingEngine
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faf27ea132fb47e35cd248e183fbec0584cb5d44414d6cacda6baac0d595c32d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610449"
---
# <a name="useunifiedschedulingengine-settingstype-element"></a>Elemento UseUnifiedSchedulingEngine (settingsType)

Especifica que o Mecanismo de Agendamento Unificado será usado para executar essa tarefa.

``` syntax
<xs:element name="UseUnifiedSchedulingEngine"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O **elemento UseUnifiedSchedulingEngine** é definido pelo [**tipo complexo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

A configuração padrão para esse elemento é False.

Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITaskSettings2::UseUnifiedSchedulingEngine.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings2-get_useunifiedschedulingengine)

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento settings que especifica que o Mecanismo de Agendamento Unificado será usado para executar essa tarefa.


```XML
<Settings>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
</Settings>
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





