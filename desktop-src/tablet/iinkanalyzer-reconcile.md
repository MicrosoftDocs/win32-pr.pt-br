---
description: 'Aplica os resultados de uma operação de análise de tinta em segundo plano à árvore de nós de contexto para as partes da árvore que não foram modificadas pelo aplicativo desde a chamada para o método IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'Método IInkAnalyzer:: Reconcilize (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752181"
---
# <a name="iinkanalyzerreconcile-method"></a><span data-ttu-id="faf58-103">Método IInkAnalyzer:: Reconcilize</span><span class="sxs-lookup"><span data-stu-id="faf58-103">IInkAnalyzer::Reconcile method</span></span>

<span data-ttu-id="faf58-104">Aplica os resultados de uma operação de análise de tinta em segundo plano à árvore de nós de contexto para as partes da árvore que não foram modificadas pelo aplicativo desde a chamada para o [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="faf58-104">Applies the results of a background ink analysis operation to the context node tree for the portions of the tree that have not been modified by the application since the call to [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="faf58-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faf58-105">Syntax</span></span>


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a><span data-ttu-id="faf58-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faf58-106">Parameters</span></span>

<span data-ttu-id="faf58-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="faf58-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="faf58-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="faf58-108">Return value</span></span>

<span data-ttu-id="faf58-109">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="faf58-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="faf58-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="faf58-110">Remarks</span></span>

<span data-ttu-id="faf58-111">Por padrão, o [**IInkAnalyzer**](iinkanalyzer.md) executa uma fase de reconciliação automática imediatamente antes de gerar os eventos [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) e [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="faf58-111">By default, the [**IInkAnalyzer**](iinkanalyzer.md) performs an automatic reconciliation phase immediately before raising the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) and [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) events.</span></span>

<span data-ttu-id="faf58-112">Para desabilitar a reconciliação automática, desmarque o sinalizador **AnalysisModes \_ AutomaticReconciliation** dos modos de análise do Ink Analyzer (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) e [**AnalysisModes**](analysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="faf58-112">To disable automatic reconciliation, clear the **AnalysisModes\_AutomaticReconciliation** flag from the ink analyzer's analysis modes (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) and [**AnalysisModes**](analysismodes.md)).</span></span> <span data-ttu-id="faf58-113">O método do [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) retorna um erro quando a reconciliação automática está desabilitada e seu aplicativo não manipula o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="faf58-113">The [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method returns an error when automatic reconciliation is disabled and your application does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="faf58-114">Seu aplicativo deve chamar o método de **método IInkAnalyzer:: reconcile** antes que o [**IInkAnalyzer**](iinkanalyzer.md) possa continuar processando os resultados ou continuar a análise para o estágio de análise correspondente.</span><span class="sxs-lookup"><span data-stu-id="faf58-114">Your application must call the **IInkAnalyzer::Reconcile Method** method before the [**IInkAnalyzer**](iinkanalyzer.md) can continue to process the results or continue further analysis for the corresponding analysis stage.</span></span>

<span data-ttu-id="faf58-115">Seu aplicativo pode fazer alterações, como adicionar ou remover traços e alterar dados de traço, na árvore de nós de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) durante a análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="faf58-115">Your application can make changes, such as adding or removing strokes and changing stroke data, in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree during background analysis.</span></span> <span data-ttu-id="faf58-116">Essas alterações podem invalidar partes dos resultados da análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="faf58-116">Such changes can invalidate portions of the background analysis results.</span></span> <span data-ttu-id="faf58-117">Esse método aplica resultados de análise somente à árvore de nós de contexto do analisador para as partes da árvore em que seu aplicativo não foi alterado.</span><span class="sxs-lookup"><span data-stu-id="faf58-117">This method applies analysis results only to the analyzer's context node tree for the portions of the tree that your application has not changed.</span></span> <span data-ttu-id="faf58-118">Esse método também adiciona regiões que contêm resultados de análise invalidados à região suja do objeto **IInkAnalyzer** (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="faf58-118">This method also adds regions containing invalidated analysis results to the **IInkAnalyzer** object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="faf58-119">Para obter mais informações sobre como usar o para analisar a tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md). [**AnalysisModes**](analysismodes.md)</span><span class="sxs-lookup"><span data-stu-id="faf58-119">For more information about using the to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).[**AnalysisModes**](analysismodes.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="faf58-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faf58-120">Requirements</span></span>



| <span data-ttu-id="faf58-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="faf58-121">Requirement</span></span> | <span data-ttu-id="faf58-122">Valor</span><span class="sxs-lookup"><span data-stu-id="faf58-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf58-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faf58-123">Minimum supported client</span></span><br/> | <span data-ttu-id="faf58-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="faf58-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="faf58-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="faf58-125">Minimum supported server</span></span><br/> | <span data-ttu-id="faf58-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="faf58-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="faf58-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="faf58-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="faf58-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="faf58-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="faf58-129">DLL</span><span class="sxs-lookup"><span data-stu-id="faf58-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faf58-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faf58-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="faf58-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="faf58-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf58-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="faf58-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="faf58-133">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="faf58-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="faf58-134">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="faf58-134">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="faf58-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="faf58-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




