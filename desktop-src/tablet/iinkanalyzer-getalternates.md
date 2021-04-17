---
description: Recupera 10 alternativas de análise para toda a tinta associada ao IInkAnalyzer.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'Método IInkAnalyzer:: getalternations (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779980"
---
# <a name="iinkanalyzergetalternates-method"></a><span data-ttu-id="1a6cd-103">Método IInkAnalyzer:: getalternations</span><span class="sxs-lookup"><span data-stu-id="1a6cd-103">IInkAnalyzer::GetAlternates method</span></span>

<span data-ttu-id="1a6cd-104">Recupera 10 alternativas de análise para toda a tinta associada ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="1a6cd-104">Retrieves 10 analysis alternates for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6cd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a6cd-105">Syntax</span></span>


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="1a6cd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a6cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6cd-107">*ppAlternates* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a6cd-107">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a6cd-108">Um ponteiro para os 10 principais objetos [**IAnalysisAlternate**](ianalysisalternate.md) para toda a tinta associada ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="1a6cd-108">A pointer to the top 10 [**IAnalysisAlternate**](ianalysisalternate.md) objects for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6cd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a6cd-109">Return value</span></span>

<span data-ttu-id="1a6cd-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1a6cd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6cd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a6cd-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1a6cd-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAlternates* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="1a6cd-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="1a6cd-113">A alternativa superior é retornada como a primeira alternativa da coleção.</span><span class="sxs-lookup"><span data-stu-id="1a6cd-113">The top alternate is returned as the first alternate of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6cd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a6cd-114">Requirements</span></span>



| <span data-ttu-id="1a6cd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a6cd-115">Requirement</span></span> | <span data-ttu-id="1a6cd-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1a6cd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6cd-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6cd-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1a6cd-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1a6cd-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a6cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6cd-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1a6cd-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1a6cd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a6cd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a6cd-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1a6cd-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1a6cd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1a6cd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a6cd-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a6cd-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1a6cd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a6cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6cd-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1a6cd-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1a6cd-127">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="1a6cd-127">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="1a6cd-128">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="1a6cd-128">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="1a6cd-129">**Método IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="1a6cd-129">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="1a6cd-130">**Método IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="1a6cd-130">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="1a6cd-131">**Método IInkAnalyzer:: ModifyTopAlternate**</span><span class="sxs-lookup"><span data-stu-id="1a6cd-131">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="1a6cd-132">**Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation**</span><span class="sxs-lookup"><span data-stu-id="1a6cd-132">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="1a6cd-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="1a6cd-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

