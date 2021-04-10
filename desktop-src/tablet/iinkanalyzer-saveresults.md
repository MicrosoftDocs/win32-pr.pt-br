---
description: Salva todos os resultados da análise de um IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'Método IInkAnalyzer:: SaveResults (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296385"
---
# <a name="iinkanalyzersaveresults-method"></a><span data-ttu-id="3b55a-103">Método IInkAnalyzer:: SaveResults</span><span class="sxs-lookup"><span data-stu-id="3b55a-103">IInkAnalyzer::SaveResults method</span></span>

<span data-ttu-id="3b55a-104">Salva todos os resultados da análise de um [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3b55a-104">Saves all analysis results for an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b55a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b55a-105">Syntax</span></span>


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="3b55a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b55a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b55a-107">*pulSerializedDataSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3b55a-107">*pulSerializedDataSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b55a-108">O número de bytes em *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="3b55a-108">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="3b55a-109">*ppbSerializedData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3b55a-109">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b55a-110">Uma matriz que contém os resultados da análise salva.</span><span class="sxs-lookup"><span data-stu-id="3b55a-110">An array containing the saved analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b55a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b55a-111">Return value</span></span>

<span data-ttu-id="3b55a-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3b55a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b55a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b55a-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3b55a-114">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppbSerializedData* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="3b55a-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="3b55a-115">Esse método salva todos os resultados da análise atual, que incluem a dica de análise atual e os nós de reconhecedor personalizados (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="3b55a-115">This method saves all the current analysis results, which include current analysis hint and custom recognizer nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="3b55a-116">Esse método não salva nenhum dado de traço.</span><span class="sxs-lookup"><span data-stu-id="3b55a-116">This method does not save any stroke data.</span></span> <span data-ttu-id="3b55a-117">É responsabilidade do seu aplicativo sincronizar os resultados da análise e os traços correspondentes se ele persistir os dados.</span><span class="sxs-lookup"><span data-stu-id="3b55a-117">It is the responsibility of your application to synchronize any analysis results and corresponding strokes if it persists data.</span></span>

<span data-ttu-id="3b55a-118">Esse método retorna um código de erro quando um objeto [**IContextNode**](icontextnode.md) a ser salvo é parcialmente preenchido (consulte [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="3b55a-118">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b55a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b55a-119">Requirements</span></span>



| <span data-ttu-id="3b55a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b55a-120">Requirement</span></span> | <span data-ttu-id="3b55a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3b55a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b55a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b55a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b55a-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3b55a-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3b55a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b55a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b55a-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3b55a-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3b55a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b55a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b55a-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3b55a-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3b55a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3b55a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b55a-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b55a-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3b55a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b55a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b55a-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3b55a-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3b55a-132">**Método IInkAnalyzer:: loadresults**</span><span class="sxs-lookup"><span data-stu-id="3b55a-132">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="3b55a-133">**Método IInkAnalyzer:: SaveResultsForNodes**</span><span class="sxs-lookup"><span data-stu-id="3b55a-133">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="3b55a-134">**Método IInkAnalyzer:: SaveResultsForStrokes**</span><span class="sxs-lookup"><span data-stu-id="3b55a-134">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="3b55a-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3b55a-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3b55a-136">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="3b55a-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

