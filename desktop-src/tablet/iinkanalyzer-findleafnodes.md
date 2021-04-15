---
description: Recupera todos os nós folha.
ms.assetid: 5534053c-c5b9-4576-857f-c8af39e821a7
title: 'Método IInkAnalyzer:: FindLeafNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindLeafNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f923afe94c25e45dbcbfe79d554282b69ebec3a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501804"
---
# <a name="iinkanalyzerfindleafnodes-method"></a><span data-ttu-id="75ee1-103">Método IInkAnalyzer:: FindLeafNodes</span><span class="sxs-lookup"><span data-stu-id="75ee1-103">IInkAnalyzer::FindLeafNodes method</span></span>

<span data-ttu-id="75ee1-104">Recupera todos os nós folha.</span><span class="sxs-lookup"><span data-stu-id="75ee1-104">Retrieves all of the leaf nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ee1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75ee1-105">Syntax</span></span>


```C++
HRESULT FindLeafNodes(
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="75ee1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75ee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ee1-107">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="75ee1-107">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75ee1-108">Um ponteiro para a coleção [**IContextNodes**](icontextnodes.md) que contém todos os nós folha.</span><span class="sxs-lookup"><span data-stu-id="75ee1-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all leaf nodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ee1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75ee1-109">Return value</span></span>

<span data-ttu-id="75ee1-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="75ee1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75ee1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="75ee1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="75ee1-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="75ee1-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="75ee1-113">Os nós folha não contêm nós filho.</span><span class="sxs-lookup"><span data-stu-id="75ee1-113">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="75ee1-114">Exemplos de nós folha de tinta são objetos InkWord, textword, Image, InkDrawing e InkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="75ee1-114">Examples of ink leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="75ee1-115">Para obter mais informações, consulte [tipos de nó de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="75ee1-115">For more information, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75ee1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75ee1-116">Requirements</span></span>



| <span data-ttu-id="75ee1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="75ee1-117">Requirement</span></span> | <span data-ttu-id="75ee1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="75ee1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75ee1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75ee1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="75ee1-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="75ee1-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75ee1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75ee1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="75ee1-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="75ee1-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="75ee1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75ee1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="75ee1-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75ee1-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75ee1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="75ee1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75ee1-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75ee1-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="75ee1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="75ee1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ee1-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="75ee1-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="75ee1-129">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="75ee1-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="75ee1-130">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="75ee1-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="75ee1-131">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="75ee1-131">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="75ee1-132">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="75ee1-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="75ee1-133">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="75ee1-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="75ee1-134">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="75ee1-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="75ee1-135">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="75ee1-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="75ee1-136">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="75ee1-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="75ee1-137">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="75ee1-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

