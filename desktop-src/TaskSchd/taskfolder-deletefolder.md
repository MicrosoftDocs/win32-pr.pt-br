---
title: Método TaskFolder. DeleteFolder
description: Para scripts, exclui uma subpasta da pasta pai.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Agendador de Tarefas do método DeleteFolder
- Método DeleteFolder Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, método DeleteFolder
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
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455401"
---
# <a name="taskfolderdeletefolder-method"></a>Método TaskFolder. DeleteFolder

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

*nome_da_pasta* \[ no\]
</dt> <dd>

O nome da subpasta a ser removida. A pasta de tarefas raiz é especificada com uma barra invertida ( \) . Esse parâmetro pode ser um caminho relativo para a pasta que você deseja excluir. Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder. O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. ' os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Não há suporte.

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

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





