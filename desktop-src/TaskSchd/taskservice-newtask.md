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
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779284"
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

## <a name="return-value"></a>Retornar valor

A definição de tarefa que especifica todas as informações necessárias para criar uma nova tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





