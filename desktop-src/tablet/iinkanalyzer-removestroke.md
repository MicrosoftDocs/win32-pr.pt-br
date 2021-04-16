---
description: Remove o traço especificado do IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'Método IInkAnalyzer:: RemoveStroke (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501800"
---
# <a name="iinkanalyzerremovestroke-method"></a><span data-ttu-id="7dcce-103">Método IInkAnalyzer:: RemoveStroke</span><span class="sxs-lookup"><span data-stu-id="7dcce-103">IInkAnalyzer::RemoveStroke method</span></span>

<span data-ttu-id="7dcce-104">Remove o traço especificado do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7dcce-104">Removes the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcce-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7dcce-105">Syntax</span></span>


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="7dcce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dcce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dcce-107">*plStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7dcce-107">*plStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dcce-108">O identificador de traço.</span><span class="sxs-lookup"><span data-stu-id="7dcce-108">The stroke identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dcce-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7dcce-109">Return value</span></span>

<span data-ttu-id="7dcce-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7dcce-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7dcce-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dcce-111">Remarks</span></span>

<span data-ttu-id="7dcce-112">Esse método remove os dados de pacote para, e referências a, o traço especificado do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7dcce-112">This method removes the packet data for, and references to, the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="7dcce-113">Esse método remove o traço do nó de contexto folha que faz referência ao traço.</span><span class="sxs-lookup"><span data-stu-id="7dcce-113">This method removes the stroke from the leaf context node that references the stroke.</span></span> <span data-ttu-id="7dcce-114">Se o [**IContextNode**](icontextnode.md) não fizer mais referência a traços, esse método excluirá os objetos **IContextNode** e **IContextNode** ancestral que não têm mais nenhum nó filho.</span><span class="sxs-lookup"><span data-stu-id="7dcce-114">If the [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="7dcce-115">Depois que esse método remove o traço do [**IContextNode**](icontextnode.md), ele atualiza a região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) para incluir a caixa delimitadora do traço removido.</span><span class="sxs-lookup"><span data-stu-id="7dcce-115">After this method removes the stroke from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed stroke.</span></span>

<span data-ttu-id="7dcce-116">Se *plStrokeId* não identificar um traço associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o analisador de tinta.</span><span class="sxs-lookup"><span data-stu-id="7dcce-116">If *plStrokeId* does not identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the ink analyzer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dcce-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dcce-117">Requirements</span></span>



| <span data-ttu-id="7dcce-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dcce-118">Requirement</span></span> | <span data-ttu-id="7dcce-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7dcce-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dcce-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dcce-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7dcce-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7dcce-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7dcce-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dcce-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7dcce-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7dcce-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7dcce-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7dcce-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dcce-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7dcce-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7dcce-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7dcce-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dcce-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dcce-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7dcce-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7dcce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dcce-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7dcce-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7dcce-130">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="7dcce-130">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="7dcce-131">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="7dcce-131">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="7dcce-132">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="7dcce-132">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="7dcce-133">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="7dcce-133">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="7dcce-134">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="7dcce-134">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="7dcce-135">**Método IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="7dcce-135">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="7dcce-136">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="7dcce-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




