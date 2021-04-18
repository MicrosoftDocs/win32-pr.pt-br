---
description: Recupera sinalizadores que controlam como o IInkAnalyzer executa a análise de tinta.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'Método IInkAnalyzer:: GetAnalysisModes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760557"
---
# <a name="iinkanalyzergetanalysismodes-method"></a><span data-ttu-id="8aa78-103">Método IInkAnalyzer:: GetAnalysisModes</span><span class="sxs-lookup"><span data-stu-id="8aa78-103">IInkAnalyzer::GetAnalysisModes method</span></span>

<span data-ttu-id="8aa78-104">Recupera sinalizadores que controlam como o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="8aa78-104">Retrieves flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aa78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8aa78-105">Syntax</span></span>


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="8aa78-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8aa78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aa78-107">*pAnalysisMode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8aa78-107">*pAnalysisMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8aa78-108">Uma combinação de bits de bit que contenha valores de enumeração [**AnalysisModes**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="8aa78-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aa78-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8aa78-109">Return value</span></span>

<span data-ttu-id="8aa78-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8aa78-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa78-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aa78-111">Requirements</span></span>



| <span data-ttu-id="8aa78-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa78-112">Requirement</span></span> | <span data-ttu-id="8aa78-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8aa78-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa78-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aa78-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa78-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8aa78-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8aa78-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8aa78-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa78-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8aa78-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8aa78-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8aa78-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa78-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8aa78-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8aa78-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8aa78-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8aa78-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8aa78-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8aa78-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8aa78-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa78-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8aa78-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8aa78-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="8aa78-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="8aa78-125">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="8aa78-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="8aa78-126">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="8aa78-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="8aa78-127">**Método IInkAnalyzer:: SetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="8aa78-127">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="8aa78-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="8aa78-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




