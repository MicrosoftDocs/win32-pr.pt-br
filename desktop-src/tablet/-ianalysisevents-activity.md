---
description: 'Ocorre quando o método IInkAnalyzer:: Analyze ou IInkAnalyzer:: BackgroundAnalyze é chamado.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: 'Evento _IAnalysisEvents:: Activity (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298012"
---
# <a name="_ianalysiseventsactivity-event"></a><span data-ttu-id="c8cf6-103">\_Evento IAnalysisEvents:: Activity</span><span class="sxs-lookup"><span data-stu-id="c8cf6-103">\_IAnalysisEvents::Activity event</span></span>

<span data-ttu-id="c8cf6-104">Ocorre quando o método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-104">Occurs when the [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) method or [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8cf6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8cf6-105">Syntax</span></span>


```C++
HRESULT Activity();
```



## <a name="parameters"></a><span data-ttu-id="c8cf6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8cf6-106">Parameters</span></span>

<span data-ttu-id="c8cf6-107">Este evento não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8cf6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8cf6-108">Return value</span></span>

<span data-ttu-id="c8cf6-109">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c8cf6-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8cf6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8cf6-110">Remarks</span></span>

<span data-ttu-id="c8cf6-111">Esse evento indica que o [**IInkAnalyzer**](iinkanalyzer.md) está executando a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-111">This event indicates that the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span> <span data-ttu-id="c8cf6-112">Esse evento não indica o progresso da operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-112">This event does not indicate the progress of the ink analysis operation.</span></span>

<span data-ttu-id="c8cf6-113">Para executar qualquer um dos procedimentos a seguir, implemente um manipulador de eventos **\_ IAnalysisEvents:: Activity** :</span><span class="sxs-lookup"><span data-stu-id="c8cf6-113">To do any of the following, implement an **\_IAnalysisEvents::Activity** event handler:</span></span>

-   <span data-ttu-id="c8cf6-114">Indique ao usuário que o analisador de tinta está executando a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-114">Indicate to the user that the ink analyzer is performing ink analysis.</span></span>
-   <span data-ttu-id="c8cf6-115">Processar a entrada do usuário durante a análise síncrona.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-115">Process user input during synchronous analysis.</span></span>
-   <span data-ttu-id="c8cf6-116">Receber notificação de solicitações do sistema, como repintura da janela do aplicativo, durante a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-116">Receive notification of system requests, such as repainting of the application's window, during ink analysis.</span></span>

<span data-ttu-id="c8cf6-117">O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento com frequência durante a fase de análise de layout e a fase de classificação de escrita e desenho da análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-117">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event frequently during the layout analysis phase and the writing and drawing classification phase of ink analysis.</span></span> <span data-ttu-id="c8cf6-118">O **IInkAnalyzer** gera esse evento durante a fase de reconhecimento de manuscrito antes e depois de acessar um reconhecedor de tinta.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-118">The **IInkAnalyzer** raises this event during the handwriting recognition phase before and after accessing an ink recognizer.</span></span>

<span data-ttu-id="c8cf6-119">O número de eventos de atividade que um [**IInkAnalyzer**](iinkanalyzer.md) gera é afetado por:</span><span class="sxs-lookup"><span data-stu-id="c8cf6-119">The number of activity events an [**IInkAnalyzer**](iinkanalyzer.md) generates is affected by:</span></span>

-   <span data-ttu-id="c8cf6-120">O reconhecedor de tinta que o [**IInkAnalyzer**](iinkanalyzer.md) se aplica ao reconhecimento de tinta.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-120">The ink recognizer that the [**IInkAnalyzer**](iinkanalyzer.md) applies to ink recognition.</span></span>
-   <span data-ttu-id="c8cf6-121">O número e o comprimento dos traços que o [**IInkAnalyzer**](iinkanalyzer.md) está analisando.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-121">The number and length of strokes that the [**IInkAnalyzer**](iinkanalyzer.md) is analyzing.</span></span>
-   <span data-ttu-id="c8cf6-122">O número de traços que são classificados como gravação.</span><span class="sxs-lookup"><span data-stu-id="c8cf6-122">The number of strokes that are classified as writing.</span></span>

<span data-ttu-id="c8cf6-123">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c8cf6-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8cf6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8cf6-124">Requirements</span></span>



| <span data-ttu-id="c8cf6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8cf6-125">Requirement</span></span> | <span data-ttu-id="c8cf6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c8cf6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8cf6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8cf6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c8cf6-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c8cf6-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8cf6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8cf6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c8cf6-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c8cf6-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c8cf6-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8cf6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8cf6-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c8cf6-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c8cf6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c8cf6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8cf6-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8cf6-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c8cf6-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8cf6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8cf6-136">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="c8cf6-136">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="c8cf6-137">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="c8cf6-137">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="c8cf6-138">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c8cf6-138">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c8cf6-139">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="c8cf6-139">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c8cf6-140">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="c8cf6-140">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="c8cf6-141">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="c8cf6-141">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="c8cf6-142">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="c8cf6-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




