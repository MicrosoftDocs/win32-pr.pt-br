---
title: Propriedade ActionCollection. Item
description: Para scripts, obtém uma ação especificada da coleção.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Agendador de Tarefas de Propriedade do item
- Propriedade do item Agendador de Tarefas, objeto ActionCollection
- Agendador de Tarefas de objeto ActionCollection, Propriedade Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369793"
---
# <a name="actioncollectionitem-property"></a>Propriedade ActionCollection. Item

Para scripts, obtém uma ação especificada da coleção.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Valor da propriedade

Um objeto de [**ação**](action.md) que representa a ação solicitada.

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
</dt> <dt>

[**Açãocollection**](actioncollection.md)
</dt> </dl>

 

 





