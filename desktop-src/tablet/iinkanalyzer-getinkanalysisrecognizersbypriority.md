---
description: Recupera uma coleção ordenada de objetos IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827173"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a><span data-ttu-id="a2fc3-103">Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority</span><span class="sxs-lookup"><span data-stu-id="a2fc3-103">IInkAnalyzer::GetInkAnalysisRecognizersByPriority method</span></span>

<span data-ttu-id="a2fc3-104">Recupera uma coleção ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="a2fc3-104">Retrieves an ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fc3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2fc3-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a><span data-ttu-id="a2fc3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2fc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2fc3-107">*ppInkAnalysisRecognizers* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a2fc3-107">*ppInkAnalysisRecognizers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2fc3-108">Uma coleção ordenada de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="a2fc3-108">An ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2fc3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2fc3-109">Return value</span></span>

<span data-ttu-id="a2fc3-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2fc3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2fc3-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a2fc3-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppInkAnalysisRecognizers* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="a2fc3-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppInkAnalysisRecognizers* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a2fc3-113">A ordem dos reconhecedores nesta coleção indica a ordem na qual o [**IInkAnalyzer**](iinkanalyzer.md) avalia os reconhecedores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a2fc3-113">The order of the recognizers in this collection indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available recognizers.</span></span> <span data-ttu-id="a2fc3-114">O **IInkAnalyzer** usa a linguagem dos traços como seu critério principal para aplicar um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc3-114">The **IInkAnalyzer** uses the language of the strokes as its primary criterion for applying an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="a2fc3-115">Como um critério secundário, o **IInkAnalyzer** compara as informações de dica de análise com os recursos com suporte de um objeto **IInkAnalysisRecognizer** (consulte [**IInkAnalysisRecognizer:: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span><span class="sxs-lookup"><span data-stu-id="a2fc3-115">As a secondary criterion, the **IInkAnalyzer** compares analysis hint information against an **IInkAnalysisRecognizer** object's supported capabilities (see [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span></span> <span data-ttu-id="a2fc3-116">Para obter mais informações sobre dicas de análise, consulte [**método IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md).</span><span class="sxs-lookup"><span data-stu-id="a2fc3-116">For more information about analysis hints, see [**IInkAnalyzer::CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span></span>

<span data-ttu-id="a2fc3-117">Se mais de um [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) der suporte a um identificador de idioma, o [**IInkAnalyzer**](iinkanalyzer.md) usará um algoritmo "primeiro ajuste" para selecionar o primeiro **IInkAnalysisRecognizer** para analisar os traços desse idioma.</span><span class="sxs-lookup"><span data-stu-id="a2fc3-117">If more than one [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports a language identifier, the [**IInkAnalyzer**](iinkanalyzer.md) uses a "first-fit" algorithm to select the first **IInkAnalysisRecognizer** to analyze strokes of that language.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2fc3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2fc3-118">Requirements</span></span>



| <span data-ttu-id="a2fc3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2fc3-119">Requirement</span></span> | <span data-ttu-id="a2fc3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a2fc3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fc3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2fc3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fc3-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a2fc3-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2fc3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2fc3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fc3-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a2fc3-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a2fc3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2fc3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fc3-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a2fc3-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a2fc3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a2fc3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2fc3-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2fc3-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a2fc3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2fc3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fc3-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a2fc3-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a2fc3-131">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="a2fc3-131">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="a2fc3-132">**Método IInkAnalyzer:: SetHighestPriorityInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="a2fc3-132">**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer Method**</span></span>](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a2fc3-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="a2fc3-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

