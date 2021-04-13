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
ms.openlocfilehash: 50bba716486910802e91cbe6d3f003d172f1cb29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501814"
---
# <a name="icontextnodegetparentnode-method"></a><span data-ttu-id="3c54c-103">Método IContextNode:: GetParentNode</span><span class="sxs-lookup"><span data-stu-id="3c54c-103">IContextNode::GetParentNode method</span></span>

<span data-ttu-id="3c54c-104">Recupera o nó pai desse [**IContextNode**](icontextnode.md) na árvore de nós de contexto.</span><span class="sxs-lookup"><span data-stu-id="3c54c-104">Retrieves the parent node of this [**IContextNode**](icontextnode.md) in the context node tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c54c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c54c-105">Syntax</span></span>


```C++
HRESULT GetParentNode(
  [out] IContextNode **ppParentContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="3c54c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c54c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c54c-107">*ppParentContextNode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3c54c-107">*ppParentContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c54c-108">Um ponteiro para o nó pai deste objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3c54c-108">A pointer to the parent node of this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c54c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c54c-109">Return value</span></span>

<span data-ttu-id="3c54c-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3c54c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c54c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c54c-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3c54c-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppParentContextNode* quando você não precisar mais usar o nó de contexto pai.</span><span class="sxs-lookup"><span data-stu-id="3c54c-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppParentContextNode* when you no longer need to use the parent context node.</span></span>

 

<span data-ttu-id="3c54c-113">Se esse for o nó raiz, o parâmetro *ppParentContextNode* será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3c54c-113">If this is the root node, the *ppParentContextNode* parameter is set to **NULL**.</span></span>

## <a name="examples"></a><span data-ttu-id="3c54c-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c54c-114">Examples</span></span>

<span data-ttu-id="3c54c-115">O exemplo a seguir mostra um método auxiliar que recupera informações sobre um nó especificado, seu parâmetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="3c54c-115">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="3c54c-116">Esse método auxiliar retorna informações dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="3c54c-116">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="3c54c-117">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="3c54c-117">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="3c54c-118">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="3c54c-118">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="3c54c-119">**IContextNode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="3c54c-119">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   <span data-ttu-id="3c54c-120">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="3c54c-120">**IContextNode::GetParentNode**</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3c54c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c54c-121">Requirements</span></span>



| <span data-ttu-id="3c54c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c54c-122">Requirement</span></span> | <span data-ttu-id="3c54c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3c54c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c54c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c54c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3c54c-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3c54c-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3c54c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c54c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3c54c-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3c54c-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3c54c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c54c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c54c-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3c54c-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c54c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3c54c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c54c-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c54c-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3c54c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c54c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c54c-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3c54c-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3c54c-134">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="3c54c-134">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="3c54c-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="3c54c-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

