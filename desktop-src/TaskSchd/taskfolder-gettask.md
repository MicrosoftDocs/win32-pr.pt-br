---
title: Propriedade TaskFolder. getTask
description: Para scripts, obtém uma tarefa em um local especificado em uma pasta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Agendador de Tarefas de propriedade getTask
- Propriedade getTask Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, Propriedade getTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644424"
---
# <a name="taskfoldergettask-property"></a>Propriedade TaskFolder. getTask

Para scripts, obtém uma tarefa em um local especificado em uma pasta.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor da propriedade

O caminho (local) para a tarefa em uma pasta. A pasta de tarefas raiz é especificada com uma barra invertida ( \) . Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder. O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. ' os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.

## <a name="error-codes"></a>Códigos do Erro

A tarefa no local especificado. A tarefa é um objeto [**RegisteredTask**](registeredtask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





