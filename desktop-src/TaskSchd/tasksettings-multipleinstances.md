---
title: Propriedade TaskSettings. MultipleInstances
description: Para scripts, Obtém ou define a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Agendador de Tarefas da propriedade MultipleInstances
- Propriedade MultipleInstances Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff0091b9051840fea4c37869b51902f0c5f4c7cfed43a47c4f3924b398fe3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059684"
---
# <a name="tasksettingsmultipleinstances-property"></a>Propriedade TaskSettings. MultipleInstances

Para scripts, Obtém ou define a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Valor da propriedade

[**Tarefa \_ do Constantes de \_ política de instâncias**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) .



| Valor                                                                                                                                                                                                                                                               | Significado                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**Tarefa \_ do INSTÂNCIAS \_ paralelas**</dt> <dt>0</dt> </dl>                 | Inicia uma nova instância enquanto uma instância existente da tarefa está em execução.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**Tarefa \_ do INSTÂNCIAS da \_ fila**</dt> <dt>1</dt> </dl>                          | Inicia uma nova instância da tarefa depois que todas as outras instâncias da tarefa são concluídas.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**Tarefa \_ do INSTÂNCIAS \_ ignoram \_ novas**</dt> <dt>2</dt> </dl>          | Não iniciará uma nova instância se uma instância existente da tarefa estiver em execução.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**Tarefa \_ do As \_ instâncias \_ param**</dt> <dt>3</dt> existentes </dl> | Interrompe uma instância existente da tarefa antes de iniciar nova instância.<br/>                 |



 

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_política de instâncias de tarefas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





