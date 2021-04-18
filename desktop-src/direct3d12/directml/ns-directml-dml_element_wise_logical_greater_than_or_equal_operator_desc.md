---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
description: Executa um valor lógico *maior que ou igual a* em cada par de elementos correspondentes dos tempos de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: bfe3c3abbabf0bd4f5dfa4d8393f3ed7d74a210f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105798327"
---
# <a name="dml_element_wise_logical_greater_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="6fef6-103">Estrutura de DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="6fef6-103">DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6fef6-104">Executa um valor lógico *maior que ou igual a* em cada par de elementos correspondentes dos tempos de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="6fef6-104">Performs a logical *greater than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >= b)
```

> [!IMPORTANT]
> <span data-ttu-id="6fef6-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="6fef6-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="6fef6-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6fef6-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fef6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fef6-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_GREATER_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="6fef6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6fef6-108">Members</span></span>

`ATensor`

<span data-ttu-id="6fef6-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6fef6-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6fef6-110">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="6fef6-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="6fef6-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6fef6-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6fef6-112">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="6fef6-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="6fef6-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6fef6-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6fef6-114">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="6fef6-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="6fef6-115">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="6fef6-115">Availability</span></span>
<span data-ttu-id="6fef6-116">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="6fef6-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6fef6-117">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="6fef6-117">Tensor constraints</span></span>
* <span data-ttu-id="6fef6-118">*ATensor* e *BTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="6fef6-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="6fef6-119">*ATensor*, *BTensor* e *OutputTensor* devem ter os mesmos *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="6fef6-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6fef6-120">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="6fef6-120">Tensor support</span></span>
| <span data-ttu-id="6fef6-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="6fef6-121">Tensor</span></span> | <span data-ttu-id="6fef6-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fef6-122">Kind</span></span> | <span data-ttu-id="6fef6-123">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="6fef6-123">Supported dimension counts</span></span> | <span data-ttu-id="6fef6-124">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="6fef6-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6fef6-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="6fef6-125">ATensor</span></span> | <span data-ttu-id="6fef6-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fef6-126">Input</span></span> | <span data-ttu-id="6fef6-127">1 a 8</span><span class="sxs-lookup"><span data-stu-id="6fef6-127">1 to 8</span></span> | <span data-ttu-id="6fef6-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="6fef6-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="6fef6-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="6fef6-129">BTensor</span></span> | <span data-ttu-id="6fef6-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fef6-130">Input</span></span> | <span data-ttu-id="6fef6-131">1 a 8</span><span class="sxs-lookup"><span data-stu-id="6fef6-131">1 to 8</span></span> | <span data-ttu-id="6fef6-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="6fef6-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="6fef6-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6fef6-133">OutputTensor</span></span> | <span data-ttu-id="6fef6-134">Saída</span><span class="sxs-lookup"><span data-stu-id="6fef6-134">Output</span></span> | <span data-ttu-id="6fef6-135">1 a 8</span><span class="sxs-lookup"><span data-stu-id="6fef6-135">1 to 8</span></span> | <span data-ttu-id="6fef6-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="6fef6-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="6fef6-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fef6-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6fef6-138">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="6fef6-138">**Header**</span></span> | <span data-ttu-id="6fef6-139">directml. h</span><span class="sxs-lookup"><span data-stu-id="6fef6-139">directml.h</span></span> |