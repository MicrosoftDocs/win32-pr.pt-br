---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Inverte os elementos de uma ou mais *subsequências* de um tensor. O conjunto de subsequências a serem revertidas é escolhido com base no eixo fornecido e nos comprimentos de sequência.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105766582"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="4be1a-104">Estrutura de DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="4be1a-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="4be1a-105">Inverte os elementos de uma ou mais *subsequências* de um tensor.</span><span class="sxs-lookup"><span data-stu-id="4be1a-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="4be1a-106">O conjunto de subsequências a serem revertidas é escolhido com base no eixo fornecido e nos comprimentos de sequência.</span><span class="sxs-lookup"><span data-stu-id="4be1a-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4be1a-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="4be1a-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="4be1a-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="4be1a-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4be1a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4be1a-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="4be1a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="4be1a-110">Members</span></span>

`InputTensor`

<span data-ttu-id="4be1a-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4be1a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4be1a-112">O tensor de entrada que contém elementos a serem revertidos.</span><span class="sxs-lookup"><span data-stu-id="4be1a-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="4be1a-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4be1a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4be1a-114">Um tensor que contém um valor para cada subsequência a ser revertida, denotando o comprimento em elementos dessa subsequência.</span><span class="sxs-lookup"><span data-stu-id="4be1a-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="4be1a-115">Somente os elementos dentro do comprimento da subsequência são revertidos; os elementos restantes ao longo desse eixo são copiados para a saída inalterada.</span><span class="sxs-lookup"><span data-stu-id="4be1a-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="4be1a-116">Esse tensor deve ter tamanhos e contagem de dimensão iguais ao *InputTensor*, *exceto* para a dimensão especificada pelo parâmetro *Axis* .</span><span class="sxs-lookup"><span data-stu-id="4be1a-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="4be1a-117">O tamanho da dimensão do *eixo* deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="4be1a-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="4be1a-118">Por exemplo, se *InputTensor* tiver tamanhos de `{2,3,4,5}` e *eixo* for 1, os tamanhos de *SequenceLengthsTensor* deverão ser `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="4be1a-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="4be1a-119">Se o comprimento de uma subsequência exceder o número máximo de elementos ao longo desse eixo, esse operador se comparará como se o valor fosse clamped ao máximo.</span><span class="sxs-lookup"><span data-stu-id="4be1a-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="4be1a-120">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4be1a-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4be1a-121">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="4be1a-121">The output tensor to write the results to.</span></span> <span data-ttu-id="4be1a-122">Esse tensor deve ter os mesmos tamanhos e tipo de dados que o *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4be1a-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="4be1a-123">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4be1a-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4be1a-124">O índice da dimensão para a qual reverter elementos.</span><span class="sxs-lookup"><span data-stu-id="4be1a-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="4be1a-125">Esse valor deve ser menor que o DimensionCount do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4be1a-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="4be1a-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4be1a-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="4be1a-127">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4be1a-127">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="4be1a-128">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="4be1a-128">Example 2.</span></span> <span data-ttu-id="4be1a-129">Revertendo ao longo de um eixo diferente</span><span class="sxs-lookup"><span data-stu-id="4be1a-129">Reversing along a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a><span data-ttu-id="4be1a-130">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4be1a-130">Availability</span></span>
<span data-ttu-id="4be1a-131">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="4be1a-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4be1a-132">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-132">Tensor constraints</span></span>
* <span data-ttu-id="4be1a-133">*InputTensor*, *OutputTensor* e *SequenceLengthsTensor* devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4be1a-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="4be1a-134">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="4be1a-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4be1a-135">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="4be1a-136">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="4be1a-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="4be1a-137">Tensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-137">Tensor</span></span> | <span data-ttu-id="4be1a-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="4be1a-138">Kind</span></span> | <span data-ttu-id="4be1a-139">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="4be1a-139">Supported dimension counts</span></span> | <span data-ttu-id="4be1a-140">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="4be1a-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4be1a-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-141">InputTensor</span></span> | <span data-ttu-id="4be1a-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="4be1a-142">Input</span></span> | <span data-ttu-id="4be1a-143">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4be1a-143">4 to 5</span></span> | <span data-ttu-id="4be1a-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4be1a-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4be1a-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="4be1a-146">Entrada</span><span class="sxs-lookup"><span data-stu-id="4be1a-146">Input</span></span> | <span data-ttu-id="4be1a-147">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4be1a-147">4 to 5</span></span> | <span data-ttu-id="4be1a-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="4be1a-148">UINT32</span></span> |
| <span data-ttu-id="4be1a-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-149">OutputTensor</span></span> | <span data-ttu-id="4be1a-150">Saída</span><span class="sxs-lookup"><span data-stu-id="4be1a-150">Output</span></span> | <span data-ttu-id="4be1a-151">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4be1a-151">4 to 5</span></span> | <span data-ttu-id="4be1a-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4be1a-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="4be1a-153">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="4be1a-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="4be1a-154">Tensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-154">Tensor</span></span> | <span data-ttu-id="4be1a-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="4be1a-155">Kind</span></span> | <span data-ttu-id="4be1a-156">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="4be1a-156">Supported dimension counts</span></span> | <span data-ttu-id="4be1a-157">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="4be1a-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4be1a-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-158">InputTensor</span></span> | <span data-ttu-id="4be1a-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="4be1a-159">Input</span></span> | <span data-ttu-id="4be1a-160">4</span><span class="sxs-lookup"><span data-stu-id="4be1a-160">4</span></span> | <span data-ttu-id="4be1a-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4be1a-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="4be1a-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="4be1a-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="4be1a-163">Input</span></span> | <span data-ttu-id="4be1a-164">4</span><span class="sxs-lookup"><span data-stu-id="4be1a-164">4</span></span> | <span data-ttu-id="4be1a-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="4be1a-165">UINT32</span></span> |
| <span data-ttu-id="4be1a-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4be1a-166">OutputTensor</span></span> | <span data-ttu-id="4be1a-167">Saída</span><span class="sxs-lookup"><span data-stu-id="4be1a-167">Output</span></span> | <span data-ttu-id="4be1a-168">4</span><span class="sxs-lookup"><span data-stu-id="4be1a-168">4</span></span> | <span data-ttu-id="4be1a-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="4be1a-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="4be1a-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4be1a-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4be1a-171">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="4be1a-171">**Header**</span></span> | <span data-ttu-id="4be1a-172">directml. h</span><span class="sxs-lookup"><span data-stu-id="4be1a-172">directml.h</span></span> |