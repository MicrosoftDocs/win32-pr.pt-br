---
description: Quando substituído em uma classe derivada, avalia se um objeto IContextNode especificado atende aos critérios.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'Método IMatchesCriteriaCallBack:: EvaluateContextNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749703"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a><span data-ttu-id="34138-103">Método IMatchesCriteriaCallBack:: EvaluateContextNode</span><span class="sxs-lookup"><span data-stu-id="34138-103">IMatchesCriteriaCallBack::EvaluateContextNode method</span></span>

<span data-ttu-id="34138-104">Quando substituído em uma classe derivada, avalia se um objeto [**IContextNode**](icontextnode.md) especificado atende aos critérios.</span><span class="sxs-lookup"><span data-stu-id="34138-104">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="34138-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34138-105">Syntax</span></span>


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a><span data-ttu-id="34138-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34138-107">*pContextNodeToEvaluate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34138-107">*pContextNodeToEvaluate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34138-108">O objeto [**IContextNode**](icontextnode.md) a ser avaliado.</span><span class="sxs-lookup"><span data-stu-id="34138-108">The [**IContextNode**](icontextnode.md) object to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="34138-109">*pbResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="34138-109">*pbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34138-110">**Variante \_ TRUE** se *pContextNodeToEvaluate* corresponder aos critérios; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="34138-110">**VARIANT\_TRUE** if *pContextNodeToEvaluate* matches the criteria; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34138-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34138-111">Return value</span></span>

<span data-ttu-id="34138-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="34138-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34138-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="34138-113">Remarks</span></span>

<span data-ttu-id="34138-114">Para usar o método [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), crie uma classe que implemente [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span><span class="sxs-lookup"><span data-stu-id="34138-114">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span></span> <span data-ttu-id="34138-115">Implemente **IMatchesCriteriaCallBack:: EvaluateContextNode** para retornar **Variant \_ true** se o objeto [**IContextNode**](icontextnode.md) corresponder aos seus critérios e **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="34138-115">Implement **IMatchesCriteriaCallBack::EvaluateContextNode** to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="34138-116">Para alguns critérios, talvez seja necessário fornecer um meio de inicializar ou manter o estado do seu objeto **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="34138-116">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="34138-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34138-117">Requirements</span></span>



| <span data-ttu-id="34138-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34138-118">Requirement</span></span> | <span data-ttu-id="34138-119">Valor</span><span class="sxs-lookup"><span data-stu-id="34138-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34138-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34138-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34138-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="34138-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="34138-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34138-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34138-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="34138-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="34138-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34138-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34138-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="34138-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="34138-126">DLL</span><span class="sxs-lookup"><span data-stu-id="34138-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34138-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34138-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="34138-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="34138-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34138-129">**IMatchesCriteriaCallBack**</span><span class="sxs-lookup"><span data-stu-id="34138-129">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md)
</dt> <dt>

[<span data-ttu-id="34138-130">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="34138-130">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="34138-131">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="34138-131">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="34138-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="34138-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




