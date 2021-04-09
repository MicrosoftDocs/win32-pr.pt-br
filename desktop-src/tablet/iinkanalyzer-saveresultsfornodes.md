---
description: Salva os resultados da análise de uma coleção de nós de contexto específica associada a um IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Método IInkAnalyzer:: SaveResultsForNodes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090518"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a><span data-ttu-id="1582f-103">Método IInkAnalyzer:: SaveResultsForNodes</span><span class="sxs-lookup"><span data-stu-id="1582f-103">IInkAnalyzer::SaveResultsForNodes method</span></span>

<span data-ttu-id="1582f-104">Salva os resultados da análise de uma coleção de nós de contexto específica associada a um [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="1582f-104">Saves analysis results for a specific context node collection associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1582f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1582f-105">Syntax</span></span>


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="1582f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1582f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1582f-107">*pContextNodes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1582f-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1582f-108">A coleção [**IContextNode**](icontextnode.md) para a qual salvar os resultados da análise.</span><span class="sxs-lookup"><span data-stu-id="1582f-108">The [**IContextNode**](icontextnode.md) collection for which to save analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="1582f-109">*pulSerializedDataSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1582f-109">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1582f-110">O número de bytes em *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="1582f-110">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="1582f-111">*ppbSerializedData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1582f-111">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1582f-112">Ponteiro para os dados de análise serializados.</span><span class="sxs-lookup"><span data-stu-id="1582f-112">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1582f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1582f-113">Return value</span></span>

<span data-ttu-id="1582f-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1582f-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1582f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1582f-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1582f-116">Para evitar um vazamento de memória, chame [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) no \* *ppbSerializedData* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="1582f-116">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="1582f-117">Esse método salva os resultados da análise atual para os objetos [**IContextNode**](icontextnode.md) no *pContextNodes* e todos os seus nós de contexto ancestral e descendente.</span><span class="sxs-lookup"><span data-stu-id="1582f-117">This method saves the current analysis results for the [**IContextNode**](icontextnode.md) objects in *pContextNodes* and all of their ancestor and descendant context nodes.</span></span> <span data-ttu-id="1582f-118">Esse método não salva nenhum dado de traço.</span><span class="sxs-lookup"><span data-stu-id="1582f-118">This method does not save any stroke data.</span></span> <span data-ttu-id="1582f-119">É responsabilidade do seu aplicativo sincronizar os resultados da análise e os dados de traço correspondentes, se ele persistir.</span><span class="sxs-lookup"><span data-stu-id="1582f-119">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="1582f-120">Se o objeto [**IContextNode**](icontextnode.md) a ser salvo for apenas parcialmente preenchido, esse método retornará um código de erro (consulte [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="1582f-120">If the [**IContextNode**](icontextnode.md) object to be saved is only partially populated, this method returns an error code (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="1582f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1582f-121">Requirements</span></span>



| <span data-ttu-id="1582f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1582f-122">Requirement</span></span> | <span data-ttu-id="1582f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1582f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1582f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1582f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1582f-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1582f-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1582f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1582f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1582f-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1582f-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1582f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1582f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1582f-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1582f-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1582f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1582f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1582f-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1582f-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1582f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1582f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1582f-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1582f-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1582f-134">**Método IInkAnalyzer:: loadresults**</span><span class="sxs-lookup"><span data-stu-id="1582f-134">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="1582f-135">**Método IInkAnalyzer:: SaveResults**</span><span class="sxs-lookup"><span data-stu-id="1582f-135">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="1582f-136">**Método IInkAnalyzer:: SaveResultsForStrokes**</span><span class="sxs-lookup"><span data-stu-id="1582f-136">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="1582f-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="1582f-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1582f-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="1582f-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

