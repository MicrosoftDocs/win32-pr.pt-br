---
description: Salva os resultados da análise para os traços especificados associados a um IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Método IInkAnalyzer:: SaveResultsForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296384"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a><span data-ttu-id="6ab2c-103">Método IInkAnalyzer:: SaveResultsForStrokes</span><span class="sxs-lookup"><span data-stu-id="6ab2c-103">IInkAnalyzer::SaveResultsForStrokes method</span></span>

<span data-ttu-id="6ab2c-104">Salva os resultados da análise para os traços especificados associados a um [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="6ab2c-104">Saves analysis results for the specified strokes associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab2c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ab2c-105">Syntax</span></span>


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="6ab2c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ab2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab2c-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ab2c-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab2c-108">O número de identificadores de traço em **plStrokeIds**.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-108">The number of stroke identifiers in **plStrokeIds**.</span></span>

</dd> <dt>

<span data-ttu-id="6ab2c-109">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ab2c-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab2c-110">A matriz de identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="6ab2c-111">*pulSerializedDataSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6ab2c-111">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab2c-112">O número de bytes em *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-112">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="6ab2c-113">*ppbSerializedData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6ab2c-113">*ppbSerializedData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab2c-114">Ponteiro para os dados de análise serializados.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-114">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab2c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ab2c-115">Return value</span></span>

<span data-ttu-id="6ab2c-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6ab2c-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab2c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ab2c-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6ab2c-118">Para evitar um vazamento de memória, chame [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) no \* *ppbSerializedData* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-118">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="6ab2c-119">Esse método salva os resultados da análise atual para os traços especificados.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-119">This method saves the current analysis results for the specified strokes.</span></span> <span data-ttu-id="6ab2c-120">Esse método salva os objetos de [**IContextNode**](icontextnode.md) folha de tinta que contêm os traços e todos os ancestrais desses nós de contexto.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-120">This method saves the ink leaf [**IContextNode**](icontextnode.md) objects containing the strokes and all of the ancestors of those context nodes.</span></span> <span data-ttu-id="6ab2c-121">Esse método não salva nenhum dado de traço nem nós de dica de análise.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-121">This method does not save any stroke data or analysis hint nodes.</span></span> <span data-ttu-id="6ab2c-122">É responsabilidade do seu aplicativo sincronizar os resultados da análise e os dados de traço correspondentes, se ele persistir.</span><span class="sxs-lookup"><span data-stu-id="6ab2c-122">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="6ab2c-123">Esse método retorna um código de erro quando um objeto [**IContextNode**](icontextnode.md) a ser salvo é parcialmente preenchido (consulte [**IContextNode:: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="6ab2c-123">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab2c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ab2c-124">Requirements</span></span>



| <span data-ttu-id="6ab2c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab2c-125">Requirement</span></span> | <span data-ttu-id="6ab2c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6ab2c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab2c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ab2c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab2c-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6ab2c-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6ab2c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ab2c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab2c-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6ab2c-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6ab2c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ab2c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab2c-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab2c-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6ab2c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6ab2c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ab2c-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ab2c-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6ab2c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ab2c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab2c-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6ab2c-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6ab2c-137">**Método IInkAnalyzer:: loadresults**</span><span class="sxs-lookup"><span data-stu-id="6ab2c-137">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="6ab2c-138">**Método IInkAnalyzer:: SaveResults**</span><span class="sxs-lookup"><span data-stu-id="6ab2c-138">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="6ab2c-139">**Método IInkAnalyzer:: SaveResultsForNodes**</span><span class="sxs-lookup"><span data-stu-id="6ab2c-139">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="6ab2c-140">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="6ab2c-140">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6ab2c-141">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="6ab2c-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

