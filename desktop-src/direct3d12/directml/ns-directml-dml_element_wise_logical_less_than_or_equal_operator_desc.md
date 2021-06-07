---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Executa um lógico menor ou *igual* a em cada par de elementos correspondentes dos tensores de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente *de OutputTensor*.
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416960"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a><span data-ttu-id="cf3cb-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="cf3cb-103">DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="cf3cb-104">Executa um lógico menor ou *igual* a em cada par de elementos correspondentes dos tensores de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente *de OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="cf3cb-104">Performs a logical *less than or equal to* on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> <span data-ttu-id="cf3cb-105">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="cf3cb-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="cf3cb-106">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="cf3cb-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf3cb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf3cb-107">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="cf3cb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cf3cb-108">Members</span></span>

`ATensor`

<span data-ttu-id="cf3cb-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf3cb-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cf3cb-110">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="cf3cb-110">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="cf3cb-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf3cb-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cf3cb-112">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="cf3cb-112">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="cf3cb-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf3cb-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cf3cb-114">O tensor de saída no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="cf3cb-114">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="cf3cb-115">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="cf3cb-115">Availability</span></span>
<span data-ttu-id="cf3cb-116">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="cf3cb-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cf3cb-117">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="cf3cb-117">Tensor constraints</span></span>
* <span data-ttu-id="cf3cb-118">*ATensor* e *BTensor* devem ter o mesmo *DataType*.</span><span class="sxs-lookup"><span data-stu-id="cf3cb-118">*ATensor* and *BTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="cf3cb-119">*ATensor,* *BTensor* e *OutputTensor* devem ter o mesmo *DimensionCount* e *Tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="cf3cb-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cf3cb-120">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="cf3cb-120">Tensor support</span></span>
| <span data-ttu-id="cf3cb-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="cf3cb-121">Tensor</span></span> | <span data-ttu-id="cf3cb-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf3cb-122">Kind</span></span> | <span data-ttu-id="cf3cb-123">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="cf3cb-123">Supported dimension counts</span></span> | <span data-ttu-id="cf3cb-124">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="cf3cb-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cf3cb-125">Atensor</span><span class="sxs-lookup"><span data-stu-id="cf3cb-125">ATensor</span></span> | <span data-ttu-id="cf3cb-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="cf3cb-126">Input</span></span> | <span data-ttu-id="cf3cb-127">1 a 8</span><span class="sxs-lookup"><span data-stu-id="cf3cb-127">1 to 8</span></span> | <span data-ttu-id="cf3cb-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="cf3cb-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="cf3cb-129">BTensor</span><span class="sxs-lookup"><span data-stu-id="cf3cb-129">BTensor</span></span> | <span data-ttu-id="cf3cb-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="cf3cb-130">Input</span></span> | <span data-ttu-id="cf3cb-131">1 a 8</span><span class="sxs-lookup"><span data-stu-id="cf3cb-131">1 to 8</span></span> | <span data-ttu-id="cf3cb-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="cf3cb-132">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="cf3cb-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cf3cb-133">OutputTensor</span></span> | <span data-ttu-id="cf3cb-134">Saída</span><span class="sxs-lookup"><span data-stu-id="cf3cb-134">Output</span></span> | <span data-ttu-id="cf3cb-135">1 a 8</span><span class="sxs-lookup"><span data-stu-id="cf3cb-135">1 to 8</span></span> | <span data-ttu-id="cf3cb-136">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="cf3cb-136">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="cf3cb-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf3cb-137">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cf3cb-138">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="cf3cb-138">**Header**</span></span> | <span data-ttu-id="cf3cb-139">directml.h</span><span class="sxs-lookup"><span data-stu-id="cf3cb-139">directml.h</span></span> |