---
UID: NS:directml.DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
description: Calcula o XOR bit a bit (eXclusive OR) entre cada elemento correspondente dos tensores de entrada e grava o resultado no tensor de saída.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
ms.openlocfilehash: fcedb2c33f1c63196a9e6783daaa9f2d863e99f0
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416974"
---
# <a name="dml_element_wise_bit_xor_operator_desc-structure-directmlh"></a><span data-ttu-id="2dbd7-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="2dbd7-103">DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="2dbd7-104">Calcula o XOR bit a bit (eXclusive OR) entre cada elemento correspondente dos tensores de entrada e grava o resultado no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="2dbd7-104">Computes the bitwise XOR (eXclusive OR) between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="2dbd7-105">O tensor de entrada e saída deve ter o mesmo *DimensionCount,* *Tamanhos* e *DataType*.</span><span class="sxs-lookup"><span data-stu-id="2dbd7-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="2dbd7-106">Esse operador dá suporte à execução in-loca, o que significa que o tensor de saída tem permissão para alias um ou mais dos tensores de entrada durante a associação.</span><span class="sxs-lookup"><span data-stu-id="2dbd7-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2dbd7-107">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="2dbd7-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2dbd7-108">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="2dbd7-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2dbd7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dbd7-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_XOR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="2dbd7-110">Membros</span><span class="sxs-lookup"><span data-stu-id="2dbd7-110">Members</span></span>

`ATensor`

<span data-ttu-id="2dbd7-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2dbd7-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2dbd7-112">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="2dbd7-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="2dbd7-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2dbd7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2dbd7-114">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="2dbd7-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="2dbd7-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2dbd7-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2dbd7-116">O tensor de saída no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="2dbd7-116">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="2dbd7-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="2dbd7-117">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="2dbd7-118">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="2dbd7-118">Availability</span></span>
<span data-ttu-id="2dbd7-119">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="2dbd7-119">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2dbd7-120">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="2dbd7-120">Tensor constraints</span></span>
<span data-ttu-id="2dbd7-121">*ATensor,* *BTensor* e *OutputTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="2dbd7-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2dbd7-122">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="2dbd7-122">Tensor support</span></span>
| <span data-ttu-id="2dbd7-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="2dbd7-123">Tensor</span></span> | <span data-ttu-id="2dbd7-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="2dbd7-124">Kind</span></span> | <span data-ttu-id="2dbd7-125">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="2dbd7-125">Supported dimension counts</span></span> | <span data-ttu-id="2dbd7-126">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="2dbd7-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2dbd7-127">Atensor</span><span class="sxs-lookup"><span data-stu-id="2dbd7-127">ATensor</span></span> | <span data-ttu-id="2dbd7-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="2dbd7-128">Input</span></span> | <span data-ttu-id="2dbd7-129">1 a 8</span><span class="sxs-lookup"><span data-stu-id="2dbd7-129">1 to 8</span></span> | <span data-ttu-id="2dbd7-130">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2dbd7-130">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2dbd7-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="2dbd7-131">BTensor</span></span> | <span data-ttu-id="2dbd7-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="2dbd7-132">Input</span></span> | <span data-ttu-id="2dbd7-133">1 a 8</span><span class="sxs-lookup"><span data-stu-id="2dbd7-133">1 to 8</span></span> | <span data-ttu-id="2dbd7-134">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2dbd7-134">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2dbd7-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="2dbd7-135">OutputTensor</span></span> | <span data-ttu-id="2dbd7-136">Saída</span><span class="sxs-lookup"><span data-stu-id="2dbd7-136">Output</span></span> | <span data-ttu-id="2dbd7-137">1 a 8</span><span class="sxs-lookup"><span data-stu-id="2dbd7-137">1 to 8</span></span> | <span data-ttu-id="2dbd7-138">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2dbd7-138">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="2dbd7-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dbd7-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2dbd7-140">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="2dbd7-140">**Header**</span></span> | <span data-ttu-id="2dbd7-141">directml.h</span><span class="sxs-lookup"><span data-stu-id="2dbd7-141">directml.h</span></span> |