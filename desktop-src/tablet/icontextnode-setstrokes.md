---
description: Associa os traços especificados a este IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'Método IContextNode:: setstrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772603"
---
# <a name="icontextnodesetstrokes-method"></a><span data-ttu-id="3dddc-103">Método IContextNode:: setstrokes</span><span class="sxs-lookup"><span data-stu-id="3dddc-103">IContextNode::SetStrokes method</span></span>

<span data-ttu-id="3dddc-104">Associa os traços especificados a este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="3dddc-104">Associates the specified strokes with this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3dddc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dddc-105">Syntax</span></span>


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="3dddc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dddc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dddc-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3dddc-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dddc-108">O número de identificadores de traço em *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="3dddc-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="3dddc-109">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3dddc-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dddc-110">Os identificadores dos traços a serem associados a este [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="3dddc-110">The identifiers of the strokes to associate with this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dddc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3dddc-111">Return value</span></span>

<span data-ttu-id="3dddc-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3dddc-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3dddc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dddc-113">Remarks</span></span>

<span data-ttu-id="3dddc-114">Esse método não atualiza a região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="3dddc-114">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="3dddc-115">Use esse método quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3dddc-115">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="3dddc-116">Use esse método para atribuir dados de traço a um nó de contexto específico.</span><span class="sxs-lookup"><span data-stu-id="3dddc-116">Use this method to assign stroke data to a specific context node.</span></span> <span data-ttu-id="3dddc-117">Para obter mais informações sobre como sincronizar os dados do aplicativo com o **IInkAnalyzer**, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3dddc-117">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="3dddc-118">Se qualquer um dos traços especificados já estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="3dddc-118">If any of the specified strokes are already associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dddc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dddc-119">Requirements</span></span>



| <span data-ttu-id="3dddc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dddc-120">Requirement</span></span> | <span data-ttu-id="3dddc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3dddc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dddc-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dddc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3dddc-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3dddc-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3dddc-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dddc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3dddc-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3dddc-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3dddc-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dddc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dddc-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3dddc-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3dddc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3dddc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dddc-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dddc-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3dddc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dddc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dddc-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3dddc-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3dddc-132">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="3dddc-132">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="3dddc-133">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="3dddc-133">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="3dddc-134">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="3dddc-134">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="3dddc-135">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="3dddc-135">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="3dddc-136">**Método IInkAnalyzer:: AddStrokesToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="3dddc-136">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="3dddc-137">**Método IInkAnalyzer:: AddStrokeToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="3dddc-137">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="3dddc-138">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="3dddc-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="3dddc-139">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="3dddc-139">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="3dddc-140">**IContextNode:: getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="3dddc-140">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="3dddc-141">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="3dddc-141">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="3dddc-142">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="3dddc-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




