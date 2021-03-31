---
title: Elemento prazo
description: Especifica quando o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção automática regular.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Elemento de prazo Agendador de Tarefas
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644482"
---
# <a name="deadline-element"></a>Elemento prazo

Especifica quando o Agendador de tarefas deve iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção automática regular.

O formato dessa cadeia de caracteres é *PnYnMnDTnHnMnS*, em que *NY* é o número de anos, nm é o número de meses, *ND* é o número de dias, *T* é o separador de data/hora, *NH* é o número de horas, o *nm* é o número de minutos e o *ns* é o número de segundos (por exemplo, "PT5M" especifica 5 minutos e "P1M4DT2H5M" especifica um mês, quatro dias, duas horas e cinco minutos). O valor mínimo é um minuto. Para obter mais informações sobre o tipo de duração, consulte [esquema XML parte 2: tipos de dados segunda edição](https://www.w3.org/TR/xmlschema-2/#duration). Prazo mínimo que uma tarefa pode usar é 1 dia. O valor do elemento **prazo** deve ser maior que o valor do elemento [**period**](taskschedulerschema-period-element.md) . Se o prazo final não for especificado, a tarefa não será iniciada durante a manutenção automática de emergência.

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

O elemento **prazo** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                          | Derivado de                                                                               | Descrição                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica as configurações de tarefa que o Agendador de tarefas usará para iniciar a tarefa durante a manutenção automática.<br/> |



## <a name="remarks"></a>Comentários

Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**IMaintenanceSettings::D Ora**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





