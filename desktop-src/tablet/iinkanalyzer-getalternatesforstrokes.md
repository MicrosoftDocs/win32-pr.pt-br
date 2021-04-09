---
description: Recupera as alternativas de análise para os traços com os identificadores de traço especificados.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Método IInkAnalyzer:: GetAlternatesForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090525"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a><span data-ttu-id="344c3-103">Método IInkAnalyzer:: GetAlternatesForStrokes</span><span class="sxs-lookup"><span data-stu-id="344c3-103">IInkAnalyzer::GetAlternatesForStrokes method</span></span>

<span data-ttu-id="344c3-104">Recupera as alternativas de análise para os traços com os identificadores de traço especificados.</span><span class="sxs-lookup"><span data-stu-id="344c3-104">Retrieves analysis alternates for the strokes with the specified stroke identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="344c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="344c3-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="344c3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="344c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="344c3-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="344c3-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="344c3-108">O número de identificadores de traço em *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="344c3-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="344c3-109">*plStrokes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="344c3-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="344c3-110">A matriz de identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="344c3-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="344c3-111">*ulMaximumAlternates* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="344c3-111">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="344c3-112">O número máximo de alternativas de análise retornado.</span><span class="sxs-lookup"><span data-stu-id="344c3-112">The maximum number of analysis alternatives returned.</span></span>

</dd> <dt>

<span data-ttu-id="344c3-113">*ppAlternates* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="344c3-113">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="344c3-114">O objeto [**IAnalysisAlternates**](ianalysisalternates.md) que contém as alternativas de análise.</span><span class="sxs-lookup"><span data-stu-id="344c3-114">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="344c3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="344c3-115">Return value</span></span>

<span data-ttu-id="344c3-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="344c3-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="344c3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="344c3-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="344c3-118">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppAlternates* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="344c3-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="344c3-119">O [**IAnalysisAlternate**](ianalysisalternate.md) superior é retornado como a primeira alternativa da coleção.</span><span class="sxs-lookup"><span data-stu-id="344c3-119">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="344c3-120">Os traços especificados não precisam representar áreas adjacentes do documento.</span><span class="sxs-lookup"><span data-stu-id="344c3-120">The specified strokes do not have to represent adjacent areas of the document.</span></span>

## <a name="requirements"></a><span data-ttu-id="344c3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="344c3-121">Requirements</span></span>



| <span data-ttu-id="344c3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="344c3-122">Requirement</span></span> | <span data-ttu-id="344c3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="344c3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="344c3-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="344c3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="344c3-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="344c3-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="344c3-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="344c3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="344c3-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="344c3-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="344c3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="344c3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="344c3-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="344c3-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="344c3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="344c3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="344c3-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="344c3-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="344c3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="344c3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344c3-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="344c3-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="344c3-134">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="344c3-134">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="344c3-135">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="344c3-135">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="344c3-136">**Método IInkAnalyzer:: getalternations**</span><span class="sxs-lookup"><span data-stu-id="344c3-136">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="344c3-137">**Método IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="344c3-137">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="344c3-138">**Método IInkAnalyzer:: ModifyTopAlternate**</span><span class="sxs-lookup"><span data-stu-id="344c3-138">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="344c3-139">**Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation**</span><span class="sxs-lookup"><span data-stu-id="344c3-139">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="344c3-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="344c3-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

