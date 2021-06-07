---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia todo o tensor de entrada para a saída e, em seguida, substitui os índices selecionados com valores correspondentes do tensor de atualizações.
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
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416985"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="af71f-103">DML_SCATTER_ND_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="af71f-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="af71f-104">Copia todo o tensor de entrada para a saída e, em seguida, substitui os índices selecionados com valores correspondentes do tensor de atualizações.</span><span class="sxs-lookup"><span data-stu-id="af71f-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="af71f-105">Esse operador executa o seguinte pseudocódigo, em que "..." representa uma série de coordenadas, com o comportamento exato determinado pelo tamanho do eixo e dos índices.</span><span class="sxs-lookup"><span data-stu-id="af71f-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="af71f-106">Se dois índices de elemento de saída se sobrepõem (o que é inválido), não há nenhuma garantia de qual última gravação vence.</span><span class="sxs-lookup"><span data-stu-id="af71f-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af71f-107">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="af71f-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="af71f-108">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="af71f-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="af71f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af71f-109">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="af71f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="af71f-110">Members</span></span>

`InputTensor`

<span data-ttu-id="af71f-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="af71f-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="af71f-112">O tensor do o que ler.</span><span class="sxs-lookup"><span data-stu-id="af71f-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="af71f-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="af71f-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="af71f-114">Um tensor que contém os índices.</span><span class="sxs-lookup"><span data-stu-id="af71f-114">A tensor containing the indices.</span></span> <span data-ttu-id="af71f-115">O *DimensionCount* desse tensor deve corresponder *a InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="af71f-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="af71f-116">A última dimensão do *IndicesTensor* é, na verdade, o número de coordenadas por tupla de índice e não deve exceder *InputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="af71f-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="af71f-117">Por exemplo, um tensor de índices de tamanho com `{1,4,5,2}` *IndicesDimensionCount* = 3 significa uma matriz 4x5 de tuplas de coordenadas de 2 valores que são indexadas em *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="af71f-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="af71f-118">Começando com `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral com sinal com esse tensor.</span><span class="sxs-lookup"><span data-stu-id="af71f-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="af71f-119">Índices negativos são interpretados como sendo relativos ao final da respectiva dimensão.</span><span class="sxs-lookup"><span data-stu-id="af71f-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="af71f-120">Por exemplo, um índice de -1 refere-se ao último elemento ao longo dessa dimensão.</span><span class="sxs-lookup"><span data-stu-id="af71f-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="af71f-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="af71f-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="af71f-122">Um tensor que contém os novos valores para substituir os valores de entrada existentes nos índices correspondentes.</span><span class="sxs-lookup"><span data-stu-id="af71f-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="af71f-123">O *DimensionCount* desse tensor deve corresponder *a InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="af71f-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="af71f-124">Os *updatesTensor.Sizes* esperados são a concatenação dos segmentos à frente *IndicesTensor.Sizes* e *InputTensor.Sizes* à frente para produzir o seguinte.</span><span class="sxs-lookup"><span data-stu-id="af71f-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="af71f-125">As dimensões são alinhadas à direita, com os valores 1 à direita pré-anexados, se necessário, para atender *a UpdatesTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="af71f-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="af71f-126">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="af71f-126">Here's an example.</span></span>

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

<span data-ttu-id="af71f-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="af71f-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="af71f-128">O tensor no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="af71f-128">The tensor to write the results to.</span></span> <span data-ttu-id="af71f-129">Os *Tamanhos* e *o DataType* desse tensor devem corresponder *a InputTensor.Sizes.*</span><span class="sxs-lookup"><span data-stu-id="af71f-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="af71f-130">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="af71f-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="af71f-131">O número de dimensões de entrada reais dentro do *InputTensor* depois de ignorar quaisquer dimensões irrelevantes à frente, variando [1, *InputTensor.DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="af71f-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="af71f-132">Por exemplo, dado *InputTensor.Sizes* = {1,1,4,6} e *InputDimensionCount* = 3, os índices significativos reais são {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="af71f-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="af71f-133">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="af71f-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="af71f-134">O número de dimensões de índice reais dentro do *IndicesTensor* depois de ignorar quaisquer dimensões irrelevantes à frente, variando [1, *IndicesTensor.DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="af71f-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="af71f-135">Por exemplo, dado *IndicesTensor.Sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, os índices significativos reais são {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="af71f-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="af71f-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af71f-136">Examples</span></span>

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

## <a name="availability"></a><span data-ttu-id="af71f-137">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="af71f-137">Availability</span></span>
<span data-ttu-id="af71f-138">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="af71f-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="af71f-139">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="af71f-139">Tensor constraints</span></span>
* <span data-ttu-id="af71f-140">*IndicesTensor*, *InputTensor,* *OutputTensor* e `UpdatesTensor` devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="af71f-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="af71f-141">*InputTensor,* *OutputTensor* e `UpdatesTensor` devem ter o mesmo *DataType*.</span><span class="sxs-lookup"><span data-stu-id="af71f-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="af71f-142">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="af71f-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="af71f-143">DML_FEATURE_LEVEL_3_0 e superior</span><span class="sxs-lookup"><span data-stu-id="af71f-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="af71f-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="af71f-144">Tensor</span></span> | <span data-ttu-id="af71f-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="af71f-145">Kind</span></span> | <span data-ttu-id="af71f-146">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="af71f-146">Supported dimension counts</span></span> | <span data-ttu-id="af71f-147">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="af71f-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="af71f-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-148">InputTensor</span></span> | <span data-ttu-id="af71f-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="af71f-149">Input</span></span> | <span data-ttu-id="af71f-150">1 a 8</span><span class="sxs-lookup"><span data-stu-id="af71f-150">1 to 8</span></span> | <span data-ttu-id="af71f-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="af71f-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="af71f-152">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-152">IndicesTensor</span></span> | <span data-ttu-id="af71f-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="af71f-153">Input</span></span> | <span data-ttu-id="af71f-154">1 a 8</span><span class="sxs-lookup"><span data-stu-id="af71f-154">1 to 8</span></span> | <span data-ttu-id="af71f-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="af71f-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="af71f-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-156">UpdatesTensor</span></span> | <span data-ttu-id="af71f-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="af71f-157">Input</span></span> | <span data-ttu-id="af71f-158">1 a 8</span><span class="sxs-lookup"><span data-stu-id="af71f-158">1 to 8</span></span> | <span data-ttu-id="af71f-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="af71f-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="af71f-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-160">OutputTensor</span></span> | <span data-ttu-id="af71f-161">Saída</span><span class="sxs-lookup"><span data-stu-id="af71f-161">Output</span></span> | <span data-ttu-id="af71f-162">1 a 8</span><span class="sxs-lookup"><span data-stu-id="af71f-162">1 to 8</span></span> | <span data-ttu-id="af71f-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="af71f-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="af71f-164">DML_FEATURE_LEVEL_2_1 e superior</span><span class="sxs-lookup"><span data-stu-id="af71f-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="af71f-165">Tensor</span><span class="sxs-lookup"><span data-stu-id="af71f-165">Tensor</span></span> | <span data-ttu-id="af71f-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="af71f-166">Kind</span></span> | <span data-ttu-id="af71f-167">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="af71f-167">Supported dimension counts</span></span> | <span data-ttu-id="af71f-168">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="af71f-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="af71f-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-169">InputTensor</span></span> | <span data-ttu-id="af71f-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="af71f-170">Input</span></span> | <span data-ttu-id="af71f-171">4</span><span class="sxs-lookup"><span data-stu-id="af71f-171">4</span></span> | <span data-ttu-id="af71f-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="af71f-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="af71f-173">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-173">IndicesTensor</span></span> | <span data-ttu-id="af71f-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="af71f-174">Input</span></span> | <span data-ttu-id="af71f-175">4</span><span class="sxs-lookup"><span data-stu-id="af71f-175">4</span></span> | <span data-ttu-id="af71f-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="af71f-176">UINT32</span></span> |
| <span data-ttu-id="af71f-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-177">UpdatesTensor</span></span> | <span data-ttu-id="af71f-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="af71f-178">Input</span></span> | <span data-ttu-id="af71f-179">4</span><span class="sxs-lookup"><span data-stu-id="af71f-179">4</span></span> | <span data-ttu-id="af71f-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="af71f-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="af71f-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="af71f-181">OutputTensor</span></span> | <span data-ttu-id="af71f-182">Saída</span><span class="sxs-lookup"><span data-stu-id="af71f-182">Output</span></span> | <span data-ttu-id="af71f-183">4</span><span class="sxs-lookup"><span data-stu-id="af71f-183">4</span></span> | <span data-ttu-id="af71f-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="af71f-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="af71f-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af71f-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="af71f-186">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="af71f-186">**Header**</span></span> | <span data-ttu-id="af71f-187">directml.h</span><span class="sxs-lookup"><span data-stu-id="af71f-187">directml.h</span></span> |