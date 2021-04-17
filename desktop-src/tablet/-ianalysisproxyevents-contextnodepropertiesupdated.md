---
description: Ocorre depois que o IInkAnalyzer atualiza uma ou mais propriedades de um objeto IContextNode.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: 'Evento _IAnalysisProxyEvents:: ContextNodePropertiesUpdated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105811629"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a><span data-ttu-id="622e6-103">\_Evento IAnalysisProxyEvents:: ContextNodePropertiesUpdated</span><span class="sxs-lookup"><span data-stu-id="622e6-103">\_IAnalysisProxyEvents::ContextNodePropertiesUpdated event</span></span>

<span data-ttu-id="622e6-104">Ocorre depois que o [**IInkAnalyzer**](iinkanalyzer.md) atualiza uma ou mais propriedades de um objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="622e6-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="622e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="622e6-105">Syntax</span></span>


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a><span data-ttu-id="622e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="622e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="622e6-107">*pInkAnalyzer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="622e6-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="622e6-108">O objeto [**IInkAnalyzer**](iinkanalyzer.md) atualizando as propriedades.</span><span class="sxs-lookup"><span data-stu-id="622e6-108">The [**IInkAnalyzer**](iinkanalyzer.md) object updating the properties.</span></span>

</dd> <dt>

<span data-ttu-id="622e6-109">*pContextNodeUpdated* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="622e6-109">*pContextNodeUpdated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="622e6-110">O objeto [**IContextNode**](icontextnode.md) cujas propriedades são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="622e6-110">The [**IContextNode**](icontextnode.md) object whose properties are updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="622e6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="622e6-111">Return value</span></span>

<span data-ttu-id="622e6-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="622e6-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="622e6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="622e6-113">Remarks</span></span>

<span data-ttu-id="622e6-114">Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="622e6-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="622e6-115">Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método do analisador de tinta que altera as propriedades de um [**IContextNode**](icontextnode.md) (consulte [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)).</span><span class="sxs-lookup"><span data-stu-id="622e6-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that changes the properties of an [**IContextNode**](icontextnode.md) (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)).</span></span>

<span data-ttu-id="622e6-116">Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="622e6-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="622e6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="622e6-117">Requirements</span></span>



| <span data-ttu-id="622e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="622e6-118">Requirement</span></span> | <span data-ttu-id="622e6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="622e6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="622e6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="622e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="622e6-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="622e6-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="622e6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="622e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="622e6-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="622e6-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="622e6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="622e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="622e6-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="622e6-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="622e6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="622e6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="622e6-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="622e6-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="622e6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="622e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="622e6-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="622e6-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="622e6-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="622e6-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="622e6-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="622e6-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="622e6-132">**Método IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="622e6-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="622e6-133">**Método IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="622e6-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="622e6-134">Propriedades do nó de contexto</span><span class="sxs-lookup"><span data-stu-id="622e6-134">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="622e6-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="622e6-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




