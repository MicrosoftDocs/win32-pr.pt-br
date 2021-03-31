---
description: Recupera todos os objetos IContextNode que correspondem aos critérios especificados e são descendentes do objeto IContextNode especificado.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Método IInkAnalyzer:: FindNodesWithCallBackInSubTree (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647231"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a><span data-ttu-id="61fd7-103">Método IInkAnalyzer:: FindNodesWithCallBackInSubTree</span><span class="sxs-lookup"><span data-stu-id="61fd7-103">IInkAnalyzer::FindNodesWithCallBackInSubTree method</span></span>

<span data-ttu-id="61fd7-104">Recupera todos os objetos [**IContextNode**](icontextnode.md) que correspondem aos critérios especificados e são descendentes do objeto **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="61fd7-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria and are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61fd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61fd7-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="61fd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61fd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61fd7-107">*pCriteria* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61fd7-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fd7-108">Um objeto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) que é usado para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em seus critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="61fd7-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="61fd7-109">*pContextNodeToSearchFrom* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="61fd7-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61fd7-110">O objeto [**IContextNode**](icontextnode.md) cujos descendentes são pesquisados.</span><span class="sxs-lookup"><span data-stu-id="61fd7-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="61fd7-111">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="61fd7-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61fd7-112">Um ponteiro para o [**IContextNodes**](icontextnodes.md) que contém todos os nós que atendem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="61fd7-112">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61fd7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61fd7-113">Return value</span></span>

<span data-ttu-id="61fd7-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="61fd7-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="61fd7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="61fd7-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="61fd7-116">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="61fd7-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="61fd7-117">Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver o nó *pContextNodeToSearchFrom* , esse método retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="61fd7-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="61fd7-118">Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver tal [**IContextNode**](icontextnode.md), uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="61fd7-118">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="61fd7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61fd7-119">Requirements</span></span>



| <span data-ttu-id="61fd7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="61fd7-120">Requirement</span></span> | <span data-ttu-id="61fd7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="61fd7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fd7-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61fd7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61fd7-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="61fd7-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="61fd7-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61fd7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61fd7-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61fd7-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="61fd7-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61fd7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="61fd7-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="61fd7-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="61fd7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="61fd7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61fd7-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61fd7-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="61fd7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="61fd7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fd7-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="61fd7-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="61fd7-132">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="61fd7-132">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="61fd7-133">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="61fd7-133">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="61fd7-134">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="61fd7-134">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="61fd7-135">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="61fd7-135">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="61fd7-136">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="61fd7-136">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="61fd7-137">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="61fd7-137">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="61fd7-138">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="61fd7-138">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="61fd7-139">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="61fd7-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="61fd7-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="61fd7-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

