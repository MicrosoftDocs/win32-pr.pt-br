---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Coleta elementos do tensor de entrada, usando os índices tensor para remapear índices para subblocos inteiros da entrada. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802898"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="13d47-104">Estrutura de DML_GATHER_ND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="13d47-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="13d47-105">Coleta elementos do tensor de entrada, usando os índices tensor para remapear índices para subblocos inteiros da entrada.</span><span class="sxs-lookup"><span data-stu-id="13d47-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="13d47-106">Esse operador executa o pseudocódigo a seguir, onde "..." representa uma série de coordenadas, com o comportamento exato dependente da contagem de dimensões de entrada e de índices.</span><span class="sxs-lookup"><span data-stu-id="13d47-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="13d47-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="13d47-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="13d47-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="13d47-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="13d47-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13d47-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="13d47-110">Membros</span><span class="sxs-lookup"><span data-stu-id="13d47-110">Members</span></span>

`InputTensor`

<span data-ttu-id="13d47-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13d47-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13d47-112">O tensor do qual ler.</span><span class="sxs-lookup"><span data-stu-id="13d47-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="13d47-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13d47-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13d47-114">O tensor que contém os índices.</span><span class="sxs-lookup"><span data-stu-id="13d47-114">The tensor containing the indices.</span></span> <span data-ttu-id="13d47-115">O *DimensionCount* desse tensor deve corresponder a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="13d47-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="13d47-116">A última dimensão de *IndicesTensor* é, na verdade, o número de coordenadas por tupla de índice e não pode exceder *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="13d47-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="13d47-117">Por exemplo, um tensor de índices de *tamanhos* `{1,4,5,2}` com *IndicesDimensionCount* = 3 significa uma matriz 4x5 de tuplas de duas coordenadas que são indexadas em *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="13d47-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="13d47-118">A partir do `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral assinado com este tensor.</span><span class="sxs-lookup"><span data-stu-id="13d47-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="13d47-119">Os índices negativos são interpretados como sendo relativos ao final da respectiva dimensão.</span><span class="sxs-lookup"><span data-stu-id="13d47-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="13d47-120">Por exemplo, um índice de-1 se refere ao último elemento ao longo dessa dimensão.</span><span class="sxs-lookup"><span data-stu-id="13d47-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="13d47-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="13d47-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="13d47-122">O tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="13d47-122">The tensor to write the results to.</span></span> <span data-ttu-id="13d47-123">O *DimensionCount* e o *tipo de dados* desse tensor devem corresponder a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="13d47-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="13d47-124">Os tamanhos esperados *OutputTensor* são a concatenação do *IndicesTensor. tamanhos* principais segmentos e *InputTensor. tamanhos* segmento à direita para produzir:</span><span class="sxs-lookup"><span data-stu-id="13d47-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="13d47-125">As dimensões de saída são alinhadas à direita, com os 1 valores iniciais precedidos, se necessário, para atender a *OutputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="13d47-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="13d47-126">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="13d47-126">Here's an example.</span></span>

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```


`InputDimensionCount`

<span data-ttu-id="13d47-127">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="13d47-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="13d47-128">O número de dimensões de entrada reais dentro do *InputTensor* depois de ignorar todas as irrelevantes, variando `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="13d47-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="13d47-129">Por exemplo, dado *InputTensor. Sizes*  =  `{1,1,4,6}` e `InputDimensionCount` = 3, os índices significativos reais são `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="13d47-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="13d47-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="13d47-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="13d47-131">O número de dimensões de índice reais dentro do *IndicesTensor* depois de ignorar qualquer ponto de entrelinha irrelevante, variando [1, *IndicesTensor. DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="13d47-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="13d47-132">Por exemplo, dado *IndicesTensor. Sizes*  =  `{1,1,4,6}` e *IndicesDimensionCount* = 3, os índices significativos reais são `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="13d47-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="13d47-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="13d47-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="13d47-134">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="13d47-134">Example 1.</span></span> <span data-ttu-id="13d47-135">remapeamento 1D</span><span class="sxs-lookup"><span data-stu-id="13d47-135">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a><span data-ttu-id="13d47-136">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="13d47-136">Example 2.</span></span> <span data-ttu-id="13d47-137">remapeamento de 2D</span><span class="sxs-lookup"><span data-stu-id="13d47-137">2D remapping</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a><span data-ttu-id="13d47-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="13d47-138">Remarks</span></span>
<span data-ttu-id="13d47-139">Uma versão mais recente desse operador, `DML_OPERATOR_GATHER_ND1` , foi introduzida no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="13d47-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="13d47-140">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="13d47-140">Availability</span></span>
<span data-ttu-id="13d47-141">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="13d47-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="13d47-142">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="13d47-142">Tensor constraints</span></span>
* <span data-ttu-id="13d47-143">*IndicesTensor*, *InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="13d47-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="13d47-144">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="13d47-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="13d47-145">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="13d47-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="13d47-146">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="13d47-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="13d47-147">Tensor</span><span class="sxs-lookup"><span data-stu-id="13d47-147">Tensor</span></span> | <span data-ttu-id="13d47-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="13d47-148">Kind</span></span> | <span data-ttu-id="13d47-149">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="13d47-149">Supported dimension counts</span></span> | <span data-ttu-id="13d47-150">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="13d47-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="13d47-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="13d47-151">InputTensor</span></span> | <span data-ttu-id="13d47-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="13d47-152">Input</span></span> | <span data-ttu-id="13d47-153">1 a 8</span><span class="sxs-lookup"><span data-stu-id="13d47-153">1 to 8</span></span> | <span data-ttu-id="13d47-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="13d47-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13d47-155">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="13d47-155">IndicesTensor</span></span> | <span data-ttu-id="13d47-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="13d47-156">Input</span></span> | <span data-ttu-id="13d47-157">1 a 8</span><span class="sxs-lookup"><span data-stu-id="13d47-157">1 to 8</span></span> | <span data-ttu-id="13d47-158">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="13d47-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="13d47-159">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="13d47-159">OutputTensor</span></span> | <span data-ttu-id="13d47-160">Saída</span><span class="sxs-lookup"><span data-stu-id="13d47-160">Output</span></span> | <span data-ttu-id="13d47-161">1 a 8</span><span class="sxs-lookup"><span data-stu-id="13d47-161">1 to 8</span></span> | <span data-ttu-id="13d47-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="13d47-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="13d47-163">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="13d47-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="13d47-164">Tensor</span><span class="sxs-lookup"><span data-stu-id="13d47-164">Tensor</span></span> | <span data-ttu-id="13d47-165">Tipo</span><span class="sxs-lookup"><span data-stu-id="13d47-165">Kind</span></span> | <span data-ttu-id="13d47-166">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="13d47-166">Supported dimension counts</span></span> | <span data-ttu-id="13d47-167">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="13d47-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="13d47-168">InputTensor</span><span class="sxs-lookup"><span data-stu-id="13d47-168">InputTensor</span></span> | <span data-ttu-id="13d47-169">Entrada</span><span class="sxs-lookup"><span data-stu-id="13d47-169">Input</span></span> | <span data-ttu-id="13d47-170">4</span><span class="sxs-lookup"><span data-stu-id="13d47-170">4</span></span> | <span data-ttu-id="13d47-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="13d47-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="13d47-172">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="13d47-172">IndicesTensor</span></span> | <span data-ttu-id="13d47-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="13d47-173">Input</span></span> | <span data-ttu-id="13d47-174">4</span><span class="sxs-lookup"><span data-stu-id="13d47-174">4</span></span> | <span data-ttu-id="13d47-175">UINT32</span><span class="sxs-lookup"><span data-stu-id="13d47-175">UINT32</span></span> |
| <span data-ttu-id="13d47-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="13d47-176">OutputTensor</span></span> | <span data-ttu-id="13d47-177">Saída</span><span class="sxs-lookup"><span data-stu-id="13d47-177">Output</span></span> | <span data-ttu-id="13d47-178">4</span><span class="sxs-lookup"><span data-stu-id="13d47-178">4</span></span> | <span data-ttu-id="13d47-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="13d47-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="13d47-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d47-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="13d47-181">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="13d47-181">**Header**</span></span> | <span data-ttu-id="13d47-182">directml. h</span><span class="sxs-lookup"><span data-stu-id="13d47-182">directml.h</span></span> |
