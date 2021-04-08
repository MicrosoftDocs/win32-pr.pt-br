---
description: Recupera o objeto IContextNode para um GUID (identificador global exclusivo) especificado.
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'Método IInkAnalyzer:: FindNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010521"
---
# <a name="iinkanalyzerfindnode-method"></a><span data-ttu-id="37fc7-103">Método IInkAnalyzer:: FindNode</span><span class="sxs-lookup"><span data-stu-id="37fc7-103">IInkAnalyzer::FindNode method</span></span>

<span data-ttu-id="37fc7-104">Recupera o objeto [**IContextNode**](icontextnode.md) para um GUID (identificador global exclusivo) especificado.</span><span class="sxs-lookup"><span data-stu-id="37fc7-104">Retrieves the [**IContextNode**](icontextnode.md) object for a specified globally unique identifier (GUID).</span></span>

## <a name="syntax"></a><span data-ttu-id="37fc7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37fc7-105">Syntax</span></span>


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a><span data-ttu-id="37fc7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37fc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37fc7-107">*pid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37fc7-107">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37fc7-108">O identificador do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="37fc7-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="37fc7-109">*ppContextNodeFound* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="37fc7-109">*ppContextNodeFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37fc7-110">Um ponteiro para o objeto [**IContextNode**](icontextnode.md) com o identificador *pid* .</span><span class="sxs-lookup"><span data-stu-id="37fc7-110">A pointer to the [**IContextNode**](icontextnode.md) object with the *pId* identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37fc7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37fc7-111">Return value</span></span>

<span data-ttu-id="37fc7-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="37fc7-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37fc7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="37fc7-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="37fc7-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeFound* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="37fc7-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="37fc7-115">Se nenhum objeto [**IContextNode**](icontextnode.md) existir como um descendente do nó raiz [**IInkAnalyzer**](iinkanalyzer.md) , **NULL** será retornado.</span><span class="sxs-lookup"><span data-stu-id="37fc7-115">If no such [**IContextNode**](icontextnode.md) object exists as a descendant of the [**IInkAnalyzer**](iinkanalyzer.md) root node, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="37fc7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37fc7-116">Requirements</span></span>



| <span data-ttu-id="37fc7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37fc7-117">Requirement</span></span> | <span data-ttu-id="37fc7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="37fc7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37fc7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37fc7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="37fc7-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="37fc7-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="37fc7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37fc7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="37fc7-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="37fc7-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="37fc7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37fc7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="37fc7-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="37fc7-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37fc7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="37fc7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37fc7-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37fc7-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="37fc7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="37fc7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fc7-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="37fc7-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="37fc7-129">**Método IInkAnalyzer:: FindInkLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="37fc7-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="37fc7-130">**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="37fc7-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="37fc7-131">**Método IInkAnalyzer:: FindLeafNodes**</span><span class="sxs-lookup"><span data-stu-id="37fc7-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="37fc7-132">**Método IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="37fc7-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="37fc7-133">**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="37fc7-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="37fc7-134">**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="37fc7-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="37fc7-135">**Método IInkAnalyzer:: FindNodesWithCallBack**</span><span class="sxs-lookup"><span data-stu-id="37fc7-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="37fc7-136">**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**</span><span class="sxs-lookup"><span data-stu-id="37fc7-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="37fc7-137">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="37fc7-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

