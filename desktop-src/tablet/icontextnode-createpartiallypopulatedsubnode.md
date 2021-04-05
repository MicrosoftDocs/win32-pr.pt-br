---
description: Cria um objeto IContextNode filho que contém apenas informações sobre o tipo, o identificador e o local.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Método IContextNode:: CreatePartiallyPopulatedSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827191"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>Método IContextNode:: CreatePartiallyPopulatedSubNode

Cria um objeto [**IContextNode**](icontextnode.md) filho que contém apenas informações sobre o tipo, o identificador e o local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNodeType* \[ no\]
</dt> <dd>

O tipo de nó de contexto a ser criado.

</dd> <dt>

*pNodeId* \[ no\]
</dt> <dd>

O identificador do novo nó.

</dd> <dt>

*pNodeLocation* \[ no\]
</dt> <dd>

O local do novo nó.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ fora\]
</dt> <dd>

Um ponteiro para o novo [**IContextNode**](icontextnode.md)parcialmente preenchido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pPartiallyPopulatedContextNodeCreated* quando você não precisar mais usar o nó de contexto.

 

O novo [**IContextNode**](icontextnode.md) é adicionado à coleção de nós filho do nó de contexto (consulte [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)). Quando há nós filho existentes, o **IContextNode** recém-criado é adicionado como o último nó filho.

Para obter mais informações sobre tipo, identificador e local, consulte [**IContextNode:: GetType**](icontextnode-gettype.md), [**IContextNode:: GetID**](icontextnode-getid.md)e [**IContextNode:: getLocation**](icontextnode-getlocation.md).

Esse método é usado para o proxy de dados como uma maneira de criar um objeto [**IContextNode**](icontextnode.md) na árvore de nós de contexto antes que todas as informações sobre ele estejam disponíveis. Para obter mais informações, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

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

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

