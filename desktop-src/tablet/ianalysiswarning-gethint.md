---
description: Recupera a dica de análise que causou este aviso.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Método IAnalysisWarning:: gethint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765048"
---
# <a name="ianalysiswarninggethint-method"></a><span data-ttu-id="fd7c1-103">Método IAnalysisWarning:: gethint</span><span class="sxs-lookup"><span data-stu-id="fd7c1-103">IAnalysisWarning::GetHint method</span></span>

<span data-ttu-id="fd7c1-104">Recupera a dica de análise que causou este aviso.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-104">Retrieves the analysis hint that caused this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd7c1-105">Syntax</span></span>


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="fd7c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd7c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd7c1-107">*pAnalysisHint* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd7c1-107">*pAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7c1-108">O nó de contexto de dica de análise que causou este aviso ou **nulo** se uma dica de análise não causar esse aviso.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-108">The analysis hint context node that caused this warning, or **NULL** if an analysis hint did not cause this warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd7c1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd7c1-109">Return value</span></span>

<span data-ttu-id="fd7c1-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fd7c1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd7c1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd7c1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fd7c1-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pAnalysisHint* quando você não precisar mais usar o nó de contexto de dica de análise.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAnalysisHint* when you no longer need to use the analysis hint context node.</span></span>

 

<span data-ttu-id="fd7c1-113">Um exemplo de uma dica de análise que gera um [**IAnalysisWarning**](ianalysiswarning.md) é uma dica de análise que contém um facto grafado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-113">An example of an analysis hint that generates an [**IAnalysisWarning**](ianalysiswarning.md) is an analysis hint that contains an incorrectly spelled factoid.</span></span> <span data-ttu-id="fd7c1-114">Nesse caso, a análise de tinta retorna um [**IAnalysisStatus**](ianalysisstatus.md) que contém um **IAnalysisWarning** que faz referência ao nó de contexto de dica de análise com o factor digitado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-114">In this case, ink analysis returns an [**IAnalysisStatus**](ianalysisstatus.md) that contains an **IAnalysisWarning** that references the analysis hint context node with the misspelled factoid.</span></span> <span data-ttu-id="fd7c1-115">Além disso, nesse caso, o método [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md) do aviso de análise retorna um valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ FactoidNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="fd7c1-115">Also, in this case, the analysis warning's [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) method returns an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_FactoidNotSupported**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7c1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd7c1-116">Requirements</span></span>



| <span data-ttu-id="fd7c1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7c1-117">Requirement</span></span> | <span data-ttu-id="fd7c1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fd7c1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7c1-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd7c1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7c1-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fd7c1-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fd7c1-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd7c1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7c1-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fd7c1-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fd7c1-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd7c1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd7c1-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fd7c1-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fd7c1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7c1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd7c1-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd7c1-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fd7c1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd7c1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7c1-128">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="fd7c1-128">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="fd7c1-129">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="fd7c1-129">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="fd7c1-130">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="fd7c1-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="fd7c1-131">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="fd7c1-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="fd7c1-132">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="fd7c1-132">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="fd7c1-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="fd7c1-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

