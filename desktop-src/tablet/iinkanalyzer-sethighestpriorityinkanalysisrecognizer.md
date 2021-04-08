---
description: Move o IInkAnalysisRecognizer especificado para a primeira posição na lista de reconhecedores de tinta do objeto IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'Método IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827171"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a><span data-ttu-id="998f0-103">Método IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="998f0-103">IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer method</span></span>

<span data-ttu-id="998f0-104">Move o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) especificado para a primeira posição na lista de reconhecedores de tinta do objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="998f0-104">Moves the specified [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to the first position in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

## <a name="syntax"></a><span data-ttu-id="998f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="998f0-105">Syntax</span></span>


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="998f0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="998f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="998f0-107">*pInkAnalysisRecognizer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="998f0-107">*pInkAnalysisRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="998f0-108">O [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) a ser colocado na primeira posição.</span><span class="sxs-lookup"><span data-stu-id="998f0-108">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to place in the first position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="998f0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="998f0-109">Return value</span></span>

<span data-ttu-id="998f0-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="998f0-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="998f0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="998f0-111">Remarks</span></span>

<span data-ttu-id="998f0-112">Para obter a lista de reconhecedores de tinta em ordem de prioridade, chame o [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span><span class="sxs-lookup"><span data-stu-id="998f0-112">To get the list of ink recognizers in priority order, call [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span></span>

<span data-ttu-id="998f0-113">Esse método não afeta a ordem do restante dos objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) na lista de reconhecedores de tinta do objeto [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="998f0-113">This method does not affect the order of the rest of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

<span data-ttu-id="998f0-114">A ordem dos reconhecedores de tinta retornados pelo [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indica a ordem em que o [**IInkAnalyzer**](iinkanalyzer.md) avalia os objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponíveis.</span><span class="sxs-lookup"><span data-stu-id="998f0-114">The order of the ink recognizers returned by [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

<span data-ttu-id="998f0-115">O uso dos reconhecedores de tinta é avaliado com base em sua ordem na lista.</span><span class="sxs-lookup"><span data-stu-id="998f0-115">Use of the ink recognizers is evaluated based on their order in the list.</span></span>

<span data-ttu-id="998f0-116">Durante a análise de tinta, o [**IInkAnalyzer**](iinkanalyzer.md) faz a iteração pelos reconhecedores de tintas em sua lista até encontrar um reconhecedor que dá suporte ao idioma e a outras propriedades dos traços.</span><span class="sxs-lookup"><span data-stu-id="998f0-116">During ink analysis, the [**IInkAnalyzer**](iinkanalyzer.md) iterates through the ink recognizers in its list until it finds a recognizer that supports the language and other properties of the strokes.</span></span> <span data-ttu-id="998f0-117">Esse reconhecedor é usado para reconhecimento de tinta para esses traços.</span><span class="sxs-lookup"><span data-stu-id="998f0-117">This recognizer is used for ink recognition for those strokes.</span></span>

<span data-ttu-id="998f0-118">Se o [**IInkAnalyzer**](iinkanalyzer.md) não encontrar um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que ofereça suporte a um conjunto de traços durante a análise, o **IInkAnalyzer** gerará um [**IAnalysisWarning**](ianalysiswarning.md) com um código de aviso de **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (consulte [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span><span class="sxs-lookup"><span data-stu-id="998f0-118">If the [**IInkAnalyzer**](iinkanalyzer.md) does not find an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that supports a set of strokes during analysis, the **IInkAnalyzer** generates an [**IAnalysisWarning**](ianalysiswarning.md) with a warning code of **AnalysisWarningCode\_InkAnalysisRecognizerNotInstalled** (see [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="998f0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="998f0-119">Requirements</span></span>



| <span data-ttu-id="998f0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="998f0-120">Requirement</span></span> | <span data-ttu-id="998f0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="998f0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="998f0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="998f0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="998f0-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="998f0-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="998f0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="998f0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="998f0-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="998f0-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="998f0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="998f0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="998f0-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="998f0-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="998f0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="998f0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="998f0-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="998f0-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="998f0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="998f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="998f0-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="998f0-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="998f0-132">**Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**</span><span class="sxs-lookup"><span data-stu-id="998f0-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="998f0-133">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="998f0-133">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="998f0-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="998f0-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="998f0-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="998f0-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




