---
title: Objeto TaskNamedValuePair
description: Objeto de script que é usado para criar um par de nome-valor no qual o nome está associado ao valor.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Agendador de Tarefas de objeto TaskNamedValuePair
- Agendador de Tarefas de objeto TaskNamedValuePair, descrito
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761339"
---
# <a name="tasknamedvaluepair-object"></a>Objeto TaskNamedValuePair

Objeto de script que é usado para criar um par de nome-valor no qual o nome está associado ao valor.

## <a name="members"></a>Membros

O objeto **TaskNamedValuePair** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **TaskNamedValuePair** tem essas propriedades.



| Propriedade                                             | Descrição                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Nome**](tasknamedvaluepair-name.md)<br/>   | Obtém ou define o nome associado a um valor em um par de nome-valor.<br/> |
| [**Valor**](tasknamedvaluepair-value.md)<br/> | Obtém ou define o valor associado a um nome em um par de nome-valor.<br/> |



 

## <a name="remarks"></a>Comentários

Ao ler ou gravar seu próprio XML para uma tarefa, um par nome-valor é especificado usando o elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TaskNamedValueCollection**](tasknamedvaluecollection.md)
</dt> </dl>

 

 





