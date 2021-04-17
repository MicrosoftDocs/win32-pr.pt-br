---
description: Obtém o número de traços associados ao objeto IContextNode.
ms.assetid: bb3c1cb3-dcf6-4465-b1bc-5c613e9747da
title: 'Método IContextNode:: GetStrokeCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2652168fa2846995aeb17ec23c194f908f22e5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461156"
---
# <a name="icontextnodegetstrokecount-method"></a><span data-ttu-id="b8d22-103">Método IContextNode:: GetStrokeCount</span><span class="sxs-lookup"><span data-stu-id="b8d22-103">IContextNode::GetStrokeCount method</span></span>

<span data-ttu-id="b8d22-104">Obtém o número de traços associados ao objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b8d22-104">Gets the number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8d22-105">Syntax</span></span>


```C++
HRESULT GetStrokeCount(
  [out] ULONG *pulStrokeCount
);
```



## <a name="parameters"></a><span data-ttu-id="b8d22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8d22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d22-107">*pulStrokeCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b8d22-107">*pulStrokeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8d22-108">O número de traços associados ao objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b8d22-108">The number of strokes associated with the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d22-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8d22-109">Return value</span></span>

<span data-ttu-id="b8d22-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b8d22-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d22-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8d22-111">Remarks</span></span>

<span data-ttu-id="b8d22-112">Somente nós de contexto de folha de tinta têm dados de traço associados (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="b8d22-112">Only ink leaf context nodes have associated stroke data (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="b8d22-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b8d22-113">Examples</span></span>

<span data-ttu-id="b8d22-114">Este exemplo mostra um método, `ExploreContextNode` , que examina um [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="b8d22-114">This example shows a method, `ExploreContextNode`, that examines an [**IContextNode**](icontextnode.md).</span></span> <span data-ttu-id="b8d22-115">O método faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b8d22-115">The method does the following:</span></span>

-   <span data-ttu-id="b8d22-116">Obtém o tipo do nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="b8d22-116">Gets the context node's type.</span></span>
-   <span data-ttu-id="b8d22-117">Examina as propriedades específicas do tipo de nó chamando um método auxiliar, se o nó de contexto for uma tinta não classificada, uma dica de análise ou um nó de reconhecedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="b8d22-117">Examines specific properties of the node type by calling a helper method, if the context node is an unclassified ink, analysis hint, or custom recognizer node.</span></span>
-   <span data-ttu-id="b8d22-118">Examina cada subnó chamando a si mesmo, se o nó tiver subnós.</span><span class="sxs-lookup"><span data-stu-id="b8d22-118">Examines each subnode by calling itself, if the node has subnodes.</span></span>
-   <span data-ttu-id="b8d22-119">Examina os dados de traço do nó chamando um método auxiliar, se o nó for um nó folha de tinta.</span><span class="sxs-lookup"><span data-stu-id="b8d22-119">Examines the stroke data for the node by calling a helper method, if the node is an ink leaf node.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b8d22-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8d22-120">Requirements</span></span>



| <span data-ttu-id="b8d22-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d22-121">Requirement</span></span> | <span data-ttu-id="b8d22-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b8d22-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d22-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8d22-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8d22-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b8d22-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b8d22-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8d22-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8d22-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b8d22-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b8d22-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8d22-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8d22-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8d22-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8d22-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b8d22-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8d22-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8d22-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b8d22-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8d22-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d22-132">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b8d22-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b8d22-133">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="b8d22-133">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="b8d22-134">**IContextNode:: getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="b8d22-134">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="b8d22-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b8d22-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




