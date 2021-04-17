---
description: Especifica o guia ou a área em que a tinta é desenhada e reconhecida.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Estrutura InkAnalysisRecognizerGuide (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790462"
---
# <a name="inkanalysisrecognizerguide-structure"></a><span data-ttu-id="7b9ee-103">Estrutura InkAnalysisRecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="7b9ee-103">InkAnalysisRecognizerGuide structure</span></span>

<span data-ttu-id="7b9ee-104">Especifica o guia ou a área em que a tinta é desenhada e reconhecida.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-104">Specifies the guide, or area where ink is drawn and recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b9ee-105">Syntax</span></span>


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a><span data-ttu-id="7b9ee-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7b9ee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b9ee-107">**rectWritingBox**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-107">**rectWritingBox**</span></span>
</dt> <dd>

<span data-ttu-id="7b9ee-108">A área de escrita invisível do guia de reconhecimento no qual a gravação pode realmente ocorrer.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-108">The invisible writing area of the recognition guide in which writing can actually take place.</span></span>

</dd> <dt>

<span data-ttu-id="7b9ee-109">**rectDrawnBox**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-109">**rectDrawnBox**</span></span>
</dt> <dd>

<span data-ttu-id="7b9ee-110">O retângulo que é desenhado na tela do Tablet e em que ocorre a gravação.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-110">The rectangle that is drawn on the tablet screen and in which writing takes place.</span></span>

</dd> <dt>

<span data-ttu-id="7b9ee-111">**Rapina**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-111">**cRows**</span></span>
</dt> <dd>

<span data-ttu-id="7b9ee-112">O número de linhas na caixa guia de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-112">The number of rows in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="7b9ee-113">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-113">**cColumns**</span></span>
</dt> <dd>

<span data-ttu-id="7b9ee-114">O número de colunas na caixa guia de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-114">The number of columns in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="7b9ee-115">**Tabs no meio**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-115">**midline**</span></span>
</dt> <dd>

<span data-ttu-id="7b9ee-116">A altura de Tabs no meio da caixa do guia de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-116">The midline height of the recognition guide box.</span></span> <span data-ttu-id="7b9ee-117">A altura de Tabs no meio é a distância da linha de base para o Tabs no meio da caixa de desenho.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-117">The midline height is the distance from the baseline to the midline, of the drawn box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b9ee-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b9ee-118">Remarks</span></span>

<span data-ttu-id="7b9ee-119">Um **InkAnalysisRecognizerGuide** define uma área esperada de entrada, como uma linha ou caixas, para caracteres.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-119">An **InkAnalysisRecognizerGuide** defines an expected area of input, such as a line or boxes, for characters.</span></span> <span data-ttu-id="7b9ee-120">Uma estrutura **InkAnalysisRecognizerGuide** pode ser definida somente em um nó de contexto de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="7b9ee-120">An **InkAnalysisRecognizerGuide** structure can be set only on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="7b9ee-121">O [**IInkAnalyzer**](iinkanalyzer.md) usa o local do nó de dica de análise e os locais dos traços de tinta para associar um traço ao nó de dica de análise.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-121">The [**IInkAnalyzer**](iinkanalyzer.md) uses the location of the analysis hint node and the locations of the ink strokes to associate a stroke with the analysis hint node.</span></span> <span data-ttu-id="7b9ee-122">Todos os traços com uma associação ao nó de dica de análise terão o **InkAnalysisRecognizerGuide** especificado usado quando reconhecidos por um **IInkAnalyzer**, desde que o **IInkAnalyzer** dê suporte ao **InkAnalysisRecognizerGuide**.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-122">Any strokes with an association to the analysis hint node will have the specified **InkAnalysisRecognizerGuide** used when recognized by an **IInkAnalyzer**, provided the **IInkAnalyzer** supports the **InkAnalysisRecognizerGuide**.</span></span> <span data-ttu-id="7b9ee-123">Os valores expressos na classe **InkAnalysisRecognizerGuide** são sempre relativos ao local do nó de dica de análise e são especificados em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="7b9ee-123">The values expressed in the **InkAnalysisRecognizerGuide** class are always relative to the location of the analysis hint node and are specified in ink space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b9ee-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b9ee-124">Requirements</span></span>



| <span data-ttu-id="7b9ee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b9ee-125">Requirement</span></span> | <span data-ttu-id="7b9ee-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7b9ee-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9ee-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b9ee-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9ee-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b9ee-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b9ee-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b9ee-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9ee-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7b9ee-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b9ee-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b9ee-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b9ee-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b9ee-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b9ee-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b9ee-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b9ee-134">Propriedades da dica de análise</span><span class="sxs-lookup"><span data-stu-id="7b9ee-134">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="7b9ee-135">**Método IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-135">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="7b9ee-136">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-136">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="7b9ee-137">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="7b9ee-137">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="7b9ee-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="7b9ee-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




