---
title: Propriedade RunningTask. EnginePID
description: Para scripts, obtém a ID do processo para o mecanismo (processo) que está executando a tarefa.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Agendador de Tarefas da propriedade EnginePID
- Propriedade EnginePID Agendador de Tarefas, objeto RunningTask
- Objeto RunningTask Agendador de Tarefas, Propriedade EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759038"
---
# <a name="runningtaskenginepid-property"></a>Propriedade RunningTask. EnginePID

Para scripts, obtém a ID do processo para o mecanismo (processo) que está executando a tarefa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valor da propriedade

A ID do processo para o mecanismo que está executando a tarefa.

## <a name="remarks"></a>Comentários

A ID de processo retornada por essa propriedade não pode ser acrescentada diretamente a uma cadeia de caracteres. O valor retornado precisa ser convertido em um valor inteiro primeiro chamando a função [CInt](/previous-versions//fctcwhw9(v=vs.85)) no valor retornado.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

