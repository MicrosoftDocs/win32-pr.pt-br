---
title: Elemento Enabled (settingsType)
description: Especifica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração é True.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Elemento habilitado Agendador de Tarefas
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff198520e354147ff092b2374bb5a766e1ce1c6db6a4b8fc6302b92670bddcda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131865"
---
# <a name="enabled-settingstype-element"></a>Elemento Enabled (settingsType)

Especifica que a tarefa está habilitada. A tarefa pode ser executada somente quando essa configuração é True.

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

O **elemento Enabled** é definido pelo tipo complexo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade habilitada de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).

Para desenvolvimento de scripts, [**consulte TaskSettings.Enabled**](tasksettings-enabled.md).

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa habilitada, consulte Exemplo [de gatilho de tempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





