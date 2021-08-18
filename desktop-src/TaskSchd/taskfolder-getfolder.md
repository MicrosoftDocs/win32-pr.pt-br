---
title: Propriedade TaskFolder.GetFolder
description: Para scripts, obtém uma pasta que contém tarefas em um local especificado.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Propriedade GetFolder Agendador de Tarefas
- Propriedade GetFolder Agendador de Tarefas objeto , TaskFolder
- Objeto TaskFolder Agendador de Tarefas propriedade , GetFolder
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
ms.openlocfilehash: 7668b2486a316fe2bf799762401459ec7da2602ff52a4d5d3dc9ddb4dd888e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758979"
---
# <a name="taskfoldergetfolder-property"></a>Propriedade TaskFolder.GetFolder

Para scripts, obtém uma pasta que contém tarefas em um local especificado.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valor da propriedade

O caminho (local) para a pasta. Não use uma faixa invertida após o nome da última pasta no caminho. A pasta da tarefa raiz é especificada com uma barra invertida ( \\ ). Um exemplo de um caminho de pasta de tarefa, na pasta de tarefas raiz, é \\ MyTaskFolder. O caractere '.' não pode ser usado para especificar a pasta de tarefas atual e o '..' Não é possível usar caracteres para especificar a pasta de tarefas pai no caminho.

## <a name="error-codes"></a>Códigos do Erro

A pasta no local especificado. A pasta é um [**objeto TaskFolder.**](taskfolder.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





