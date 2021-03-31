---
title: Propriedade TaskSettings. AllowHardTerminate
description: Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser encerrada pelo serviço de Agendador de Tarefas usando o TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Agendador de Tarefas da propriedade AllowHardTerminate
- Propriedade AllowHardTerminate Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644878"
---
# <a name="tasksettingsallowhardterminate-property"></a>Propriedade TaskSettings. AllowHardTerminate

Para scripts, Obtém ou define um valor booliano que indica que a tarefa pode ser encerrada pelo serviço de Agendador de Tarefas usando o [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). O serviço tentará fechar a tarefa em execução enviando a notificação [**de \_ fechamento do WM**](../winmsg/wm-close.md) e, se a tarefa não responder, a tarefa será encerrada somente se essa propriedade for definida como true.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>Valor da propriedade

Se for true, a tarefa poderá ser encerrada usando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Se for false, a tarefa não poderá ser encerrada usando **TerminateProcess**.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

