---
description: Obtém os objetos IContextNode associados a essa alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Método IAnalysisAlternate:: GetAlternateNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759921"
---
# <a name="ianalysisalternategetalternatenodes-method"></a><span data-ttu-id="a32b1-103">Método IAnalysisAlternate:: GetAlternateNodes</span><span class="sxs-lookup"><span data-stu-id="a32b1-103">IAnalysisAlternate::GetAlternateNodes method</span></span>

<span data-ttu-id="a32b1-104">Obtém os objetos [**IContextNode**](icontextnode.md) associados a essa alternativa.</span><span class="sxs-lookup"><span data-stu-id="a32b1-104">Gets the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="a32b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a32b1-105">Syntax</span></span>


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a><span data-ttu-id="a32b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a32b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a32b1-107">*ppAlternateNodes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a32b1-107">*ppAlternateNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a32b1-108">Um ponteiro para a coleção [**IContextNodes**](icontextnodes.md) que contém objetos [**IContextNode**](icontextnode.md) associados a essa alternativa.</span><span class="sxs-lookup"><span data-stu-id="a32b1-108">A pointer to the [**IContextNodes**](icontextnodes.md) collection that contains [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a32b1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a32b1-109">Return value</span></span>

<span data-ttu-id="a32b1-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a32b1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a32b1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a32b1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a32b1-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppAlternateNodes* quando você não precisar mais usar a coleção de nós de contexto.</span><span class="sxs-lookup"><span data-stu-id="a32b1-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternateNodes* when you no longer need to use the context node collection.</span></span>

 

<span data-ttu-id="a32b1-113">Esse método retorna os nós de contexto folha que estão associados a essa alternativa.</span><span class="sxs-lookup"><span data-stu-id="a32b1-113">This method returns the leaf context nodes that are associated with this alternate.</span></span> <span data-ttu-id="a32b1-114">Exemplos de nós folha são nós de contexto InkWord, textword, Image, InkDrawing e InkBullet.</span><span class="sxs-lookup"><span data-stu-id="a32b1-114">Examples of leaf nodes are InkWord, TextWord, Image, InkDrawing, and InkBullet context nodes.</span></span> <span data-ttu-id="a32b1-115">Para obter mais informações, consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipos de nó de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="a32b1-115">For more information, see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md).</span></span>

<span data-ttu-id="a32b1-116">Como elas correspondem a alternativas, esses objetos [**IContextNode**](icontextnode.md) não são descendentes do **IContextNode** raiz do objeto [**IInkAnalyzer**](iinkanalyzer.md) (Confira o [**método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)), a menos que eles sejam a alternativa principal, que é o primeiro elemento em uma coleção [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="a32b1-116">Because they correspond to alternates, these [**IContextNode**](icontextnode.md) objects are not descendants of the [**IInkAnalyzer**](iinkanalyzer.md) object's root **IContextNode** (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)) unless they are the top alternate, which is the first element in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a32b1-117">Requirements</span></span>



| <span data-ttu-id="a32b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a32b1-118">Requirement</span></span> | <span data-ttu-id="a32b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a32b1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a32b1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a32b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a32b1-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a32b1-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a32b1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a32b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a32b1-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a32b1-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a32b1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a32b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a32b1-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a32b1-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a32b1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a32b1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a32b1-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a32b1-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a32b1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a32b1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a32b1-129">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="a32b1-129">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="a32b1-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a32b1-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a32b1-131">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="a32b1-131">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="a32b1-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="a32b1-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> <dt>

[<span data-ttu-id="a32b1-133">System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes</span><span class="sxs-lookup"><span data-stu-id="a32b1-133">System.Windows.Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes</span></span>](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

