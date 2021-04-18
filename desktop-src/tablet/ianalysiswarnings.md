---
description: Contém uma coleção de objetos que implementam a interface IAnalysisWarning e que são o resultado de uma operação de análise de tinta.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: Interface IAnalysisWarnings (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781242"
---
# <a name="ianalysiswarnings-interface"></a><span data-ttu-id="7d9d4-103">Interface IAnalysisWarnings</span><span class="sxs-lookup"><span data-stu-id="7d9d4-103">IAnalysisWarnings interface</span></span>

<span data-ttu-id="7d9d4-104">Contém uma coleção de objetos que implementam a interface [**IAnalysisWarning**](ianalysiswarning.md) e que são o resultado de uma operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="7d9d4-104">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="7d9d4-105">Membros</span><span class="sxs-lookup"><span data-stu-id="7d9d4-105">Members</span></span>

<span data-ttu-id="7d9d4-106">A interface **IAnalysisWarnings** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7d9d4-106">The **IAnalysisWarnings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7d9d4-107">**IAnalysisWarnings** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7d9d4-107">**IAnalysisWarnings** also has these types of members:</span></span>

-   [<span data-ttu-id="7d9d4-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7d9d4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7d9d4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7d9d4-109">Methods</span></span>

<span data-ttu-id="7d9d4-110">A interface **IAnalysisWarnings** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7d9d4-110">The **IAnalysisWarnings** interface has these methods.</span></span>



| <span data-ttu-id="7d9d4-111">Método</span><span class="sxs-lookup"><span data-stu-id="7d9d4-111">Method</span></span>                                                             | <span data-ttu-id="7d9d4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d9d4-112">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d9d4-113">**GetAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="7d9d4-113">**GetAnalysisWarning**</span></span>](ianalysiswarnings-getanalysiswarning.md) | <span data-ttu-id="7d9d4-114">Recupera o objeto [**IAnalysisWarning**](ianalysiswarning.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7d9d4-114">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span><br/>                                       |
| [<span data-ttu-id="7d9d4-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="7d9d4-115">**GetCount**</span></span>](ianalysiswarnings-getcount.md)                     | <span data-ttu-id="7d9d4-116">Recupera o número de objetos [**IAnalysisWarning**](ianalysiswarning.md) contidos na coleção **IAnalysisWarnings** .</span><span class="sxs-lookup"><span data-stu-id="7d9d4-116">Retrieves the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the **IAnalysisWarnings** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="7d9d4-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7d9d4-117">Examples</span></span>

<span data-ttu-id="7d9d4-118">O exemplo a seguir mostra um contorno de um manipulador de eventos para o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="7d9d4-118">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="7d9d4-119">O manipulador verifica [**IAnalysisStatus:: Issuccessfully**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="7d9d4-119">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="7d9d4-120">Se a operação de análise gerou avisos, o manipulador itera pela coleção de objetos [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="7d9d4-120">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7d9d4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d9d4-121">Requirements</span></span>



| <span data-ttu-id="7d9d4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d9d4-122">Requirement</span></span> | <span data-ttu-id="7d9d4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7d9d4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d9d4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9d4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d9d4-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7d9d4-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7d9d4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d9d4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d9d4-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7d9d4-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7d9d4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d9d4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d9d4-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7d9d4-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7d9d4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7d9d4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d9d4-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d9d4-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7d9d4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d9d4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d9d4-133">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="7d9d4-133">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="7d9d4-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="7d9d4-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="7d9d4-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="7d9d4-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

