---
description: Ocorre depois que o IInkAnalyzer cria um objeto IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Evento _IAnalysisProxyEvents:: ContextNodeCreated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930233"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a><span data-ttu-id="683c5-103">\_Evento IAnalysisProxyEvents:: ContextNodeCreated</span><span class="sxs-lookup"><span data-stu-id="683c5-103">\_IAnalysisProxyEvents::ContextNodeCreated event</span></span>

<span data-ttu-id="683c5-104">Ocorre depois que o [**IInkAnalyzer**](iinkanalyzer.md) cria um objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="683c5-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="683c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="683c5-105">Syntax</span></span>


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="683c5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="683c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="683c5-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="683c5-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683c5-108">O [**IInkAnalyzer**](iinkanalyzer.md) criando o objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="683c5-108">The [**IInkAnalyzer**](iinkanalyzer.md) creating the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="683c5-109">*pContextNodeCreated* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="683c5-109">*pContextNodeCreated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="683c5-110">O novo objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="683c5-110">The new [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="683c5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="683c5-111">Return value</span></span>

<span data-ttu-id="683c5-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="683c5-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="683c5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="683c5-113">Remarks</span></span>

<span data-ttu-id="683c5-114">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="683c5-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="683c5-115">Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método do analisador de tinta que cria um [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="683c5-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that creates an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="683c5-116">Quando o [**IInkAnalyzer**](iinkanalyzer.md) cria um [**IContextNode**](icontextnode.md), o novo **IContextNode** não contém traços, não contém links para outros objetos do **IContextNode** e pode não ter todas as suas propriedades definidas.</span><span class="sxs-lookup"><span data-stu-id="683c5-116">When the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md), the new **IContextNode** does not contain any strokes, does not contain links to other **IContextNode** objects, and may not have all of its properties set.</span></span> <span data-ttu-id="683c5-117">Além disso, o novo **IContextNode** é adicionado ao final da coleção de subnós do seu nó pai (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="683c5-117">Also, the new **IContextNode** is added to the end of its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="683c5-118">Após esse evento, o **IInkAnalyzer** pode gerar os eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="683c5-118">After this event, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="683c5-119">O evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando move um traço de um nó de contexto para outro.</span><span class="sxs-lookup"><span data-stu-id="683c5-119">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from one context node to another.</span></span>
-   <span data-ttu-id="683c5-120">O evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) quando ele adiciona um [**IContextLink**](icontextlink.md) a um [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="683c5-120">The [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) event when it adds an [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="683c5-121">O evento [**\_ IAnalysisProxyEvents:: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) quando ele altera a ordem de um [**IContextNode**](icontextnode.md) dentro de sua coleção de subnós do nó pai.</span><span class="sxs-lookup"><span data-stu-id="683c5-121">The [**\_IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) event when it changes the order of an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes.</span></span>
-   <span data-ttu-id="683c5-122">O [**IInkAnalyzer**](iinkanalyzer.md) gera o evento [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) depois de resolver o estado do [**IContextNode**](icontextnode.md) para esta fase de análise.</span><span class="sxs-lookup"><span data-stu-id="683c5-122">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) event after it resolves the state of the [**IContextNode**](icontextnode.md) for this analysis phase.</span></span>

<span data-ttu-id="683c5-123">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="683c5-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="683c5-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683c5-124">Requirements</span></span>



| <span data-ttu-id="683c5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="683c5-125">Requirement</span></span> | <span data-ttu-id="683c5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="683c5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="683c5-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683c5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="683c5-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="683c5-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="683c5-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="683c5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="683c5-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="683c5-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="683c5-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="683c5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="683c5-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="683c5-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="683c5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="683c5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="683c5-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683c5-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="683c5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="683c5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683c5-136">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="683c5-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="683c5-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="683c5-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="683c5-138">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="683c5-138">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="683c5-139">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="683c5-139">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="683c5-140">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="683c5-140">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="683c5-141">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="683c5-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




