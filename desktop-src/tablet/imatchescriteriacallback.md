---
description: Expõe um método para avaliar se um objeto IContextNode atende ou falha em um critério especificado.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interface IMatchesCriteriaCallBack (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501411"
---
# <a name="imatchescriteriacallback-interface"></a><span data-ttu-id="5f9a6-103">Interface IMatchesCriteriaCallBack</span><span class="sxs-lookup"><span data-stu-id="5f9a6-103">IMatchesCriteriaCallBack interface</span></span>

<span data-ttu-id="5f9a6-104">Expõe um método para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em um critério especificado.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-104">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span>

## <a name="members"></a><span data-ttu-id="5f9a6-105">Membros</span><span class="sxs-lookup"><span data-stu-id="5f9a6-105">Members</span></span>

<span data-ttu-id="5f9a6-106">A interface **IMatchesCriteriaCallBack** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5f9a6-106">The **IMatchesCriteriaCallBack** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5f9a6-107">**IMatchesCriteriaCallBack** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f9a6-107">**IMatchesCriteriaCallBack** also has these types of members:</span></span>

-   [<span data-ttu-id="5f9a6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f9a6-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5f9a6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f9a6-109">Methods</span></span>

<span data-ttu-id="5f9a6-110">A interface **IMatchesCriteriaCallBack** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-110">The **IMatchesCriteriaCallBack** interface has these methods.</span></span>



| <span data-ttu-id="5f9a6-111">Método</span><span class="sxs-lookup"><span data-stu-id="5f9a6-111">Method</span></span>                                                                      | <span data-ttu-id="5f9a6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f9a6-112">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f9a6-113">**EvaluateContextNode**</span><span class="sxs-lookup"><span data-stu-id="5f9a6-113">**EvaluateContextNode**</span></span>](imatchescriteriacallback-evaluatecontextnode.md) | <span data-ttu-id="5f9a6-114">Quando substituído em uma classe derivada, avalia se um objeto [**IContextNode**](icontextnode.md) especificado atende aos critérios.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-114">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f9a6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f9a6-115">Remarks</span></span>

<span data-ttu-id="5f9a6-116">Para usar o método [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), crie uma classe que implemente **IMatchesCriteriaCallBack**.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-116">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements **IMatchesCriteriaCallBack**.</span></span> <span data-ttu-id="5f9a6-117">Implemente [**IMatchesCriteriaCallBack:: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) para retornar **Variant \_ true** se o objeto [**IContextNode**](icontextnode.md) corresponder aos seus critérios e **Variant \_ false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5f9a6-117">Implement [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="5f9a6-118">Para alguns critérios, talvez seja necessário fornecer um meio de inicializar ou manter o estado do seu objeto **IMatchesCriteriaCallBack** .</span><span class="sxs-lookup"><span data-stu-id="5f9a6-118">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f9a6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f9a6-119">Requirements</span></span>



| <span data-ttu-id="5f9a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f9a6-120">Requirement</span></span> | <span data-ttu-id="5f9a6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5f9a6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9a6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f9a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9a6-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5f9a6-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f9a6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f9a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9a6-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5f9a6-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5f9a6-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f9a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f9a6-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5f9a6-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5f9a6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5f9a6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f9a6-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f9a6-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5f9a6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f9a6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9a6-131">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="5f9a6-131">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="5f9a6-132">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="5f9a6-132">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="5f9a6-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="5f9a6-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

