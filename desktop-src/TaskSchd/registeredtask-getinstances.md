---
title: Método RegisteredTask.GetInstances
description: Para scripts, retorna todas as instâncias atualmente em execução da tarefa registrada.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Método GetInstances Agendador de Tarefas
- Método GetInstances Agendador de Tarefas , objeto RegisteredTask
- Método Agendador de Tarefas objeto RegisteredTask , GetInstances
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
ms.openlocfilehash: 4f9224922e70242304423950a67bf4acd866d1a551a90f4c9a6dadb94470ba1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126056"
---
# <a name="registeredtaskgetinstances-method"></a>Método RegisteredTask.GetInstances

Para scripts, retorna todas as instâncias atualmente em execução da tarefa registrada.

> [!Note]  
> **RegisteredTask.GetInstances** retornará apenas instâncias da tarefa registrada em execução no momento que estão em execução no contexto de segurança de um usuário ou abaixo. Por exemplo, para membros do grupo Administradores, **GetInstances** retornará todas as instâncias da tarefa registrada em execução no momento, mas para membros do grupo Usuários, **GetInstances** retornará apenas instâncias da tarefa registrada em execução no momento em execução no contexto de segurança do grupo Usuários.

 

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

*runningTasks* \[ out\]
</dt> <dd>

Um [**objeto RunningTaskCollection**](runningtaskcollection.md) que contém todas as instâncias em execução atualmente da tarefa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

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
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





