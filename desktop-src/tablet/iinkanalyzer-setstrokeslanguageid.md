---
description: Altera o identificador de localidade para os traços especificados.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'Método IInkAnalyzer:: SetStrokesLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760564"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a><span data-ttu-id="4edd6-103">Método IInkAnalyzer:: SetStrokesLanguageId</span><span class="sxs-lookup"><span data-stu-id="4edd6-103">IInkAnalyzer::SetStrokesLanguageId method</span></span>

<span data-ttu-id="4edd6-104">Altera o identificador de localidade para os traços especificados.</span><span class="sxs-lookup"><span data-stu-id="4edd6-104">Changes the locale identifier for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4edd6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4edd6-105">Syntax</span></span>


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a><span data-ttu-id="4edd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4edd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4edd6-107">*ulStrokeIdCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4edd6-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4edd6-108">O número de identificadores de traço em *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="4edd6-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="4edd6-109">*plStrokes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4edd6-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4edd6-110">A matriz de identificadores para os traços aos quais atribuir o identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="4edd6-110">The array of identifiers for the strokes to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4edd6-111">*lStrokesLCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4edd6-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4edd6-112">O identificador de localidade a ser atribuído aos traços.</span><span class="sxs-lookup"><span data-stu-id="4edd6-112">The locale identifier to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4edd6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4edd6-113">Return value</span></span>

<span data-ttu-id="4edd6-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4edd6-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4edd6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4edd6-115">Remarks</span></span>

<span data-ttu-id="4edd6-116">A localidade de um traço é definida quando você adiciona o traço chamando [**IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md), o método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), o método [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)ou o [**método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="4edd6-116">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="4edd6-117">Para obter a localidade atualmente atribuída a um traço, chame o [**método IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="4edd6-117">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="4edd6-118">Os traços especificados são movidos para um nó de tinta não classificado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)) que contém traços do mesmo idioma.</span><span class="sxs-lookup"><span data-stu-id="4edd6-118">The specified strokes are moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="4edd6-119">Se não existir tal [**IContextNode**](icontextnode.md) , esse método criará um novo nó de tinta não classificada e moverá os traços para ele.</span><span class="sxs-lookup"><span data-stu-id="4edd6-119">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the strokes to it.</span></span> <span data-ttu-id="4edd6-120">Um nó de tinta não classificado é um **IContextNode** que tem um tipo de UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="4edd6-120">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="4edd6-121">Se esse método mover traços de um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado, esse método também adicionará as caixas delimitadoras de traços à região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="4edd6-121">If this method moves strokes from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the strokes' bounding boxes to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="4edd6-122">Esse método não moverá um traço se o parâmetro *lStrokeLCID* corresponder ao identificador de idioma atual do traço.</span><span class="sxs-lookup"><span data-stu-id="4edd6-122">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="4edd6-123">Se um traço especificado não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.</span><span class="sxs-lookup"><span data-stu-id="4edd6-123">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="4edd6-124">Se nenhum dos traços especificados identificar um traço associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="4edd6-124">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="4edd6-125">Esse método retorna um código de erro quando strokeIds é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4edd6-125">This method returns an error code when strokeIds is **NULL**.</span></span>

<span data-ttu-id="4edd6-126">Para obter mais informações sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="4edd6-126">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="4edd6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4edd6-127">Requirements</span></span>



| <span data-ttu-id="4edd6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4edd6-128">Requirement</span></span> | <span data-ttu-id="4edd6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4edd6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4edd6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4edd6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4edd6-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4edd6-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4edd6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4edd6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4edd6-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4edd6-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4edd6-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4edd6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4edd6-135"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4edd6-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4edd6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4edd6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4edd6-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4edd6-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4edd6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4edd6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4edd6-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4edd6-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4edd6-140">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="4edd6-140">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="4edd6-141">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="4edd6-141">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="4edd6-142">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="4edd6-142">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="4edd6-143">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="4edd6-143">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="4edd6-144">**Método IInkAnalyzer:: GetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="4edd6-144">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="4edd6-145">**Método IInkAnalyzer:: SetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="4edd6-145">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="4edd6-146">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="4edd6-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

