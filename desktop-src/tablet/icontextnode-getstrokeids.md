---
description: Recupera uma matriz de identificadores para os traços dentro do objeto IContextNode.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'Método IContextNode:: GetStrokeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090546"
---
# <a name="icontextnodegetstrokeids-method"></a><span data-ttu-id="b7143-103">Método IContextNode:: GetStrokeIds</span><span class="sxs-lookup"><span data-stu-id="b7143-103">IContextNode::GetStrokeIds method</span></span>

<span data-ttu-id="b7143-104">Recupera uma matriz de identificadores para os traços dentro do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b7143-104">Retrieves an array of identifiers for the strokes within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7143-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7143-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="b7143-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7143-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7143-107">*pulStrokeIdsCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b7143-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7143-108">O número de traços.</span><span class="sxs-lookup"><span data-stu-id="b7143-108">The number of strokes.</span></span> <span data-ttu-id="b7143-109">O valor que é passado não é usado.</span><span class="sxs-lookup"><span data-stu-id="b7143-109">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b7143-110">*pplStrokes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b7143-110">*pplStrokes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7143-111">Um ponteiro para a matriz de identificadores de traço para este objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b7143-111">A pointer to the array of stroke identifiers for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7143-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7143-112">Return value</span></span>

<span data-ttu-id="b7143-113">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b7143-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7143-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7143-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b7143-115">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *pplStrokes* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="b7143-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokes* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b7143-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7143-116">Requirements</span></span>



| <span data-ttu-id="b7143-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7143-117">Requirement</span></span> | <span data-ttu-id="b7143-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b7143-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7143-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7143-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7143-120">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b7143-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7143-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7143-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7143-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b7143-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b7143-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7143-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7143-124"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b7143-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b7143-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7143-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7143-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7143-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b7143-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7143-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7143-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b7143-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="b7143-129">**IContextNode:: getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="b7143-129">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="b7143-130">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="b7143-130">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="b7143-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="b7143-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

