---
title: Propriedade TaskFolder. GetFolder
description: Para scripts, obtém uma pasta que contém tarefas em um local especificado.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Agendador de Tarefas de propriedade GetFolder
- Agendador de Tarefas de propriedade GetFolder, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, Propriedade GetFolder
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387025"
---
# <a name="taskfoldergetfolder-property"></a>Propriedade TaskFolder. GetFolder

Para scripts, obtém uma pasta que contém tarefas em um local especificado.

## <a name="syntax"></a>Sintaxe


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor da propriedade

O caminho (local) para a pasta. Não use uma barra invertida após o nome da última pasta no caminho. A pasta de tarefas raiz é especificada com uma barra invertida ( \\ ). Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder. O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. ' os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.

## <a name="error-codes"></a>Códigos do Erro

A pasta no local especificado. A pasta é um objeto [**TaskFolder**](taskfolder.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





