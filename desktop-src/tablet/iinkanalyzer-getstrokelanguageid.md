---
description: Retorna o identificador de localidade do traço especificado.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Método IInkAnalyzer:: GetStrokeLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647225"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a><span data-ttu-id="8d3d6-103">Método IInkAnalyzer:: GetStrokeLanguageId</span><span class="sxs-lookup"><span data-stu-id="8d3d6-103">IInkAnalyzer::GetStrokeLanguageId method</span></span>

<span data-ttu-id="8d3d6-104">Retorna o identificador de localidade do traço especificado.</span><span class="sxs-lookup"><span data-stu-id="8d3d6-104">Returns the locale identifier of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d3d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d3d6-105">Syntax</span></span>


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="8d3d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d3d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d3d6-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d3d6-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d3d6-108">O identificador de traço.</span><span class="sxs-lookup"><span data-stu-id="8d3d6-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8d3d6-109">*lStrokeLCID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d3d6-109">*lStrokeLCID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d3d6-110">O identificador de localidade para o traço especificado.</span><span class="sxs-lookup"><span data-stu-id="8d3d6-110">The locale identifier for the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d3d6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d3d6-111">Return value</span></span>

<span data-ttu-id="8d3d6-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8d3d6-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d3d6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d3d6-113">Remarks</span></span>

<span data-ttu-id="8d3d6-114">A localidade do traço é definida quando você adiciona o traço chamando [**IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md), o método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), o método [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)ou o [**método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="8d3d6-114">The stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="8d3d6-115">Para alterar a localidade do traço, use o método [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) ou o método [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="8d3d6-115">To change the stroke's locale, use [**IInkAnalyzer::SetStrokeLanguageId Method**](iinkanalyzer-setstrokelanguageid.md) or [**IInkAnalyzer::SetStrokesLanguageId Method**](iinkanalyzer-setstrokeslanguageid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d3d6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d3d6-116">Requirements</span></span>



| <span data-ttu-id="8d3d6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d3d6-117">Requirement</span></span> | <span data-ttu-id="8d3d6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8d3d6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d3d6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d3d6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d3d6-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8d3d6-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8d3d6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d3d6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d3d6-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8d3d6-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8d3d6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d3d6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d3d6-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8d3d6-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8d3d6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8d3d6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d3d6-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d3d6-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8d3d6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d3d6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d3d6-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8d3d6-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8d3d6-129">**Método IInkAnalyzer:: SetStrokeLanguageId**</span><span class="sxs-lookup"><span data-stu-id="8d3d6-129">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="8d3d6-130">**Método IInkAnalyzer:: SetStrokesLanguageId**</span><span class="sxs-lookup"><span data-stu-id="8d3d6-130">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="8d3d6-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="8d3d6-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




