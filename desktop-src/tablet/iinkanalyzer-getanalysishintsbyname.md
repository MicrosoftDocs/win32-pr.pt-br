---
description: Recupera todos os objetos IContextNode da dica de análise que estão anexados ao IInkAnalyzer e que têm o nome especificado.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'Método IInkAnalyzer:: GetAnalysisHintsByName (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164539"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a><span data-ttu-id="ca2ef-103">Método IInkAnalyzer:: GetAnalysisHintsByName</span><span class="sxs-lookup"><span data-stu-id="ca2ef-103">IInkAnalyzer::GetAnalysisHintsByName method</span></span>

<span data-ttu-id="ca2ef-104">Recupera todos os objetos [**IContextNode**](icontextnode.md) da dica de análise que estão anexados ao [**IInkAnalyzer**](iinkanalyzer.md) e que têm o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="ca2ef-104">Retrieves all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md) and that have the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca2ef-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="ca2ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca2ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca2ef-107">*dicaname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca2ef-107">*hintName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2ef-108">O nome da dica para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ca2ef-108">The hint name for which to search.</span></span>

</dd> <dt>

<span data-ttu-id="ca2ef-109">*ppAnalysisHints* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ca2ef-109">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca2ef-110">A dica de análise [**IContextNode**](icontextnode.md) objetos no [**IInkAnalyzer**](iinkanalyzer.md) que têm o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="ca2ef-110">The analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) that have the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca2ef-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca2ef-111">Return value</span></span>

<span data-ttu-id="ca2ef-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md) os valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="ca2ef-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca2ef-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca2ef-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ca2ef-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAnalysisHints* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ca2ef-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ca2ef-115">Esse método retornará uma coleção vazia se nenhum nó de dica de análise for anexado ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ca2ef-115">This method returns an empty collection if no such analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="ca2ef-116">Um nó de dica de análise é um [**IContextNode**](icontextnode.md) com um tipo de nó de contexto AnalysisHint (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="ca2ef-116">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="ca2ef-117">Para adicionar informações de contexto à dica, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) com o parâmetro *pPropertyDataId* definido como um dos identificadores GLOBALmente exclusivos (GUIDs) nas constantes de [Propriedades da dica de análise](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="ca2ef-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="ca2ef-118">Para descobrir quais valores de propriedade são definidos em um nó de contexto, use [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="ca2ef-118">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="ca2ef-119">Para localizar o valor de uma propriedade, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="ca2ef-119">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2ef-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca2ef-120">Requirements</span></span>



| <span data-ttu-id="ca2ef-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca2ef-121">Requirement</span></span> | <span data-ttu-id="ca2ef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ca2ef-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2ef-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca2ef-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2ef-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ca2ef-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca2ef-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca2ef-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2ef-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ca2ef-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ca2ef-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca2ef-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca2ef-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ca2ef-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ca2ef-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ca2ef-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca2ef-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca2ef-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ca2ef-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca2ef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca2ef-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ca2ef-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ca2ef-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ca2ef-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ca2ef-134">**Método IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="ca2ef-134">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="ca2ef-135">**IInkAnalyzer: método eleteAnalysisHint de:D**</span><span class="sxs-lookup"><span data-stu-id="ca2ef-135">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="ca2ef-136">**Método IInkAnalyzer:: GetAnalysisHints**</span><span class="sxs-lookup"><span data-stu-id="ca2ef-136">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="ca2ef-137">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="ca2ef-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

