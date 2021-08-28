---
title: Elemento StartWhenAvailable (settingsType)
description: Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após a hora agendada ter passado.
ms.assetid: 1d65fd51-3a94-4083-8e38-2a652383656a
keywords:
- Elemento StartWhenAvailable Agendador de Tarefas
topic_type:
- apiref
api_name:
- StartWhenAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa87fe438cb2916757e5ad9ecf88e08ce944eb6c71749c116afc75b253da6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401756"
---
# <a name="startwhenavailable-settingstype-element"></a>Elemento StartWhenAvailable (settingsType)

Especifica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento após a hora agendada ter passado.

``` syntax
<xs:element name="StartWhenAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O **elemento StartWhenAvailable** é definido pelo tipo complexo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Essa propriedade se aplica somente a tarefas com tempo.

Para desenvolvimento em C++, consulte [**Propriedade StartWhenAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable).

Para desenvolvimento de scripts, [**consulte TaskSettings.StartWhenAvailable**](tasksettings-startwhenavailable.md).

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de configurações que permite que o Agendador de Tarefas inicie a tarefa quando ela estiver disponível.


```XML
<Settings>
    <StartWhenAvailable>true</StartWhenAvailable>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





