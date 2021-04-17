---
description: Executa a análise de tinta síncrona.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Método IInkAnalyzer:: Analyze (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768282"
---
# <a name="iinkanalyzeranalyze-method"></a><span data-ttu-id="bc215-103">Método IInkAnalyzer:: Analyze</span><span class="sxs-lookup"><span data-stu-id="bc215-103">IInkAnalyzer::Analyze method</span></span>

<span data-ttu-id="bc215-104">Executa a análise de tinta síncrona.</span><span class="sxs-lookup"><span data-stu-id="bc215-104">Performs synchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc215-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc215-105">Syntax</span></span>


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a><span data-ttu-id="bc215-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc215-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc215-107">*ppStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bc215-107">*ppStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc215-108">Um ponteiro para um [**IAnalysisStatus**](ianalysisstatus.md) que descreve o status da operação de análise.</span><span class="sxs-lookup"><span data-stu-id="bc215-108">A pointer to an [**IAnalysisStatus**](ianalysisstatus.md) that describes the status of the analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc215-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc215-109">Return value</span></span>

<span data-ttu-id="bc215-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bc215-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc215-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc215-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="bc215-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppStatus* quando você não precisar mais usar o status da análise.</span><span class="sxs-lookup"><span data-stu-id="bc215-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppStatus* when you no longer need to use the analysis status.</span></span>

 

<span data-ttu-id="bc215-113">Esse método inicia uma operação de análise de tinta síncrona.</span><span class="sxs-lookup"><span data-stu-id="bc215-113">This method starts a synchronous ink analysis operation.</span></span> <span data-ttu-id="bc215-114">A análise de tinta inclui análise de layout, gravação e classificação de desenho e reconhecimento de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="bc215-114">Ink analysis includes layout analysis, writing and drawing classification, and handwriting recognition.</span></span> <span data-ttu-id="bc215-115">Esse método retorna após a conclusão da operação de análise.</span><span class="sxs-lookup"><span data-stu-id="bc215-115">This method returns after the analysis operation is complete.</span></span>

<span data-ttu-id="bc215-116">Esse método retornará **o \_ ponteiro E** se *ppStatus* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="bc215-116">This method returns **E\_POINTER** if *ppStatus* is **NULL**.</span></span>

<span data-ttu-id="bc215-117">Durante uma chamada para o método **IInkAnalyzer:: Analyze** ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), o [**IInkAnalyzer**](iinkanalyzer.md) analisa a tinta em sua região suja (Confira o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="bc215-117">During a call to **IInkAnalyzer::Analyze Method** or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), the [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span> <span data-ttu-id="bc215-118">No entanto, o **IInkAnalyzer** pode expandir a operação de análise para incluir regiões vizinhas.</span><span class="sxs-lookup"><span data-stu-id="bc215-118">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="bc215-119">Esse método define a região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) para uma região vazia.</span><span class="sxs-lookup"><span data-stu-id="bc215-119">This method sets the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region to an empty region.</span></span> <span data-ttu-id="bc215-120">Se outro thread tiver adicionado dados de traço que não foram analisados, o **IInkAnalyzer** adicionará a caixa delimitadora dos traços não analisados à sua região suja durante a fase de reconciliação da análise.</span><span class="sxs-lookup"><span data-stu-id="bc215-120">If another thread has added stroke data that has not been analyzed, the **IInkAnalyzer** adds the bounding box of the unanalyzed strokes to its dirty region during the reconcile phase of the analysis.</span></span>

<span data-ttu-id="bc215-121">Esse método retornará um erro se seu aplicativo não tratar o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="bc215-121">This method returns an error if your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

<span data-ttu-id="bc215-122">O [**IInkAnalyzer**](iinkanalyzer.md) não gera os eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) em resposta a esse método.</span><span class="sxs-lookup"><span data-stu-id="bc215-122">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) events in response to this method.</span></span>

<span data-ttu-id="bc215-123">Para modificar a maneira como a análise de tinta é executada, use o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md).</span><span class="sxs-lookup"><span data-stu-id="bc215-123">To modify the way ink analysis is performed, use [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md).</span></span>

<span data-ttu-id="bc215-124">Para obter mais informações sobre a análise de tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bc215-124">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bc215-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc215-125">Examples</span></span>

<span data-ttu-id="bc215-126">O exemplo a seguir executa a análise de tinta em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="bc215-126">The following example performs foreground ink analysis.</span></span>


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="bc215-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc215-127">Requirements</span></span>



| <span data-ttu-id="bc215-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc215-128">Requirement</span></span> | <span data-ttu-id="bc215-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bc215-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc215-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc215-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bc215-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bc215-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc215-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc215-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bc215-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bc215-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bc215-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc215-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc215-135"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bc215-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bc215-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bc215-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc215-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc215-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bc215-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc215-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc215-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="bc215-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="bc215-140">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="bc215-140">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="bc215-141">**Método IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="bc215-141">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="bc215-142">**Método IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="bc215-142">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="bc215-143">**Método IInkAnalyzer:: GetRootNode**</span><span class="sxs-lookup"><span data-stu-id="bc215-143">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="bc215-144">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="bc215-144">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

