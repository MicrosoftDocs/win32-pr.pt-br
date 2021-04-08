---
description: Recupera o objeto IAnalysisWarning no índice especificado.
ms.assetid: 8f5d5642-73ec-496e-bad7-9f636fc00217
title: 'Método IAnalysisWarnings:: GetAnalysisWarning (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 88ed3686ecf3861a2b097ebfc005214ab0cdd1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010529"
---
# <a name="ianalysiswarningsgetanalysiswarning-method"></a><span data-ttu-id="8a04b-103">Método IAnalysisWarnings:: GetAnalysisWarning</span><span class="sxs-lookup"><span data-stu-id="8a04b-103">IAnalysisWarnings::GetAnalysisWarning method</span></span>

<span data-ttu-id="8a04b-104">Recupera o objeto [**IAnalysisWarning**](ianalysiswarning.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8a04b-104">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a04b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a04b-105">Syntax</span></span>


```C++
HRESULT GetAnalysisWarning(
  [in]  ULONG            ulIndex,
  [out] IAnalysisWarning **ppWarning
);
```



## <a name="parameters"></a><span data-ttu-id="8a04b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a04b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a04b-107">*ulIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a04b-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a04b-108">O índice de base zero do objeto [**IAnalysisWarning**](ianalysiswarning.md) a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="8a04b-108">The zero-based index of the [**IAnalysisWarning**](ianalysiswarning.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="8a04b-109">*ppWarning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8a04b-109">*ppWarning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a04b-110">Um ponteiro para o objeto [**IAnalysisWarning**](ianalysiswarning.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8a04b-110">A pointer to the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a04b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a04b-111">Return value</span></span>

<span data-ttu-id="8a04b-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8a04b-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a04b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a04b-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8a04b-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppWarning* quando você não precisar mais usar o aviso.</span><span class="sxs-lookup"><span data-stu-id="8a04b-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppWarning* when you no longer need to use the warning.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8a04b-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a04b-115">Examples</span></span>

<span data-ttu-id="8a04b-116">O exemplo a seguir mostra um contorno de um manipulador de eventos para o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="8a04b-116">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="8a04b-117">O manipulador verifica [**IAnalysisStatus:: Issuccessfully**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="8a04b-117">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="8a04b-118">Se a operação de análise gerar avisos, o manipulador iterará pela coleção de objetos [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="8a04b-118">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8a04b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a04b-119">Requirements</span></span>



| <span data-ttu-id="8a04b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a04b-120">Requirement</span></span> | <span data-ttu-id="8a04b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8a04b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a04b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a04b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8a04b-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8a04b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a04b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a04b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8a04b-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8a04b-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a04b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a04b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a04b-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8a04b-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a04b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8a04b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a04b-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a04b-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a04b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a04b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a04b-131">**IAnalysisWarnings**</span><span class="sxs-lookup"><span data-stu-id="8a04b-131">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="8a04b-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="8a04b-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

