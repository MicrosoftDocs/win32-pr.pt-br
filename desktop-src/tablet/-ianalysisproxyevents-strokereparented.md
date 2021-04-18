---
description: Ocorre quando o IInkAnalyzer move um traço de um objeto IContextNode para outro.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: 'Evento _IAnalysisProxyEvents:: StrokeReparented (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105793260"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a><span data-ttu-id="d8bca-103">\_Evento IAnalysisProxyEvents:: StrokeReparented</span><span class="sxs-lookup"><span data-stu-id="d8bca-103">\_IAnalysisProxyEvents::StrokeReparented event</span></span>

<span data-ttu-id="d8bca-104">Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) move um traço de um objeto [**IContextNode**](icontextnode.md) para outro.</span><span class="sxs-lookup"><span data-stu-id="d8bca-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8bca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8bca-105">Syntax</span></span>


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="d8bca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8bca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8bca-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bca-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bca-108">O objeto [**IInkAnalyzer**](iinkanalyzer.md) que move o traço.</span><span class="sxs-lookup"><span data-stu-id="d8bca-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="d8bca-109">*lStrokeIdToMove* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bca-109">*lStrokeIdToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bca-110">O identificador do traço a ser movido.</span><span class="sxs-lookup"><span data-stu-id="d8bca-110">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="d8bca-111">*pSourceContextNode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bca-111">*pSourceContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bca-112">O objeto [**IContextNode**](icontextnode.md) do qual o traço é movido.</span><span class="sxs-lookup"><span data-stu-id="d8bca-112">The [**IContextNode**](icontextnode.md) object from which the stroke is moved.</span></span>

</dd> <dt>

<span data-ttu-id="d8bca-113">*pDestinationContextNode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8bca-113">*pDestinationContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8bca-114">O objeto [**IContextNode**](icontextnode.md) para o qual o traço é movido.</span><span class="sxs-lookup"><span data-stu-id="d8bca-114">The [**IContextNode**](icontextnode.md) object to which the stroke is moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8bca-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8bca-115">Return value</span></span>

<span data-ttu-id="d8bca-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d8bca-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8bca-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8bca-117">Remarks</span></span>

<span data-ttu-id="d8bca-118">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="d8bca-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d8bca-119">Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método **IInkAnalyzer** que move dados de traço de um [**IContextNode**](icontextnode.md) para outro.</span><span class="sxs-lookup"><span data-stu-id="d8bca-119">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that moves stroke data from one [**IContextNode**](icontextnode.md) to another.</span></span>

<span data-ttu-id="d8bca-120">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d8bca-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8bca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8bca-121">Requirements</span></span>



| <span data-ttu-id="d8bca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8bca-122">Requirement</span></span> | <span data-ttu-id="d8bca-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d8bca-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8bca-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8bca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d8bca-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d8bca-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d8bca-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8bca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d8bca-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d8bca-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d8bca-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8bca-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8bca-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d8bca-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d8bca-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d8bca-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8bca-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8bca-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d8bca-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8bca-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8bca-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="d8bca-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d8bca-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d8bca-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d8bca-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d8bca-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d8bca-136">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="d8bca-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d8bca-137">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="d8bca-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d8bca-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="d8bca-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




