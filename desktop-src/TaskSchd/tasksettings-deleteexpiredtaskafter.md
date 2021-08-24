---
title: Propriedade TaskSettings.DeleteExpiredTaskAfter
description: Para scripts, obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Propriedade DeleteExpiredTaskAfter Agendador de Tarefas
- Propriedade DeleteExpiredTaskAfter Agendador de Tarefas objeto , TaskSettings
- O objeto TaskSettings Agendador de Tarefas propriedade , DeleteExpiredTaskAfter
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
ms.openlocfilehash: 521f07a5712165c282a36bbfe2c3b66769239c53d652ae49a03fa6a50c19cb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658446"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a>Propriedade TaskSettings.DeleteExpiredTaskAfter

Para scripts, obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar. Se nenhum valor for especificado para essa propriedade, o Agendador de Tarefas serviço não excluirá a tarefa.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres que obtém ou define a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, em que nY é o número de anos, nM é o número de meses, nD é o número de dias, 'T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="remarks"></a>Comentários

Uma tarefa expira depois que o limite final é excedido para todos os gatilhos associados à tarefa. O limite final de um gatilho é especificado pela [propriedade EndBoundary](trigger-endboundary.md) herdada por todos os objetos de gatilho.

Ao ler ou escrever XML para uma tarefa, essa configuração é especificada no elemento [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) do esquema Agendador de Tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





