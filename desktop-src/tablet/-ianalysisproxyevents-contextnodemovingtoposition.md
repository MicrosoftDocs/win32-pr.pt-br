---
description: Ocorre antes de o IInkAnalyzer mover um objeto IContextNode para uma nova posição dentro de sua coleção de subnós do nó pai.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: 'Evento _IAnalysisProxyEvents:: ContextNodeMovingToPosition (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105782480"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a><span data-ttu-id="b81df-103">\_Evento IAnalysisProxyEvents:: ContextNodeMovingToPosition</span><span class="sxs-lookup"><span data-stu-id="b81df-103">\_IAnalysisProxyEvents::ContextNodeMovingToPosition event</span></span>

<span data-ttu-id="b81df-104">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) mover um objeto [**IContextNode**](icontextnode.md) para uma nova posição dentro de sua coleção de subnós do nó pai.</span><span class="sxs-lookup"><span data-stu-id="b81df-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b81df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b81df-105">Syntax</span></span>


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b81df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b81df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b81df-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b81df-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b81df-108">O objeto [**IInkAnalyzer**](iinkanalyzer.md) que move o objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b81df-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b81df-109">*pISubNodeToMove* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b81df-109">*pISubNodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b81df-110">O objeto [**IContextNode**](icontextnode.md) a ser movido.</span><span class="sxs-lookup"><span data-stu-id="b81df-110">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="b81df-111">*pParentContextNode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b81df-111">*pParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b81df-112">O objeto [**IContextNode**](icontextnode.md) pai de *pISubNodeToMove*.</span><span class="sxs-lookup"><span data-stu-id="b81df-112">The parent [**IContextNode**](icontextnode.md) object of *pISubNodeToMove*.</span></span>

</dd> <dt>

<span data-ttu-id="b81df-113">*ulNewIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b81df-113">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b81df-114">O novo local de *pISubNodeToMove* em sua coleção de subnós do nó pai.</span><span class="sxs-lookup"><span data-stu-id="b81df-114">The new location of *pISubNodeToMove* in its parent node's collection of subnodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b81df-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b81df-115">Return value</span></span>

<span data-ttu-id="b81df-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b81df-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b81df-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b81df-117">Remarks</span></span>

<span data-ttu-id="b81df-118">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b81df-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="b81df-119">Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método do analisador de tinta que move um [**IContextNode**](icontextnode.md) dentro de sua coleção de subnós do nó pai (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="b81df-119">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that moves an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="b81df-120">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b81df-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b81df-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b81df-121">Requirements</span></span>



| <span data-ttu-id="b81df-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81df-122">Requirement</span></span> | <span data-ttu-id="b81df-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b81df-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b81df-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b81df-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b81df-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b81df-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b81df-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b81df-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b81df-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b81df-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b81df-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b81df-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b81df-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b81df-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b81df-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b81df-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b81df-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b81df-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b81df-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b81df-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81df-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="b81df-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="b81df-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b81df-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b81df-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b81df-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b81df-136">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="b81df-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b81df-137">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="b81df-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b81df-138">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="b81df-138">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="b81df-139">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="b81df-139">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="b81df-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b81df-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




