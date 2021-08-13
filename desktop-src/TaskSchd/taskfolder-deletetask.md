---
title: Método TaskFolder.DeleteTask
description: Para scripts, exclui uma tarefa da pasta .
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Método DeleteTask Agendador de Tarefas
- Método DeleteTask Agendador de Tarefas objeto , TaskFolder
- O objeto TaskFolder Agendador de Tarefas , método DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c12b3ca9d66817972d75bd3ffbab61bcdcdff5dcc227e680ed6548f77d1b0de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402396"
---
# <a name="taskfolderdeletetask-method"></a>Método TaskFolder.DeleteTask

Para scripts, exclui uma tarefa da pasta .

## <a name="syntax"></a>Sintaxe


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ Em\]
</dt> <dd>

O nome da tarefa especificada quando a tarefa foi registrada. O caractere '.' não pode ser usado para especificar a pasta de tarefas atual e o '..' Não é possível usar caracteres para especificar a pasta de tarefas pai no caminho.

</dd> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Sem suporte. O valor é 0

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
</dt> </dl>

 

 





