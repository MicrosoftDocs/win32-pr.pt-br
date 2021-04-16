---
description: Especifica os eventos associados às etapas de proxy de dados de um objeto IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Interface _IAnalysisProxyEvents (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105754231"
---
# <a name="_ianalysisproxyevents-interface"></a><span data-ttu-id="57e95-103">\_Interface IAnalysisProxyEvents</span><span class="sxs-lookup"><span data-stu-id="57e95-103">\_IAnalysisProxyEvents interface</span></span>

<span data-ttu-id="57e95-104">Especifica os eventos associados às etapas de proxy de dados de um objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="57e95-104">Specifies events associated with the data proxy steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="57e95-105">Eventos</span><span class="sxs-lookup"><span data-stu-id="57e95-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="57e95-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="57e95-106">Events</span></span>

<span data-ttu-id="57e95-107">A interface **\_ IAnalysisProxyEvents** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="57e95-107">The **\_IAnalysisProxyEvents** interface has these events.</span></span>



| <span data-ttu-id="57e95-108">Evento</span><span class="sxs-lookup"><span data-stu-id="57e95-108">Event</span></span>                                                                                      | <span data-ttu-id="57e95-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="57e95-109">Description</span></span>                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57e95-110">**ContextNodeCreated**</span><span class="sxs-lookup"><span data-stu-id="57e95-110">**ContextNodeCreated**</span></span>](-ianalysisproxyevents-contextnodecreated.md)                     | <span data-ttu-id="57e95-111">Ocorre depois que o [**IInkAnalyzer**](iinkanalyzer.md) cria um objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="57e95-111">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                  |
| [<span data-ttu-id="57e95-112">**ContextNodeDeleting**</span><span class="sxs-lookup"><span data-stu-id="57e95-112">**ContextNodeDeleting**</span></span>](-ianalysisproxyevents-contextnodedeleting.md)                   | <span data-ttu-id="57e95-113">Ocorre antes de [**IInkAnalyzer**](iinkanalyzer.md) excluir um objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="57e95-113">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                 |
| [<span data-ttu-id="57e95-114">**ContextNodeLinkAdding**</span><span class="sxs-lookup"><span data-stu-id="57e95-114">**ContextNodeLinkAdding**</span></span>](-ianalysisproxyevents-contextnodelinkadding.md)               | <span data-ttu-id="57e95-115">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) adicionar um objeto [**IContextLink**](icontextlink.md) entre dois objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="57e95-115">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>           |
| [<span data-ttu-id="57e95-116">**ContextNodeLinkDeleting**</span><span class="sxs-lookup"><span data-stu-id="57e95-116">**ContextNodeLinkDeleting**</span></span>](-ianalysisproxyevents-contextnodelinkdeleting.md)           | <span data-ttu-id="57e95-117">Ocorre antes de [**IInkAnalyzer**](iinkanalyzer.md) excluir um objeto [**IContextLink**](icontextlink.md) entre dois objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="57e95-117">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>         |
| [<span data-ttu-id="57e95-118">**ContextNodeMovingToPosition**</span><span class="sxs-lookup"><span data-stu-id="57e95-118">**ContextNodeMovingToPosition**</span></span>](-ianalysisproxyevents-contextnodemovingtoposition.md)   | <span data-ttu-id="57e95-119">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) mover um objeto [**IContextNode**](icontextnode.md) para uma nova posição dentro de sua coleção de subnós do nó pai.</span><span class="sxs-lookup"><span data-stu-id="57e95-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span><br/> |
| [<span data-ttu-id="57e95-120">**ContextNodePropertiesUpdated**</span><span class="sxs-lookup"><span data-stu-id="57e95-120">**ContextNodePropertiesUpdated**</span></span>](-ianalysisproxyevents-contextnodepropertiesupdated.md) | <span data-ttu-id="57e95-121">Ocorre depois que o [**IInkAnalyzer**](iinkanalyzer.md) atualiza uma ou mais propriedades de um objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="57e95-121">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                        |
| [<span data-ttu-id="57e95-122">**ContextNodeReparenting**</span><span class="sxs-lookup"><span data-stu-id="57e95-122">**ContextNodeReparenting**</span></span>](-ianalysisproxyevents-contextnodereparenting.md)             | <span data-ttu-id="57e95-123">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) mover um objeto [**IContextNode**](icontextnode.md) alterando seu nó pai.</span><span class="sxs-lookup"><span data-stu-id="57e95-123">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span><br/>                                       |
| [<span data-ttu-id="57e95-124">**InkAnalyzerStateChanging**</span><span class="sxs-lookup"><span data-stu-id="57e95-124">**InkAnalyzerStateChanging**</span></span>](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | <span data-ttu-id="57e95-125">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) reconciliar os resultados da análise para que um aplicativo possa sincronizar dados com o **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="57e95-125">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span><br/>                      |
| [<span data-ttu-id="57e95-126">**PopulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="57e95-126">**PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)                   | <span data-ttu-id="57e95-127">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) executar a análise dentro da região de um objeto [**IContextNode**](icontextnode.md) parcialmente populado.</span><span class="sxs-lookup"><span data-stu-id="57e95-127">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span><br/>               |
| [<span data-ttu-id="57e95-128">**StrokeReparented**</span><span class="sxs-lookup"><span data-stu-id="57e95-128">**StrokeReparented**</span></span>](-ianalysisproxyevents-strokereparented.md)                         | <span data-ttu-id="57e95-129">Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) move um traço de um objeto [**IContextNode**](icontextnode.md) para outro.</span><span class="sxs-lookup"><span data-stu-id="57e95-129">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span><br/>                                           |



 

## <a name="remarks"></a><span data-ttu-id="57e95-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="57e95-130">Remarks</span></span>

<span data-ttu-id="57e95-131">Use esses eventos quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="57e95-131">Use these events when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="57e95-132">Para obter mais informações sobre como sincronizar os dados do aplicativo com o **IInkAnalyzer**, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="57e95-132">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57e95-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57e95-133">Requirements</span></span>



| <span data-ttu-id="57e95-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="57e95-134">Requirement</span></span> | <span data-ttu-id="57e95-135">Valor</span><span class="sxs-lookup"><span data-stu-id="57e95-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e95-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57e95-136">Minimum supported client</span></span><br/> | <span data-ttu-id="57e95-137">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="57e95-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="57e95-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57e95-138">Minimum supported server</span></span><br/> | <span data-ttu-id="57e95-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="57e95-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="57e95-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57e95-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="57e95-141"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="57e95-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="57e95-142">DLL</span><span class="sxs-lookup"><span data-stu-id="57e95-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57e95-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57e95-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="57e95-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="57e95-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57e95-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="57e95-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="57e95-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="57e95-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="57e95-147">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="57e95-147">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="57e95-148">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="57e95-148">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="57e95-149">\_IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="57e95-149">\_IAnalysisEvents</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="57e95-150">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="57e95-150">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

