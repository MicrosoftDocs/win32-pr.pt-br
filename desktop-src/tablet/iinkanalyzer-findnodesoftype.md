---
description: Recupera todos os objetos IContextNode do tipo especificado.
ms.assetid: e6e68d78-9697-40e6-a4ae-a187ef01a769
title: 'Método IInkAnalyzer:: FindNodesOfType (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 51611fd4b3c77b43f2ea0d967f81dcc9547edb24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827175"
---
# <a name="iinkanalyzerfindnodesoftype-method"></a><span data-ttu-id="adf07-103">Método IInkAnalyzer:: FindNodesOfType</span><span class="sxs-lookup"><span data-stu-id="adf07-103">IInkAnalyzer::FindNodesOfType method</span></span>

<span data-ttu-id="adf07-104">Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="adf07-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adf07-105">Syntax</span></span>


```C++
HRESULT FindNodesOfType(
  [in]  const GUID          *pNodeType,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="adf07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adf07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf07-107">*pNodeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adf07-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adf07-108">O **GUID** que especifica o tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="adf07-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="adf07-109">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="adf07-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adf07-110">Um ponteiro para o [**IContextNodes**](icontextnodes.md) que contém todos os nós do tipo *pNodeType*.</span><span class="sxs-lookup"><span data-stu-id="adf07-110">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes of type *pNodeType*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf07-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="adf07-111">Return value</span></span>

<span data-ttu-id="adf07-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="adf07-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="adf07-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="adf07-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="adf07-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="adf07-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="adf07-115">A propriedade *pNodeType* deve conter um GUID das constantes de [tipos de nó de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="adf07-115">The *pNodeType* property must contain a GUID from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="adf07-116">Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver tal [**IContextNode**](icontextnode.md), uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="adf07-116">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf07-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adf07-117">Requirements</span></span>



| <span data-ttu-id="adf07-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf07-118">Requirement</span></span> | <span data-ttu-id="adf07-119">Valor</span><span class="sxs-lookup"><span data-stu-id="adf07-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf07-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf07-120">Minimum supported client</span></span><br/> | <span data-ttu-id="adf07-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="adf07-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="adf07-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf07-122">Minimum supported server</span></span><br/> | <span data-ttu-id="adf07-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="adf07-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="adf07-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="adf07-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf07-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="adf07-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="adf07-126">DLL</span><span class="sxs-lookup"><span data-stu-id="adf07-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adf07-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf07-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="adf07-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="adf07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf07-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="adf07-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="adf07-130">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="adf07-130">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="adf07-131">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="adf07-131">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="adf07-132">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="adf07-132">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="adf07-133">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="adf07-133">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="adf07-134">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="adf07-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="adf07-135">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="adf07-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="adf07-136">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="adf07-136">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="adf07-137">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="adf07-137">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="adf07-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="adf07-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

