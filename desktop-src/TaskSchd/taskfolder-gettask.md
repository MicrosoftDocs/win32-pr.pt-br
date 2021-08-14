---
title: Propriedade TaskFolder.GetTask
description: Para scripts, obtém uma tarefa em um local especificado em uma pasta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Propriedade GetTask Agendador de Tarefas
- Propriedade GetTask Agendador de Tarefas objeto , TaskFolder
- Objeto TaskFolder Agendador de Tarefas propriedade , GetTask
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
ms.openlocfilehash: 8369c09ad62329fa583bfba1cf718a3543c565f3e3d41f1d20f88339e37c44ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253416"
---
# <a name="taskfoldergettask-property"></a>Propriedade TaskFolder.GetTask

Para scripts, obtém uma tarefa em um local especificado em uma pasta.

## <a name="syntax"></a>Sintaxe


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor da propriedade

O caminho (local) para a tarefa em uma pasta. A pasta da tarefa raiz é especificada com uma barra invertida ( \\ ). Um exemplo de um caminho de pasta de tarefa, na pasta de tarefas raiz, é \\ MyTaskFolder. O caractere '.' não pode ser usado para especificar a pasta de tarefas atual e o '..' Não é possível usar caracteres para especificar a pasta de tarefas pai no caminho.

## <a name="error-codes"></a>Códigos do Erro

A tarefa no local especificado. A tarefa é um [**objeto RegisteredTask.**](registeredtask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





