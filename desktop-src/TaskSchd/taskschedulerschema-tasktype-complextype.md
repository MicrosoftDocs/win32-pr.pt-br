---
title: Tipo complexo de taskType (Agendador de Tarefas)
description: Define os elementos filho e as informações de sequenciamento para o elemento Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- tipo complexo de taskType Agendador de Tarefas
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e2465773fb784c87fe560bdc8f6306771578cb22cf9aa26bf79b84867deb61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611053"
---
# <a name="tasktype-complex-type"></a>Tipo complexo de taskType

Define os elementos filho e as informações de sequenciamento para o elemento [**Task**](taskschedulerschema-task-element.md) .

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type                                                                                 | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md)                   | [**ActionType**](taskschedulerschema-actionstype-complextype.md)                   | Especifica as ações executadas pela tarefa.<br/>                                                                             |
| [**Dados**](taskschedulerschema-data-tasktype-element.md)                         | [**Tipo de dados**](taskschedulerschema-datatype-complextype.md)                         | Especifica os dados de adição associados à tarefa, mas, caso contrário, não são usados pelo serviço de Agendador de Tarefas.<br/>         |
| [**Principals**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Especifica os contextos de segurança que podem ser usados para executar a tarefa.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingstype**](taskschedulerschema-settingstype-complextype.md)                 | Especifica as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/>                                                 |
| [**Gatilhos**](taskschedulerschema-triggers-tasktype-element.md)                 | [**TriggerType**](taskschedulerschema-triggerstype-complextype.md)                 | Especifica os gatilhos que iniciam a tarefa.<br/>                                                                              |



## <a name="attributes"></a>Atributos



| Nome    | Tipo                                                              | Descrição                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| version | [**versãotype**](taskschedulerschema-versiontype-simpletype.md) | Especifica a versão da tarefa.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





