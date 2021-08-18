---
title: Tipo complexo maintenanceSettingsType
description: Define os elementos filho e as informações de sequenciamento para o elemento MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- Agendador de Tarefas tipo complexo maintenanceSettingsType
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0733d16ec929b4e67774fc436c1530b67d70392b2655525b2aaaa642c2ea346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139199"
---
# <a name="maintenancesettingstype-complex-type"></a>Tipo complexo maintenanceSettingsType

Define os elementos filho e as informações de sequenciamento para o elemento [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                        | Type    | Descrição                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Prazo**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Especifica o período de tempo após o qual o Agendador de tarefas tentará iniciar a tarefa durante a manutenção automática de emergência, se ela não for concluída durante a manutenção regular.<br/> |
| **Exclusive**                                                                  | booleano | Se definido como true, a tarefa será iniciada exclusivamente entre outras tarefas de manutenção.<br/>                                                                                                 |
| [**Período**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Especifica com que frequência a tarefa precisa ser iniciada durante a manutenção automática.<br/>                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>           |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





