---
description: Altera a alternativa superior atual para a alternativa especificada e limpa o tipo de confirmação para todos os objetos IContextNode associados à alternativa.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Método IInkAnalyzer:: ModifyTopAlternate (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793615"
---
# <a name="iinkanalyzermodifytopalternate-method"></a><span data-ttu-id="44b6c-103">Método IInkAnalyzer:: ModifyTopAlternate</span><span class="sxs-lookup"><span data-stu-id="44b6c-103">IInkAnalyzer::ModifyTopAlternate method</span></span>

<span data-ttu-id="44b6c-104">Altera a alternativa superior atual para a alternativa especificada e limpa o tipo de confirmação para todos os objetos [**IContextNode**](icontextnode.md) associados à alternativa.</span><span class="sxs-lookup"><span data-stu-id="44b6c-104">Changes the current top alternate to the specified alternate and clears the confirmation type for all [**IContextNode**](icontextnode.md) objects associated with the alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="44b6c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44b6c-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="44b6c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44b6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44b6c-107">*pAlternate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="44b6c-107">*pAlternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44b6c-108">O objeto [**IAnalysisAlternate**](ianalysisalternate.md) que contém a nova alternativa Top.</span><span class="sxs-lookup"><span data-stu-id="44b6c-108">The [**IAnalysisAlternate**](ianalysisalternate.md) object containing the new top alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44b6c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44b6c-109">Return value</span></span>

<span data-ttu-id="44b6c-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="44b6c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44b6c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="44b6c-111">Remarks</span></span>

<span data-ttu-id="44b6c-112">Para obter alternativas de análise, use o método [**IInkAnalyzer:: Getalternations**](iinkanalyzer-getalternates.md), [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="44b6c-112">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="44b6c-113">Para obter os objetos [**IContextNode**](icontextnode.md) associados a uma alternativa de análise, use o [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="44b6c-113">To get the [**IContextNode**](icontextnode.md) objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="44b6c-114">Para alterar o tipo de confirmação para um nó de contexto, use [**IContextNode:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="44b6c-114">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44b6c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44b6c-115">Requirements</span></span>



| <span data-ttu-id="44b6c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b6c-116">Requirement</span></span> | <span data-ttu-id="44b6c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="44b6c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b6c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44b6c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44b6c-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="44b6c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="44b6c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44b6c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44b6c-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="44b6c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="44b6c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44b6c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="44b6c-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="44b6c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="44b6c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="44b6c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44b6c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44b6c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="44b6c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="44b6c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b6c-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="44b6c-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="44b6c-128">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="44b6c-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="44b6c-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="44b6c-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="44b6c-130">**Confirmtype**</span><span class="sxs-lookup"><span data-stu-id="44b6c-130">**ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="44b6c-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="44b6c-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




