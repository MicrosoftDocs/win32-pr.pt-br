---
title: Tipo complexo idleSettingsType
description: Define os elementos filho e as informações de sequenciamento para o elemento IdleSettings (settingstype).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- Agendador de Tarefas tipo complexo idleSettingsType
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782887"
---
# <a name="idlesettingstype-complex-type"></a>Tipo complexo idleSettingsType

Define os elementos filho e as informações de sequenciamento para o elemento [**IdleSettings (settingstype)**](taskschedulerschema-idlesettings-settingstype-element.md) .

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="WaitTimeout"
            default="PT1H"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                  | Type    | Descrição                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)                |         | Especifica a quantidade de tempo permitido para iniciar a tarefa enquanto estiver em uma condição ociosa.<br/>                                                                                                                     |
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | booleano | A tarefa é reiniciada assim que uma condição ociosa é iniciada.<br/>                                                                                                                                             |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | booleano | Especifica que a tarefa será encerrada se a condição de ociosidade terminar antes que a duração de ociosidade seja excedida.<br/>                                                                                                 |
| [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | Especifica a quantidade de tempo de espera para que uma condição ociosa seja iniciada. Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas aguardará indefinidamente se uma condição ociosa ocorrer.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





