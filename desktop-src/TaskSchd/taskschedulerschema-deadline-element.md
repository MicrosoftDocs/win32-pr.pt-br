---
title: Elemento Deadline
description: Especifica quando o agendador de tarefas deve iniciar a tarefa durante a manutenção automática de emergência, se ela não foi concluída durante a manutenção automática regular.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Elemento Deadline Agendador de Tarefas
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19d5560b57cfaa2a3fd3fa5167d13fa1722fe3f7dd736f19742e2efc895e15e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857306"
---
# <a name="deadline-element"></a>Elemento Deadline

Especifica quando o agendador de tarefas deve iniciar a tarefa durante a manutenção automática de emergência, se ela não foi concluída durante a manutenção automática regular.

O formato dessa cadeia de caracteres *é PnYnMnDTnHnMnS,* em que *nY* é o número de anos, nM é o número de meses, *nD* é o número de dias, *T* é o separador de data/hora, *nH* é o número de horas, *nM* é o número de minutos e *nS* é o número de segundos (por exemplo, "PT5M" especifica 5 minutos e "P1M4DT2H5M" especifica um mês, quatro dias, duas horas e cinco minutos). O valor mínimo é um minuto. Para obter mais informações sobre o tipo de duração, [consulte Xml Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration). O prazo mínimo que uma tarefa pode usar é de 1 dia. O valor do elemento **Deadline** deve ser maior que o valor do [**elemento Period.**](taskschedulerschema-period-element.md) Se o prazo não for especificado, a tarefa não será iniciada durante a manutenção automática de emergência.

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O **elemento Deadline** é definido pelo tipo complexo [**maintenanceSettingsType.**](taskschedulerschema-maintenancesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                          | Derivado de                                                                               | Descrição                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica as configurações de tarefa que o agendador de tarefas usará para iniciar a tarefa durante a Manutenção automática.<br/> |



## <a name="remarks"></a>Comentários

Para programação C++, essa configuração ociosa é especificada usando a [**propriedade IMaintenanceSettings::D eadline.**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline)

## <a name="examples"></a>Exemplos

O XML a seguir define um calendário de meses que executa a tarefa em março.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
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

 

 





