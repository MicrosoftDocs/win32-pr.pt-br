---
title: Propriedade TriggerCollection. Item
description: Para scripts, obtém o gatilho especificado da coleção.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Agendador de Tarefas de Propriedade do item
- Propriedade do item Agendador de tarefas, objeto disparador
- Agendador de Tarefas de objeto TriggerCollection, Propriedade Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644468"
---
# <a name="triggercollectionitem-property"></a>Propriedade TriggerCollection. Item

Para scripts, obtém o gatilho especificado da coleção.

## <a name="syntax"></a>Sintaxe


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Valor da propriedade

Um objeto de [**gatilho**](trigger.md) que representa o gatilho solicitado.

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

 

 





