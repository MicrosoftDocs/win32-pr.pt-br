---
title: Elemento RestartOnIdle (idleSettingsType)
description: Especifica se a tarefa é reiniciada quando o computador percorre uma condição ociosa mais de uma vez.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Agendador de Tarefas do elemento RestartOnIdle
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760137"
---
# <a name="restartonidle-idlesettingstype-element"></a>Elemento RestartOnIdle (idleSettingsType)

Especifica se a tarefa é reiniciada quando o computador percorre uma condição ociosa mais de uma vez.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O elemento **RestartOnIdle** é definido pelo tipo complexo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/> |



## <a name="remarks"></a>Comentários

Esse elemento será usado somente se o elemento [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) estiver definido como true.

Para o desenvolvimento de script, essas configurações de tarefa são especificadas usando a propriedade [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .

Para desenvolvimento em C++, essas configurações de tarefa são especificadas usando a propriedade [**IIdleSettings:: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .

## <a name="examples"></a>Exemplos

O XML a seguir define uma configuração ociosa que indica que a tarefa não deve ser reiniciada quando a condição ociosa ciclos.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





