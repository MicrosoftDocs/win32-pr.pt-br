---
description: Altera a alternativa superior atual para o IAnalysisAlternate especificado.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296387"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a><span data-ttu-id="2a7a2-103">Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation</span><span class="sxs-lookup"><span data-stu-id="2a7a2-103">IInkAnalyzer::ModifyTopAlternateWithConfirmation method</span></span>

<span data-ttu-id="2a7a2-104">Altera a alternativa superior atual para o [**IAnalysisAlternate**](ianalysisalternate.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="2a7a2-104">Changes the current top alternate to the specified [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a7a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a7a2-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a><span data-ttu-id="2a7a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a7a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a7a2-107">*alternativo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a7a2-107">*alternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7a2-108">A análise alterna para definir como a nova alternativa principal.</span><span class="sxs-lookup"><span data-stu-id="2a7a2-108">The analysis alternate to set as the new top alternate.</span></span>

</dd> <dt>

<span data-ttu-id="2a7a2-109">*fconfirmAutomatically* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2a7a2-109">*fconfirmAutomatically* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a7a2-110">**Variante \_ TRUE** para definir todos os nós de contexto de folha de tinta que correspondem à análise alternada para um tipo de confirmação de **confirmation \_ NodeTypeAndProperties** (consulte [**IContextNode::**](icontextnode-isconfirmed.md) IsDeleted [**e confirmtype**](confirmationtype.md)); **Variante \_ FALSE** para definir todos os nós de contexto de folha de tinta que correspondem à análise alternada para um tipo de confirmação de **confirmações \_ nenhum**.</span><span class="sxs-lookup"><span data-stu-id="2a7a2-110">**VARIANT\_TRUE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_NodeTypeAndProperties** (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) and [**ConfirmationType**](confirmationtype.md)); **VARIANT\_FALSE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_None**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a7a2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a7a2-111">Return value</span></span>

<span data-ttu-id="2a7a2-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2a7a2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a7a2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a7a2-113">Remarks</span></span>

<span data-ttu-id="2a7a2-114">Para obter alternativas de análise, use o método [**IInkAnalyzer:: Getalternations**](iinkanalyzer-getalternates.md), [**IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)ou [**IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="2a7a2-114">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="2a7a2-115">Para obter os objetos de nó de contexto associados a uma alternativa de análise, use o [**método IAnalysisAlternate:: GetAlternateNodes**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="2a7a2-115">To get the context node objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="2a7a2-116">Para alterar o tipo de confirmação para um nó de contexto, use [**IContextNode:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="2a7a2-116">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7a2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a7a2-117">Requirements</span></span>



| <span data-ttu-id="2a7a2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a7a2-118">Requirement</span></span> | <span data-ttu-id="2a7a2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2a7a2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7a2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a7a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a7a2-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2a7a2-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2a7a2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a7a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a7a2-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2a7a2-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2a7a2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a7a2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a7a2-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2a7a2-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2a7a2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2a7a2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a7a2-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a7a2-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2a7a2-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a7a2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7a2-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="2a7a2-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2a7a2-130">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="2a7a2-130">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="2a7a2-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="2a7a2-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2a7a2-132">**Confirmação de análise de tinta**</span><span class="sxs-lookup"><span data-stu-id="2a7a2-132">**Ink Analysis ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="2a7a2-133">Referência</span><span class="sxs-lookup"><span data-stu-id="2a7a2-133">Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




