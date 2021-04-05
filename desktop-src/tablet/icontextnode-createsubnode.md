---
description: Cria um novo objeto filho IContextNode.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Método IContextNode:: CreateSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827190"
---
# <a name="icontextnodecreatesubnode-method"></a>Método IContextNode:: CreateSubNode

Cria um novo objeto filho [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNodeType* \[ no\]
</dt> <dd>

Um **GUID** que representa o tipo de [**IContextNode**](icontextnode.md) a ser criado.

</dd> <dt>

*ppContextNodeCreated* \[ fora\]
</dt> <dd>

Um ponteiro para o novo [**IContextNode**](icontextnode.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextNodeCreated* quando você não precisar mais usar o nó de contexto.

 

O novo [**IContextNode**](icontextnode.md) é adicionado à coleção de nós filho do nó de contexto (consulte [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)). Quando há nós filho existentes, o **IContextNode** recém-criado é adicionado como o último nó filho.

Para obter uma lista de tipos de nó de contexto, consulte [tipos de nó de contexto](context-node-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::D eleteSubNode**](icontextnode-deletesubnode.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

