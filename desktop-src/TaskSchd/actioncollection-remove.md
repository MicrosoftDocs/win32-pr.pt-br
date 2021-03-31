---
title: Método ActionCollection. Remove
description: Para scripts, remove a ação especificada da coleção.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Remover o método Agendador de Tarefas
- Método Remove Agendador de Tarefas, objeto ActionCollection
- Método de ação Agendador de Tarefas do objeto, remover
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644890"
---
# <a name="actioncollectionremove-method"></a>Método ActionCollection. Remove

Para scripts, remove a ação especificada da coleção.

## <a name="syntax"></a>Sintaxe


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ do no\]
</dt> <dd>

O índice da ação a ser removida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Ao remover itens, observe que o índice do primeiro item na coleção é 1 e o índice do último item é o valor da propriedade [**ActionCollection. Count**](actioncollection-count.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Açãocollection**](actioncollection.md)
</dt> </dl>

 

 





