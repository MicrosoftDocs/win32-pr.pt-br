---
description: Recupera todos os objetos IContextNode do tipo especificado que são descendentes do objeto IContextNode especificado.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'Método IInkAnalyzer:: FindNodesOfTypeInSubTree (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 545e56d297b053b5b6f5dc61f944d6a4f6d4e03c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772537"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a><span data-ttu-id="2cff0-103">Método IInkAnalyzer:: FindNodesOfTypeInSubTree</span><span class="sxs-lookup"><span data-stu-id="2cff0-103">IInkAnalyzer::FindNodesOfTypeInSubTree method</span></span>

<span data-ttu-id="2cff0-104">Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado que são descendentes do objeto **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="2cff0-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects of the specified type that are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cff0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cff0-105">Syntax</span></span>


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="2cff0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cff0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cff0-107">*pNodeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cff0-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cff0-108">O **GUID** que especifica o tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="2cff0-108">The **GUID** that specifies the node type.</span></span>

</dd> <dt>

<span data-ttu-id="2cff0-109">*pContextNodeToSearchFrom* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cff0-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cff0-110">O objeto [**IContextNode**](icontextnode.md) cujos descendentes são pesquisados.</span><span class="sxs-lookup"><span data-stu-id="2cff0-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="2cff0-111">*ppContextNodesFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2cff0-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cff0-112">A coleção [**IContextNodes**](icontextnodes.md) que contém todos os nós do tipo *pNodeType* que são descendentes de *pContextNodeToSearchFrom*.</span><span class="sxs-lookup"><span data-stu-id="2cff0-112">The [**IContextNodes**](icontextnodes.md) collection containing all nodes of type *pNodeType* that are descendants of *pContextNodeToSearchFrom*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cff0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cff0-113">Return value</span></span>

<span data-ttu-id="2cff0-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2cff0-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2cff0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cff0-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="2cff0-116">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="2cff0-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="2cff0-117">Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver o nó *pContextNodeToSearchFrom* , esse método retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="2cff0-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="2cff0-118">A propriedade *pNodeType* deve conter um GUID (identificador global exclusivo) das constantes de [tipos de nó de contexto](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="2cff0-118">The *pNodeType* property must contain a globally unique identifier (GUID) from the [Context Node Types](context-node-types.md) constants.</span></span>

<span data-ttu-id="2cff0-119">Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver tal [**IContextNode**](icontextnode.md), uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.</span><span class="sxs-lookup"><span data-stu-id="2cff0-119">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cff0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cff0-120">Requirements</span></span>



| <span data-ttu-id="2cff0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cff0-121">Requirement</span></span> | <span data-ttu-id="2cff0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2cff0-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cff0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cff0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2cff0-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2cff0-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2cff0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cff0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2cff0-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2cff0-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2cff0-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2cff0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cff0-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2cff0-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2cff0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2cff0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cff0-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cff0-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2cff0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cff0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cff0-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2cff0-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2cff0-133">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="2cff0-133">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="2cff0-134">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="2cff0-134">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="2cff0-135">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="2cff0-135">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="2cff0-136">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="2cff0-136">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="2cff0-137">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="2cff0-137">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="2cff0-138">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="2cff0-138">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="2cff0-139">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="2cff0-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="2cff0-140">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="2cff0-140">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="2cff0-141">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="2cff0-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

