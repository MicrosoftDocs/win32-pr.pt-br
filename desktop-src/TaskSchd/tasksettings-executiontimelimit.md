---
title: TaskSettings.ExePropriedade cutionTimeLimit
description: Para scripts, Obtém ou define a quantidade de tempo permitido para concluir a tarefa.
ms.assetid: 5b8b8d4b-e705-4407-95c9-bf8baacb58c1
keywords:
- Agendador de Tarefas da propriedade ExecutionTimeLimit
- Propriedade ExecutionTimeLimit Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade ExecutionTimeLimit
topic_type:
- apiref
api_name:
- TaskSettings.ExecutionTimeLimit
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de01d68fa7fe6c21f022d8a21863887e57016c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760319"
---
# <a name="tasksettingsexecutiontimelimit-property"></a>TaskSettings.ExePropriedade cutionTimeLimit

Para scripts, Obtém ou define a quantidade de tempo permitido para concluir a tarefa. Por padrão, uma tarefa será interrompida em 72 horas depois de começar a ser executada. Você pode alterar isso alterando essa configuração.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.ExecutionTimeLimit As String
```



## <a name="property-value"></a>Valor da propriedade

A quantidade de tempo permitido para concluir a tarefa. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Um valor de PT0S permitirá que a tarefa seja executada indefinidamente. Quando esse parâmetro é definido como Nothing, o limite de tempo de execução é infinito.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md) do esquema de Agendador de tarefas.

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

 

 





