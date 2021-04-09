---
description: Recupera alternativas de análise para os nós em uma coleção IContextNodes especificada.
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'Método IInkAnalyzer:: GetAlternatesForContextNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090526"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a><span data-ttu-id="6c4c2-103">Método IInkAnalyzer:: GetAlternatesForContextNodes</span><span class="sxs-lookup"><span data-stu-id="6c4c2-103">IInkAnalyzer::GetAlternatesForContextNodes method</span></span>

<span data-ttu-id="6c4c2-104">Recupera alternativas de análise para os nós em uma coleção [**IContextNodes**](icontextnodes.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-104">Retrieves analysis alternates for the nodes in a specified [**IContextNodes**](icontextnodes.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c4c2-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="6c4c2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c4c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4c2-107">*pContextNodes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c4c2-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4c2-108">A coleção [**IContextNodes**](icontextnodes.md) para a qual as alternativas de análise são retornadas.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-108">The [**IContextNodes**](icontextnodes.md) collection for which the analysis alternatives are returned.</span></span>

</dd> <dt>

<span data-ttu-id="6c4c2-109">*ulMaximumAlternates* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6c4c2-109">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4c2-110">O número máximo de alternativas a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-110">The maximum number of alternatives to return.</span></span>

</dd> <dt>

<span data-ttu-id="6c4c2-111">*ppAlternates* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6c4c2-111">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4c2-112">O objeto [**IAnalysisAlternates**](ianalysisalternates.md) que contém as alternativas de análise.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-112">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4c2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-113">Return value</span></span>

<span data-ttu-id="6c4c2-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6c4c2-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c4c2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c4c2-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6c4c2-116">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAlternates* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="6c4c2-117">O [**IAnalysisAlternate**](ianalysisalternate.md) superior é retornado como a primeira alternativa da coleção.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-117">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="6c4c2-118">Os objetos [**IContextNode**](icontextnode.md) em *pContextNodes* não precisam representar áreas adjacentes do documento.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-118">The [**IContextNode**](icontextnode.md) objects in *pContextNodes* do not have to represent adjacent areas of the document.</span></span>

<span data-ttu-id="6c4c2-119">Para cada dica de análise em nós, o [**IInkAnalyzer**](iinkanalyzer.md) retorna apenas a alternativa superior.</span><span class="sxs-lookup"><span data-stu-id="6c4c2-119">For each analysis hint in nodes, the [**IInkAnalyzer**](iinkanalyzer.md) returns only the top alternate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c4c2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c4c2-120">Requirements</span></span>



| <span data-ttu-id="6c4c2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4c2-121">Requirement</span></span> | <span data-ttu-id="6c4c2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6c4c2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4c2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c4c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6c4c2-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6c4c2-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6c4c2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c4c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6c4c2-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6c4c2-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6c4c2-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c4c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c4c2-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c2-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6c4c2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6c4c2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c4c2-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c2-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6c4c2-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c4c2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4c2-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6c4c2-133">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-133">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="6c4c2-134">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-134">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="6c4c2-135">**Método IInkAnalyzer:: getalternations**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-135">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="6c4c2-136">**Método IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-136">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="6c4c2-137">**Método IInkAnalyzer:: ModifyTopAlternate**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-137">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="6c4c2-138">**Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation**</span><span class="sxs-lookup"><span data-stu-id="6c4c2-138">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="6c4c2-139">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="6c4c2-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

