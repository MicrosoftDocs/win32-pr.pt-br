---
title: Propriedade TaskSettings. DeleteExpiredTaskAfter
description: Para scripts, Obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Agendador de Tarefas da propriedade DeleteExpiredTaskAfter
- Propriedade DeleteExpiredTaskAfter Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454893"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>Propriedade TaskSettings. DeleteExpiredTaskAfter

Para scripts, Obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar. Se nenhum valor for especificado para essa propriedade, o serviço de Agendador de Tarefas não excluirá a tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres que Obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="remarks"></a>Comentários

Uma tarefa expira depois que o limite final foi excedido para todos os gatilhos associados à tarefa. O limite final de um gatilho é especificado pela propriedade de [limite](trigger-endboundary.md) de extremidade herdada por todos os objetos de gatilho.

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**DeleteExpiredTaskAfter (settingstype)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





