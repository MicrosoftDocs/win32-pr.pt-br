---
description: Remove uma dica de análise do IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: 'IInkAnalyzer: método eleteAnalysisHint de:D (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090530"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a><span data-ttu-id="aee68-103">IInkAnalyzer: método eleteAnalysisHint de:D</span><span class="sxs-lookup"><span data-stu-id="aee68-103">IInkAnalyzer::DeleteAnalysisHint method</span></span>

<span data-ttu-id="aee68-104">Remove uma dica de análise do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="aee68-104">Removes an analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aee68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aee68-105">Syntax</span></span>


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="aee68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aee68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee68-107">*pHintToDelete* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aee68-107">*pHintToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee68-108">A dica de análise do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="aee68-108">The analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee68-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aee68-109">Return value</span></span>

<span data-ttu-id="aee68-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="aee68-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aee68-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="aee68-111">Remarks</span></span>

<span data-ttu-id="aee68-112">Remover uma dica de análise não marca a área da dica para reanálise.</span><span class="sxs-lookup"><span data-stu-id="aee68-112">Removing an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="aee68-113">Para marcar a área dentro da dica para reanálise, use o [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para definir a região suja como a União da região suja atual e da área da dica de análise.</span><span class="sxs-lookup"><span data-stu-id="aee68-113">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="aee68-114">A dica é removida do analisador; no entanto, o próprio [**IContextNode**](icontextnode.md) não é excluído.</span><span class="sxs-lookup"><span data-stu-id="aee68-114">The hint is removed from the analyzer; however, the [**IContextNode**](icontextnode.md) itself is not deleted.</span></span>

<span data-ttu-id="aee68-115">Esse método retorna um código de erro quando *pHintToDelete* é um [**IContextNode**](icontextnode.md) que não é do tipo AnalysisHint (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="aee68-115">This method returns an error code when *pHintToDelete* is a [**IContextNode**](icontextnode.md) that is not of type AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="aee68-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aee68-116">Requirements</span></span>



| <span data-ttu-id="aee68-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee68-117">Requirement</span></span> | <span data-ttu-id="aee68-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aee68-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aee68-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee68-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aee68-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="aee68-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aee68-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee68-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aee68-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="aee68-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="aee68-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aee68-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee68-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="aee68-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aee68-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aee68-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee68-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee68-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="aee68-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="aee68-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee68-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="aee68-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="aee68-129">**Método IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="aee68-129">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="aee68-130">**Método IInkAnalyzer:: GetAnalysisHints**</span><span class="sxs-lookup"><span data-stu-id="aee68-130">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="aee68-131">**Método IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="aee68-131">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="aee68-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="aee68-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




