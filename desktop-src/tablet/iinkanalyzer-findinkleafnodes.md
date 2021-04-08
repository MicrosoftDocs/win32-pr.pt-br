---
description: Recupera todos os nós folha de tinta.
ms.assetid: 988ae9f9-8fca-4757-8eb0-ae161e5690c9
title: 'Método IInkAnalyzer:: FindInkLeafNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5ebcfe542ab03f2e3d3a24c29142e41433c9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827178"
---
# <a name="iinkanalyzerfindinkleafnodes-method"></a><span data-ttu-id="a6859-103">Método IInkAnalyzer:: FindInkLeafNodes</span><span class="sxs-lookup"><span data-stu-id="a6859-103">IInkAnalyzer::FindInkLeafNodes method</span></span>

<span data-ttu-id="a6859-104">Recupera todos os nós folha de tinta.</span><span class="sxs-lookup"><span data-stu-id="a6859-104">Retrieves all of the ink leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6859-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6859-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="a6859-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6859-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6859-107">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a6859-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6859-108">Um ponteiro para a coleção [**IContextNodes**](icontextnodes.md) que contém todos os nós folha de tinta.</span><span class="sxs-lookup"><span data-stu-id="a6859-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all ink leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6859-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6859-109">Return value</span></span>

<span data-ttu-id="a6859-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a6859-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6859-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6859-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a6859-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="a6859-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a6859-113">Os nós folha não contêm nós filho.</span><span class="sxs-lookup"><span data-stu-id="a6859-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="a6859-114">Os nós de tinta contêm dados de traço.</span><span class="sxs-lookup"><span data-stu-id="a6859-114">Ink nodes contain stroke data.</span></span> <span data-ttu-id="a6859-115">Exemplos de nós folha de tinta são objetos InkWord, InkDrawing e InkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="a6859-115">Examples of ink leaf nodes are InkWord, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="a6859-116">Para obter mais informações, consulte [tipos de nó de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="a6859-116">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6859-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6859-117">Requirements</span></span>



| <span data-ttu-id="a6859-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6859-118">Requirement</span></span> | <span data-ttu-id="a6859-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a6859-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6859-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6859-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a6859-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a6859-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a6859-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6859-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a6859-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a6859-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a6859-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6859-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6859-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a6859-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a6859-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a6859-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6859-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6859-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a6859-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6859-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6859-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a6859-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a6859-130">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="a6859-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a6859-131">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="a6859-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="a6859-132">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="a6859-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="a6859-133">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="a6859-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="a6859-134">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="a6859-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="a6859-135">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="a6859-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="a6859-136">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="a6859-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="a6859-137">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="a6859-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="a6859-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="a6859-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

