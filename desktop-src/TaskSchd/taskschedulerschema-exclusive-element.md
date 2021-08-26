---
title: Elemento exclusivo
description: Indica se o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática no modo exclusivo.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Elemento exclusivo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab796abfdcad67a348b6d42186732d402bbe8eeeb359ac772588fe809dbf73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991326"
---
# <a name="exclusive-element"></a>Elemento exclusivo

Indica se o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática no modo exclusivo.

O exclusividade é garantido apenas entre outras tarefas de manutenção e não concede nenhuma prioridade de ordenação da tarefa. Se exclusividade não for especificado, a tarefa será iniciada em paralelo com outras tarefas de manutenção.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

O elemento **exclusivo** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                          | Derivado de                                                                               | Descrição                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica as configurações de tarefa que o Agendador de tarefas usará para iniciar a tarefa durante a manutenção automática.<br/> |



## <a name="remarks"></a>Comentários

Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**IMaintenanceSettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .

## <a name="examples"></a>Exemplos

O XML a seguir define a tarefa de manutenção com o requisito de prazo definido como 15 dias.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>           |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





