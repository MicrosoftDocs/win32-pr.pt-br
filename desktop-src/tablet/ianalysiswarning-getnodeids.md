---
description: Retorna os identificadores de todos os nós de contexto relevantes associados a este aviso.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Método IAnalysisWarning:: GetNodeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501818"
---
# <a name="ianalysiswarninggetnodeids-method"></a><span data-ttu-id="d32a9-103">Método IAnalysisWarning:: GetNodeIds</span><span class="sxs-lookup"><span data-stu-id="d32a9-103">IAnalysisWarning::GetNodeIds method</span></span>

<span data-ttu-id="d32a9-104">Retorna os identificadores de todos os nós de contexto relevantes associados a este aviso.</span><span class="sxs-lookup"><span data-stu-id="d32a9-104">Returns the identifiers of any relevant context nodes that are associated with this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="d32a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d32a9-105">Syntax</span></span>


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a><span data-ttu-id="d32a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d32a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d32a9-107">*pulCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d32a9-107">*pulCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d32a9-108">O número de identificadores globalmente exclusivos (GUIDs) em *ppNodeIds*.</span><span class="sxs-lookup"><span data-stu-id="d32a9-108">The number of globally unique identifiers (GUIDs) in *ppNodeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="d32a9-109">*ppNodeIds* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d32a9-109">*ppNodeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d32a9-110">Um ponteiro para uma matriz de GUIDs que identifica os nós de contexto associados a esse aviso de análise, ou **NULL** se nenhum nó de contexto estiver associado ao aviso.</span><span class="sxs-lookup"><span data-stu-id="d32a9-110">A pointer to an array of GUIDs that identifies the context nodes that are associated with this analysis warning, or **NULL** if no context nodes are associated with the warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d32a9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d32a9-111">Return value</span></span>

<span data-ttu-id="d32a9-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d32a9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d32a9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d32a9-113">Remarks</span></span>

<span data-ttu-id="d32a9-114">Se *ppNodeIds* for passado como **NULL**, o método **GetNodeIds** retornará **S \_ OK** e o número de retângulos será retornado em *pulCount*.</span><span class="sxs-lookup"><span data-stu-id="d32a9-114">If *ppNodeIds* is passed as **NULL**, the **GetNodeIds** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="d32a9-115">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppNodeIds* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="d32a9-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppNodeIds* when you no longer need the information.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d32a9-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d32a9-116">Examples</span></span>

<span data-ttu-id="d32a9-117">O exemplo a seguir mostra como obter os objetos [**IContextNode**](icontextnode.md) que estão no [**IAnalysisWarning**](ianalysiswarning.md), `warning` e como obter apenas o número de objetos **IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d32a9-117">The following example shows how to get the [**IContextNode**](icontextnode.md) objects that are in the [**IAnalysisWarning**](ianalysiswarning.md), `warning`, and how to get only the number of **IContextNode** objects</span></span>


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="d32a9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d32a9-118">Requirements</span></span>



| <span data-ttu-id="d32a9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d32a9-119">Requirement</span></span> | <span data-ttu-id="d32a9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d32a9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32a9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d32a9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d32a9-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d32a9-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d32a9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d32a9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d32a9-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d32a9-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d32a9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d32a9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d32a9-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d32a9-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d32a9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d32a9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d32a9-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d32a9-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d32a9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d32a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d32a9-130">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="d32a9-130">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="d32a9-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d32a9-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d32a9-132">**Método IInkAnalyzer:: FindNode**</span><span class="sxs-lookup"><span data-stu-id="d32a9-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="d32a9-133">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="d32a9-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

