---
description: Cria um objeto IContextNode filho que contém apenas informações sobre tipo, identificador e local.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: Método IContextNode::CreatePartiallyPopulatedSubNode (IACom.h)
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
ms.openlocfilehash: 7233c6e0303f0634c71a67fde13f237feb2b2f6c6518dd8edc0b1624b4e2b6b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940286"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a>Método IContextNode::CreatePartiallyPopulatedSubNode

Cria um objeto [**IContextNode filho**](icontextnode.md) que contém apenas informações sobre tipo, identificador e local.

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

*pNodeType* \[ Em\]
</dt> <dd>

O tipo de nó de contexto a ser criado.

</dd> <dt>

*pNodeId* \[ Em\]
</dt> <dd>

O identificador do novo nó.

</dd> <dt>

*pNodeLocation* \[ Em\]
</dt> <dd>

O local do novo nó.

</dd> <dt>

*pPartiallyPopulatedContextNodeCreated* \[ out\]
</dt> <dd>

Um ponteiro para o novo [**IContextNode**](icontextnode.md)parcialmente preenchido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pPartiallyPopulatedContextNodeCreated* quando não precisar mais usar o nó de contexto.

 

O novo [**IContextNode**](icontextnode.md) é adicionado à coleção de nós filho desse nó de contexto (consulte [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)). Quando há nós filho existentes, o **IContextNode** recém-criado é adicionado como o último nó filho.

Para obter mais informações sobre tipo, identificador e local, consulte [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md)e [**IContextNode::GetLocation**](icontextnode-getlocation.md).

Esse método é usado para proxy de dados como uma maneira de criar um objeto [**IContextNode**](icontextnode.md) na árvore de nós de contexto antes que todas as informações sobre ele estão disponíveis. Para obter mais informações, consulte [Proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
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

 

