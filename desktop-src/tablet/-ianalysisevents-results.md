---
description: Ocorre quando o estágio de análise final é concluído.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: 'Evento _IAnalysisEvents:: Results (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763167"
---
# <a name="_ianalysiseventsresults-event"></a><span data-ttu-id="12c68-103">\_Evento IAnalysisEvents:: Results</span><span class="sxs-lookup"><span data-stu-id="12c68-103">\_IAnalysisEvents::Results event</span></span>

<span data-ttu-id="12c68-104">Ocorre quando o estágio de análise final é concluído.</span><span class="sxs-lookup"><span data-stu-id="12c68-104">Occurs when the final analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12c68-105">Syntax</span></span>


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="12c68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12c68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c68-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12c68-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c68-108">O [**IInkAnalyzer**](iinkanalyzer.md) que produz os resultados da análise.</span><span class="sxs-lookup"><span data-stu-id="12c68-108">The [**IInkAnalyzer**](iinkanalyzer.md) that produces the analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="12c68-109">*pAnalysisStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12c68-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12c68-110">O objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa o status da análise.</span><span class="sxs-lookup"><span data-stu-id="12c68-110">The [**IAnalysisStatus**](ianalysisstatus.md) object that represents the status of the analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c68-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12c68-111">Return value</span></span>

<span data-ttu-id="12c68-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="12c68-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12c68-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="12c68-113">Remarks</span></span>

<span data-ttu-id="12c68-114">O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de ter reconciliado os resultados para o estágio de análise final.</span><span class="sxs-lookup"><span data-stu-id="12c68-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the results for the final analysis stage.</span></span>

<span data-ttu-id="12c68-115">Se seu aplicativo chamar o [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), esse evento sinalizará quando os resultados da análise estiverem prontos.</span><span class="sxs-lookup"><span data-stu-id="12c68-115">If your application calls [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), this event signals when analysis results are ready.</span></span>

<span data-ttu-id="12c68-116">Se seu aplicativo mantém sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md), esse evento indica que o **IInkAnalyzer** terminou de fazer alterações em seus dados internos para este estágio de análise.</span><span class="sxs-lookup"><span data-stu-id="12c68-116">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="12c68-117">Bloqueie sua estrutura de dados quando o [**IInkAnalyzer**](iinkanalyzer.md) gerar o evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .</span><span class="sxs-lookup"><span data-stu-id="12c68-117">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="12c68-118">As alterações na estrutura de dados durante esta fase de análise podem causar erros na análise de tinta e na sincronização.</span><span class="sxs-lookup"><span data-stu-id="12c68-118">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="12c68-119">Desbloqueie sua estrutura de dados quando o **IInkAnalyzer** gerar o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou **\_ IAnalysisEvents:: Results** .</span><span class="sxs-lookup"><span data-stu-id="12c68-119">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or **\_IAnalysisEvents::Results** event.</span></span>

<span data-ttu-id="12c68-120">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="12c68-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12c68-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12c68-121">Requirements</span></span>



| <span data-ttu-id="12c68-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="12c68-122">Requirement</span></span> | <span data-ttu-id="12c68-123">Valor</span><span class="sxs-lookup"><span data-stu-id="12c68-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c68-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c68-124">Minimum supported client</span></span><br/> | <span data-ttu-id="12c68-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="12c68-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12c68-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c68-126">Minimum supported server</span></span><br/> | <span data-ttu-id="12c68-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="12c68-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="12c68-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12c68-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c68-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="12c68-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="12c68-130">DLL</span><span class="sxs-lookup"><span data-stu-id="12c68-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12c68-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12c68-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="12c68-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="12c68-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c68-133">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="12c68-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="12c68-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="12c68-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="12c68-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="12c68-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="12c68-136">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="12c68-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="12c68-137">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="12c68-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="12c68-138">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="12c68-138">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="12c68-139">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="12c68-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




