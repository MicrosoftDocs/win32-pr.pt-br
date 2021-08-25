---
title: Propriedade ActionCollection.Item
description: Para scripts, obtém uma ação especificada da coleção.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Propriedades do item Agendador de Tarefas
- Propriedade item Agendador de Tarefas objeto , ActionCollection
- Objeto ActionCollection Agendador de Tarefas propriedade , Item
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
ms.openlocfilehash: fff95b707a4a99ce54cba4d175ce9fd094f7a6bd400147d7942a42a39d65bb7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796636"
---
# <a name="actioncollectionitem-property"></a>Propriedade ActionCollection.Item

Para scripts, obtém uma ação especificada da coleção.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Valor da propriedade

Um [**objeto Action**](action.md) que representa a ação solicitada.

## <a name="remarks"></a>Comentários

As coleções são baseadas em 1. Em outras palavras, o índice do primeiro item na coleção é 1.

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
</dt> <dt>

[**Actioncollection**](actioncollection.md)
</dt> </dl>

 

 





