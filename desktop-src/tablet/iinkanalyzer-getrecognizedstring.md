---
description: Recupera a cadeia de caracteres de melhor resultado da operação de reconhecimento para toda a árvore de nós de contexto no IInkAnalyzer.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'Método IInkAnalyzer:: reconhecívelstring (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647226"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a><span data-ttu-id="be0ca-103">Método IInkAnalyzer:: reconhecívelstring</span><span class="sxs-lookup"><span data-stu-id="be0ca-103">IInkAnalyzer::GetRecognizedString method</span></span>

<span data-ttu-id="be0ca-104">Recupera a cadeia de caracteres de melhor resultado da operação de reconhecimento para toda a árvore de nós de contexto no [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="be0ca-104">Retrieves the best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="be0ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be0ca-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="be0ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be0ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be0ca-107">*pbstrRecognizedString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="be0ca-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be0ca-108">A cadeia de caracteres de resultado máximo da operação de reconhecimento para toda a árvore de nós de contexto no [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="be0ca-108">The best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be0ca-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be0ca-109">Return value</span></span>

<span data-ttu-id="be0ca-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="be0ca-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be0ca-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="be0ca-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="be0ca-112">Para evitar um vazamento de memória, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para *pbstrRecognizedString* quando você não precisar mais usar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="be0ca-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) for *pbstrRecognizedString* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="be0ca-113">Esse método retorna o mesmo valor que os dados de Propriedade do nó raiz para a cadeia de caracteres reconhecida.</span><span class="sxs-lookup"><span data-stu-id="be0ca-113">This method returns the same value as the root node's property data for the recognized string.</span></span> <span data-ttu-id="be0ca-114">(Consulte [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)e [Propriedades de nó de contexto](context-node-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="be0ca-114">(See [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md), and [Context Node Properties](context-node-properties.md).)</span></span>

## <a name="examples"></a><span data-ttu-id="be0ca-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be0ca-115">Examples</span></span>

<span data-ttu-id="be0ca-116">O exemplo a seguir mostra um método que percorre a árvore de resultados do [**IContextNode**](icontextnode.md) do Ink Analyzer.</span><span class="sxs-lookup"><span data-stu-id="be0ca-116">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="be0ca-117">Se o IInkAnlyzer não estiver executando a análise de tinta no momento, o método fará o seguinte.</span><span class="sxs-lookup"><span data-stu-id="be0ca-117">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="be0ca-118">Obtém a cadeia de caracteres de reconhecimento superior.</span><span class="sxs-lookup"><span data-stu-id="be0ca-118">Gets the top recognition string.</span></span>
-   <span data-ttu-id="be0ca-119">Obtém o nó raiz do analisador de tinta.</span><span class="sxs-lookup"><span data-stu-id="be0ca-119">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="be0ca-120">Chama um método auxiliar, `ExploreContextNode` , para examinar o nó raiz e seus nós filho.</span><span class="sxs-lookup"><span data-stu-id="be0ca-120">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="be0ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be0ca-121">Requirements</span></span>



| <span data-ttu-id="be0ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="be0ca-122">Requirement</span></span> | <span data-ttu-id="be0ca-123">Valor</span><span class="sxs-lookup"><span data-stu-id="be0ca-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be0ca-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be0ca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be0ca-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be0ca-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be0ca-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be0ca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be0ca-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="be0ca-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be0ca-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be0ca-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be0ca-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be0ca-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be0ca-130">DLL</span><span class="sxs-lookup"><span data-stu-id="be0ca-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be0ca-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be0ca-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be0ca-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="be0ca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be0ca-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="be0ca-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="be0ca-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="be0ca-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

