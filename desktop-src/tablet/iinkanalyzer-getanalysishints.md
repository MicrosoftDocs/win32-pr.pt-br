---
description: Obtém todos os objetos IContextNode da dica de análise que estão anexados ao IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'Método IInkAnalyzer:: GetAnalysisHints (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090524"
---
# <a name="iinkanalyzergetanalysishints-method"></a><span data-ttu-id="77e51-103">Método IInkAnalyzer:: GetAnalysisHints</span><span class="sxs-lookup"><span data-stu-id="77e51-103">IInkAnalyzer::GetAnalysisHints method</span></span>

<span data-ttu-id="77e51-104">Obtém todos os objetos [**IContextNode**](icontextnode.md) da dica de análise que estão anexados ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="77e51-104">Gets all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="77e51-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77e51-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="77e51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77e51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e51-107">*ppAnalysisHints* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="77e51-107">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77e51-108">Um ponteiro para todos os objetos de dica de análise [**IContextNode**](icontextnode.md) no [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="77e51-108">A pointer to all the analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e51-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77e51-109">Return value</span></span>

<span data-ttu-id="77e51-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="77e51-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77e51-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="77e51-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="77e51-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAnalysisHints* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="77e51-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="77e51-113">Esse método retornará uma coleção vazia se nenhum nó de dica de análise estiver anexado ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="77e51-113">This method returns an empty collection if no analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="77e51-114">Um nó de dica de análise é um [**IContextNode**](icontextnode.md) com um tipo de nó de contexto AnalysisHint (consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="77e51-114">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="77e51-115">Para adicionar informações de contexto à dica, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) com o parâmetro *pPropertyDataId* definido como um dos identificadores GLOBALmente exclusivos (GUIDs) nas constantes de [Propriedades da dica de análise](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="77e51-115">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="77e51-116">Para descobrir quais valores de propriedade são definidos em um nó de contexto, use [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="77e51-116">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="77e51-117">Para localizar o valor de uma propriedade, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="77e51-117">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77e51-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77e51-118">Requirements</span></span>



| <span data-ttu-id="77e51-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e51-119">Requirement</span></span> | <span data-ttu-id="77e51-120">Valor</span><span class="sxs-lookup"><span data-stu-id="77e51-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e51-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77e51-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77e51-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="77e51-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="77e51-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77e51-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77e51-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="77e51-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="77e51-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77e51-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="77e51-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="77e51-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="77e51-127">DLL</span><span class="sxs-lookup"><span data-stu-id="77e51-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77e51-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e51-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="77e51-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="77e51-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e51-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="77e51-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="77e51-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="77e51-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="77e51-132">**Método IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="77e51-132">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="77e51-133">**IInkAnalyzer: método eleteAnalysisHint de:D**</span><span class="sxs-lookup"><span data-stu-id="77e51-133">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="77e51-134">**Método IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="77e51-134">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="77e51-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="77e51-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

