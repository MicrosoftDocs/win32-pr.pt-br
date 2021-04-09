---
title: Propriedade RunningTaskCollection. Item
description: Para scripts, obtém a tarefa especificada da coleção.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Agendador de Tarefas de Propriedade do item
- Propriedade do item Agendador de Tarefas, objeto RunningTaskCollection
- Agendador de Tarefas de objeto RunningTaskCollection, Propriedade Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085879"
---
# <a name="runningtaskcollectionitem-property"></a>Propriedade RunningTaskCollection. Item

Para scripts, obtém a tarefa especificada da coleção.

## <a name="syntax"></a>Syntax


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**RunningTask**](runningtask.md) que contém o contexto solicitado.

## <a name="remarks"></a>Comentários

As coleções são baseadas em 1. Em outras palavras, o índice do primeiro item na coleção é 1.

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

 

 





