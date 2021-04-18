---
description: Ocorre antes que o IInkAnalyzer acesse os dados de traço.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: 'Evento _IAnalysisEvents:: UpdateStrokesCache (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105810632"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a><span data-ttu-id="d4571-103">\_Evento IAnalysisEvents:: UpdateStrokesCache</span><span class="sxs-lookup"><span data-stu-id="d4571-103">\_IAnalysisEvents::UpdateStrokesCache event</span></span>

<span data-ttu-id="d4571-104">Ocorre antes que o [**IInkAnalyzer**](iinkanalyzer.md) acesse os dados de traço.</span><span class="sxs-lookup"><span data-stu-id="d4571-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4571-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4571-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="d4571-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4571-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4571-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4571-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4571-108">O número de identificadores de traço em *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="d4571-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="d4571-109">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d4571-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4571-110">Os identificadores dos traços cujos dados de pacote foram apagados.</span><span class="sxs-lookup"><span data-stu-id="d4571-110">The identifiers of the strokes whose packet data has been cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4571-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4571-111">Return value</span></span>

<span data-ttu-id="d4571-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d4571-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4571-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4571-113">Remarks</span></span>

<span data-ttu-id="d4571-114">O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento durante a análise de tinta quando acessa um ou mais traços para os quais os dados de pacote foram limpos.</span><span class="sxs-lookup"><span data-stu-id="d4571-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during ink analysis when it accesses one or more strokes for which the packet data has been cleared.</span></span> <span data-ttu-id="d4571-115">Para atualizar os dados do pacote de traço, use o método do [**método IInkAnalyzer:: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d4571-115">To update the stroke packet data, use the [**IInkAnalyzer::UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) method.</span></span>

<span data-ttu-id="d4571-116">O [**IInkAnalyzer**](iinkanalyzer.md) não gera esse evento ao acessar um nó folha de tinta parcialmente preenchido quando o local do nó não foi definido pelo **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="d4571-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise this event when accessing a partially populated ink leaf node when the location of the node has not been set by the **IInkAnalyzer**.</span></span>

<span data-ttu-id="d4571-117">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d4571-117">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4571-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4571-118">Requirements</span></span>



| <span data-ttu-id="d4571-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4571-119">Requirement</span></span> | <span data-ttu-id="d4571-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d4571-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4571-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4571-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d4571-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d4571-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d4571-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4571-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d4571-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d4571-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d4571-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4571-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4571-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d4571-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d4571-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d4571-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4571-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4571-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d4571-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4571-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4571-130">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="d4571-130">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="d4571-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="d4571-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d4571-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d4571-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d4571-133">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="d4571-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d4571-134">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="d4571-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d4571-135">**Método IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="d4571-135">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="d4571-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="d4571-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="d4571-137">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="d4571-137">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="d4571-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="d4571-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




