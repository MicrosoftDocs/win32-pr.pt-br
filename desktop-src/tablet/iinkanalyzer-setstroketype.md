---
description: Altera o tipo do traço especificado.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'Método IInkAnalyzer:: setstroketype (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090514"
---
# <a name="iinkanalyzersetstroketype-method"></a><span data-ttu-id="4b2cd-103">Método IInkAnalyzer:: setstroketype</span><span class="sxs-lookup"><span data-stu-id="4b2cd-103">IInkAnalyzer::SetStrokeType method</span></span>

<span data-ttu-id="4b2cd-104">Altera o tipo do traço especificado.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-104">Changes the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b2cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b2cd-105">Syntax</span></span>


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="4b2cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b2cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b2cd-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b2cd-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2cd-108">O identificador de traço do traço ao qual atribuir *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-108">The stroke identifier of the stroke to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="4b2cd-109">*StrokeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4b2cd-109">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2cd-110">O valor de [**StrokeType**](stroketype.md) a ser atribuído ao traço.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-110">The [**StrokeType**](stroketype.md) value to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b2cd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b2cd-111">Return value</span></span>

<span data-ttu-id="4b2cd-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4b2cd-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b2cd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b2cd-113">Remarks</span></span>

<span data-ttu-id="4b2cd-114">Se o tipo do traço for o [**valor de StrokeType**](stroketype.md) como não **\_ classificado**, o [**IInkAnalyzer**](iinkanalyzer.md) classificará o traço durante a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-114">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="4b2cd-115">Caso contrário, o **IInkAnalyzer** usará o tipo definido no traço.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="4b2cd-116">O [**IInkAnalyzer**](iinkanalyzer.md) não define o valor do tipo Stroke como parte da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="4b2cd-117">Para especificar ou alterar o tipo de traço, use o método **IInkAnalyzer:: Setstroketype** ou [**IInkAnalyzer:: setstrokestype**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="4b2cd-117">To specify or change the stroke type, use **IInkAnalyzer::SetStrokeType Method** or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

<span data-ttu-id="4b2cd-118">Se um traço estiver associado a um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)), esse método move o traço para um nó de tinta não classificado que contém traços do mesmo idioma.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-118">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="4b2cd-119">Se esse nó de contexto não existir, esse método criará um novo nó de tinta não classificada e adicionará o traço a ele.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-119">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="4b2cd-120">Um nó de tinta não classificado é um **IContextNode** que é do tipo UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-120">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="4b2cd-121">Se esse método mover um traço de um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado, esse método também adicionará a caixa delimitadora do traço à região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="4b2cd-121">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="4b2cd-122">Esse método não moverá um traço se o parâmetro *StrokeType* corresponder ao tipo atual do traço.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-122">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="4b2cd-123">Definir o tipo de traço em traços associados a um ContextNode que tenha NodeTypeAndProperties confirmado gerará um InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-123">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="4b2cd-124">Se o traço especificado não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="4b2cd-124">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b2cd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b2cd-125">Requirements</span></span>



| <span data-ttu-id="4b2cd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b2cd-126">Requirement</span></span> | <span data-ttu-id="4b2cd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4b2cd-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2cd-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b2cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b2cd-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4b2cd-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4b2cd-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b2cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b2cd-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4b2cd-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4b2cd-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b2cd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b2cd-133"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4b2cd-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4b2cd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4b2cd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b2cd-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b2cd-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4b2cd-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b2cd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b2cd-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4b2cd-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4b2cd-138">**Método IInkAnalyzer:: getstroketype**</span><span class="sxs-lookup"><span data-stu-id="4b2cd-138">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="4b2cd-139">**Método IInkAnalyzer:: setstrokestype**</span><span class="sxs-lookup"><span data-stu-id="4b2cd-139">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="4b2cd-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="4b2cd-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




