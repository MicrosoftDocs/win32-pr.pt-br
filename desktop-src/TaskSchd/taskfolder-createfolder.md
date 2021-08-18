---
title: Método TaskFolder.CreateFolder
description: Para scripts, cria uma pasta para tarefas relacionadas.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Método CreateFolder Agendador de Tarefas
- Método CreateFolder Agendador de Tarefas objeto , TaskFolder
- Objeto TaskFolder Agendador de Tarefas , método CreateFolder
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
ms.openlocfilehash: 2a5de913ccf98ee8369430425e423813168c083cbde737b5831917a5ee594e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759016"
---
# <a name="taskfoldercreatefolder-method"></a>Método TaskFolder.CreateFolder

Para scripts, cria uma pasta para tarefas relacionadas.

## <a name="syntax"></a>Sintaxe


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*folderName* \[ Em\]
</dt> <dd>

O nome usado para identificar a pasta. Se "FolderName \\ SubFolder1 SubFolder2" for especificado, toda a árvore de pastas será criada se as pastas \\ não existirem. Esse parâmetro pode ser um caminho relativo para a instância [**taskFolder**](taskfolder.md) atual. A pasta da tarefa raiz é especificada com uma barra invertida ( \\ ). Um exemplo de um caminho de pasta de tarefa, na pasta de tarefas raiz, é \\ MyTaskFolder. O caractere '.' não pode ser usado para especificar a pasta de tarefas atual e o '..' Não é possível usar caracteres para especificar a pasta de tarefas pai no caminho.

</dd> <dt>

*sddl* \[ Em\]
</dt> <dd>

O descritor de segurança associado à pasta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um [**objeto TaskFolder**](taskfolder.md) que representa a nova subpasta.

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

 

 





