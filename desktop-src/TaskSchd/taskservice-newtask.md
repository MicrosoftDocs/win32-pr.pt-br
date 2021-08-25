---
title: Método TaskService. NewTask
description: Para scripts, retorna um objeto de definição de tarefa vazio a ser preenchido com configurações e propriedades e, em seguida, registrado usando o método TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Método NewTask Agendador de Tarefas
- Método NewTask Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, método NewTask
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22da6f62f59bf24ded0eed9dea21e3a1a9d1c3e7ecc36fb6f425f58124aee71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990926"
---
# <a name="taskservicenewtask-method"></a>Método TaskService. NewTask

Para scripts, retorna um objeto de definição de tarefa vazio a ser preenchido com configurações e propriedades e, em seguida, registrado usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .

## <a name="syntax"></a>Sintaxe


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro e deve ser definido como 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A definição de tarefa que especifica todas as informações necessárias para criar uma nova tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





