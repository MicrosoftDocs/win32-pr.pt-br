---
description: Recupera todos os objetos IContextNode do tipo especificado que contêm os traços especificados.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'Método IInkAnalyzer:: FindNodesOfTypeForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815475"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a><span data-ttu-id="10956-103">Método IInkAnalyzer:: FindNodesOfTypeForStrokes</span><span class="sxs-lookup"><span data-stu-id="10956-103">IInkAnalyzer::FindNodesOfTypeForStrokes method</span></span>

<span data-ttu-id="10956-104">Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado que contêm os traços especificados.</span><span class="sxs-lookup"><span data-stu-id="10956-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that contain the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="10956-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10956-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="10956-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10956-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10956-107">*pNodeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10956-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10956-108">O GUID (identificador global exclusivo) que especifica o tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="10956-108">The globally unique identifier (GUID) that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="10956-109">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10956-109">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10956-110">O número de identificadores de traço passados.</span><span class="sxs-lookup"><span data-stu-id="10956-110">The number of stroke identifiers passed in.</span></span>

</dd> <dt>

<span data-ttu-id="10956-111">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10956-111">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10956-112">Uma matriz dos identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="10956-112">An array of the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="10956-113">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10956-113">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10956-114">A coleção de objetos [**IContextNode**](icontextnode.md) que contém todos os nós do tipo *pNodeType* que contêm os traços com identificadores na matriz *plStrokeIds* .</span><span class="sxs-lookup"><span data-stu-id="10956-114">The collection of [**IContextNode**](icontextnode.md) objects that contain all the nodes of type *pNodeType* that contain the strokes with identifiers in the *plStrokeIds* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10956-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10956-115">Return value</span></span>

<span data-ttu-id="10956-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="10956-116">For a description of return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10956-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="10956-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="10956-118">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="10956-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="10956-119">A propriedade *pNodeType* deve conter um GUID das constantes de [tipos de nó de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="10956-119">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="10956-120">Se o tipo de nó especificado não for um nó folha, mas um dos descendentes do nó fizer referência a um traço na coleção de traços, esse nó será adicionado à coleção retornada.</span><span class="sxs-lookup"><span data-stu-id="10956-120">If the specified node type is not a leaf node, but one of the node's descendants references a stroke in the strokes collection, that node is added to the collection that is returned.</span></span>

<span data-ttu-id="10956-121">Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver tal [**IContextNode**](icontextnode.md), uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="10956-121">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="10956-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10956-122">Requirements</span></span>



| <span data-ttu-id="10956-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="10956-123">Requirement</span></span> | <span data-ttu-id="10956-124">Valor</span><span class="sxs-lookup"><span data-stu-id="10956-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10956-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10956-125">Minimum supported client</span></span><br/> | <span data-ttu-id="10956-126">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="10956-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="10956-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10956-127">Minimum supported server</span></span><br/> | <span data-ttu-id="10956-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="10956-128">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="10956-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10956-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="10956-130"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="10956-130"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="10956-131">DLL</span><span class="sxs-lookup"><span data-stu-id="10956-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10956-132"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10956-132"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="10956-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="10956-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10956-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="10956-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="10956-135">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="10956-135">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="10956-136">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="10956-136">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="10956-137">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="10956-137">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="10956-138">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="10956-138">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="10956-139">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="10956-139">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="10956-140">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="10956-140">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="10956-141">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="10956-141">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="10956-142">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="10956-142">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="10956-143">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="10956-143">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

