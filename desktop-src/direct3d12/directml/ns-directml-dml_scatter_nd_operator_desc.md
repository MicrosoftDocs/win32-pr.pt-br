---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia todo o tensor de entrada para a saída e, em seguida, substitui índices selecionados por valores correspondentes das atualizações tensor.
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105773939"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="d3af0-103">Estrutura de DML_SCATTER_ND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="d3af0-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="d3af0-104">Copia todo o tensor de entrada para a saída e, em seguida, substitui índices selecionados por valores correspondentes das atualizações tensor.</span><span class="sxs-lookup"><span data-stu-id="d3af0-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="d3af0-105">Esse operador executa o pseudocódigo a seguir, onde "..." representa uma série de coordenadas, com o comportamento exato determinado pelo eixo e pelo tamanho dos índices.</span><span class="sxs-lookup"><span data-stu-id="d3af0-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="d3af0-106">Se dois índices de elementos de saída se sobrepõem (que é inválido), não há garantia de qual última gravação vence.</span><span class="sxs-lookup"><span data-stu-id="d3af0-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3af0-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="d3af0-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="d3af0-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="d3af0-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3af0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3af0-109">Syntax</span></span>
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="d3af0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d3af0-110">Members</span></span>

`InputTensor`

<span data-ttu-id="d3af0-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d3af0-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d3af0-112">O tensor do qual ler.</span><span class="sxs-lookup"><span data-stu-id="d3af0-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="d3af0-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d3af0-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d3af0-114">Um tensor que contém os índices.</span><span class="sxs-lookup"><span data-stu-id="d3af0-114">A tensor containing the indices.</span></span> <span data-ttu-id="d3af0-115">O *DimensionCount* desse tensor deve corresponder a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d3af0-116">A última dimensão de *IndicesTensor* é, na verdade, o número de coordenadas por tupla de índice e não deve excede *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d3af0-117">Por exemplo, um tensor de índices de tamanho `{1,4,5,2}` com *IndicesDimensionCount* = 3 significa uma matriz 4x5 de tuplas de coordenadas de 2 valores que são indexadas em *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="d3af0-118">A partir do `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral assinado com este tensor.</span><span class="sxs-lookup"><span data-stu-id="d3af0-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="d3af0-119">Os índices negativos são interpretados como sendo relativos ao final da respectiva dimensão.</span><span class="sxs-lookup"><span data-stu-id="d3af0-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="d3af0-120">Por exemplo, um índice de-1 se refere ao último elemento ao longo dessa dimensão.</span><span class="sxs-lookup"><span data-stu-id="d3af0-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="d3af0-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d3af0-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d3af0-122">Um tensor que contém os novos valores para substituir os valores de entrada existentes nos índices correspondentes.</span><span class="sxs-lookup"><span data-stu-id="d3af0-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="d3af0-123">O *DimensionCount* desse tensor deve corresponder a *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d3af0-124">Os tamanhos esperados *UpdatesTensor* são a concatenação do *IndicesTensor. tamanhos* principais segmentos e *InputTensor. tamanhos* segmento à direita para produzir o seguinte.</span><span class="sxs-lookup"><span data-stu-id="d3af0-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="d3af0-125">As dimensões são alinhadas à direita, com os 1 valores iniciais precedidos, se necessário, para atender a *UpdatesTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="d3af0-126">Aqui está um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d3af0-126">Here's an example.</span></span>

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

<span data-ttu-id="d3af0-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d3af0-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d3af0-128">O tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="d3af0-128">The tensor to write the results to.</span></span> <span data-ttu-id="d3af0-129">Os *tamanhos* e o *tipo de dados* deste tensor devem corresponder a *InputTensor. Sizes*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="d3af0-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d3af0-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d3af0-131">O número de dimensões de entrada reais dentro do *InputTensor* depois de ignorar qualquer ponto à esquerda irrelevante, variando [1, *InputTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="d3af0-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="d3af0-132">Por exemplo, dado *InputTensor. Sizes* = {1,1,4,6} e *InputDimensionCount* = 3, os índices significativos reais são {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="d3af0-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="d3af0-133">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d3af0-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d3af0-134">O número de dimensões de índice reais dentro do *IndicesTensor* depois de ignorar qualquer ponto de entrelinha irrelevante, variando [1, *IndicesTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="d3af0-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="d3af0-135">Por exemplo, dado *IndicesTensor. Sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, os índices significativos reais são {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="d3af0-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="d3af0-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d3af0-136">Examples</span></span>

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a><span data-ttu-id="d3af0-137">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d3af0-137">Availability</span></span>
<span data-ttu-id="d3af0-138">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="d3af0-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d3af0-139">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-139">Tensor constraints</span></span>
* <span data-ttu-id="d3af0-140">*IndicesTensor*, *InputTensor*, *OutputTensor* e `UpdatesTensor` devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="d3af0-141">*InputTensor*, *OutputTensor* e `UpdatesTensor` deve ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="d3af0-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d3af0-142">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="d3af0-143">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="d3af0-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="d3af0-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-144">Tensor</span></span> | <span data-ttu-id="d3af0-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3af0-145">Kind</span></span> | <span data-ttu-id="d3af0-146">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="d3af0-146">Supported dimension counts</span></span> | <span data-ttu-id="d3af0-147">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="d3af0-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d3af0-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-148">InputTensor</span></span> | <span data-ttu-id="d3af0-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3af0-149">Input</span></span> | <span data-ttu-id="d3af0-150">1 a 8</span><span class="sxs-lookup"><span data-stu-id="d3af0-150">1 to 8</span></span> | <span data-ttu-id="d3af0-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3af0-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d3af0-152">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-152">IndicesTensor</span></span> | <span data-ttu-id="d3af0-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3af0-153">Input</span></span> | <span data-ttu-id="d3af0-154">1 a 8</span><span class="sxs-lookup"><span data-stu-id="d3af0-154">1 to 8</span></span> | <span data-ttu-id="d3af0-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="d3af0-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="d3af0-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-156">UpdatesTensor</span></span> | <span data-ttu-id="d3af0-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3af0-157">Input</span></span> | <span data-ttu-id="d3af0-158">1 a 8</span><span class="sxs-lookup"><span data-stu-id="d3af0-158">1 to 8</span></span> | <span data-ttu-id="d3af0-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3af0-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d3af0-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-160">OutputTensor</span></span> | <span data-ttu-id="d3af0-161">Saída</span><span class="sxs-lookup"><span data-stu-id="d3af0-161">Output</span></span> | <span data-ttu-id="d3af0-162">1 a 8</span><span class="sxs-lookup"><span data-stu-id="d3af0-162">1 to 8</span></span> | <span data-ttu-id="d3af0-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3af0-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="d3af0-164">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="d3af0-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="d3af0-165">Tensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-165">Tensor</span></span> | <span data-ttu-id="d3af0-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3af0-166">Kind</span></span> | <span data-ttu-id="d3af0-167">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="d3af0-167">Supported dimension counts</span></span> | <span data-ttu-id="d3af0-168">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="d3af0-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d3af0-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-169">InputTensor</span></span> | <span data-ttu-id="d3af0-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3af0-170">Input</span></span> | <span data-ttu-id="d3af0-171">4</span><span class="sxs-lookup"><span data-stu-id="d3af0-171">4</span></span> | <span data-ttu-id="d3af0-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3af0-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d3af0-173">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-173">IndicesTensor</span></span> | <span data-ttu-id="d3af0-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3af0-174">Input</span></span> | <span data-ttu-id="d3af0-175">4</span><span class="sxs-lookup"><span data-stu-id="d3af0-175">4</span></span> | <span data-ttu-id="d3af0-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="d3af0-176">UINT32</span></span> |
| <span data-ttu-id="d3af0-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-177">UpdatesTensor</span></span> | <span data-ttu-id="d3af0-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="d3af0-178">Input</span></span> | <span data-ttu-id="d3af0-179">4</span><span class="sxs-lookup"><span data-stu-id="d3af0-179">4</span></span> | <span data-ttu-id="d3af0-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3af0-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d3af0-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d3af0-181">OutputTensor</span></span> | <span data-ttu-id="d3af0-182">Saída</span><span class="sxs-lookup"><span data-stu-id="d3af0-182">Output</span></span> | <span data-ttu-id="d3af0-183">4</span><span class="sxs-lookup"><span data-stu-id="d3af0-183">4</span></span> | <span data-ttu-id="d3af0-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d3af0-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="d3af0-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3af0-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d3af0-186">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="d3af0-186">**Header**</span></span> | <span data-ttu-id="d3af0-187">directml. h</span><span class="sxs-lookup"><span data-stu-id="d3af0-187">directml.h</span></span> |