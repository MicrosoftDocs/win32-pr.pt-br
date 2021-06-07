---
title: Método TaskFolder. CreateFolder
description: Para scripts, o cria uma pasta para tarefas relacionadas.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Método CreateFolder Agendador de Tarefas
- Método CreateFolder Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, método CreateFolder
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387067"
---
# <a name="taskfoldercreatefolder-method"></a>Método TaskFolder. CreateFolder

Para scripts, o cria uma pasta para tarefas relacionadas.

## <a name="syntax"></a>Sintaxe


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome_da_pasta* \[ no\]
</dt> <dd>

O nome usado para identificar a pasta. Se "nome_da_pasta \\ subpasta1 \\ SubFolder2" for especificado, toda a árvore de pastas será criada se as pastas não existirem. Esse parâmetro pode ser um caminho relativo para a instância de [**TaskFolder**](taskfolder.md) atual. A pasta de tarefas raiz é especificada com uma barra invertida ( \\ ). Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder. O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. ' os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.

</dd> <dt>

*SDDL* \[ no\]
</dt> <dd>

O descritor de segurança associado à pasta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um objeto [**TaskFolder**](taskfolder.md) que representa a nova subpasta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





