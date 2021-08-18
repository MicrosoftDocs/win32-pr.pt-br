---
title: Elemento IdleSettings (settingstype)
description: Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Agendador de Tarefas do elemento IdleSettings
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0a4c3fc978c93d13be8faa62012d3928d47da5b5a214ce50f5506992f1fc8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991210"
---
# <a name="idlesettings-settingstype-element"></a>Elemento IdleSettings (settingstype)

Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso. Para obter informações sobre condições ociosas, consulte [condições de ociosidade da tarefa](task-idle-conditions.md).

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

O elemento **IdleSettings** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai

| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |

## <a name="child-elements"></a>Elementos filho

> [!NOTE]
> As configurações de *duração* e *WaitTimeout* são preteridas. Eles ainda estão presentes na interface do usuário Agendador de Tarefas, e seus métodos de interface ainda podem retornar valores válidos, mas não são mais usados.

| Elemento                                                                                  | Type     | Descrição                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | booleano  | Especifica se a tarefa é reiniciada quando o computador percorre uma condição ociosa mais de uma vez.<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | booleano  | Especifica que o Agendador de Tarefas interromperá a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.<br/> |
| **Preterido**: [ **duração**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Especifica por quanto tempo o computador deve estar em um estado ocioso antes que a tarefa seja executada.<br/>                              |
| **Preterido**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Especifica a quantidade de tempo que o Agendador de Tarefas aguardará a ocorrência de uma condição ociosa.<br/>                |

## <a name="remarks"></a>Comentários

Para desenvolvimento de script, as configurações ociosas são especificadas usando a propriedade [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .

Para desenvolvimento em C++, as configurações ociosas são especificadas usando a propriedade [**ITaskSettings:: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que permite que Agendador de Tarefas Aguarde 24 horas para uma condição ociosa e, em seguida, permite que apenas 10 minutos {IdleDuration) iniciem a tarefa.

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |

## <a name="see-also"></a>Confira também

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)

[Agendador de Tarefas](task-scheduler-start-page.md)
