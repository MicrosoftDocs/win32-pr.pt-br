---
description: Remove os traços especificados do IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Método IInkAnalyzer:: RemoveStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090521"
---
# <a name="iinkanalyzerremovestrokes-method"></a><span data-ttu-id="9bb5c-103">Método IInkAnalyzer:: RemoveStrokes</span><span class="sxs-lookup"><span data-stu-id="9bb5c-103">IInkAnalyzer::RemoveStrokes method</span></span>

<span data-ttu-id="9bb5c-104">Remove os traços especificados do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9bb5c-104">Removes the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb5c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bb5c-105">Syntax</span></span>


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="9bb5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bb5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bb5c-107">*ulStrokeIdCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9bb5c-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb5c-108">O número de identificadores de traço em *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="9bb5c-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="9bb5c-109">*plStrokes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9bb5c-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb5c-110">Os identificadores para os traços a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="9bb5c-110">The identifiers for the strokes to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bb5c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9bb5c-111">Return value</span></span>

<span data-ttu-id="9bb5c-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9bb5c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9bb5c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bb5c-113">Remarks</span></span>

<span data-ttu-id="9bb5c-114">Esse método remove os dados de pacote e faz referência aos traços especificados do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9bb5c-114">This method removes the packet data for and references to the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="9bb5c-115">Esse método remove os traços do nó de contexto folha que faz referência aos traços.</span><span class="sxs-lookup"><span data-stu-id="9bb5c-115">This method removes the strokes from the leaf context node that references the strokes.</span></span> <span data-ttu-id="9bb5c-116">Se qualquer [**IContextNode**](icontextnode.md) não fizer mais referência a traços, esse método excluirá os objetos **IContextNode** e **IContextNode** ancestral que não têm mais nenhum nó filho.</span><span class="sxs-lookup"><span data-stu-id="9bb5c-116">If any [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="9bb5c-117">Depois que esse método remove os traços do [**IContextNode**](icontextnode.md), ele atualiza a região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) para incluir a caixa delimitadora dos traços removidos.</span><span class="sxs-lookup"><span data-stu-id="9bb5c-117">After this method removes the strokes from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed strokes.</span></span>

<span data-ttu-id="9bb5c-118">Se um traço identificado em *plStrokes* não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.</span><span class="sxs-lookup"><span data-stu-id="9bb5c-118">If a stroke identified in *plStrokes* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="9bb5c-119">Se nenhum dos traços identificados em *plStrokes* estiver associado ao analisador de tinta, esse método retornará sem Atualizar o [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9bb5c-119">If none of the strokes identified in *plStrokes* are associated with the ink analyzer, this method returns without updating the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="9bb5c-120">Esse método retorna e o código de erro quando *plStrokes* é nulo.</span><span class="sxs-lookup"><span data-stu-id="9bb5c-120">This method returns and error code when *plStrokes* is null.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb5c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bb5c-121">Requirements</span></span>



| <span data-ttu-id="9bb5c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bb5c-122">Requirement</span></span> | <span data-ttu-id="9bb5c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9bb5c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb5c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bb5c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9bb5c-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9bb5c-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9bb5c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bb5c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9bb5c-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9bb5c-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9bb5c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bb5c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bb5c-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9bb5c-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9bb5c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9bb5c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bb5c-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bb5c-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9bb5c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bb5c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb5c-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9bb5c-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9bb5c-134">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="9bb5c-134">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="9bb5c-135">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="9bb5c-135">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="9bb5c-136">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="9bb5c-136">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="9bb5c-137">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="9bb5c-137">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="9bb5c-138">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="9bb5c-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="9bb5c-139">**Método IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="9bb5c-139">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="9bb5c-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="9bb5c-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




