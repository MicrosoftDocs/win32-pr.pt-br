---
UID: NS:directml.DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
title: DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
description: Subtrai cada elemento de *BTensor* do elemento correspondente de *ATensor*, multiplica o resultado por si mesmo e coloca o resultado no elemento correspondente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
ms.openlocfilehash: 3e3e7ab8f222f42def82a168ed861e58347f3b20
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804410"
---
# <a name="dml_element_wise_difference_square_operator_desc-directmlh"></a><span data-ttu-id="935b4-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="935b4-103">DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="935b4-104">Subtrai cada elemento de *BTensor* do elemento correspondente de *ATensor*, multiplica o resultado por si mesmo e coloca o resultado no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="935b4-104">Subtracts each element of *BTensor* from the corresponding element of *ATensor*, multiplies the result by itself, and places the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a - b) * (a - b)
```

<span data-ttu-id="935b4-105">Esse operador dá suporte à execução in-loco, o que significa que *OutputTensor* é permitido para alias *ATensor* ou *BTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="935b4-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="935b4-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="935b4-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="935b4-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="935b4-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="935b4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="935b4-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_DIFFERENCE_SQUARE_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="935b4-109">Membros</span><span class="sxs-lookup"><span data-stu-id="935b4-109">Members</span></span>

`ATensor`

<span data-ttu-id="935b4-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="935b4-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="935b4-111">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="935b4-111">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="935b4-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="935b4-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="935b4-113">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="935b4-113">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="935b4-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="935b4-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="935b4-115">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="935b4-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="935b4-116">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="935b4-116">Availability</span></span>
<span data-ttu-id="935b4-117">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="935b4-117">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="935b4-118">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="935b4-118">Tensor constraints</span></span>
<span data-ttu-id="935b4-119">*ATensor*, *BTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="935b4-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="935b4-120">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="935b4-120">Tensor support</span></span>
| <span data-ttu-id="935b4-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="935b4-121">Tensor</span></span> | <span data-ttu-id="935b4-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="935b4-122">Kind</span></span> | <span data-ttu-id="935b4-123">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="935b4-123">Supported dimension counts</span></span> | <span data-ttu-id="935b4-124">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="935b4-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="935b4-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="935b4-125">ATensor</span></span> | <span data-ttu-id="935b4-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="935b4-126">Input</span></span> | <span data-ttu-id="935b4-127">1 a 8</span><span class="sxs-lookup"><span data-stu-id="935b4-127">1 to 8</span></span> | <span data-ttu-id="935b4-128">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="935b4-128">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="935b4-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="935b4-129">BTensor</span></span> | <span data-ttu-id="935b4-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="935b4-130">Input</span></span> | <span data-ttu-id="935b4-131">1 a 8</span><span class="sxs-lookup"><span data-stu-id="935b4-131">1 to 8</span></span> | <span data-ttu-id="935b4-132">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="935b4-132">FLOAT32, FLOAT16, INT32, UINT32</span></span> |
| <span data-ttu-id="935b4-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="935b4-133">OutputTensor</span></span> | <span data-ttu-id="935b4-134">Saída</span><span class="sxs-lookup"><span data-stu-id="935b4-134">Output</span></span> | <span data-ttu-id="935b4-135">1 a 8</span><span class="sxs-lookup"><span data-stu-id="935b4-135">1 to 8</span></span> | <span data-ttu-id="935b4-136">FLOAT32, FLOAT16, INT32, UINT32</span><span class="sxs-lookup"><span data-stu-id="935b4-136">FLOAT32, FLOAT16, INT32, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="935b4-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="935b4-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="935b4-138">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="935b4-138">**Header**</span></span> | <span data-ttu-id="935b4-139">directml. h</span><span class="sxs-lookup"><span data-stu-id="935b4-139">directml.h</span></span> |
