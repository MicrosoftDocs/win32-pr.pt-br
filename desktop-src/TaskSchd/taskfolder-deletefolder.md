---
title: Método TaskFolder.DeleteFolder
description: Para scripts, exclui uma subpasta da pasta pai.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Método DeleteFolder Agendador de Tarefas
- Método DeleteFolder Agendador de Tarefas , objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas , método DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73dfe168b599de6e09d5437d0be4ec7a851d246f9fcbce0f79f662b62c56212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974896"
---
# <a name="taskfolderdeletefolder-method"></a>Método TaskFolder.DeleteFolder

Para scripts, exclui uma subpasta da pasta pai.

## <a name="syntax"></a>Sintaxe


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*folderName* \[ Em\]
</dt> <dd>

O nome da subpasta a ser removida. A pasta da tarefa raiz é especificada com uma barra invertida ( \\ ). Esse parâmetro pode ser um caminho relativo para a pasta que você deseja excluir. Um exemplo de um caminho de pasta de tarefa, na pasta de tarefas raiz, é \\ MyTaskFolder. O caractere '.' não pode ser usado para especificar a pasta de tarefas atual e o '..' Não é possível usar caracteres para especificar a pasta de tarefas pai no caminho.

</dd> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Sem suporte.

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

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





