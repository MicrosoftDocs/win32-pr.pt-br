---
description: Representa um aviso ou erro que ocorre durante uma operação de análise de tinta.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Interface IAnalysisWarning (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090554"
---
# <a name="ianalysiswarning-interface"></a><span data-ttu-id="0b4a7-103">Interface IAnalysisWarning</span><span class="sxs-lookup"><span data-stu-id="0b4a7-103">IAnalysisWarning interface</span></span>

<span data-ttu-id="0b4a7-104">Representa um aviso ou erro que ocorre durante uma operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="0b4a7-104">Represents a warning or error that occurs during an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="0b4a7-105">Membros</span><span class="sxs-lookup"><span data-stu-id="0b4a7-105">Members</span></span>

<span data-ttu-id="0b4a7-106">A interface **IAnalysisWarning** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0b4a7-106">The **IAnalysisWarning** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0b4a7-107">**IAnalysisWarning** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0b4a7-107">**IAnalysisWarning** also has these types of members:</span></span>

-   [<span data-ttu-id="0b4a7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b4a7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0b4a7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b4a7-109">Methods</span></span>

<span data-ttu-id="0b4a7-110">A interface **IAnalysisWarning** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0b4a7-110">The **IAnalysisWarning** interface has these methods.</span></span>



| <span data-ttu-id="0b4a7-111">Método</span><span class="sxs-lookup"><span data-stu-id="0b4a7-111">Method</span></span>                                                            | <span data-ttu-id="0b4a7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b4a7-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b4a7-113">**GetBackgroundError**</span><span class="sxs-lookup"><span data-stu-id="0b4a7-113">**GetBackgroundError**</span></span>](ianalysiswarning-getbackgrounderror.md) | <span data-ttu-id="0b4a7-114">Recupera o código de erro para a operação de análise de tinta em segundo plano se ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="0b4a7-114">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span><br/>                                    |
| [<span data-ttu-id="0b4a7-115">**Gethint**</span><span class="sxs-lookup"><span data-stu-id="0b4a7-115">**GetHint**</span></span>](ianalysiswarning-gethint.md)                       | <span data-ttu-id="0b4a7-116">Recupera a dica de análise que causou este aviso</span><span class="sxs-lookup"><span data-stu-id="0b4a7-116">Retrieves the analysis hint that caused this warning</span></span><br/>                                                                        |
| [<span data-ttu-id="0b4a7-117">**GetNodeIds**</span><span class="sxs-lookup"><span data-stu-id="0b4a7-117">**GetNodeIds**</span></span>](ianalysiswarning-getnodeids.md)                 | <span data-ttu-id="0b4a7-118">Recupera os identificadores de todos os nós de contexto relevantes associados a este aviso.</span><span class="sxs-lookup"><span data-stu-id="0b4a7-118">Retrieves the identifiers of any relevant context nodes that are associated with this warning.</span></span><br/>                              |
| [<span data-ttu-id="0b4a7-119">**GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="0b4a7-119">**GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)         | <span data-ttu-id="0b4a7-120">Recupera o tipo de aviso que ocorreu usando a enumeração [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="0b4a7-120">Retrieves the type of warning that occurred by using the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b4a7-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b4a7-121">Remarks</span></span>

<span data-ttu-id="0b4a7-122">Os tipos de avisos que podem ocorrer são descritos pela enumeração [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="0b4a7-122">The types of warnings that can occur are described by the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span> <span data-ttu-id="0b4a7-123">Geralmente, os avisos ocorrem quando você tenta usar um recurso que não é suportado pelo [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que o [**IInkAnalyzer**](iinkanalyzer.md) está usando.</span><span class="sxs-lookup"><span data-stu-id="0b4a7-123">Often warnings occur when you try to use a feature that is not supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that the [**IInkAnalyzer**](iinkanalyzer.md) is using.</span></span>

<span data-ttu-id="0b4a7-124">Alguns avisos indicam que o [**IInkAnalyzer**](iinkanalyzer.md) não concluiu a operação de análise.</span><span class="sxs-lookup"><span data-stu-id="0b4a7-124">Some warnings indicate that the [**IInkAnalyzer**](iinkanalyzer.md) did not complete the analysis operation.</span></span> <span data-ttu-id="0b4a7-125">Para obter mais informações, consulte [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span><span class="sxs-lookup"><span data-stu-id="0b4a7-125">For more information, see [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span></span>

## <a name="examples"></a><span data-ttu-id="0b4a7-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b4a7-126">Examples</span></span>

<span data-ttu-id="0b4a7-127">O exemplo a seguir mostra um contorno de um manipulador de eventos para o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="0b4a7-127">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="0b4a7-128">O manipulador verifica [**IAnalysisStatus:: Issuccessfully**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="0b4a7-128">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="0b4a7-129">Se a operação de análise gerar avisos, o manipulador iterará pela coleção de objetos **IAnalysisWarning** .</span><span class="sxs-lookup"><span data-stu-id="0b4a7-129">If the analysis operation generates warnings, the handler iterates through the collection of **IAnalysisWarning** objects.</span></span>


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0b4a7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b4a7-130">Requirements</span></span>



| <span data-ttu-id="0b4a7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b4a7-131">Requirement</span></span> | <span data-ttu-id="0b4a7-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0b4a7-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4a7-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b4a7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0b4a7-134">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0b4a7-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0b4a7-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b4a7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0b4a7-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0b4a7-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0b4a7-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b4a7-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b4a7-138"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0b4a7-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0b4a7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0b4a7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b4a7-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b4a7-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0b4a7-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b4a7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4a7-142">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="0b4a7-142">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="0b4a7-143">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="0b4a7-143">**AnalysisWarningCode**</span></span>](analysiswarningcode.md)
</dt> <dt>

[<span data-ttu-id="0b4a7-144">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="0b4a7-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

