---
title: Método TriggerCollection. Remove
description: Para scripts, remove o gatilho especificado da coleção de gatilhos usados pela tarefa.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- disparadores Agendador de Tarefas, removendo
- Remover o método Agendador de Tarefas
- Método Remove Agendador de tarefas, objeto disparador
- Agendador de Tarefas de objeto TriggerCollection, método remove
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295770"
---
# <a name="triggercollectionremove-method"></a>Método TriggerCollection. Remove

Para scripts, remove o gatilho especificado da coleção de gatilhos usados pela tarefa.

## <a name="syntax"></a>Sintaxe


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

O índice do gatilho a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Ao remover itens, observe que o índice do primeiro item na coleção é 1 e o índice do último item é o valor da propriedade [**TriggerCollection. Count**](triggercollection-count.md) .

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

 

 





