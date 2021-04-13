---
description: Recupera um valor que indica se o IInkAnalyzer está executando a análise de tinta.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'Método IInkAnalyzer:: isanalisáion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501801"
---
# <a name="iinkanalyzerisanalyzing-method"></a><span data-ttu-id="3991e-103">Método IInkAnalyzer:: isanalization</span><span class="sxs-lookup"><span data-stu-id="3991e-103">IInkAnalyzer::IsAnalyzing method</span></span>

<span data-ttu-id="3991e-104">Recupera um valor que indica se o [**IInkAnalyzer**](iinkanalyzer.md) está executando a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="3991e-104">Retrieves a value indicating whether the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="3991e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3991e-105">Syntax</span></span>


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a><span data-ttu-id="3991e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3991e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3991e-107">*pbAnalyzing* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3991e-107">*pbAnalyzing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3991e-108">**Variante \_ TRUE** se o [**IInkAnalyzer**](iinkanalyzer.md) estiver executando a análise de tinta; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="3991e-108">**VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3991e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3991e-109">Return value</span></span>

<span data-ttu-id="3991e-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3991e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3991e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3991e-111">Remarks</span></span>

<span data-ttu-id="3991e-112">Essa propriedade será **Variant \_ true** se o [**IInkAnalyzer**](iinkanalyzer.md) estiver executando a análise síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3991e-112">This property is **VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing synchronous or asynchronous analysis.</span></span>

## <a name="examples"></a><span data-ttu-id="3991e-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3991e-113">Examples</span></span>

<span data-ttu-id="3991e-114">O exemplo a seguir mostra um método que percorre a árvore de resultados do [**IContextNode**](icontextnode.md) do Ink Analyzer.</span><span class="sxs-lookup"><span data-stu-id="3991e-114">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="3991e-115">Se o Ink Analyzer não estiver executando a análise de tinta no momento, o método fará o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3991e-115">If the ink analyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="3991e-116">Obtém a cadeia de caracteres de reconhecimento superior.</span><span class="sxs-lookup"><span data-stu-id="3991e-116">Gets the top recognition string.</span></span>
-   <span data-ttu-id="3991e-117">Obtém o nó raiz do analisador de tinta.</span><span class="sxs-lookup"><span data-stu-id="3991e-117">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="3991e-118">Chama um método auxiliar, `ExploreContextNode` , para examinar o nó raiz e seus nós filho.</span><span class="sxs-lookup"><span data-stu-id="3991e-118">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3991e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3991e-119">Requirements</span></span>



| <span data-ttu-id="3991e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3991e-120">Requirement</span></span> | <span data-ttu-id="3991e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3991e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3991e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3991e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3991e-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3991e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3991e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3991e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3991e-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3991e-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3991e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3991e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3991e-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3991e-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3991e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3991e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3991e-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3991e-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3991e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3991e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3991e-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3991e-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3991e-132">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="3991e-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="3991e-133">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="3991e-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="3991e-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="3991e-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




