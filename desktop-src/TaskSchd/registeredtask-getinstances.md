---
title: Método RegisteredTask. GetInstances
description: Para scripts, retorna todas as instâncias atualmente em execução da tarefa registrada.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Método GetInstances Agendador de Tarefas
- Método GetInstances Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método GetInstances
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086077"
---
# <a name="registeredtaskgetinstances-method"></a>Método RegisteredTask. GetInstances

Para scripts, retorna todas as instâncias atualmente em execução da tarefa registrada.

> [!Note]  
> **RegisteredTask. GetInstances** retornará apenas instâncias da tarefa registrada em execução no momento que estão em execução no contexto de segurança de um usuário ou abaixo dele. Por exemplo, para membros do grupo Administradores, as **GetInstances** retornarão todas as instâncias da tarefa registrada atualmente em execução, mas, para os membros do grupo usuários, **GetInstances** retornará apenas as instâncias da tarefa registrada atualmente em execução no contexto de segurança do grupo de usuários.

 

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* 
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser definido como 0.

</dd> <dt>

*runningTasks* \[ fora\]
</dt> <dd>

Um objeto [**RunningTaskCollection**](runningtaskcollection.md) que contém todas as instâncias atualmente em execução da tarefa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

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
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





