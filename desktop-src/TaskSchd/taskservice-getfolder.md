---
title: Método TaskService. GetFolder
description: Para scripts, obtém uma pasta de tarefas registradas.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Método GetFolder Agendador de Tarefas
- Método GetFolder Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, método GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632595e462abd5d6bba5c2e91ebcd590f4ec9a7289092eaf56626e4586691be3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072426"
---
# <a name="taskservicegetfolder-method"></a>Método TaskService. GetFolder

Para scripts, obtém uma pasta de tarefas registradas.

## <a name="syntax"></a>Sintaxe


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*caminho* \[ do no\]
</dt> <dd>

O caminho para a pasta a ser recuperada. Não use uma barra invertida após o nome da última pasta no caminho. A pasta de tarefas raiz é especificada com uma barra invertida ( \\ ). Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder. O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. ' os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um objeto [**TaskFolder**](taskfolder.md) para a pasta solicitada.

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

 

 





