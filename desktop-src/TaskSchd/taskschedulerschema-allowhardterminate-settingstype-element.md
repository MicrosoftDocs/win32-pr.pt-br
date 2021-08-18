---
title: Elemento AllowHardTerminate (settingsType)
description: Especifica que a tarefa pode ser encerrada usando TerminateProcess.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Elemento AllowHardTerminate (settingsType) Agendador de Tarefas
- Elemento AllowHardTerminate Agendador de Tarefas
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d7a143dfb0024cced8a67595e17b12fba9d037b335b425272e1ad2a7999e0b11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010916"
---
# <a name="allowhardterminate-settingstype-element"></a>Elemento AllowHardTerminate (settingsType)

Especifica que a tarefa pode ser encerrada usando TerminateProcess.

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

O **elemento AllowHardTerminate** é definido pelo tipo complexo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                 | Descrição                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**Tasktype**](taskschedulerschema-tasktype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**propriedade AllowHardTerminate de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).

Para desenvolvimento de scripts, [**consulte TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que permite o encerramento rígido, consulte Exemplo [de gatilho de tempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





