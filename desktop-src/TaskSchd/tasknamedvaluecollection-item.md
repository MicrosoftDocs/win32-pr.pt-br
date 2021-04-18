---
title: Propriedade TaskNamedValueCollection. Item
description: Para scripts, obtém o par nome-valor especificado da coleção.
ms.assetid: 89c87b22-e459-435d-8c15-69907e9b1329
keywords:
- Agendador de Tarefas de Propriedade do item
- Propriedade do item Agendador de Tarefas, objeto TaskNamedValueCollection
- Agendador de Tarefas de objeto TaskNamedValueCollection, Propriedade Item
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd0abff47d699fd6d85f04745f28e2feb31c6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810117"
---
# <a name="tasknamedvaluecollectionitem-property"></a>Propriedade TaskNamedValueCollection. Item

Para scripts, obtém o par nome-valor especificado da coleção.

## <a name="syntax"></a>Syntax


```VB
TaskNamedValueCollection.Item( _
  ByVal index, _
  ByRef pair _
) As long
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**TaskNamedValuePair**](tasknamedvaluepair.md) que representa o par solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





