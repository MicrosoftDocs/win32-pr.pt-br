---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Reorganiza (permuta) dados da profundidade em blocos de dados espaciais. O operador de saída de uma cópia do tensor de entrada em que os valores da dimensão de profundidade são movidos em blocos espaciais para as dimensões de altura e largura.
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 89b62a9916ee77dd6907d01710624d6e9a40a20a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417022"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a><span data-ttu-id="5529c-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="5529c-104">DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5529c-105">Reorganiza (permuta) dados da profundidade em blocos de dados espaciais.</span><span class="sxs-lookup"><span data-stu-id="5529c-105">Rearranges (permutes) data from depth into blocks of spatial data.</span></span> <span data-ttu-id="5529c-106">O operador de saída de uma cópia do tensor de entrada em que os valores da dimensão de profundidade são movidos em blocos espaciais para as dimensões de altura e largura.</span><span class="sxs-lookup"><span data-stu-id="5529c-106">The operator outputs a copy of the input tensor where values from the depth dimension are moved in spatial blocks to the height and width dimensions.</span></span>

<span data-ttu-id="5529c-107">Essa é a transformação inversa de [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="5529c-107">This is the inverse transformation of [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5529c-108">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="5529c-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5529c-109">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="5529c-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5529c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5529c-110">Syntax</span></span>
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="5529c-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5529c-111">Members</span></span>

`InputTensor`

<span data-ttu-id="5529c-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5529c-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5529c-113">O tensor do o que ler.</span><span class="sxs-lookup"><span data-stu-id="5529c-113">The tensor to read from.</span></span> <span data-ttu-id="5529c-114">As dimensões do tensor de entrada são `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5529c-114">The input tensor's dimensions are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`OutputTensor`

<span data-ttu-id="5529c-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5529c-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5529c-116">O tensor no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="5529c-116">The tensor to write the results to.</span></span> <span data-ttu-id="5529c-117">As dimensões do tensor de saída são `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , em que:</span><span class="sxs-lookup"><span data-stu-id="5529c-117">The output tensor's dimensions are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`, where:</span></span>

* <span data-ttu-id="5529c-118">OutputChannelCount é computado como InputChannelCount/ ( `BlockSize`  \*  `BlockSize` )</span><span class="sxs-lookup"><span data-stu-id="5529c-118">OutputChannelCount is computed as InputChannelCount / (`BlockSize` \* `BlockSize`)</span></span>
* <span data-ttu-id="5529c-119">OutputHeight é computado como InputHeight \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="5529c-119">OutputHeight is computed as InputHeight \* `BlockSize`</span></span>
* <span data-ttu-id="5529c-120">OutputWidth é computado como InputWidth \* `BlockSize`</span><span class="sxs-lookup"><span data-stu-id="5529c-120">OutputWidth is computed as InputWidth \* `BlockSize`</span></span>


`BlockSize`

<span data-ttu-id="5529c-121">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5529c-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5529c-122">A largura e a altura dos blocos que são movidos.</span><span class="sxs-lookup"><span data-stu-id="5529c-122">The width and height of the blocks that are moved.</span></span>


`Order`

<span data-ttu-id="5529c-123">Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="5529c-123">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="5529c-124">Consulte [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="5529c-124">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5529c-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5529c-125">Examples</span></span>

<span data-ttu-id="5529c-126">Todos os exemplos nesta seção usam a entrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="5529c-126">The examples in this section all use the input below.</span></span>

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
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

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="5529c-127">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="5529c-127">Example 1.</span></span> <span data-ttu-id="5529c-128">Ordem de linha de coluna de profundidade</span><span class="sxs-lookup"><span data-stu-id="5529c-128">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="5529c-129">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="5529c-129">Example 2.</span></span> <span data-ttu-id="5529c-130">Ordem de profundidade de linha de coluna</span><span class="sxs-lookup"><span data-stu-id="5529c-130">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="5529c-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5529c-131">Remarks</span></span>
<span data-ttu-id="5529c-132">Quando *Order* é definido como [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** é equivalente [a DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span><span class="sxs-lookup"><span data-stu-id="5529c-132">When *Order* is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** is equivalent to [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().</span></span>

## <a name="availability"></a><span data-ttu-id="5529c-133">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="5529c-133">Availability</span></span>
<span data-ttu-id="5529c-134">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="5529c-134">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5529c-135">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="5529c-135">Tensor constraints</span></span>
<span data-ttu-id="5529c-136">*InputTensor* e *OutputTensor* devem ter o mesmo *DataType*.</span><span class="sxs-lookup"><span data-stu-id="5529c-136">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5529c-137">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="5529c-137">Tensor support</span></span>
| <span data-ttu-id="5529c-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="5529c-138">Tensor</span></span> | <span data-ttu-id="5529c-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="5529c-139">Kind</span></span> | <span data-ttu-id="5529c-140">Dimensões</span><span class="sxs-lookup"><span data-stu-id="5529c-140">Dimensions</span></span> | <span data-ttu-id="5529c-141">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="5529c-141">Supported dimension counts</span></span> | <span data-ttu-id="5529c-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="5529c-142">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="5529c-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5529c-143">InputTensor</span></span> | <span data-ttu-id="5529c-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="5529c-144">Input</span></span> | <span data-ttu-id="5529c-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="5529c-145">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="5529c-146">4</span><span class="sxs-lookup"><span data-stu-id="5529c-146">4</span></span> | <span data-ttu-id="5529c-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5529c-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="5529c-148">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5529c-148">OutputTensor</span></span> | <span data-ttu-id="5529c-149">Saída</span><span class="sxs-lookup"><span data-stu-id="5529c-149">Output</span></span> | <span data-ttu-id="5529c-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="5529c-150">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="5529c-151">4</span><span class="sxs-lookup"><span data-stu-id="5529c-151">4</span></span> | <span data-ttu-id="5529c-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="5529c-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="5529c-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5529c-153">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5529c-154">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="5529c-154">**Header**</span></span> | <span data-ttu-id="5529c-155">directml.h</span><span class="sxs-lookup"><span data-stu-id="5529c-155">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="5529c-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="5529c-156">See also</span></span>

* [<span data-ttu-id="5529c-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="5529c-157">DML_DEPTH_TO_SPACE_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [<span data-ttu-id="5529c-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="5529c-158">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)