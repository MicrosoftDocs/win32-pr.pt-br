---
description: Recupera a área que foi alterada desde a última operação de análise.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'Método IInkAnalyzer:: GetDirtyRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164538"
---
# <a name="iinkanalyzergetdirtyregion-method"></a><span data-ttu-id="dbb42-103">Método IInkAnalyzer:: GetDirtyRegion</span><span class="sxs-lookup"><span data-stu-id="dbb42-103">IInkAnalyzer::GetDirtyRegion method</span></span>

<span data-ttu-id="dbb42-104">Recupera a área que foi alterada desde a última operação de análise.</span><span class="sxs-lookup"><span data-stu-id="dbb42-104">Retrieves the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbb42-105">Syntax</span></span>


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="dbb42-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbb42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbb42-107">*ppDirtyRegion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dbb42-107">*ppDirtyRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbb42-108">Um [**IAnalysisRegion**](ianalysisregion.md) que descreve a área que foi alterada desde a última operação de análise.</span><span class="sxs-lookup"><span data-stu-id="dbb42-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbb42-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbb42-109">Return value</span></span>

<span data-ttu-id="dbb42-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dbb42-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbb42-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbb42-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dbb42-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppDirtyRegion* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="dbb42-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppDirtyRegion* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="dbb42-113">Esse método identifica as áreas que precisam ser analisadas ou analisadas novamente.</span><span class="sxs-lookup"><span data-stu-id="dbb42-113">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="dbb42-114">Todos os métodos [**IInkAnalyzer**](iinkanalyzer.md) que adicionam, atualizam ou removem dados de traço atualizam a região suja.</span><span class="sxs-lookup"><span data-stu-id="dbb42-114">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="dbb42-115">Para marcar manualmente uma área para reanálise:</span><span class="sxs-lookup"><span data-stu-id="dbb42-115">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="dbb42-116">Obtenha a região suja usando o **método IInkAnalyzer:: GetDirtyRegion**.</span><span class="sxs-lookup"><span data-stu-id="dbb42-116">Get the dirty region using **IInkAnalyzer::GetDirtyRegion Method**.</span></span>
2.  <span data-ttu-id="dbb42-117">Use o método [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) ou [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) para adicionar a área à região da etapa 1.</span><span class="sxs-lookup"><span data-stu-id="dbb42-117">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="dbb42-118">Use o [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para atualizar a região suja.</span><span class="sxs-lookup"><span data-stu-id="dbb42-118">Use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to update the dirty region.</span></span>

<span data-ttu-id="dbb42-119">O [**IInkAnalyzer**](iinkanalyzer.md) analisa a tinta em sua região suja durante uma chamada para o método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="dbb42-119">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="dbb42-120">No entanto, o **IInkAnalyzer** pode expandir a operação de análise para incluir regiões vizinhas.</span><span class="sxs-lookup"><span data-stu-id="dbb42-120">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="dbb42-121">Esta propriedade pode conter áreas não adjacentes.</span><span class="sxs-lookup"><span data-stu-id="dbb42-121">This property may contain nonadjacent areas.</span></span>

<span data-ttu-id="dbb42-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória da matriz *ppDirtyRegion* quando tiver terminado de usá-la.</span><span class="sxs-lookup"><span data-stu-id="dbb42-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory from the *ppDirtyRegion* array when you are finished with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb42-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbb42-123">Requirements</span></span>



| <span data-ttu-id="dbb42-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbb42-124">Requirement</span></span> | <span data-ttu-id="dbb42-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dbb42-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb42-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb42-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb42-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dbb42-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dbb42-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbb42-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb42-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dbb42-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dbb42-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbb42-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb42-131"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dbb42-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dbb42-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dbb42-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbb42-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbb42-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dbb42-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbb42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb42-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="dbb42-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dbb42-136">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="dbb42-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="dbb42-137">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="dbb42-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="dbb42-138">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="dbb42-138">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="dbb42-139">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="dbb42-139">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="dbb42-140">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="dbb42-140">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="dbb42-141">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="dbb42-141">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="dbb42-142">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="dbb42-142">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="dbb42-143">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="dbb42-143">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="dbb42-144">**Método IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="dbb42-144">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="dbb42-145">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="dbb42-145">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

