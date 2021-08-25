---
title: Método ActionCollection.Remove
description: Para scripts, remove a ação especificada da coleção.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Remover o método Agendador de Tarefas
- Remover método Agendador de Tarefas objeto , ActionCollection
- O objeto ActionCollection Agendador de Tarefas , remover método
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
ms.openlocfilehash: c0c176f41c59bd473e25e82082ada1934a25641e6144f4187e7f25075779b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011736"
---
# <a name="actioncollectionremove-method"></a>Método ActionCollection.Remove

Para scripts, remove a ação especificada da coleção.

## <a name="syntax"></a>Sintaxe


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*índice* \[ Em\]
</dt> <dd>

O índice da ação a ser removida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Ao remover itens, observe que o índice do primeiro item na coleção é 1 e o índice do último item é o valor da propriedade [**ActionCollection.Count.**](actioncollection-count.md)

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

 

 





