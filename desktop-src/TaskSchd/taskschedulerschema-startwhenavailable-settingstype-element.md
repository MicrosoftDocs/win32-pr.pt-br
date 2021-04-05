---
title: Elemento StartWhenAvailable (settingstype)
description: Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Agendador de Tarefas do elemento StartWhenAvailable
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d86f6f6e75457d08e10ef40d728eaf3e3b00aa7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918143"
---
# <a name="startwhenavailable-settingstype-element"></a>Elemento StartWhenAvailable (settingstype)

Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após o horário agendado ter passado.

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O elemento **StartWhenAvailable** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Essa propriedade só se aplica a tarefas com tempo.

Para desenvolvimento em C++, consulte a [**Propriedade StartWhenAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).

Para desenvolvimento de script, consulte [**TaskSettings. StartWhenAvailable**](tasksettings-startwhenavailable.md).

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que permite que o Agendador de Tarefas inicie a tarefa quando ela estiver disponível.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





