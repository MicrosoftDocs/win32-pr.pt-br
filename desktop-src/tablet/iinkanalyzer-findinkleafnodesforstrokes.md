---
description: Recupera os nós folha de tinta que contêm os traços especificados.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: 'Método IInkAnalyzer:: FindInkLeafNodesForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d19bed823f5385533dfc938eb9f6013b4a5640c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827176"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a><span data-ttu-id="d7631-103">Método IInkAnalyzer:: FindInkLeafNodesForStrokes</span><span class="sxs-lookup"><span data-stu-id="d7631-103">IInkAnalyzer::FindInkLeafNodesForStrokes method</span></span>

<span data-ttu-id="d7631-104">Recupera os nós folha de tinta que contêm os traços especificados.</span><span class="sxs-lookup"><span data-stu-id="d7631-104">Retrieves the ink leaf nodes that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7631-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7631-105">Syntax</span></span>


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="d7631-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7631-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7631-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7631-108">O número de identificadores de traço passados.</span><span class="sxs-lookup"><span data-stu-id="d7631-108">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="d7631-109">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7631-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7631-110">Uma matriz dos identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="d7631-110">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="d7631-111">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7631-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7631-112">A coleção de objetos [**IContextNode**](icontextnode.md) que contém todos os nós folha de tinta que contêm os traços com identificadores na matriz *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="d7631-112">The collection of [**IContextNode**](icontextnode.md) objects that contain all the ink leaf nodes that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7631-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7631-113">Return value</span></span>

<span data-ttu-id="d7631-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d7631-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7631-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7631-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d7631-116">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="d7631-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="d7631-117">Os nós folha não contêm nós filho.</span><span class="sxs-lookup"><span data-stu-id="d7631-117">Leaf nodes do not contain child nodes.</span></span> <span data-ttu-id="d7631-118">Os nós de tinta contêm dados de traço.</span><span class="sxs-lookup"><span data-stu-id="d7631-118">Ink nodes contain stroke data.</span></span> <span data-ttu-id="d7631-119">Exemplos de nós de folha de tinta são objetos InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d7631-119">Examples of ink leaf nodes are InkWord, InkDrawing, andInkBullet [**IContextNode**](icontextnode.md) objects.</span></span> <span data-ttu-id="d7631-120">Para obter mais informações, consulte [tipos de nó de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="d7631-120">For more information, see [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="d7631-121">Se nenhum nó contiver os traços especificados, uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="d7631-121">If no nodes contain the specified strokes, an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span> <span data-ttu-id="d7631-122">Da mesma forma, se *ulStrokeIdsCount* for zero, uma coleção **IContextNodes** vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="d7631-122">Similarly, if *ulStrokeIdsCount* is zero, an empty **IContextNodes** collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7631-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7631-123">Requirements</span></span>



| <span data-ttu-id="d7631-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7631-124">Requirement</span></span> | <span data-ttu-id="d7631-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d7631-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7631-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7631-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7631-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d7631-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d7631-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7631-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7631-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d7631-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d7631-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7631-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7631-131"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d7631-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d7631-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d7631-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7631-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7631-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d7631-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7631-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7631-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d7631-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d7631-136">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="d7631-136">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="d7631-137">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="d7631-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="d7631-138">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="d7631-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="d7631-139">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="d7631-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="d7631-140">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="d7631-140">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="d7631-141">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="d7631-141">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="d7631-142">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="d7631-142">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="d7631-143">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="d7631-143">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="d7631-144">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="d7631-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

