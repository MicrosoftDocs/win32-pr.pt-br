---
description: Ocorre antes de o IInkAnalyzer mover um objeto IContextNode alterando seu nó pai.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: 'Evento _IAnalysisProxyEvents:: ContextNodeReparenting (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105782479"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a><span data-ttu-id="2419f-103">\_Evento IAnalysisProxyEvents:: ContextNodeReparenting</span><span class="sxs-lookup"><span data-stu-id="2419f-103">\_IAnalysisProxyEvents::ContextNodeReparenting event</span></span>

<span data-ttu-id="2419f-104">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) mover um objeto [**IContextNode**](icontextnode.md) alterando seu nó pai.</span><span class="sxs-lookup"><span data-stu-id="2419f-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span>

## <a name="syntax"></a><span data-ttu-id="2419f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2419f-105">Syntax</span></span>


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a><span data-ttu-id="2419f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2419f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2419f-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2419f-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2419f-108">O objeto [**IInkAnalyzer**](iinkanalyzer.md) que move o objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="2419f-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2419f-109">*pNewParentContextNode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2419f-109">*pNewParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2419f-110">O novo objeto pai [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="2419f-110">The new parent [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2419f-111">*pContextNodeToBeReparented* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2419f-111">*pContextNodeToBeReparented* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2419f-112">O objeto [**IContextNode**](icontextnode.md) a ser movido.</span><span class="sxs-lookup"><span data-stu-id="2419f-112">The [**IContextNode**](icontextnode.md) object to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2419f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2419f-113">Return value</span></span>

<span data-ttu-id="2419f-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2419f-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2419f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2419f-115">Remarks</span></span>

<span data-ttu-id="2419f-116">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="2419f-116">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="2419f-117">Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método que move um [**IContextNode**](icontextnode.md) de uma coleção de subnós para outra (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="2419f-117">This event occurs during the reconcile phase of ink analysis, or in response to a method that moves an [**IContextNode**](icontextnode.md) from one collection of subnodes to another (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="2419f-118">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2419f-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2419f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2419f-119">Requirements</span></span>



| <span data-ttu-id="2419f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2419f-120">Requirement</span></span> | <span data-ttu-id="2419f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2419f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2419f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2419f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2419f-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2419f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2419f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2419f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2419f-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2419f-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2419f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2419f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2419f-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2419f-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2419f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2419f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2419f-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2419f-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2419f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2419f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2419f-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="2419f-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="2419f-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2419f-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2419f-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="2419f-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2419f-134">**IContextNode::GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="2419f-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="2419f-135">**IContextNode::GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="2419f-135">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="2419f-136">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="2419f-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="2419f-137">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="2419f-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="2419f-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="2419f-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




