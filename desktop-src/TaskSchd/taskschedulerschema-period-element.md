---
title: Elemento period
description: Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Agendador de Tarefas de elemento de período
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455984"
---
# <a name="period-element"></a>Elemento period

Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática.

O formato dessa cadeia de caracteres é *PnYnMnDTnHnMnS*, em que *NY* é o número de anos, nm é o número de meses, *ND* é o número de dias, *T* é o separador de data/hora, *NH* é o número de horas, o *nm* é o número de minutos e o *ns* é o número de segundos (por exemplo, "PT5M" especifica 5 minutos e "P1M4DT2H5M" especifica um mês, quatro dias, duas horas e cinco minutos). O valor mínimo é um minuto. Para obter mais informações sobre o tipo de duração, consulte [esquema XML parte 2: tipos de dados segunda edição](https://www.w3.org/TR/xmlschema-2/#duration).

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

O elemento **period** é definido pelo tipo complexo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                                                          | Derivado de                                                                               | Descrição                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica as configurações de tarefa que o Agendador de tarefas usará para iniciar a tarefa durante a manutenção automática.<br/> |



## <a name="remarks"></a>Comentários

Para a programação C++, essa configuração ociosa é especificada usando a propriedade [**IMaintenanceSettings::P eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .

## <a name="examples"></a>Exemplos

O XML a seguir define a tarefa de manutenção com o requisito de periodicidade definido como 5 dias.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
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

 

 





