---
description: Recupera a posição e o tamanho do objeto IContextNode.
ms.assetid: 40787a9b-1017-4209-aec8-09b7332bfa8a
title: 'Método IContextNode:: getLocation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13366442399961eaba7a411b1b3c87171f0879b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814465"
---
# <a name="icontextnodegetlocation-method"></a><span data-ttu-id="222c2-103">Método IContextNode:: getLocation</span><span class="sxs-lookup"><span data-stu-id="222c2-103">IContextNode::GetLocation method</span></span>

<span data-ttu-id="222c2-104">Recupera a posição e o tamanho do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="222c2-104">Retrieves the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="222c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="222c2-105">Syntax</span></span>


```C++
HRESULT GetLocation(
  [out] IAnalysisRegion **ppIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="222c2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="222c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="222c2-107">*ppIAnalysisRegion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="222c2-107">*ppIAnalysisRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="222c2-108">Um ponteiro para a posição e o tamanho do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="222c2-108">A pointer to the position and size of the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="222c2-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="222c2-109">Return value</span></span>

<span data-ttu-id="222c2-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="222c2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="222c2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="222c2-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="222c2-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppIAnalysisRegion* quando você não precisar mais usar a região de análise.</span><span class="sxs-lookup"><span data-stu-id="222c2-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppIAnalysisRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="222c2-113">O local de um nó de contêiner é determinado pela localização da União de todos os locais de folha.</span><span class="sxs-lookup"><span data-stu-id="222c2-113">The location for a container node is determined by finding the union of all the leaf's locations.</span></span> <span data-ttu-id="222c2-114">O local de um nó folha de tinta é determinado pela localização da União da caixa delimitadora dos traços associados.</span><span class="sxs-lookup"><span data-stu-id="222c2-114">The location for an ink leaf node is determined by finding the union of the bounding box of the associated strokes.</span></span> <span data-ttu-id="222c2-115">O local de um nó folha que não é de tinta é definido quando o nó é criado e pode ser atualizado usando [**IContextNode:: SetLocation**](icontextnode-setlocation.md).</span><span class="sxs-lookup"><span data-stu-id="222c2-115">The location for a non-ink leaf node is set when the node is created and can be updated using [**IContextNode::SetLocation**](icontextnode-setlocation.md).</span></span>

## <a name="examples"></a><span data-ttu-id="222c2-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="222c2-116">Examples</span></span>

<span data-ttu-id="222c2-117">O exemplo a seguir mostra um método auxiliar que recupera informações sobre um nó especificado, seu parâmetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="222c2-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="222c2-118">Esse método auxiliar retorna informações dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="222c2-118">This helper method returns information from the following methods.</span></span>

-   [<span data-ttu-id="222c2-119">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="222c2-119">**IContextNode::GetId**</span></span>](icontextnode-getid.md)
-   [<span data-ttu-id="222c2-120">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="222c2-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   <span data-ttu-id="222c2-121">**IContextNode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="222c2-121">**IContextNode::GetLocation**</span></span>
-   [<span data-ttu-id="222c2-122">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="222c2-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="222c2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="222c2-123">Requirements</span></span>



| <span data-ttu-id="222c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="222c2-124">Requirement</span></span> | <span data-ttu-id="222c2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="222c2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="222c2-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="222c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="222c2-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="222c2-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="222c2-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="222c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="222c2-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="222c2-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="222c2-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="222c2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="222c2-131"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="222c2-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="222c2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="222c2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="222c2-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="222c2-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="222c2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="222c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222c2-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="222c2-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="222c2-136">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="222c2-136">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="222c2-137">**IContextNode:: SetLocation**</span><span class="sxs-lookup"><span data-stu-id="222c2-137">**IContextNode::SetLocation**</span></span>](icontextnode-setlocation.md)
</dt> <dt>

[<span data-ttu-id="222c2-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="222c2-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

