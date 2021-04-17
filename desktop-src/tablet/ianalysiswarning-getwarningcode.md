---
description: Retorna o tipo de aviso que ocorreu usando a Enumeração AnalysisWarningCode.
ms.assetid: ec67a5ac-a7a2-4805-b9b5-915ea956d228
title: 'Método IAnalysisWarning:: GetWarningCode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetWarningCode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e129b410de9e8ca9e3944b6a371fe0cac673fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812014"
---
# <a name="ianalysiswarninggetwarningcode-method"></a><span data-ttu-id="24035-103">Método IAnalysisWarning:: GetWarningCode</span><span class="sxs-lookup"><span data-stu-id="24035-103">IAnalysisWarning::GetWarningCode method</span></span>

<span data-ttu-id="24035-104">Retorna o tipo de aviso que ocorreu usando a enumeração [**AnalysisWarningCode**](analysiswarningcode.md) .</span><span class="sxs-lookup"><span data-stu-id="24035-104">Returns the type of warning that occurred by using the [**AnalysisWarningCode**](analysiswarningcode.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="24035-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24035-105">Syntax</span></span>


```C++
HRESULT GetWarningCode(
  [out] AnalysisWarningCode *pWarningCode
);
```



## <a name="parameters"></a><span data-ttu-id="24035-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24035-107">*pWarningCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="24035-107">*pWarningCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24035-108">O tipo de aviso que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="24035-108">The type of warning that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24035-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24035-109">Return value</span></span>

<span data-ttu-id="24035-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="24035-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="24035-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="24035-111">Examples</span></span>

<span data-ttu-id="24035-112">O exemplo a seguir mostra um contorno de um manipulador de eventos para o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="24035-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="24035-113">O manipulador verifica [**IAnalysisStatus:: Issuccessfully**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="24035-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="24035-114">Se a operação de análise gerou avisos, o manipulador itera pela coleção de objetos [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="24035-114">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="24035-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24035-115">Requirements</span></span>



| <span data-ttu-id="24035-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="24035-116">Requirement</span></span> | <span data-ttu-id="24035-117">Valor</span><span class="sxs-lookup"><span data-stu-id="24035-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24035-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24035-118">Minimum supported client</span></span><br/> | <span data-ttu-id="24035-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="24035-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="24035-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24035-120">Minimum supported server</span></span><br/> | <span data-ttu-id="24035-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="24035-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="24035-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24035-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="24035-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="24035-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="24035-124">DLL</span><span class="sxs-lookup"><span data-stu-id="24035-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24035-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24035-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="24035-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="24035-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24035-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="24035-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="24035-128">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="24035-128">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="24035-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="24035-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

