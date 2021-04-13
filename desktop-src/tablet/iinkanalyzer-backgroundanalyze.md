---
description: Executa a análise de tinta assíncrona.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Método IInkAnalyzer:: BackgroundAnalyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501806"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a><span data-ttu-id="37f12-103">Método IInkAnalyzer:: BackgroundAnalyze</span><span class="sxs-lookup"><span data-stu-id="37f12-103">IInkAnalyzer::BackgroundAnalyze method</span></span>

<span data-ttu-id="37f12-104">Executa a análise de tinta assíncrona.</span><span class="sxs-lookup"><span data-stu-id="37f12-104">Performs asynchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="37f12-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37f12-105">Syntax</span></span>


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a><span data-ttu-id="37f12-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37f12-106">Parameters</span></span>

<span data-ttu-id="37f12-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37f12-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37f12-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37f12-108">Return value</span></span>

<span data-ttu-id="37f12-109">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="37f12-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37f12-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="37f12-110">Remarks</span></span>

<span data-ttu-id="37f12-111">Quando esse método é chamado, o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise de tinta em um thread em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="37f12-111">When this method is called, the [**IInkAnalyzer**](iinkanalyzer.md) performs the ink analysis on a background thread.</span></span>

<span data-ttu-id="37f12-112">Esse método retorna **S \_ false** e não inicia uma nova operação de análise em segundo plano nas seguintes circunstâncias.</span><span class="sxs-lookup"><span data-stu-id="37f12-112">This method returns **S\_FALSE** and does not start a new background analysis operation under the following circumstances.</span></span>

-   <span data-ttu-id="37f12-113">No momento, o [**IInkAnalyzer**](iinkanalyzer.md) está executando a análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="37f12-113">The [**IInkAnalyzer**](iinkanalyzer.md) is currently performing background analysis.</span></span>
-   <span data-ttu-id="37f12-114">a região suja (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) representa uma área vazia.</span><span class="sxs-lookup"><span data-stu-id="37f12-114">the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) represents an empty area.</span></span>

<span data-ttu-id="37f12-115">O [**IInkAnalyzer**](iinkanalyzer.md) analisa a tinta em sua região suja durante uma chamada para o método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou **IInkAnalyzer:: BackgroundAnalyze**.</span><span class="sxs-lookup"><span data-stu-id="37f12-115">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or **IInkAnalyzer::BackgroundAnalyze Method**.</span></span> <span data-ttu-id="37f12-116">No entanto, o **IInkAnalyzer** pode expandir a operação de análise para incluir regiões vizinhas.</span><span class="sxs-lookup"><span data-stu-id="37f12-116">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="37f12-117">Esse método define a região suja para uma região vazia.</span><span class="sxs-lookup"><span data-stu-id="37f12-117">This method sets the dirty region to an empty region.</span></span>

<span data-ttu-id="37f12-118">Se os dados de traço tiverem sido adicionados ao [**IInkAnalyzer**](iinkanalyzer.md) após a chamada para o **método IInkAnalyzer:: BackgroundAnalyze**, o **IInkAnalyzer** poderá atualizar a região suja durante a fase reconciliar da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="37f12-118">If stroke data was added to the [**IInkAnalyzer**](iinkanalyzer.md) after the call to **IInkAnalyzer::BackgroundAnalyze Method**, the **IInkAnalyzer** may update the dirty region during the reconcile phase of ink analysis.</span></span>

<span data-ttu-id="37f12-119">A configuração de modos de análise (consulte o [**método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)) especifica como o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="37f12-119">The analysis modes setting (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs background analysis.</span></span> <span data-ttu-id="37f12-120">Para obter mais informações sobre a análise de tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="37f12-120">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

<span data-ttu-id="37f12-121">Esse método retorna um código de erro sob as circunstâncias a seguir.</span><span class="sxs-lookup"><span data-stu-id="37f12-121">This method returns an error code under the following circumstances.</span></span>

-   <span data-ttu-id="37f12-122">Seu aplicativo definiu o valor de [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ IntermediateResults** no [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e não trata o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) .</span><span class="sxs-lookup"><span data-stu-id="37f12-122">Your application has set [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_IntermediateResults** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) event.</span></span>
-   <span data-ttu-id="37f12-123">Seu aplicativo limpou o valor de [**AnalysisModes**](analysismodes.md) **AnalysisModes \_ AutomaticReconciliation** no [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)) e não trata o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="37f12-123">Your application has cleared [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_AutomaticReconciliation** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>
-   <span data-ttu-id="37f12-124">Seu aplicativo não manipula o evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="37f12-124">Your application does not handle the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>
-   <span data-ttu-id="37f12-125">Seu aplicativo não manipula o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="37f12-125">Your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

## <a name="examples"></a><span data-ttu-id="37f12-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37f12-126">Examples</span></span>

<span data-ttu-id="37f12-127">O exemplo a seguir verifica a região suja do Ink Analyzer e inicia a análise de tinta em segundo plano se a região suja não estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="37f12-127">The following example checks the ink analyzer's dirty region, and then initiates background ink analysis if the dirty region is not empty.</span></span>


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



## <a name="requirements"></a><span data-ttu-id="37f12-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37f12-128">Requirements</span></span>



| <span data-ttu-id="37f12-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f12-129">Requirement</span></span> | <span data-ttu-id="37f12-130">Valor</span><span class="sxs-lookup"><span data-stu-id="37f12-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f12-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37f12-131">Minimum supported client</span></span><br/> | <span data-ttu-id="37f12-132">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="37f12-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="37f12-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37f12-133">Minimum supported server</span></span><br/> | <span data-ttu-id="37f12-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="37f12-134">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="37f12-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37f12-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f12-136"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="37f12-136"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37f12-137">DLL</span><span class="sxs-lookup"><span data-stu-id="37f12-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37f12-138"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37f12-138"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="37f12-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="37f12-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f12-140">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="37f12-140">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="37f12-141">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="37f12-141">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="37f12-142">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="37f12-142">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="37f12-143">**Método IInkAnalyzer:: GetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="37f12-143">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="37f12-144">**Método IInkAnalyzer:: SetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="37f12-144">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="37f12-145">**Método IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="37f12-145">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="37f12-146">**Método IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="37f12-146">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="37f12-147">**Método IInkAnalyzer:: GetRootNode**</span><span class="sxs-lookup"><span data-stu-id="37f12-147">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="37f12-148">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="37f12-148">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




