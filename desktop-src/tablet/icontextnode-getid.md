---
description: Recupera o identificador para o objeto IContextNode.
ms.assetid: 7578bcc1-7c69-45fc-b3c2-7350ce4df99c
title: 'Método IContextNode:: GetId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ef316111c7464bac0339a4888b887bc5cf20b93f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827189"
---
# <a name="icontextnodegetid-method"></a><span data-ttu-id="e429b-103">Método IContextNode:: GetId</span><span class="sxs-lookup"><span data-stu-id="e429b-103">IContextNode::GetId method</span></span>

<span data-ttu-id="e429b-104">Recupera o identificador para o objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="e429b-104">Retrieves the identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e429b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e429b-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="e429b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e429b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e429b-107">*pid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e429b-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e429b-108">O identificador do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="e429b-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e429b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e429b-109">Return value</span></span>

<span data-ttu-id="e429b-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e429b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e429b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e429b-111">Remarks</span></span>

<span data-ttu-id="e429b-112">O analisador de tinta atribui um identificador exclusivo a todos os nós de contexto que ele cria.</span><span class="sxs-lookup"><span data-stu-id="e429b-112">The ink analyzer assigns a unique identifier to all context nodes it creates.</span></span> <span data-ttu-id="e429b-113">Durante a análise de tinta, o analisador de tinta pode alterar o identificador de um nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="e429b-113">During ink analysis, the ink analyzer may change the identifier for a context node.</span></span> <span data-ttu-id="e429b-114">Por exemplo, o analisador de tinta pode reclassificar um nó de palavra como dois nós de palavra e, em seguida, atribuir o identificador original a um e um novo identificador para o outro.</span><span class="sxs-lookup"><span data-stu-id="e429b-114">For example, the ink analyzer may reclassify one word node as two word nodes and then assign the original identifier to one and a new identifier to the other.</span></span> <span data-ttu-id="e429b-115">Ou o analisador de tinta pode reclassificar dois nós de Word como um nó de palavra e atribuir um dos identificadores originais ao novo nó de palavra.</span><span class="sxs-lookup"><span data-stu-id="e429b-115">Or, the ink analyzer may reclassify two word nodes as one word node and assign one of the original identifiers to the new word node.</span></span>

## <a name="examples"></a><span data-ttu-id="e429b-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e429b-116">Examples</span></span>

<span data-ttu-id="e429b-117">O exemplo a seguir mostra um método auxiliar que recupera informações sobre um nó especificado, seu parâmetro *pContextNode* .</span><span class="sxs-lookup"><span data-stu-id="e429b-117">The following example shows a helper method that retrieves information about a specified node, its *pContextNode* parameter.</span></span> <span data-ttu-id="e429b-118">Esse método auxiliar retorna informações dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e429b-118">This helper method returns information from the following methods.</span></span>

-   <span data-ttu-id="e429b-119">**IContextNode:: GetId**</span><span class="sxs-lookup"><span data-stu-id="e429b-119">**IContextNode::GetId**</span></span>
-   [<span data-ttu-id="e429b-120">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="e429b-120">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
-   [<span data-ttu-id="e429b-121">**IContextNode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="e429b-121">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
-   [<span data-ttu-id="e429b-122">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="e429b-122">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)


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



## <a name="requirements"></a><span data-ttu-id="e429b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e429b-123">Requirements</span></span>



| <span data-ttu-id="e429b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e429b-124">Requirement</span></span> | <span data-ttu-id="e429b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e429b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e429b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e429b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e429b-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e429b-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e429b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e429b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e429b-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e429b-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e429b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e429b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e429b-131"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e429b-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e429b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e429b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e429b-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e429b-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e429b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e429b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e429b-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e429b-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e429b-136">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="e429b-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




