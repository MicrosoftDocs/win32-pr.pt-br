---
description: Recupera o tipo do objeto IContextNode.
ms.assetid: 285384ce-5cdc-47f5-a1c4-6c6d7f18e215
title: 'Método IContextNode:: GetType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 68b657d9acd6f25f7c067e339ec42c6994a34c48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090543"
---
# <a name="icontextnodegettype-method"></a><span data-ttu-id="4f133-103">Método IContextNode:: GetType</span><span class="sxs-lookup"><span data-stu-id="4f133-103">IContextNode::GetType method</span></span>

<span data-ttu-id="4f133-104">Recupera o tipo do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="4f133-104">Retrieves the type of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f133-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f133-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] GUID *pContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="4f133-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f133-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f133-107">*pContextNodeType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4f133-107">*pContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f133-108">O tipo do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="4f133-108">The type of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f133-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f133-109">Return value</span></span>

<span data-ttu-id="4f133-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4f133-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f133-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f133-111">Remarks</span></span>

<span data-ttu-id="4f133-112">Os tipos de nós são descritos nas constantes de [tipos de nó de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="4f133-112">Types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="4f133-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f133-113">Examples</span></span>

<span data-ttu-id="4f133-114">O exemplo a seguir mostra um método auxiliar que recupera informações sobre um nó especificado, seu parâmetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="4f133-114">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="4f133-115">Esse método auxiliar retorna informações dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f133-115">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="4f133-116">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="4f133-116">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   <span data-ttu-id="4f133-117">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="4f133-117">**IContextNode::GetType**</span></span>
-   [<span data-ttu-id="4f133-118">**IContextNode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="4f133-118">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="4f133-119">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="4f133-119">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="4f133-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f133-120">Requirements</span></span>



| <span data-ttu-id="4f133-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f133-121">Requirement</span></span> | <span data-ttu-id="4f133-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4f133-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f133-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f133-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4f133-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4f133-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f133-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f133-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4f133-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4f133-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4f133-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f133-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f133-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4f133-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4f133-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4f133-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f133-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f133-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4f133-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f133-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f133-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4f133-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4f133-133">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="4f133-133">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="4f133-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="4f133-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




