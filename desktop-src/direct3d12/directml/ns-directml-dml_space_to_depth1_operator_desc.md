---
UID: NS:directml.DML_SPACE_TO_DEPTH1_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH1_OPERATOR_DESC
description: Reorganiza blocos de dados espaciais em profundidade. O operador gera uma cópia do tensor de entrada, onde os valores das dimensões de altura e largura são movidos para a dimensão de profundidade.
helpviewer_keywords:
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure
- direct3d12.dml_space_to_depth1_operator_desc
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.openlocfilehash: 35e64d83fa6b8df42428869f72249e9846e50596
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802867"
---
# <a name="dml_space_to_depth1_operator_desc-structure-directmlh"></a><span data-ttu-id="f5de6-104">Estrutura de DML_SPACE_TO_DEPTH1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="f5de6-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="f5de6-105">Reorganiza blocos de dados espaciais em profundidade.</span><span class="sxs-lookup"><span data-stu-id="f5de6-105">Rearranges blocks of spatial data into depth.</span></span> <span data-ttu-id="f5de6-106">O operador gera uma cópia do tensor de entrada, onde os valores das dimensões de altura e largura são movidos para a dimensão de profundidade.</span><span class="sxs-lookup"><span data-stu-id="f5de6-106">The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.</span></span>

<span data-ttu-id="f5de6-107">Esta é a transformação inversa de [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="f5de6-107">This is the inverse transformation of [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5de6-108">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="f5de6-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f5de6-109">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f5de6-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5de6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5de6-110">Syntax</span></span>
```cpp
struct DML_SPACE_TO_DEPTH1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="f5de6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="f5de6-111">Members</span></span>

`InputTensor`

<span data-ttu-id="f5de6-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f5de6-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f5de6-113">O tensor do qual ler.</span><span class="sxs-lookup"><span data-stu-id="f5de6-113">The tensor to read from.</span></span> <span data-ttu-id="f5de6-114">As dimensões do tensor de entrada são `{ Batch, Channels, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="f5de6-114">The input tensor's dimensions are `{ Batch, Channels, Height, Width }`.</span></span>


`OutputTensor`

<span data-ttu-id="f5de6-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f5de6-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f5de6-116">O tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="f5de6-116">The tensor to write the results to.</span></span> <span data-ttu-id="f5de6-117">As dimensões de saída do tensor são `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }` .</span><span class="sxs-lookup"><span data-stu-id="f5de6-117">The output tensor's dimensions are `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }`.</span></span>


`BlockSize`

<span data-ttu-id="f5de6-118">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f5de6-118">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f5de6-119">A largura e a altura dos blocos que são movidos.</span><span class="sxs-lookup"><span data-stu-id="f5de6-119">The width and height of the Blocks that are moved.</span></span>


`Order`

<span data-ttu-id="f5de6-120">Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="f5de6-120">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="f5de6-121">Consulte [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="f5de6-121">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f5de6-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5de6-122">Examples</span></span>

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="f5de6-123">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="f5de6-123">Example 1.</span></span> <span data-ttu-id="f5de6-124">Profundidade-coluna-ordem de linha</span><span class="sxs-lookup"><span data-stu-id="f5de6-124">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]

OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="f5de6-125">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="f5de6-125">Example 2.</span></span> <span data-ttu-id="f5de6-126">Ordem de profundidade de linha de coluna</span><span class="sxs-lookup"><span data-stu-id="f5de6-126">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="f5de6-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5de6-127">Remarks</span></span>
<span data-ttu-id="f5de6-128">Quando o parâmetro *Order* é definido como [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), esse operador é equivalente a [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f5de6-128">When the *Order* parameter is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), this operator is equivalent to [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="f5de6-129">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="f5de6-129">Availability</span></span>
<span data-ttu-id="f5de6-130">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="f5de6-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f5de6-131">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="f5de6-131">Tensor constraints</span></span>
<span data-ttu-id="f5de6-132">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="f5de6-132">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f5de6-133">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="f5de6-133">Tensor support</span></span>
| <span data-ttu-id="f5de6-134">Tensor</span><span class="sxs-lookup"><span data-stu-id="f5de6-134">Tensor</span></span> | <span data-ttu-id="f5de6-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5de6-135">Kind</span></span> | <span data-ttu-id="f5de6-136">Dimensões</span><span class="sxs-lookup"><span data-stu-id="f5de6-136">Dimensions</span></span> | <span data-ttu-id="f5de6-137">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="f5de6-137">Supported dimension counts</span></span> | <span data-ttu-id="f5de6-138">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="f5de6-138">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="f5de6-139">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f5de6-139">InputTensor</span></span> | <span data-ttu-id="f5de6-140">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5de6-140">Input</span></span> | <span data-ttu-id="f5de6-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="f5de6-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="f5de6-142">4</span><span class="sxs-lookup"><span data-stu-id="f5de6-142">4</span></span> | <span data-ttu-id="f5de6-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f5de6-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f5de6-144">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f5de6-144">OutputTensor</span></span> | <span data-ttu-id="f5de6-145">Saída</span><span class="sxs-lookup"><span data-stu-id="f5de6-145">Output</span></span> | <span data-ttu-id="f5de6-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="f5de6-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="f5de6-147">4</span><span class="sxs-lookup"><span data-stu-id="f5de6-147">4</span></span> | <span data-ttu-id="f5de6-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f5de6-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="f5de6-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5de6-149">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f5de6-150">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="f5de6-150">**Header**</span></span> | <span data-ttu-id="f5de6-151">directml. h</span><span class="sxs-lookup"><span data-stu-id="f5de6-151">directml.h</span></span> |