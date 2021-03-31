---
title: Propriedade TaskSettings. Compatibility
description: Para scripts, Obtém ou define um valor inteiro que indica a qual versão do Agendador de Tarefas uma tarefa é compatível.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Agendador de Tarefas de propriedade de compatibilidade
- Propriedade de compatibilidade Agendador de Tarefas, objeto TaskSettings
- Agendador de Tarefas de objeto TaskSettings, propriedade de compatibilidade
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644478"
---
# <a name="tasksettingscompatibility-property"></a>Propriedade TaskSettings. Compatibility

Para scripts, Obtém ou define um valor inteiro que indica a qual versão do Agendador de Tarefas uma tarefa é compatível.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a>Valor da propriedade



| Valor                                                                                                                                                                                                                                         | Significado                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <dt>**Tarefa \_ do COMPATIBILIDADE \_ em**</dt> <dt>0</dt> </dl> | A tarefa é compatível com o comando AT.<br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <dt>**Tarefa \_ do COMPATIBILIDADE \_ v1**</dt> <dt>1</dt> </dl> | A tarefa é compatível com o Agendador de Tarefas 1,0.<br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <dt>**Tarefa \_ do COMPATIBILIDADE \_ v2**</dt> <dt>2</dt> </dl> | A tarefa é compatível com o Agendador de Tarefas 2,0.<br/> |



 

## <a name="remarks"></a>Comentários

A compatibilidade de tarefas, que é definida por meio da propriedade de [**compatibilidade**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , só deve ser definida como compatibilidade de tarefas \_ \_ v1 se uma tarefa precisar ser acessada ou modificada de um computador com Windows XP, Windows Server 2003 ou Windows 2000. Caso contrário, é recomendável que Agendador de Tarefas compatibilidade 2,0 seja usada porque a tarefa terá mais recursos.

As tarefas compatíveis com o comando AT podem ter apenas um gatilho de tempo.

As tarefas compatíveis com Agendador de Tarefas 1,0 só podem ter um gatilho de tempo, um gatilho de logon ou um gatilho de inicialização, e a tarefa pode ter apenas uma ação executável.

Para obter mais informações sobre a compatibilidade de tarefas, consulte [What ' s New in Agendador de tarefas](what-s-new-in-task-scheduler.md) and [Tasks](tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**compatibilidade de tarefas \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





