---
title: Método TaskService. GetRunningTasks
description: Para scripts, obtém uma coleção de tarefas em execução.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Agendador de Tarefas do método GetRunningTasks
- Método GetRunningTasks Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, método GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecbc52451a4ed3dcc5f3ecc9984009e94dd9bf18b4c8dc667c0b040c43cc68c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072416"
---
# <a name="taskservicegetrunningtasks-method"></a>Método TaskService. GetRunningTasks

Para scripts, obtém uma coleção de tarefas em execução.

> [!Note]  
> **TaskService. GetRunningTasks** retornará apenas uma coleção de tarefas em execução em execução no contexto de segurança de um usuário ou abaixo dele. Por exemplo, para membros do grupo Administradores, **GetRunningTasks** retornará uma coleção de todas as tarefas em execução, mas para os membros do grupo usuários, o **GetRunningTasks** retornará apenas uma coleção de tarefas que estão sendo executadas no contexto de segurança do grupo usuários.

 

## <a name="syntax"></a>Sintaxe


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Passe 1 para retornar todas as tarefas em execução, incluindo tarefas ocultas. Passe 0 para retornar uma coleção de tarefas em execução que não são tarefas ocultas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um objeto [**RunningTaskCollection**](runningtaskcollection.md) que contém as tarefas em execução no momento.

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

 

 





