---
description: Indica o nível de confiança que o IInkAnalyzer tem na precisão do resultado do reconhecimento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumeração RecognitionConfidence (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785113"
---
# <a name="recognitionconfidence-enumeration"></a><span data-ttu-id="12158-103">Enumeração RecognitionConfidence</span><span class="sxs-lookup"><span data-stu-id="12158-103">RecognitionConfidence enumeration</span></span>

<span data-ttu-id="12158-104">Indica o nível de confiança que o [**IInkAnalyzer**](iinkanalyzer.md) tem na precisão do resultado do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="12158-104">Indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the recognition result.</span></span>

## <a name="syntax"></a><span data-ttu-id="12158-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12158-105">Syntax</span></span>


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a><span data-ttu-id="12158-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="12158-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="12158-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ Strong**</span><span class="sxs-lookup"><span data-stu-id="12158-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence\_Strong**</span></span>
</dt> <dd>

<span data-ttu-id="12158-108">Forte confiança no resultado ou alternativo.</span><span class="sxs-lookup"><span data-stu-id="12158-108">Strong confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="12158-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermediário**</span><span class="sxs-lookup"><span data-stu-id="12158-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence\_Intermediate**</span></span>
</dt> <dd>

<span data-ttu-id="12158-110">Confiança intermediária no resultado ou alternativa.</span><span class="sxs-lookup"><span data-stu-id="12158-110">Intermediate confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="12158-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ ruim**</span><span class="sxs-lookup"><span data-stu-id="12158-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence\_Poor**</span></span>
</dt> <dd>

<span data-ttu-id="12158-112">Má confiança no resultado ou alternativo.</span><span class="sxs-lookup"><span data-stu-id="12158-112">Poor confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="12158-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="12158-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="12158-114">O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que gerou o texto reconhecido não dá suporte a níveis de confiança.</span><span class="sxs-lookup"><span data-stu-id="12158-114">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that generated the recognized text does not support confidence levels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12158-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="12158-115">Remarks</span></span>

<span data-ttu-id="12158-116">O [**IInkAnalyzer**](iinkanalyzer.md) usa um ou mais objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para converter manuscrito em texto.</span><span class="sxs-lookup"><span data-stu-id="12158-116">The [**IInkAnalyzer**](iinkanalyzer.md) uses one or more [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects to convert handwriting to text.</span></span>

## <a name="requirements"></a><span data-ttu-id="12158-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12158-117">Requirements</span></span>



| <span data-ttu-id="12158-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="12158-118">Requirement</span></span> | <span data-ttu-id="12158-119">Valor</span><span class="sxs-lookup"><span data-stu-id="12158-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12158-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12158-120">Minimum supported client</span></span><br/> | <span data-ttu-id="12158-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="12158-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12158-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12158-122">Minimum supported server</span></span><br/> | <span data-ttu-id="12158-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="12158-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="12158-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12158-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="12158-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="12158-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12158-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="12158-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12158-127">**Método IAnalysisAlternate:: GetRecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="12158-127">**IAnalysisAlternate::GetRecognitionConfidence Method**</span></span>](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="12158-128">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="12158-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="12158-129">Propriedades do nó de contexto</span><span class="sxs-lookup"><span data-stu-id="12158-129">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="12158-130">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="12158-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




