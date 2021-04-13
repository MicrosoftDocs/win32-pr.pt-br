---
description: Modifica os sinalizadores que controlam como o IInkAnalyzer executa a análise de tinta.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'Método IInkAnalyzer:: SetAnalysisModes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 826d31fd5b61db2332ef953d55b2cf6c6331995b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501797"
---
# <a name="iinkanalyzersetanalysismodes-method"></a><span data-ttu-id="72627-103">Método IInkAnalyzer:: SetAnalysisModes</span><span class="sxs-lookup"><span data-stu-id="72627-103">IInkAnalyzer::SetAnalysisModes method</span></span>

<span data-ttu-id="72627-104">Modifica os sinalizadores que controlam como o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="72627-104">Modifies flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="72627-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72627-105">Syntax</span></span>


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="72627-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72627-107">*analysismode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72627-107">*analysisMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72627-108">Uma combinação de bits de bit que contenha valores de enumeração [**AnalysisModes**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="72627-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72627-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72627-109">Return value</span></span>

<span data-ttu-id="72627-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="72627-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72627-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72627-111">Requirements</span></span>



| <span data-ttu-id="72627-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="72627-112">Requirement</span></span> | <span data-ttu-id="72627-113">Valor</span><span class="sxs-lookup"><span data-stu-id="72627-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72627-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72627-114">Minimum supported client</span></span><br/> | <span data-ttu-id="72627-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="72627-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="72627-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72627-116">Minimum supported server</span></span><br/> | <span data-ttu-id="72627-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="72627-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="72627-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72627-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="72627-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="72627-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="72627-120">DLL</span><span class="sxs-lookup"><span data-stu-id="72627-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72627-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72627-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="72627-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="72627-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72627-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="72627-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="72627-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="72627-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="72627-125">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="72627-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="72627-126">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="72627-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="72627-127">**Método IInkAnalyzer:: GetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="72627-127">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="72627-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="72627-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




