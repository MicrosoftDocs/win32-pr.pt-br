---
description: Altera o tipo dos traços especificados.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'Método IInkAnalyzer:: setstrokestype (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768389"
---
# <a name="iinkanalyzersetstrokestype-method"></a><span data-ttu-id="694d1-103">Método IInkAnalyzer:: setstrokestype</span><span class="sxs-lookup"><span data-stu-id="694d1-103">IInkAnalyzer::SetStrokesType method</span></span>

<span data-ttu-id="694d1-104">Altera o tipo dos traços especificados.</span><span class="sxs-lookup"><span data-stu-id="694d1-104">Changes the type of the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="694d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="694d1-105">Syntax</span></span>


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="694d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="694d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="694d1-107">*strokeIdCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="694d1-107">*strokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="694d1-108">O número de identificadores de traço em *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="694d1-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="694d1-109">*plStrokes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="694d1-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="694d1-110">Uma matriz que contém os identificadores de traço dos traços aos quais atribuir *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="694d1-110">An array containing the stroke identifiers of the strokes to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="694d1-111">*StrokeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="694d1-111">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="694d1-112">O valor de [**StrokeType**](stroketype.md) a ser atribuído aos traços.</span><span class="sxs-lookup"><span data-stu-id="694d1-112">The [**StrokeType**](stroketype.md) value to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="694d1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="694d1-113">Return value</span></span>

<span data-ttu-id="694d1-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="694d1-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="694d1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="694d1-115">Remarks</span></span>

<span data-ttu-id="694d1-116">Se o tipo do traço for o [**valor de StrokeType**](stroketype.md) como não **\_ classificado**, o [**IInkAnalyzer**](iinkanalyzer.md) classificará o traço durante a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="694d1-116">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="694d1-117">Caso contrário, o **IInkAnalyzer** usará o tipo definido no traço.</span><span class="sxs-lookup"><span data-stu-id="694d1-117">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="694d1-118">O [**IInkAnalyzer**](iinkanalyzer.md) não define o valor do tipo Stroke como parte da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="694d1-118">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="694d1-119">Para especificar ou alterar o tipo de traço, use o método [**IInkAnalyzer:: Setstroketype**](iinkanalyzer-setstroketype.md) ou **IInkAnalyzer:: setstrokestype**.</span><span class="sxs-lookup"><span data-stu-id="694d1-119">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or **IInkAnalyzer::SetStrokesType Method**.</span></span>

<span data-ttu-id="694d1-120">Se um traço estiver associado a um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)), esse método move o traço para um nó de tinta não classificado que contém traços do mesmo idioma.</span><span class="sxs-lookup"><span data-stu-id="694d1-120">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="694d1-121">Se esse nó de contexto não existir, esse método criará um novo nó de tinta não classificada e adicionará o traço a ele.</span><span class="sxs-lookup"><span data-stu-id="694d1-121">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="694d1-122">Um nó de tinta não classificado é um **IContextNode** que é do tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="694d1-122">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="694d1-123">Se esse método mover um traço de um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado, esse método também adicionará a caixa delimitadora do traço à região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="694d1-123">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="694d1-124">Esse método não moverá um traço se o parâmetro *StrokeType* corresponder ao tipo atual do traço.</span><span class="sxs-lookup"><span data-stu-id="694d1-124">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="694d1-125">Se um traço identificado em *strokeIds* não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.</span><span class="sxs-lookup"><span data-stu-id="694d1-125">If a stroke identified in *strokeIds* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="694d1-126">Se nenhum dos traços especificados identificar um traço associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="694d1-126">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="694d1-127">Definir o tipo de traço em traços associados a um ContextNode que tenha NodeTypeAndProperties confirmado gerará um InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="694d1-127">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="694d1-128">Esse método retorna um código de erro quando *plStrokes* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="694d1-128">This method returns an error code when *plStrokes* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="694d1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="694d1-129">Requirements</span></span>



| <span data-ttu-id="694d1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="694d1-130">Requirement</span></span> | <span data-ttu-id="694d1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="694d1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="694d1-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="694d1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="694d1-133">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="694d1-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="694d1-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="694d1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="694d1-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="694d1-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="694d1-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="694d1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="694d1-137"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="694d1-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="694d1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="694d1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="694d1-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="694d1-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="694d1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="694d1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="694d1-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="694d1-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="694d1-142">**Método IInkAnalyzer:: getstroketype**</span><span class="sxs-lookup"><span data-stu-id="694d1-142">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="694d1-143">**Método IInkAnalyzer:: setstroketype**</span><span class="sxs-lookup"><span data-stu-id="694d1-143">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="694d1-144">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="694d1-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




