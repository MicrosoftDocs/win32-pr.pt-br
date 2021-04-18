---
description: Cancela a operação de análise atual.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'Método IInkAnalyzer:: Abort (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793378"
---
# <a name="iinkanalyzerabort-method"></a><span data-ttu-id="e2d8b-103">Método IInkAnalyzer:: Abort</span><span class="sxs-lookup"><span data-stu-id="e2d8b-103">IInkAnalyzer::Abort method</span></span>

<span data-ttu-id="e2d8b-104">Cancela a operação de análise atual.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-104">Cancels the current analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d8b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2d8b-105">Syntax</span></span>


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="e2d8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2d8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2d8b-107">*ppAbortedRegion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e2d8b-107">*ppAbortedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2d8b-108">Um ponteiro para um [**IAnalysisRegion**](ianalysisregion.md) que representa a região suja (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) da operação de análise atual.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-108">A pointer to an [**IAnalysisRegion**](ianalysisregion.md) that represents the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) of the current analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2d8b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2d8b-109">Return value</span></span>

<span data-ttu-id="e2d8b-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e2d8b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2d8b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2d8b-111">Remarks</span></span>

<span data-ttu-id="e2d8b-112">Chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAbortedRegion* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-112">Call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAbortedRegion* when you no longer need to use the object.</span></span>

<span data-ttu-id="e2d8b-113">Esse método cancela a operação de análise atual.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-113">This method cancels the current analysis operation.</span></span>

<span data-ttu-id="e2d8b-114">Quando *ppAbortedRegion* é **NULL**, esse método executa a anulação como normal, porque isso indica que o chamador não tem interesse no valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-114">When *ppAbortedRegion* is **NULL**, this method performs the abort as normal, because this indicates that the caller has no interest in the return value.</span></span>

<span data-ttu-id="e2d8b-115">O **método IInkAnalyzer:: Abort** silencia os eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) e [**\_ IAnalysisEvents:: Activity**](-ianalysisevents-activity.md) para a operação de análise atual.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-115">**IInkAnalyzer::Abort Method** silences the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::Activity**](-ianalysisevents-activity.md) events for the current analysis operation.</span></span>

<span data-ttu-id="e2d8b-116">O **método IInkAnalyzer:: Abort** é executado de forma assíncrona até a operação de análise em segundo plano atual ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-116">**IInkAnalyzer::Abort Method** runs asynchronously until the current background analysis operation is canceled.</span></span> <span data-ttu-id="e2d8b-117">Como o processo de cancelamento é assíncrono, o aplicativo pode executar outras tarefas enquanto o operações de análise atual é cancelado.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-117">Because the cancellation process is asynchronous, the application can perform other tasks while the current analysis opertions is canceled.</span></span>

<span data-ttu-id="e2d8b-118">Se nenhuma operação de análise estiver em andamento, esse método retornará uma região de análise vazia.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-118">If no analysis operations are in progress, this method returns an empty analysis region.</span></span>

<span data-ttu-id="e2d8b-119">Se uma operação de análise estiver em andamento, esse método cancelará a operação.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-119">If one analysis operation is in progress, this method cancels the operation.</span></span>

<span data-ttu-id="e2d8b-120">Se as operações de análise síncrona e assíncrona estiverem em andamento, esse método cancelará a operação síncrona.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-120">If both synchronous and asynchronous analysis operations are in progress, this method cancels the synchronous operation.</span></span>

<span data-ttu-id="e2d8b-121">Se esse método for chamado mais de uma vez para a mesma operação de análise, a primeira chamada retornará a região suja para a operação e as chamadas subsequentes retornarão uma região vazia.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-121">If this method is called more than once for the same analysis operation, the first call returns the dirty region for the operation, and the subsequent calls return an empty region.</span></span>

<span data-ttu-id="e2d8b-122">Se seu aplicativo mantém sua própria estrutura de dados que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md), chamar o **método IInkAnalyzer:: Abort** pode deixar o documento com resultados parciais.</span><span class="sxs-lookup"><span data-stu-id="e2d8b-122">If your application maintains its own data structure that is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), calling **IInkAnalyzer::Abort Method** can leave your document with partial results.</span></span> <span data-ttu-id="e2d8b-123">Para evitar isso, não chame o **método IInkAnalyzer:: Abort** entre a hora em que o **IInkAnalyzer** recebe o evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) e a hora em que o **IInkAnalyzer** recebe o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="e2d8b-123">To avoid this, do not call **IInkAnalyzer::Abort Method** between the time the **IInkAnalyzer** receives the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event and the time the **IInkAnalyzer** receives the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="e2d8b-124">Para obter mais informações sobre como sincronizar os dados do aplicativo com o Ink Analyzer, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e2d8b-124">For more information about synchronizing your application data with the ink analyzer, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d8b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d8b-125">Requirements</span></span>



| <span data-ttu-id="e2d8b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d8b-126">Requirement</span></span> | <span data-ttu-id="e2d8b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e2d8b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d8b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2d8b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d8b-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e2d8b-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e2d8b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2d8b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d8b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e2d8b-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e2d8b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2d8b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2d8b-133"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d8b-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e2d8b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e2d8b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2d8b-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2d8b-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e2d8b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2d8b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d8b-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e2d8b-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e2d8b-138">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="e2d8b-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="e2d8b-139">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="e2d8b-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="e2d8b-140">**Método IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="e2d8b-140">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="e2d8b-141">**Método IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="e2d8b-141">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="e2d8b-142">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="e2d8b-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

