---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Executa um valor lógico *menor que ou igual a* em cada par de elementos correspondentes dos tempos de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: d1b8a282154b2b714daf061e2bb3f88b359209d4
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803077"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="c595a-103">Estrutura de DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c595a-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c595a-104">Executa um valor lógico *menor que ou igual a* em cada par de elementos correspondentes dos tempos de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="c595a-104">Performs a logical *less than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> <span data-ttu-id="c595a-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c595a-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c595a-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c595a-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c595a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c595a-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="c595a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c595a-108">Members</span></span>

`ATensor`

<span data-ttu-id="c595a-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c595a-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c595a-110">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="c595a-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="c595a-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c595a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c595a-112">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="c595a-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="c595a-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c595a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c595a-114">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="c595a-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="c595a-115">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="c595a-115">Availability</span></span>
<span data-ttu-id="c595a-116">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="c595a-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c595a-117">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="c595a-117">Tensor constraints</span></span>
* <span data-ttu-id="c595a-118">*ATensor* e *BTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="c595a-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="c595a-119">*ATensor*, *BTensor* e *OutputTensor* devem ter os mesmos *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="c595a-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c595a-120">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="c595a-120">Tensor support</span></span>
| <span data-ttu-id="c595a-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="c595a-121">Tensor</span></span> | <span data-ttu-id="c595a-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="c595a-122">Kind</span></span> | <span data-ttu-id="c595a-123">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="c595a-123">Supported dimension counts</span></span> | <span data-ttu-id="c595a-124">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="c595a-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c595a-125">ATensor</span><span class="sxs-lookup"><span data-stu-id="c595a-125">ATensor</span></span> | <span data-ttu-id="c595a-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="c595a-126">Input</span></span> | <span data-ttu-id="c595a-127">1 a 8</span><span class="sxs-lookup"><span data-stu-id="c595a-127">1 to 8</span></span> | <span data-ttu-id="c595a-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c595a-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c595a-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="c595a-129">BTensor</span></span> | <span data-ttu-id="c595a-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="c595a-130">Input</span></span> | <span data-ttu-id="c595a-131">1 a 8</span><span class="sxs-lookup"><span data-stu-id="c595a-131">1 to 8</span></span> | <span data-ttu-id="c595a-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c595a-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c595a-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c595a-133">OutputTensor</span></span> | <span data-ttu-id="c595a-134">Saída</span><span class="sxs-lookup"><span data-stu-id="c595a-134">Output</span></span> | <span data-ttu-id="c595a-135">1 a 8</span><span class="sxs-lookup"><span data-stu-id="c595a-135">1 to 8</span></span> | <span data-ttu-id="c595a-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="c595a-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="c595a-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c595a-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c595a-138">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="c595a-138">**Header**</span></span> | <span data-ttu-id="c595a-139">directml. h</span><span class="sxs-lookup"><span data-stu-id="c595a-139">directml.h</span></span> |