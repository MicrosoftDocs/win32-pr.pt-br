---
description: Recupera um resumo booliano dos resultados da operação de análise.
ms.assetid: 9bc690f4-fb5f-449e-bde0-bd2277c4573b
title: 'Método IAnalysisStatus:: issuccessfully (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.IsSuccessful
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: daf7ec801773d855f0ed85a795bc492ef673a74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296396"
---
# <a name="ianalysisstatusissuccessful-method"></a><span data-ttu-id="3a40b-103">Método IAnalysisStatus:: issuccessfully</span><span class="sxs-lookup"><span data-stu-id="3a40b-103">IAnalysisStatus::IsSuccessful method</span></span>

<span data-ttu-id="3a40b-104">Recupera um resumo booliano dos resultados da operação de análise.</span><span class="sxs-lookup"><span data-stu-id="3a40b-104">Retrieves a Boolean summary of the results of the analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a40b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a40b-105">Syntax</span></span>


```C++
HRESULT IsSuccessful(
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="3a40b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a40b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a40b-107">*pfSuccessful* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3a40b-107">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a40b-108">**Variante \_ TRUE** se a operação de análise for concluída sem avisos ou **Variant \_ false** se pelo menos um aviso tiver ocorrido.</span><span class="sxs-lookup"><span data-stu-id="3a40b-108">**VARIANT\_TRUE** if the analysis operation completed without any warnings, or **VARIANT\_FALSE** if at least one warning occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a40b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a40b-109">Return value</span></span>

<span data-ttu-id="3a40b-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3a40b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3a40b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3a40b-111">Examples</span></span>

<span data-ttu-id="3a40b-112">O exemplo a seguir mostra um contorno de um manipulador de eventos para o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="3a40b-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="3a40b-113">O manipulador verifica **IAnalysisStatus:: Issuccessfully**.</span><span class="sxs-lookup"><span data-stu-id="3a40b-113">The handler checks **IAnalysisStatus::IsSuccessful**.</span></span> <span data-ttu-id="3a40b-114">Se a operação de análise gerar avisos, o manipulador iterará pela coleção de objetos [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="3a40b-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3a40b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a40b-115">Requirements</span></span>



| <span data-ttu-id="3a40b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a40b-116">Requirement</span></span> | <span data-ttu-id="3a40b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3a40b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a40b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a40b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a40b-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3a40b-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3a40b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a40b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a40b-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3a40b-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3a40b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a40b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a40b-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3a40b-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3a40b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3a40b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a40b-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a40b-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3a40b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a40b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a40b-127">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="3a40b-127">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="3a40b-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="3a40b-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




