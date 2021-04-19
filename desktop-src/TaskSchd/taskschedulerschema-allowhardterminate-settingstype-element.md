---
title: Elemento AllowHardTerminate (settingstype)
description: Especifica que a tarefa pode ser encerrada usando TerminateProcess.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Elemento AllowHardTerminate (settingstype) Agendador de Tarefas
- Agendador de Tarefas do elemento AllowHardTerminate
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105800011"
---
# <a name="allowhardterminate-settingstype-element"></a>Elemento AllowHardTerminate (settingstype)

Especifica que a tarefa pode ser encerrada usando TerminateProcess.

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

O elemento **AllowHardTerminate** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                 | Descrição                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade AllowHardTerminate de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).

Para desenvolvimento de script, consulte [**TaskSettings. AllowHardTerminate**](tasksettings-allowhardterminate.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que permite um encerramento rígido, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





