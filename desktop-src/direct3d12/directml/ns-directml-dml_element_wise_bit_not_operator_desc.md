---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Computa a contagem de população bit-a-bit (o número de bits definidos como 1) para cada elemento da entrada tensor e grava o resultado na tensor de saída.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.openlocfilehash: 4b292b1b6e12f4643e928022f59603fd75e080fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105793768"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a><span data-ttu-id="a2aa4-103">Estrutura de DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="a2aa4-103">DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a2aa4-104">Computa a contagem de população bit-a-bit (o número de bits definidos como 1) para cada elemento da entrada tensor e grava o resultado na tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-104">Computes the bitwise population count (the number of bits set to 1) for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="a2aa4-105">O tensor de entrada e saída deve ter os mesmos *DimensionCount* e *tamanhos*, embora eles possam ser diferentes no *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-105">The input and output tensor must have the same *DimensionCount* and *Sizes*, although they may differ in *DataType*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2aa4-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="a2aa4-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="a2aa4-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a2aa4-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2aa4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2aa4-108">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="a2aa4-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a2aa4-109">Members</span></span>

`InputTensor`

<span data-ttu-id="a2aa4-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a2aa4-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a2aa4-111">O tensor de entrada para leitura.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-111">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="a2aa4-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a2aa4-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a2aa4-113">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-113">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="a2aa4-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a2aa4-114">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a><span data-ttu-id="a2aa4-115">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a2aa4-115">Availability</span></span>
<span data-ttu-id="a2aa4-116">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a2aa4-116">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a2aa4-117">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="a2aa4-117">Tensor constraints</span></span>
<span data-ttu-id="a2aa4-118">*InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="a2aa4-118">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a2aa4-119">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="a2aa4-119">Tensor support</span></span>
| <span data-ttu-id="a2aa4-120">Tensor</span><span class="sxs-lookup"><span data-stu-id="a2aa4-120">Tensor</span></span> | <span data-ttu-id="a2aa4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2aa4-121">Kind</span></span> | <span data-ttu-id="a2aa4-122">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="a2aa4-122">Supported dimension counts</span></span> | <span data-ttu-id="a2aa4-123">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="a2aa4-123">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a2aa4-124">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a2aa4-124">InputTensor</span></span> | <span data-ttu-id="a2aa4-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="a2aa4-125">Input</span></span> | <span data-ttu-id="a2aa4-126">1 a 8</span><span class="sxs-lookup"><span data-stu-id="a2aa4-126">1 to 8</span></span> | <span data-ttu-id="a2aa4-127">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a2aa4-127">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a2aa4-128">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a2aa4-128">OutputTensor</span></span> | <span data-ttu-id="a2aa4-129">Saída</span><span class="sxs-lookup"><span data-stu-id="a2aa4-129">Output</span></span> | <span data-ttu-id="a2aa4-130">1 a 8</span><span class="sxs-lookup"><span data-stu-id="a2aa4-130">1 to 8</span></span> | <span data-ttu-id="a2aa4-131">UINT32, UINT8</span><span class="sxs-lookup"><span data-stu-id="a2aa4-131">UINT32, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="a2aa4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2aa4-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a2aa4-133">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a2aa4-133">**Header**</span></span> | <span data-ttu-id="a2aa4-134">directml. h</span><span class="sxs-lookup"><span data-stu-id="a2aa4-134">directml.h</span></span> |