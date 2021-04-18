---
description: Ocorre antes que o analisador de tinta adicione um objeto IContextLink entre dois objetos IContextNode.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: 'Evento _IAnalysisProxyEvents:: ContextNodeLinkAdding (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105760631"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a><span data-ttu-id="e58e0-103">\_Evento IAnalysisProxyEvents:: ContextNodeLinkAdding</span><span class="sxs-lookup"><span data-stu-id="e58e0-103">\_IAnalysisProxyEvents::ContextNodeLinkAdding event</span></span>

<span data-ttu-id="e58e0-104">Ocorre antes que o analisador de tinta adicione um objeto [**IContextLink**](icontextlink.md) entre dois objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="e58e0-104">Occurs before the ink analyzer adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="e58e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e58e0-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a><span data-ttu-id="e58e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e58e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58e0-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e58e0-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58e0-108">O [**IInkAnalyzer**](iinkanalyzer.md) adicionando o link.</span><span class="sxs-lookup"><span data-stu-id="e58e0-108">The [**IInkAnalyzer**](iinkanalyzer.md) adding the link.</span></span>

</dd> <dt>

<span data-ttu-id="e58e0-109">*pContextLinkToBeAdded* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e58e0-109">*pContextLinkToBeAdded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58e0-110">O objeto [**IContextLink**](icontextlink.md) a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="e58e0-110">The [**IContextLink**](icontextlink.md) object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e58e0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e58e0-111">Return value</span></span>

<span data-ttu-id="e58e0-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e58e0-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e58e0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e58e0-113">Remarks</span></span>

<span data-ttu-id="e58e0-114">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e58e0-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="e58e0-115">Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método do analisador de tinta que adiciona um novo [**IContextLink**](icontextlink.md) a um [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="e58e0-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that adds a new [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="e58e0-116">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e58e0-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e58e0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e58e0-117">Requirements</span></span>



| <span data-ttu-id="e58e0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e58e0-118">Requirement</span></span> | <span data-ttu-id="e58e0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e58e0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58e0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e58e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e58e0-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e58e0-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e58e0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e58e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e58e0-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e58e0-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e58e0-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e58e0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e58e0-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e58e0-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e58e0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e58e0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e58e0-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e58e0-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e58e0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e58e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58e0-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="e58e0-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="e58e0-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e58e0-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e58e0-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="e58e0-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e58e0-132">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="e58e0-132">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="e58e0-133">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="e58e0-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="e58e0-134">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="e58e0-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="e58e0-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="e58e0-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




