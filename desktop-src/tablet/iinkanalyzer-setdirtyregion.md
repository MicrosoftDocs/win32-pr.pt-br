---
description: Modifica a área que foi alterada desde a última operação de análise.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Método IInkAnalyzer:: SetDirtyRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090516"
---
# <a name="iinkanalyzersetdirtyregion-method"></a><span data-ttu-id="f39aa-103">Método IInkAnalyzer:: SetDirtyRegion</span><span class="sxs-lookup"><span data-stu-id="f39aa-103">IInkAnalyzer::SetDirtyRegion method</span></span>

<span data-ttu-id="f39aa-104">Modifica a área que foi alterada desde a última operação de análise.</span><span class="sxs-lookup"><span data-stu-id="f39aa-104">Modifies the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f39aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f39aa-105">Syntax</span></span>


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="f39aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f39aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f39aa-107">*pDirtyRegion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f39aa-107">*pDirtyRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f39aa-108">Um [**IAnalysisRegion**](ianalysisregion.md) que descreve a área que foi alterada desde a última operação de análise.</span><span class="sxs-lookup"><span data-stu-id="f39aa-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f39aa-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f39aa-109">Return value</span></span>

<span data-ttu-id="f39aa-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f39aa-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f39aa-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f39aa-111">Remarks</span></span>

<span data-ttu-id="f39aa-112">Esse método identifica as áreas que precisam ser analisadas ou analisadas novamente.</span><span class="sxs-lookup"><span data-stu-id="f39aa-112">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="f39aa-113">Todos os métodos [**IInkAnalyzer**](iinkanalyzer.md) que adicionam, atualizam ou removem dados de traço atualizam a região suja.</span><span class="sxs-lookup"><span data-stu-id="f39aa-113">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="f39aa-114">Para marcar manualmente uma área para reanálise:</span><span class="sxs-lookup"><span data-stu-id="f39aa-114">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="f39aa-115">Obtenha a região suja usando o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).</span><span class="sxs-lookup"><span data-stu-id="f39aa-115">Get the dirty region using [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md).</span></span>
2.  <span data-ttu-id="f39aa-116">Use o método [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) ou [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) para adicionar a área à região da etapa 1.</span><span class="sxs-lookup"><span data-stu-id="f39aa-116">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="f39aa-117">Use o **método IInkAnalyzer:: SetDirtyRegion** para atualizar a região suja.</span><span class="sxs-lookup"><span data-stu-id="f39aa-117">Use **IInkAnalyzer::SetDirtyRegion Method** to update the dirty region.</span></span>

<span data-ttu-id="f39aa-118">O [**IInkAnalyzer**](iinkanalyzer.md) analisa a tinta em sua região suja durante uma chamada para o método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="f39aa-118">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="f39aa-119">No entanto, o **IInkAnalyzer** pode expandir a operação de análise para incluir regiões vizinhas.</span><span class="sxs-lookup"><span data-stu-id="f39aa-119">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f39aa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f39aa-120">Requirements</span></span>



| <span data-ttu-id="f39aa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f39aa-121">Requirement</span></span> | <span data-ttu-id="f39aa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f39aa-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f39aa-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f39aa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f39aa-124">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f39aa-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f39aa-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f39aa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f39aa-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f39aa-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f39aa-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f39aa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f39aa-128"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f39aa-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f39aa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f39aa-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f39aa-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f39aa-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f39aa-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f39aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f39aa-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f39aa-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f39aa-133">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="f39aa-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="f39aa-134">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="f39aa-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="f39aa-135">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="f39aa-135">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="f39aa-136">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="f39aa-136">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="f39aa-137">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="f39aa-137">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="f39aa-138">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="f39aa-138">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="f39aa-139">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="f39aa-139">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="f39aa-140">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="f39aa-140">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="f39aa-141">**Método IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="f39aa-141">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="f39aa-142">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="f39aa-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




