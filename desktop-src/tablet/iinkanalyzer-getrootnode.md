---
description: Obtém a IContextNode raiz da árvore de contexto do objeto IInkAnalyzer.
ms.assetid: 6c073952-7962-4f38-89ae-f543e64e904f
title: 'Método IInkAnalyzer:: GetRootNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRootNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 280c1907558372d247f25a0f760990d7c3c53a07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796101"
---
# <a name="iinkanalyzergetrootnode-method"></a><span data-ttu-id="38e89-103">Método IInkAnalyzer:: GetRootNode</span><span class="sxs-lookup"><span data-stu-id="38e89-103">IInkAnalyzer::GetRootNode method</span></span>

<span data-ttu-id="38e89-104">Obtém a [**IContextNode**](icontextnode.md) raiz da árvore de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="38e89-104">Gets the root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38e89-105">Syntax</span></span>


```C++
HRESULT GetRootNode(
  [out] IContextNode **ppRootNode
);
```



## <a name="parameters"></a><span data-ttu-id="38e89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38e89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38e89-107">*ppRootNode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38e89-107">*ppRootNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38e89-108">O [**IContextNode**](icontextnode.md) raiz da árvore de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="38e89-108">The root [**IContextNode**](icontextnode.md) of the [**IInkAnalyzer**](iinkanalyzer.md) object's context tree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38e89-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38e89-109">Return value</span></span>

<span data-ttu-id="38e89-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="38e89-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="38e89-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="38e89-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="38e89-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppRootNode* quando você não precisar mais usar o nó raiz.</span><span class="sxs-lookup"><span data-stu-id="38e89-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppRootNode* when you no longer need to use the root node.</span></span>

 

<span data-ttu-id="38e89-113">O [**IInkAnalyzer**](iinkanalyzer.md) mantém uma árvore de objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="38e89-113">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a tree of [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="38e89-114">Esses objetos contêm a entrada para análise e os resultados da análise.</span><span class="sxs-lookup"><span data-stu-id="38e89-114">These objects contain both input for analysis and the results of analysis.</span></span> <span data-ttu-id="38e89-115">Quando os traços são adicionados inicialmente ao **IInkAnalyzer**, o **IInkAnalyzer** os atribui a um **IContextNode** do tipo UnclassifiedInk (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e tipos de [nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="38e89-115">When strokes are initially added to the **IInkAnalyzer**, the **IInkAnalyzer** assigns them to a **IContextNode** of type UnclassifiedInk (See [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="38e89-116">Depois que os traços são analisados, o **IInkAnalyzer** os atribui aos objetos **IContextNode** apropriados na árvore.</span><span class="sxs-lookup"><span data-stu-id="38e89-116">After the strokes are analyzed, the **IInkAnalyzer** assigns them to appropriate **IContextNode** objects in the tree.</span></span> <span data-ttu-id="38e89-117">Para obter mais informações sobre como usar o **IInkAnalyzer** para analisar a tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="38e89-117">For more information about using the **IInkAnalyzer** to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="38e89-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38e89-118">Examples</span></span>

<span data-ttu-id="38e89-119">O exemplo a seguir mostra um método que percorre a árvore de resultados do [**IContextNode**](icontextnode.md) do Ink Analyzer.</span><span class="sxs-lookup"><span data-stu-id="38e89-119">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="38e89-120">Se o IInkAnlyzer não estiver executando a análise de tinta no momento, o método fará o seguinte.</span><span class="sxs-lookup"><span data-stu-id="38e89-120">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="38e89-121">Obtém a cadeia de caracteres de reconhecimento superior.</span><span class="sxs-lookup"><span data-stu-id="38e89-121">Gets the top recognition string.</span></span>
-   <span data-ttu-id="38e89-122">Obtém o nó raiz do analisador de tinta.</span><span class="sxs-lookup"><span data-stu-id="38e89-122">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="38e89-123">Chama um método auxiliar, `ExploreContextNode` , para examinar o nó raiz e seus nós filho.</span><span class="sxs-lookup"><span data-stu-id="38e89-123">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="38e89-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38e89-124">Requirements</span></span>



| <span data-ttu-id="38e89-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="38e89-125">Requirement</span></span> | <span data-ttu-id="38e89-126">Valor</span><span class="sxs-lookup"><span data-stu-id="38e89-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e89-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38e89-127">Minimum supported client</span></span><br/> | <span data-ttu-id="38e89-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="38e89-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="38e89-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38e89-129">Minimum supported server</span></span><br/> | <span data-ttu-id="38e89-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="38e89-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="38e89-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38e89-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="38e89-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="38e89-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="38e89-133">DLL</span><span class="sxs-lookup"><span data-stu-id="38e89-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38e89-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38e89-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="38e89-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="38e89-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e89-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="38e89-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="38e89-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="38e89-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="38e89-138">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="38e89-138">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="38e89-139">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="38e89-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

