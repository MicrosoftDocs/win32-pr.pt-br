---
description: Indica se um traço deve ser analisado como parte de um desenho ou como parte da gravação.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumeração StrokeType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170688"
---
# <a name="stroketype-enumeration"></a><span data-ttu-id="91ef3-103">Enumeração StrokeType</span><span class="sxs-lookup"><span data-stu-id="91ef3-103">StrokeType enumeration</span></span>

<span data-ttu-id="91ef3-104">Indica se um traço deve ser analisado como parte de um desenho ou como parte da gravação.</span><span class="sxs-lookup"><span data-stu-id="91ef3-104">Indicates whether a stroke should be analyzed as part of a drawing or as part of writing.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ef3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91ef3-105">Syntax</span></span>


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a><span data-ttu-id="91ef3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="91ef3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="91ef3-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType não \_ classificado**</span><span class="sxs-lookup"><span data-stu-id="91ef3-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType\_Unclassified**</span></span>
</dt> <dd>

<span data-ttu-id="91ef3-108">O traço pode ser qualquer parte de um desenho ou parte da escrita.</span><span class="sxs-lookup"><span data-stu-id="91ef3-108">The stroke might be either part of a drawing or part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="91ef3-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Escrita de StrokeType \_**</span><span class="sxs-lookup"><span data-stu-id="91ef3-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType\_Writing**</span></span>
</dt> <dd>

<span data-ttu-id="91ef3-110">O traço faz parte da gravação.</span><span class="sxs-lookup"><span data-stu-id="91ef3-110">The stroke is part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="91ef3-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**Desenho de StrokeType \_**</span><span class="sxs-lookup"><span data-stu-id="91ef3-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType\_Drawing**</span></span>
</dt> <dd>

<span data-ttu-id="91ef3-112">O traço faz parte de um desenho.</span><span class="sxs-lookup"><span data-stu-id="91ef3-112">The stroke is part of a drawing.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="91ef3-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91ef3-113">Examples</span></span>

<span data-ttu-id="91ef3-114">O exemplo a seguir mostra parte de um manipulador de eventos de traço, implementado de maneira semelhante ao [exemplo de coletores de eventos C++](c---event-sinks-sample.md).</span><span class="sxs-lookup"><span data-stu-id="91ef3-114">The following example shows part of a stroke event handler, implemented in a similar fashion to the [C++ Event Sinks Sample](c---event-sinks-sample.md).</span></span> <span data-ttu-id="91ef3-115">O traço adicionado é verificado para ver se a parte superior da caixa delimitadora foi desenhada abaixo de uma margem, `drawingMargin` .</span><span class="sxs-lookup"><span data-stu-id="91ef3-115">The added stroke is checked to see if the top of its bounding box has been drawn below a margin, `drawingMargin`.</span></span> <span data-ttu-id="91ef3-116">Nesse caso, o objeto [**IInkAnalyzer**](iinkanalyzer.md) , `m_spInkAnalyzer` , é definido para analisar o traço como um traço de desenho, e não como um traço de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="91ef3-116">If so, the [**IInkAnalyzer**](iinkanalyzer.md) object, `m_spInkAnalyzer`, is set to analyze the stroke as a drawing stroke, rather than as a handwriting stroke.</span></span> <span data-ttu-id="91ef3-117">`CheckHResult` é uma função que usa um `HRESULT` e uma cadeia de caracteres e gera uma exceção criada com a cadeia de caracteres se o `HRESULT` não for **êxito**.</span><span class="sxs-lookup"><span data-stu-id="91ef3-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a><span data-ttu-id="91ef3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ef3-118">Requirements</span></span>



| <span data-ttu-id="91ef3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ef3-119">Requirement</span></span> | <span data-ttu-id="91ef3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="91ef3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ef3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ef3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91ef3-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="91ef3-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="91ef3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91ef3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91ef3-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="91ef3-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="91ef3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91ef3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ef3-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="91ef3-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ef3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="91ef3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ef3-128">**Método IInkAnalyzer:: setstroketype**</span><span class="sxs-lookup"><span data-stu-id="91ef3-128">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




