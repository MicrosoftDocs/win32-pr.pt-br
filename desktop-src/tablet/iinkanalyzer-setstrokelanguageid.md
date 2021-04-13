---
description: Altera o identificador de localidade para o traço especificado.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'Método IInkAnalyzer:: SetStrokeLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501796"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a><span data-ttu-id="57a8c-103">Método IInkAnalyzer:: SetStrokeLanguageId</span><span class="sxs-lookup"><span data-stu-id="57a8c-103">IInkAnalyzer::SetStrokeLanguageId method</span></span>

<span data-ttu-id="57a8c-104">Altera o identificador de localidade para o traço especificado.</span><span class="sxs-lookup"><span data-stu-id="57a8c-104">Changes the locale identifier for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57a8c-105">Syntax</span></span>


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="57a8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57a8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a8c-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57a8c-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a8c-108">O identificador do traço ao qual atribuir o identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="57a8c-108">The identifier of the stroke to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="57a8c-109">*lStrokeLCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57a8c-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a8c-110">O identificador de localidade a ser atribuído ao traço.</span><span class="sxs-lookup"><span data-stu-id="57a8c-110">The locale identifier to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a8c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57a8c-111">Return value</span></span>

<span data-ttu-id="57a8c-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="57a8c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="57a8c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="57a8c-113">Remarks</span></span>

<span data-ttu-id="57a8c-114">A localidade de um traço é definida quando você adiciona o traço chamando [**IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md), o método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), o método [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)ou o [**método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="57a8c-114">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="57a8c-115">Para obter a localidade atualmente atribuída a um traço, chame o [**método IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="57a8c-115">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="57a8c-116">O traço especificado é movido para um nó de tinta não classificado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)) que contém traços do mesmo idioma.</span><span class="sxs-lookup"><span data-stu-id="57a8c-116">The specified stroke is moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="57a8c-117">Se não existir tal [**IContextNode**](icontextnode.md) , esse método criará um novo nó de tinta não classificada e moverá o traço para ele.</span><span class="sxs-lookup"><span data-stu-id="57a8c-117">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the stroke to it.</span></span> <span data-ttu-id="57a8c-118">Um nó de tinta não classificado é um **IContextNode** que tem um tipo de UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="57a8c-118">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="57a8c-119">Se esse método mover um traço de um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado, esse método também adicionará a caixa delimitadora do traço à região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="57a8c-119">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="57a8c-120">Esse método não moverá um traço se o parâmetro *lStrokeLCID* corresponder ao identificador de idioma atual do traço.</span><span class="sxs-lookup"><span data-stu-id="57a8c-120">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="57a8c-121">Se o traço especificado não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="57a8c-121">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="57a8c-122">Para obter mais informações sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="57a8c-122">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="57a8c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a8c-123">Requirements</span></span>



| <span data-ttu-id="57a8c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a8c-124">Requirement</span></span> | <span data-ttu-id="57a8c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="57a8c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a8c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a8c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="57a8c-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="57a8c-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="57a8c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57a8c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="57a8c-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="57a8c-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="57a8c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57a8c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a8c-131"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="57a8c-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="57a8c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="57a8c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57a8c-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57a8c-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="57a8c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="57a8c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a8c-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="57a8c-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="57a8c-136">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="57a8c-136">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="57a8c-137">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="57a8c-137">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="57a8c-138">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="57a8c-138">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="57a8c-139">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="57a8c-139">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="57a8c-140">**Método IInkAnalyzer:: GetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="57a8c-140">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="57a8c-141">**Método IInkAnalyzer:: SetStrokesLanguageId**</span><span class="sxs-lookup"><span data-stu-id="57a8c-141">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="57a8c-142">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="57a8c-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

