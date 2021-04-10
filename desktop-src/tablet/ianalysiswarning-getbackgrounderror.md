---
description: Recupera o código de erro para a operação de análise de tinta em segundo plano se ocorreu um erro.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Método IAnalysisWarning:: GetBackgroundError (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164554"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a><span data-ttu-id="5bc66-103">Método IAnalysisWarning:: GetBackgroundError</span><span class="sxs-lookup"><span data-stu-id="5bc66-103">IAnalysisWarning::GetBackgroundError method</span></span>

<span data-ttu-id="5bc66-104">Recupera o código de erro para a operação de análise de tinta em segundo plano se ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="5bc66-104">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bc66-105">Syntax</span></span>


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a><span data-ttu-id="5bc66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bc66-106">Parameters</span></span>

<span data-ttu-id="5bc66-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5bc66-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5bc66-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bc66-108">Return value</span></span>

<span data-ttu-id="5bc66-109">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5bc66-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc66-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bc66-110">Remarks</span></span>

<span data-ttu-id="5bc66-111">Se ocorrer um erro dentro de uma operação de análise em segundo plano, o [**IInkAnalyzer**](iinkanalyzer.md) não poderá retornar o código de erro porque ele está ocorrendo em um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="5bc66-111">If an error occurs within a background analysis operation, the [**IInkAnalyzer**](iinkanalyzer.md) cannot return the error code because it is occurring in a different thread.</span></span> <span data-ttu-id="5bc66-112">Em vez disso, o manipulador de eventos [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) recebe um [**IAnalysisStatus**](ianalysisstatus.md) que contém um [**IAnalysisWarning**](ianalysiswarning.md) com um [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ BackgroundException**.</span><span class="sxs-lookup"><span data-stu-id="5bc66-112">Instead, the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event handler receives an [**IAnalysisStatus**](ianalysisstatus.md) that contains an [**IAnalysisWarning**](ianalysiswarning.md) with an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) of **AnalysisWarningCode\_BackgroundException**.</span></span> <span data-ttu-id="5bc66-113">Este **IAnalysisWarning** contém o código de erro para a operação de análise em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5bc66-113">This **IAnalysisWarning** contains the error code for the background analysis operation.</span></span> <span data-ttu-id="5bc66-114">Em geral, o manipulador de eventos **\_ IAnalysisEvents:: Results** retornará esse código de erro para que ele possa ser tratado em outro lugar em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5bc66-114">In general, your **\_IAnalysisEvents::Results** event handler will return this error code so that it can be handled elsewhere in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc66-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc66-115">Requirements</span></span>



| <span data-ttu-id="5bc66-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc66-116">Requirement</span></span> | <span data-ttu-id="5bc66-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5bc66-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc66-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bc66-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc66-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5bc66-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5bc66-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bc66-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc66-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5bc66-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5bc66-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bc66-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bc66-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5bc66-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5bc66-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5bc66-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bc66-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bc66-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5bc66-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bc66-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc66-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="5bc66-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="5bc66-128">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="5bc66-128">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="5bc66-129">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="5bc66-129">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5bc66-130">**\_IAnalysisEvents:: resultados**</span><span class="sxs-lookup"><span data-stu-id="5bc66-130">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="5bc66-131">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="5bc66-131">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="5bc66-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="5bc66-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

