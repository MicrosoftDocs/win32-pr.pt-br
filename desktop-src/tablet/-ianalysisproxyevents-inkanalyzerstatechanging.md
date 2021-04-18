---
description: Ocorre antes de o IInkAnalyzer reconciliar os resultados da análise para que um aplicativo possa sincronizar dados com o IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: 'Evento _IAnalysisProxyEvents:: InkAnalyzerStateChanging (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105789288"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a><span data-ttu-id="fb471-103">\_Evento IAnalysisProxyEvents:: InkAnalyzerStateChanging</span><span class="sxs-lookup"><span data-stu-id="fb471-103">\_IAnalysisProxyEvents::InkAnalyzerStateChanging event</span></span>

<span data-ttu-id="fb471-104">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) reconciliar os resultados da análise para que um aplicativo possa sincronizar dados com o **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="fb471-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb471-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb471-105">Syntax</span></span>


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a><span data-ttu-id="fb471-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb471-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb471-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fb471-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb471-108">O [**IInkAnalyzer**](iinkanalyzer.md) que está prestes a reconciliar seus resultados de análise.</span><span class="sxs-lookup"><span data-stu-id="fb471-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is about to reconcile its analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb471-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb471-109">Return value</span></span>

<span data-ttu-id="fb471-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fb471-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb471-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb471-111">Remarks</span></span>

<span data-ttu-id="fb471-112">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="fb471-112">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="fb471-113">Quando o **IInkAnalyzer** gera esse evento, seu aplicativo deve preencher os subnós do nó raiz do analisador de tinta (consulte o método [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="fb471-113">When the **IInkAnalyzer** raises this event, your application should populate the subnodes of the ink analyzer's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="fb471-114">O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de gerar o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="fb471-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="fb471-115">Ele gera esse evento somente durante a execução da análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fb471-115">It raises this event only while performing background analysis.</span></span>

<span data-ttu-id="fb471-116">Bloqueie sua estrutura de dados quando o [**IInkAnalyzer**](iinkanalyzer.md) gerar o evento **\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging** .</span><span class="sxs-lookup"><span data-stu-id="fb471-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the **\_IAnalysisProxyEvents::InkAnalyzerStateChanging** event.</span></span> <span data-ttu-id="fb471-117">As alterações na estrutura de dados durante esta fase de análise podem causar erros na análise de tinta e na sincronização.</span><span class="sxs-lookup"><span data-stu-id="fb471-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="fb471-118">Desbloqueie sua estrutura de dados quando o **IInkAnalyzer** gerar o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="fb471-118">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="fb471-119">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fb471-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb471-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb471-120">Requirements</span></span>



| <span data-ttu-id="fb471-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb471-121">Requirement</span></span> | <span data-ttu-id="fb471-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fb471-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb471-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb471-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fb471-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fb471-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb471-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb471-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fb471-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fb471-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fb471-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb471-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb471-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fb471-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb471-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fb471-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb471-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb471-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fb471-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb471-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb471-132">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="fb471-132">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="fb471-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fb471-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fb471-134">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="fb471-134">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="fb471-135">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="fb471-135">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="fb471-136">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="fb471-136">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="fb471-137">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="fb471-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




