---
title: Elemento WakeToRun (settingstype)
description: Especifica que Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.
ms.assetid: 5fb53016-5778-463d-bb32-3c1da2de6fc2
keywords:
- Agendador de Tarefas do elemento WakeToRun
topic_type:
- apiref
api_name:
- WakeToRun
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12d16f9f06685a427a8f3e7c4f2356dff0bc6415e50379ba752a4bc3a3fec8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872056"
---
# <a name="waketorun-settingstype-element"></a>Elemento WakeToRun (settingstype)

Especifica que Agendador de Tarefas ativará o computador quando for hora de executar a tarefa.

``` syntax
<xs:element name="WakeToRun"
    type="boolean"
 />
```

O elemento **WakeToRun** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Quando o serviço de Agendador de Tarefas ativa o computador para executar uma tarefa, a tela pode permanecer desativada, mesmo que o computador não esteja mais no modo de suspensão ou hibernação. a tela será ativada quando Windows o Vista detectar que um usuário voltou a usar o computador.

Para desenvolvimento em C++, consulte a [**Propriedade WakeToRun de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_waketorun).

Para desenvolvimento de script, consulte [**TaskSettings. WakeToRun**](tasksettings-waketorun.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





