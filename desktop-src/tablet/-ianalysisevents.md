---
description: Especifica os eventos associados às etapas de análise de um objeto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interface _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763438"
---
# <a name="_ianalysisevents-interface"></a><span data-ttu-id="8d784-103">\_Interface IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="8d784-103">\_IAnalysisEvents interface</span></span>

<span data-ttu-id="8d784-104">Especifica os eventos associados às etapas de análise de um objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="8d784-104">Specifies events associated with the analysis steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="8d784-105">Eventos</span><span class="sxs-lookup"><span data-stu-id="8d784-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="8d784-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="8d784-106">Events</span></span>

<span data-ttu-id="8d784-107">A interface **\_ IAnalysisEvents** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="8d784-107">The **\_IAnalysisEvents** interface has these events.</span></span>



| <span data-ttu-id="8d784-108">Evento</span><span class="sxs-lookup"><span data-stu-id="8d784-108">Event</span></span>                                                               | <span data-ttu-id="8d784-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d784-109">Description</span></span>                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d784-110">**Actividade**</span><span class="sxs-lookup"><span data-stu-id="8d784-110">**Activity**</span></span>](-ianalysisevents-activity.md)                       | <span data-ttu-id="8d784-111">Ocorre durante chamadas para o método de método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="8d784-111">Occurs during calls to the [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method.</span></span><br/> |
| [<span data-ttu-id="8d784-112">**IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="8d784-112">**IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md) | <span data-ttu-id="8d784-113">Ocorre quando o estágio de análise intermediária atual é concluído.</span><span class="sxs-lookup"><span data-stu-id="8d784-113">Occurs when the current intermediate analysis stage is finished.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8d784-114">**ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="8d784-114">**ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)       | <span data-ttu-id="8d784-115">Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) está pronto para reconciliar seus resultados de análise em segundo plano com seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="8d784-115">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span><br/>                                                  |
| [<span data-ttu-id="8d784-116">**Resultados**</span><span class="sxs-lookup"><span data-stu-id="8d784-116">**Results**</span></span>](-ianalysisevents-results.md)                         | <span data-ttu-id="8d784-117">Ocorre quando o estágio de análise final é concluído.</span><span class="sxs-lookup"><span data-stu-id="8d784-117">Occurs when the final analysis stage is finished.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="8d784-118">**UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="8d784-118">**UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)   | <span data-ttu-id="8d784-119">Ocorre antes que o [**IInkAnalyzer**](iinkanalyzer.md) acesse os dados de traço.</span><span class="sxs-lookup"><span data-stu-id="8d784-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span><br/>                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="8d784-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d784-120">Requirements</span></span>



| <span data-ttu-id="8d784-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d784-121">Requirement</span></span> | <span data-ttu-id="8d784-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8d784-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8d784-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d784-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8d784-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8d784-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d784-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d784-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8d784-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8d784-126">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="8d784-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d784-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d784-128">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="8d784-128">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="8d784-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8d784-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8d784-130">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="8d784-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="8d784-131">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="8d784-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="8d784-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="8d784-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

