---
description: Ocorre antes de o IInkAnalyzer executar a análise dentro da região de um objeto IContextNode parcialmente populado.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P evento opulateContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172544"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a><span data-ttu-id="a7d78-103">\_IAnalysisProxyEvents: evento opulateContextNode de:P</span><span class="sxs-lookup"><span data-stu-id="a7d78-103">\_IAnalysisProxyEvents::PopulateContextNode event</span></span>

<span data-ttu-id="a7d78-104">Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) executar a análise dentro da região de um objeto [**IContextNode**](icontextnode.md) parcialmente populado.</span><span class="sxs-lookup"><span data-stu-id="a7d78-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d78-105">Syntax</span></span>


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a><span data-ttu-id="a7d78-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7d78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d78-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7d78-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d78-108">O objeto [**IInkAnalyzer**](iinkanalyzer.md) prestes a executar a análise.</span><span class="sxs-lookup"><span data-stu-id="a7d78-108">The [**IInkAnalyzer**](iinkanalyzer.md) object about to perform analysis.</span></span>

</dd> <dt>

<span data-ttu-id="a7d78-109">*pContextNodeToPopulate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7d78-109">*pContextNodeToPopulate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d78-110">O objeto [**IContextNode**](icontextnode.md) parcialmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="a7d78-110">The partially populated [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d78-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7d78-111">Return value</span></span>

<span data-ttu-id="a7d78-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a7d78-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d78-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7d78-113">Remarks</span></span>

<span data-ttu-id="a7d78-114">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a7d78-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="a7d78-115">Quando o **IInkAnalyzer** gera esse evento, seu aplicativo deve preencher o *pContextNodeToPopulate*.</span><span class="sxs-lookup"><span data-stu-id="a7d78-115">When the **IInkAnalyzer** raises this event, your application should populate the *pContextNodeToPopulate*.</span></span> <span data-ttu-id="a7d78-116">Durante a fase de análise, o **IInkAnalyzer** gera esse evento para obter informações sobre áreas nas quais está analisando a tinta.</span><span class="sxs-lookup"><span data-stu-id="a7d78-116">During the analysis phase, the **IInkAnalyzer** raises this event to get information for areas in which it is analyzing ink.</span></span>

<span data-ttu-id="a7d78-117">Se o documento contiver links para o *pContextNodeToPopulate*, seu aplicativo deverá criar e adicionar esses links.</span><span class="sxs-lookup"><span data-stu-id="a7d78-117">If the document contains links for the *pContextNodeToPopulate*, your application should create and add these links.</span></span> <span data-ttu-id="a7d78-118">Esse processo requer que os nós de origem e de destino, incluindo seus ancestrais, sejam totalmente preenchidos antes que o manipulador de eventos para esse evento saia (consulte [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).</span><span class="sxs-lookup"><span data-stu-id="a7d78-118">This process requires that both the source and destination nodes, including their ancestors, are fully populated before the event handler for this event exits (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span>

<span data-ttu-id="a7d78-119">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a7d78-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="a7d78-120">Durante a análise em segundo plano, o [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de gerar o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d78-120">During background analysis, the [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d78-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7d78-121">Requirements</span></span>



| <span data-ttu-id="a7d78-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d78-122">Requirement</span></span> | <span data-ttu-id="a7d78-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d78-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d78-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d78-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d78-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a7d78-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a7d78-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d78-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d78-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a7d78-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a7d78-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7d78-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7d78-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d78-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a7d78-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a7d78-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7d78-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7d78-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a7d78-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7d78-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d78-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="a7d78-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="a7d78-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a7d78-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a7d78-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="a7d78-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="a7d78-136">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="a7d78-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a7d78-137">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="a7d78-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a7d78-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="a7d78-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




