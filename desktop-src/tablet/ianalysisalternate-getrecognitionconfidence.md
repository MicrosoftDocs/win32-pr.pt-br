---
description: Obtém um valor que indica o nível de confiança que o IInkAnalyzer tem na precisão do IAnalysisAlternate.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'Método IAnalysisAlternate:: GetRecognitionConfidence (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647245"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a><span data-ttu-id="fb998-103">Método IAnalysisAlternate:: GetRecognitionConfidence</span><span class="sxs-lookup"><span data-stu-id="fb998-103">IAnalysisAlternate::GetRecognitionConfidence method</span></span>

<span data-ttu-id="fb998-104">Obtém um valor que indica o nível de confiança que o [**IInkAnalyzer**](iinkanalyzer.md) tem na precisão do [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="fb998-104">Gets a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb998-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb998-105">Syntax</span></span>


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a><span data-ttu-id="fb998-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb998-107">*pConfidence* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fb998-107">*pConfidence* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb998-108">Um ponteiro para uma [**Enumeração InkRecognitionConfidence**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) que indica o nível de confiança que o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) tem na precisão da alternativa de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="fb998-108">A pointer to an [**InkRecognitionConfidence Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) that indicates the level of confidence that the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) has in the accuracy of the recognition alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb998-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb998-109">Return value</span></span>

<span data-ttu-id="fb998-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fb998-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb998-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb998-111">Requirements</span></span>



| <span data-ttu-id="fb998-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb998-112">Requirement</span></span> | <span data-ttu-id="fb998-113">Valor</span><span class="sxs-lookup"><span data-stu-id="fb998-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb998-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb998-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fb998-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fb998-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fb998-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb998-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fb998-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fb998-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fb998-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb998-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb998-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fb998-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb998-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fb998-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb998-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb998-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fb998-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb998-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb998-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="fb998-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="fb998-124">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fb998-124">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fb998-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="fb998-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="fb998-126">**RecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="fb998-126">**RecognitionConfidence**</span></span>](recognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="fb998-127">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="fb998-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




