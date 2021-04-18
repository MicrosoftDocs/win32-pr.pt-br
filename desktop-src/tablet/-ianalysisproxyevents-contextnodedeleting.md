---
description: Ocorre antes de IInkAnalyzer excluir um objeto IContextNode.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: 'Evento _IAnalysisProxyEvents:: ContextNodeDeleting (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763014"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a><span data-ttu-id="ef1a2-103">\_Evento IAnalysisProxyEvents:: ContextNodeDeleting</span><span class="sxs-lookup"><span data-stu-id="ef1a2-103">\_IAnalysisProxyEvents::ContextNodeDeleting event</span></span>

<span data-ttu-id="ef1a2-104">Ocorre antes de [**IInkAnalyzer**](iinkanalyzer.md) excluir um objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ef1a2-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef1a2-105">Syntax</span></span>


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="ef1a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef1a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1a2-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef1a2-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1a2-108">O objeto [**IInkAnalyzer**](iinkanalyzer.md) excluindo o objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ef1a2-108">The [**IInkAnalyzer**](iinkanalyzer.md) object deleting the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ef1a2-109">*pContextNodeToBeDeleted* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef1a2-109">*pContextNodeToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1a2-110">O objeto [**IContextNode**](icontextnode.md) a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ef1a2-110">The [**IContextNode**](icontextnode.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1a2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef1a2-111">Return value</span></span>

<span data-ttu-id="ef1a2-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ef1a2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1a2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef1a2-113">Remarks</span></span>

<span data-ttu-id="ef1a2-114">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ef1a2-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ef1a2-115">Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método do analisador de tinta que exclui um [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="ef1a2-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that deletes an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="ef1a2-116">Antes que o [**IInkAnalyzer**](iinkanalyzer.md) exclua um [**IContextNode**](icontextnode.md), o **IInkAnalyzer** remove todos os traços do nó de contexto e remove todos os links para outros nós de contexto.</span><span class="sxs-lookup"><span data-stu-id="ef1a2-116">Before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md), the **IInkAnalyzer** removes all of the strokes from the context node and removes all of the links to other context nodes.</span></span> <span data-ttu-id="ef1a2-117">Antes de o nó de contexto ser removido, o **IInkAnalyzer** pode gerar os seguintes eventos.</span><span class="sxs-lookup"><span data-stu-id="ef1a2-117">Before the context node is removed, the **IInkAnalyzer** may raise the following events.</span></span>

-   <span data-ttu-id="ef1a2-118">O evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando move um traço do [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="ef1a2-118">The [**\_IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) event when it moves a stroke from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="ef1a2-119">O evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) antes de remover um [**IContextLink**](icontextlink.md) do [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="ef1a2-119">The [**\_IAnalysisProxyEvents::ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) event before it removes a [**IContextLink**](icontextlink.md) from the [**IContextNode**](icontextnode.md).</span></span>
-   <span data-ttu-id="ef1a2-120">O evento **\_ IAnalysisProxyEvents:: ContextNodeDeleting** antes de remover um nó de contexto pai que não tem mais nós filho.</span><span class="sxs-lookup"><span data-stu-id="ef1a2-120">The **\_IAnalysisProxyEvents::ContextNodeDeleting** event before it removes a parent context node that no longer has child nodes.</span></span>

<span data-ttu-id="ef1a2-121">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ef1a2-121">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1a2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef1a2-122">Requirements</span></span>



| <span data-ttu-id="ef1a2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1a2-123">Requirement</span></span> | <span data-ttu-id="ef1a2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ef1a2-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1a2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef1a2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1a2-126">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ef1a2-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ef1a2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef1a2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1a2-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ef1a2-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ef1a2-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef1a2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef1a2-130"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a2-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ef1a2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1a2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1a2-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1a2-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ef1a2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef1a2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1a2-134">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="ef1a2-134">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="ef1a2-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ef1a2-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ef1a2-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ef1a2-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ef1a2-137">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="ef1a2-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ef1a2-138">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="ef1a2-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ef1a2-139">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="ef1a2-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




