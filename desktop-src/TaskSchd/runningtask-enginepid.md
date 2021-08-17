---
title: Propriedade RunningTask.EnginePID
description: Para scripts, obtém a ID do processo para o mecanismo (processo) que está executando a tarefa.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- A propriedade EnginePID Agendador de Tarefas
- Propriedade EnginePID Agendador de Tarefas objeto , RunningTask
- Objeto RunningTask Agendador de Tarefas , propriedade EnginePID
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
ms.openlocfilehash: eed259ccc92e954ae1acde076f0cc09167d15071ea71a33039e7298479875b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759062"
---
# <a name="runningtaskenginepid-property"></a>Propriedade RunningTask.EnginePID

Para scripts, obtém a ID do processo para o mecanismo (processo) que está executando a tarefa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a>Valor da propriedade

A ID do processo para o mecanismo que está executando a tarefa.

## <a name="remarks"></a>Comentários

A ID do processo retornada por essa propriedade não pode ser anexada diretamente a uma cadeia de caracteres. O valor retornado precisa ser convertido em um valor inteiro primeiro chamando a [função CInt](/previous-versions//fctcwhw9(v=vs.85)) no valor retornado.


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

