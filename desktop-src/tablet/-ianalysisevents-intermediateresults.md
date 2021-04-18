---
description: Ocorre quando o estágio de análise intermediária atual é concluído.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: 'Evento _IAnalysisEvents:: IntermediateResults (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105810739"
---
# <a name="_ianalysiseventsintermediateresults-event"></a><span data-ttu-id="fac70-103">\_Evento IAnalysisEvents:: IntermediateResults</span><span class="sxs-lookup"><span data-stu-id="fac70-103">\_IAnalysisEvents::IntermediateResults event</span></span>

<span data-ttu-id="fac70-104">Ocorre quando o estágio de análise intermediária atual é concluído.</span><span class="sxs-lookup"><span data-stu-id="fac70-104">Occurs when the current intermediate analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac70-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fac70-105">Syntax</span></span>


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="fac70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fac70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac70-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fac70-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac70-108">O [**IInkAnalyzer**](iinkanalyzer.md) que está executando a análise.</span><span class="sxs-lookup"><span data-stu-id="fac70-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is performing the analysis.</span></span>

</dd> <dt>

<span data-ttu-id="fac70-109">*pAnalysisStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fac70-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac70-110">O objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa o status dos resultados intermediários.</span><span class="sxs-lookup"><span data-stu-id="fac70-110">The [**IAnalysisStatus**](ianalysisstatus.md) object representing the status of the intermediate results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac70-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fac70-111">Return value</span></span>

<span data-ttu-id="fac70-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fac70-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fac70-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fac70-113">Remarks</span></span>

<span data-ttu-id="fac70-114">O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de ter reconciliado os resultados intermediários para o estágio de análise atual.</span><span class="sxs-lookup"><span data-stu-id="fac70-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the intermediate results for the current analysis stage.</span></span>

<span data-ttu-id="fac70-115">Se seu aplicativo mantém sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md), esse evento indica que o **IInkAnalyzer** terminou de fazer alterações em seus dados internos para este estágio de análise.</span><span class="sxs-lookup"><span data-stu-id="fac70-115">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="fac70-116">Bloqueie sua estrutura de dados quando o [**IInkAnalyzer**](iinkanalyzer.md) gerar o evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="fac70-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="fac70-117">As alterações na estrutura de dados durante esta fase de análise podem causar erros na análise de tinta e na sincronização.</span><span class="sxs-lookup"><span data-stu-id="fac70-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="fac70-118">Você pode desbloquear sua estrutura de dados quando o **IInkAnalyzer** gera o evento **\_ IAnalysisEvents:: IntermediateResults** ou [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="fac70-118">You can unlock your data structure when the **IInkAnalyzer** raises the **\_IAnalysisEvents::IntermediateResults** or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="fac70-119">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fac70-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="fac70-120">O [**IInkAnalyzer**](iinkanalyzer.md) gera resultados intermediários somente quando seus modos de análise têm o sinalizador **AnalysisModes \_ IntermediateResults** definido (consulte o [**método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="fac70-120">The [**IInkAnalyzer**](iinkanalyzer.md) generates intermediate results only when its analysis modes has the **AnalysisModes\_IntermediateResults** flag set (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="fac70-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac70-121">Requirements</span></span>



| <span data-ttu-id="fac70-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac70-122">Requirement</span></span> | <span data-ttu-id="fac70-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fac70-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fac70-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fac70-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fac70-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fac70-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fac70-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fac70-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fac70-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fac70-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fac70-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fac70-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fac70-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fac70-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fac70-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fac70-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac70-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac70-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fac70-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fac70-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac70-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="fac70-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="fac70-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="fac70-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="fac70-135">**\_IAnalysisEvents:: resultados**</span><span class="sxs-lookup"><span data-stu-id="fac70-135">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="fac70-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="fac70-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="fac70-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fac70-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fac70-138">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="fac70-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="fac70-139">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="fac70-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="fac70-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="fac70-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>
