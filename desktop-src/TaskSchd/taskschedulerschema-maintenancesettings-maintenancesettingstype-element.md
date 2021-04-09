---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Especifica como a Agendador de Tarefas executa tarefas durante a manutenção automática.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Agendador de Tarefas do elemento MaintenanceSettings
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086068"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>Elemento MaintenanceSettings (maintenanceSettingsType)

Especifica como a Agendador de Tarefas executa tarefas durante a manutenção automática.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

O elemento **MaintenanceSettings** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                    | Type    | Descrição                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Prazo**](taskschedulerschema-deadline-element.md)   |         | Especifica o período de tempo após o qual o Agendador de tarefas tentará iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção regular. <br/> |
| [**Exclusivo**](taskschedulerschema-exclusive-element.md) | booleano | Se definido como true, a tarefa será iniciada exclusivamente entre outras tarefas de manutenção. <br/>                                                                                                 |
| [**Período**](taskschedulerschema-period-element.md)       |         | Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática. <br/>                                                                                                      |



## <a name="remarks"></a>Comentários

Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**ITaskSettings3:: MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings) .

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que instrui Agendador de Tarefas a executar a tarefa uma vez em 5 dias durante a manutenção automática regular e, se houver falha por 15 dias, começar a tentar a tarefa durante a manutenção automática de emergência.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





