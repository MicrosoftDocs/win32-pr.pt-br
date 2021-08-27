---
title: Propriedade TaskSettings. RestartCount
description: Para scripts, Obtém ou define o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Agendador de Tarefas da propriedade RestartCount
- Propriedade RestartCount Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a34e8eef84575548998e39ab47bc5492baca368f7012d5fa096c831539ceb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072406"
---
# <a name="tasksettingsrestartcount-property"></a>Propriedade TaskSettings. RestartCount

Para scripts, Obtém ou define o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>Valor da propriedade

O número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.

## <a name="remarks"></a>Comentários

Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**Count**](taskschedulerschema-count-restarttype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





