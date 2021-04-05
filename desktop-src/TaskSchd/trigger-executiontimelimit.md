---
title: Trigger.ExePropriedade cutionTimeLimit
description: Para scripts, Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.
ms.assetid: 9993b362-f8f7-429b-a16a-1845d6f0f5e0
keywords:
- Agendador de Tarefas da propriedade ExecutionTimeLimit
- Agendador de Tarefas da propriedade ExecutionTimeLimit, objeto de gatilho
- Objeto disparador Agendador de Tarefas, Propriedade ExecutionTimeLimit
topic_type:
- apiref
api_name:
- Trigger.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974a9adebf8ca29fe8626c938c37580d0628771b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918208"
---
# <a name="triggerexecutiontimelimit-property"></a>Trigger.ExePropriedade cutionTimeLimit

Para scripts, Obtém ou define a quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada.

## <a name="syntax"></a>Syntax


```VB
Trigger.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valor da propriedade

A quantidade máxima de tempo que a tarefa iniciada pelo gatilho tem permissão para ser executada. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos).

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, o limite de tempo de execução é especificado no elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) do esquema de Agendador de tarefas.

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

 

 





