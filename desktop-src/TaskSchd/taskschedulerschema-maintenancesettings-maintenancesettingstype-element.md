---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Especifica como o Agendador de Tarefas executa tarefas durante a manutenção automática.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Elemento MaintenanceSettings Agendador de Tarefas
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5724a5dff942377af783970e5d011e8f8a1ce9123039112917a3f652372495d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309336"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>Elemento MaintenanceSettings (maintenanceSettingsType)

Especifica como o Agendador de Tarefas executa tarefas durante a manutenção automática.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

O **elemento MaintenanceSettings** é definido pelo tipo complexo [**maintenanceSettingsType.**](taskschedulerschema-maintenancesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                    | Type    | Descrição                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Prazo**](taskschedulerschema-deadline-element.md)   |         | Especifica a quantidade de tempo após a qual o agendador de tarefas tentará iniciar a tarefa durante a manutenção automática de emergência, se ela não tiver concluído durante a manutenção regular. <br/> |
| [**Exclusivo**](taskschedulerschema-exclusive-element.md) | booleano | Se definido como true, a tarefa será iniciada exclusivamente entre outras tarefas de manutenção. <br/>                                                                                                 |
| [**Período**](taskschedulerschema-period-element.md)       |         | Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática. <br/>                                                                                                      |



## <a name="remarks"></a>Comentários

Para programação C++, essa configuração ociosa é especificada usando a [**propriedade ITaskSettings3::MaintenanceSettings.**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de configurações que instrui o Agendador de Tarefas a executar a tarefa uma vez em cinco dias durante a manutenção automática regular e, se falhar por 15 dias, comece a tentar a tarefa durante a manutenção automática de emergência.


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>           |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





