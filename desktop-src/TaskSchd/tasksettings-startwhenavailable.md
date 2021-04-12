---
title: Propriedade TaskSettings. StartWhenAvailable
description: Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento depois que o horário agendado tiver passado.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Agendador de Tarefas da propriedade StartWhenAvailable
- Propriedade StartWhenAvailable Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455695"
---
# <a name="tasksettingsstartwhenavailable-property"></a>Propriedade TaskSettings. StartWhenAvailable

Para scripts, Obtém ou define um valor booliano que indica que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento depois que o horário agendado tiver passado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a propriedade indicará que o Agendador de Tarefas pode iniciar a tarefa a qualquer momento depois que o horário agendado tiver passado. O padrão é False.

## <a name="remarks"></a>Comentários

Essa propriedade se aplica somente a tarefas baseadas em tempo com um limite final ou tarefas baseadas em tempo que são definidas para repetir infinitamente.

As tarefas que são iniciadas após o horário agendado passaram (devido à propriedade [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) ser definida como true) são enfileiradas na fila de tarefas do serviço de Agendador de tarefas e elas são iniciadas após um atraso. O atraso padrão é 10 minutos.

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





