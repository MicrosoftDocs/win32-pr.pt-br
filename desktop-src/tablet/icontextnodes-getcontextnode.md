---
description: Recupera o objeto IContextNode no índice especificado dentro desta coleção.
ms.assetid: 4b266512-9e58-43d2-8430-68310230fc27
title: 'Método IContextNodes:: GetContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ec907fdcac5a1ed18cca54c79a876959868f2ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461154"
---
# <a name="icontextnodesgetcontextnode-method"></a><span data-ttu-id="21f28-103">Método IContextNodes:: GetContextNode</span><span class="sxs-lookup"><span data-stu-id="21f28-103">IContextNodes::GetContextNode method</span></span>

<span data-ttu-id="21f28-104">Recupera o objeto [**IContextNode**](icontextnode.md) no índice especificado dentro desta coleção.</span><span class="sxs-lookup"><span data-stu-id="21f28-104">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f28-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21f28-105">Syntax</span></span>


```C++
HRESULT GetContextNode(
  [in]  ULONG        ulIndex,
  [out] IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="21f28-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21f28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f28-107">*ulIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="21f28-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f28-108">O índice de base zero do objeto [**IContextNode**](icontextnode.md) a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="21f28-108">The zero-based index of the [**IContextNode**](icontextnode.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="21f28-109">*ppContextNode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="21f28-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21f28-110">Ponteiro para o [**IContextNode**](icontextnode.md) referenciado no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="21f28-110">Pointer to the [**IContextNode**](icontextnode.md) referenced at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f28-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21f28-111">Return value</span></span>

<span data-ttu-id="21f28-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="21f28-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="21f28-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="21f28-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="21f28-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextNode* quando você não precisar mais usar o nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="21f28-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNode* when you no longer need to use the context node.</span></span>

 

## <a name="examples"></a><span data-ttu-id="21f28-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21f28-115">Examples</span></span>

<span data-ttu-id="21f28-116">Este exemplo mostra um método, `ExploreContextNode` , que examina um [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="21f28-116">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="21f28-117">O método faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="21f28-117">The method does the following:</span></span>

-   <span data-ttu-id="21f28-118">Obtém o tipo do nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="21f28-118">Gets the context node's type.</span></span>
-   <span data-ttu-id="21f28-119">Examina as propriedades específicas do tipo de nó chamando um método auxiliar, se o nó de contexto for uma tinta não classificada, uma dica de análise ou um nó de reconhecedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="21f28-119">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="21f28-120">Examina cada subnó chamando a si mesmo, se o nó tiver subnós.</span><span class="sxs-lookup"><span data-stu-id="21f28-120">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="21f28-121">Examina os dados de traço do nó chamando um método auxiliar, se o nó for um nó folha de tinta.</span><span class="sxs-lookup"><span data-stu-id="21f28-121">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="21f28-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21f28-122">Requirements</span></span>



| <span data-ttu-id="21f28-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="21f28-123">Requirement</span></span> | <span data-ttu-id="21f28-124">Valor</span><span class="sxs-lookup"><span data-stu-id="21f28-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21f28-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21f28-125">Minimum supported client</span></span><br/> | <span data-ttu-id="21f28-126">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="21f28-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21f28-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21f28-127">Minimum supported server</span></span><br/> | <span data-ttu-id="21f28-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="21f28-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="21f28-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21f28-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="21f28-130"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="21f28-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="21f28-131">DLL</span><span class="sxs-lookup"><span data-stu-id="21f28-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21f28-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21f28-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="21f28-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="21f28-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f28-134">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="21f28-134">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="21f28-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="21f28-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

