---
description: Recupera todos os objetos IContextNode que correspondem aos critérios especificados.
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'Método IInkAnalyzer:: FindNodesWithCallBack (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647232"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a><span data-ttu-id="43d2a-103">Método IInkAnalyzer:: FindNodesWithCallBack</span><span class="sxs-lookup"><span data-stu-id="43d2a-103">IInkAnalyzer::FindNodesWithCallBack method</span></span>

<span data-ttu-id="43d2a-104">Recupera todos os objetos [**IContextNode**](icontextnode.md) que correspondem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="43d2a-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="43d2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43d2a-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="43d2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43d2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43d2a-107">*pCriteria* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43d2a-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43d2a-108">Um objeto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) que é usado para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em seus critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="43d2a-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="43d2a-109">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43d2a-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43d2a-110">Um ponteiro para a coleção [**IContextNodes**](icontextnodes.md) que contém todos os nós que atendem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="43d2a-110">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43d2a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43d2a-111">Return value</span></span>

<span data-ttu-id="43d2a-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="43d2a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43d2a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="43d2a-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="43d2a-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="43d2a-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="43d2a-115">Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver tal [**IContextNode**](icontextnode.md), uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="43d2a-115">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d2a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43d2a-116">Requirements</span></span>



| <span data-ttu-id="43d2a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="43d2a-117">Requirement</span></span> | <span data-ttu-id="43d2a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="43d2a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d2a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43d2a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43d2a-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="43d2a-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="43d2a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43d2a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43d2a-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="43d2a-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="43d2a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43d2a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d2a-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="43d2a-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="43d2a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="43d2a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43d2a-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43d2a-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="43d2a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="43d2a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d2a-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="43d2a-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="43d2a-129">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="43d2a-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="43d2a-130">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="43d2a-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="43d2a-131">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="43d2a-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="43d2a-132">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="43d2a-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="43d2a-133">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="43d2a-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="43d2a-134">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="43d2a-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="43d2a-135">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="43d2a-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="43d2a-136">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="43d2a-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="43d2a-137">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="43d2a-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

