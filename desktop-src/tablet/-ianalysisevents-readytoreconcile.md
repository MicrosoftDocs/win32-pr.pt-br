---
description: Ocorre quando o IInkAnalyzer está pronto para reconciliar seus resultados de análise em segundo plano com seu estado atual.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: 'Evento _IAnalysisEvents:: ReadyToReconcile (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172537"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a><span data-ttu-id="7a5d3-103">\_Evento IAnalysisEvents:: ReadyToReconcile</span><span class="sxs-lookup"><span data-stu-id="7a5d3-103">\_IAnalysisEvents::ReadyToReconcile event</span></span>

<span data-ttu-id="7a5d3-104">Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) está pronto para reconciliar seus resultados de análise em segundo plano com seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a5d3-105">Syntax</span></span>


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a><span data-ttu-id="7a5d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a5d3-106">Parameters</span></span>

<span data-ttu-id="7a5d3-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a5d3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a5d3-108">Return value</span></span>

<span data-ttu-id="7a5d3-109">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7a5d3-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7a5d3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a5d3-110">Remarks</span></span>

<span data-ttu-id="7a5d3-111">O [**IInkAnalyzer**](iinkanalyzer.md) executa a reconciliação automática quando o sinalizador **\_ AutomaticReconciliation de AnalysisModes** do Ink Analyzer é definido (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="7a5d3-111">The [**IInkAnalyzer**](iinkanalyzer.md) performs automatic reconciliation when the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag is set (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)).</span></span> <span data-ttu-id="7a5d3-112">Quando o sinalizador **AnalysisModes \_ AutomaticReconciliation** não é definido, seu aplicativo precisa reconciliar os resultados da análise em segundo plano manualmente.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-112">When the **AnalysisModes\_AutomaticReconciliation** flag is not set, your application needs to reconcile background analysis results manually.</span></span>

<span data-ttu-id="7a5d3-113">Para executar a reconciliação manual, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-113">To perform manual reconciliation, follow these steps.</span></span>

1.  <span data-ttu-id="7a5d3-114">Limpe o sinalizador **AnalysisModes \_ AutomaticReconciliation** do Ink Analyzer.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-114">Clear the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag.</span></span>
2.  <span data-ttu-id="7a5d3-115">Manipule o evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="7a5d3-115">Handle the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>
3.  <span data-ttu-id="7a5d3-116">Para reconciliar os resultados da análise, chame o método de [**método IInkAnalyzer:: reconcile**](iinkanalyzer-reconcile.md) do manipulador de eventos para o evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="7a5d3-116">To reconcile the analysis results, call the [**IInkAnalyzer::Reconcile Method**](iinkanalyzer-reconcile.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span> <span data-ttu-id="7a5d3-117">Para cancelar a operação atual de análise em segundo plano, chame o método do [**método IInkAnalyzer:: Abort**](iinkanalyzer-abort.md) do manipulador de eventos para o evento **\_ IAnalysisEvents:: ReadyToReconcile** .</span><span class="sxs-lookup"><span data-stu-id="7a5d3-117">To cancel the current background analysis operation, call the [**IInkAnalyzer::Abort Method**](iinkanalyzer-abort.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>

<span data-ttu-id="7a5d3-118">O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento antes de gerar o evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="7a5d3-118">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event before it raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span>

<span data-ttu-id="7a5d3-119">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7a5d3-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="7a5d3-120">O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento durante a análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7a5d3-120">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during background analysis.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5d3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a5d3-121">Requirements</span></span>



| <span data-ttu-id="7a5d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a5d3-122">Requirement</span></span> | <span data-ttu-id="7a5d3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7a5d3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5d3-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a5d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5d3-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7a5d3-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a5d3-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a5d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5d3-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7a5d3-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7a5d3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a5d3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a5d3-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7a5d3-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7a5d3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7a5d3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a5d3-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a5d3-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7a5d3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a5d3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5d3-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="7a5d3-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="7a5d3-135">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-135">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="7a5d3-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7a5d3-137">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="7a5d3-138">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="7a5d3-139">**Método IInkAnalyzer:: Reconcilize**</span><span class="sxs-lookup"><span data-stu-id="7a5d3-139">**IInkAnalyzer::Reconcile Method**</span></span>](iinkanalyzer-reconcile.md)
</dt> <dt>

[<span data-ttu-id="7a5d3-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="7a5d3-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




