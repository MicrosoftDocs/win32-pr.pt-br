---
description: Recupera o nó pai desse IContextNode na árvore de nós de contexto.
ms.assetid: 782fd973-f8f3-4902-b8e0-cc5e70a66d28
title: 'Método IContextNode:: GetParentNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetParentNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 23739bd92da2e8337c949ac7b1fd66e456da1c803cccbe4d0980821a062ec9da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935376"
---
# <a name="icontextnodegetparentnode-method"></a>Método IContextNode:: GetParentNode

Recupera o nó pai desse [**IContextNode**](icontextnode.md) na árvore de nós de contexto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppParentContextNode* \[ fora\]
</dt> <dd>

Um ponteiro para o nó pai deste objeto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppParentContextNode* quando você não precisar mais usar o nó de contexto pai.

 

Se esse for o nó raiz, o parâmetro *ppParentContextNode* será definido como **NULL**.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um método auxiliar que recupera informações sobre um nó especificado, seu parâmetro *pContextNode* . Esse método auxiliar retorna informações dos métodos a seguir.

-   [**IContextNode:: GetId**](icontextnode-getid.md)
-   [**IContextNode:: GetType**](icontextnode-gettype.md)
-   [**IContextNode:: getLocation**](icontextnode-getlocation.md)
-   **IContextNode::GetParentNode**


```C++
// Helper method for collecting information about a context node.
HRESULT CMyClass::GetNodeInformation(
    IContextNode *pContextNode,
    GUID *pNodeIdentifier,
    GUID *pContextNodeType,
    IAnalysisRegion **ppAnalysisRegion,
    IContextNode **ppParentNode,
    IContextNodes **ppSubNodes)
{
    // Get the identifier of the context node.
    HRESULT hr = pContextNode->GetId(pNodeIdentifier);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the type identifier for the context node.
    hr = pContextNode->GetType(pContextNodeType);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the location of the context node.
    hr = pContextNode->GetLocation(ppAnalysisRegion);

    if (FAILED(hr))
    {
        return hr;
    }

    // Get the parent node of the context node.
    hr = pContextNode->GetParentNode(ppParentNode);

    if (FAILED(hr))
    {
        if ((*ppAnalysisRegion) != NULL)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        return hr;
    }

    // Get the subnodes of the context node.
    hr = pContextNode->GetSubNodes(ppSubNodes);

    if (FAILED(hr))
    {
        if (*ppAnalysisRegion)
        {
            (*ppAnalysisRegion)->Release();
            (*ppAnalysisRegion) = NULL;
        }
        if (*ppParentNode)
        {
            (*ppParentNode)->Release();
            (*ppParentNode) = NULL;
        }
        return hr;
    }

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

