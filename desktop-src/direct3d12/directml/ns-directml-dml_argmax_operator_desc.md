---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Gera os índices dos elementos com valor máximo em uma ou mais dimensões do tensor de entrada.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 4c2852c3d301a12d318c5e3006b26830c6eaa6e1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417000"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="18ca5-103">Estrutura de DML_ARGMAX_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="18ca5-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="18ca5-104">Gera os índices dos elementos com valor máximo em uma ou mais dimensões do tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="18ca5-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="18ca5-105">Cada elemento de saída é o resultado da aplicação de uma redução de *ARGMAX* em um subconjunto do tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="18ca5-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="18ca5-106">A função *ARGMAX* gera o índice do elemento com valor máximo em um conjunto de elementos de entrada.</span><span class="sxs-lookup"><span data-stu-id="18ca5-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="18ca5-107">Os elementos de entrada envolvidos em cada redução são determinados pelos eixos de entrada fornecidos.</span><span class="sxs-lookup"><span data-stu-id="18ca5-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="18ca5-108">Da mesma forma, cada índice de saída é relativo aos eixos de entrada fornecidos.</span><span class="sxs-lookup"><span data-stu-id="18ca5-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="18ca5-109">Se todos os eixos de entrada forem especificados, o operador aplicará uma única redução de *ARGMAX* e produzirá um único elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="18ca5-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18ca5-110">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="18ca5-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="18ca5-111">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="18ca5-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="18ca5-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18ca5-112">Syntax</span></span>
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="18ca5-113">Membros</span><span class="sxs-lookup"><span data-stu-id="18ca5-113">Members</span></span>

`InputTensor`

<span data-ttu-id="18ca5-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="18ca5-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="18ca5-115">O tensor do qual ler.</span><span class="sxs-lookup"><span data-stu-id="18ca5-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="18ca5-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="18ca5-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="18ca5-117">O tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="18ca5-117">The tensor to write the results to.</span></span> <span data-ttu-id="18ca5-118">Cada elemento de saída é o resultado de uma redução de *ARGMAX* em um subconjunto de elementos do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="18ca5-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="18ca5-119">*DimensionCount* deve corresponder a *InputTensor. DimensionCount* (a classificação da entrada tensor é preservada).</span><span class="sxs-lookup"><span data-stu-id="18ca5-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="18ca5-120">Os *tamanhos* devem corresponder a *InputTensor. Sizes*, exceto as dimensões incluídas nos *eixos* reduzidos, que devem ser de tamanho 1.</span><span class="sxs-lookup"><span data-stu-id="18ca5-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="18ca5-121">Tipo: **[uint](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18ca5-121">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18ca5-122">O número de eixos a serem reduzidos.</span><span class="sxs-lookup"><span data-stu-id="18ca5-122">The number of axes to reduce.</span></span> <span data-ttu-id="18ca5-123">Este campo determina o tamanho da matriz de *eixos* .</span><span class="sxs-lookup"><span data-stu-id="18ca5-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="18ca5-124">Tipo: \_ Field_size \_ (AxisCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="18ca5-124">Type: \_Field_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="18ca5-125">Os eixos ao longo do qual reduzir.</span><span class="sxs-lookup"><span data-stu-id="18ca5-125">The axes along which to reduce.</span></span> <span data-ttu-id="18ca5-126">Os valores devem estar no intervalo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="18ca5-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="18ca5-127">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="18ca5-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="18ca5-128">Determina qual índice deve ser selecionado quando vários elementos de entrada têm o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="18ca5-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="18ca5-129">**DML_AXIS_DIRECTION_INCREASING** retorna o índice do primeiro elemento com valor máximo (por exemplo, `argmax({3,2,1,2,3}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="18ca5-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="18ca5-130">**DML_AXIS_DIRECTION_DECREASING** retorna o índice do último elemento com valor máximo (por exemplo, `argmax({3,2,1,2,3}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="18ca5-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="18ca5-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18ca5-131">Examples</span></span>

<span data-ttu-id="18ca5-132">Os exemplos nesta seção usam esse mesmo tensor de entrada bidimensional.</span><span class="sxs-lookup"><span data-stu-id="18ca5-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="18ca5-133">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="18ca5-133">Example 1.</span></span> <span data-ttu-id="18ca5-134">Aplicando *ARGMAX* a colunas</span><span class="sxs-lookup"><span data-stu-id="18ca5-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="18ca5-135">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="18ca5-135">Example 2.</span></span> <span data-ttu-id="18ca5-136">Aplicando *ARGMAX* a linhas</span><span class="sxs-lookup"><span data-stu-id="18ca5-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="18ca5-137">Exemplo 3.</span><span class="sxs-lookup"><span data-stu-id="18ca5-137">Example 3.</span></span> <span data-ttu-id="18ca5-138">Aplicando *ARGMAX* a todos os eixos (toda a tensor)</span><span class="sxs-lookup"><span data-stu-id="18ca5-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="18ca5-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="18ca5-139">Remarks</span></span>
<span data-ttu-id="18ca5-140">Os tamanhos de tensor de saída devem ser iguais aos tamanhos de tensor de entrada, exceto para os eixos reduzidos, que devem ser 1.</span><span class="sxs-lookup"><span data-stu-id="18ca5-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="18ca5-141">Quando *AxisDirection* é [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), essa API é equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) com [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="18ca5-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="18ca5-142">Um subconjunto dessa funcionalidade é exposto por meio do operador de [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) e tem suporte em níveis de recursos de DirectML anteriores.</span><span class="sxs-lookup"><span data-stu-id="18ca5-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="18ca5-143">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="18ca5-143">Availability</span></span>
<span data-ttu-id="18ca5-144">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="18ca5-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="18ca5-145">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="18ca5-145">Tensor constraints</span></span>
<span data-ttu-id="18ca5-146">*InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="18ca5-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="18ca5-147">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="18ca5-147">Tensor support</span></span>
| <span data-ttu-id="18ca5-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="18ca5-148">Tensor</span></span> | <span data-ttu-id="18ca5-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="18ca5-149">Kind</span></span> | <span data-ttu-id="18ca5-150">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="18ca5-150">Supported dimension counts</span></span> | <span data-ttu-id="18ca5-151">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="18ca5-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="18ca5-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="18ca5-152">InputTensor</span></span> | <span data-ttu-id="18ca5-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="18ca5-153">Input</span></span> | <span data-ttu-id="18ca5-154">1 a 8</span><span class="sxs-lookup"><span data-stu-id="18ca5-154">1 to 8</span></span> | <span data-ttu-id="18ca5-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="18ca5-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="18ca5-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="18ca5-156">OutputTensor</span></span> | <span data-ttu-id="18ca5-157">Saída</span><span class="sxs-lookup"><span data-stu-id="18ca5-157">Output</span></span> | <span data-ttu-id="18ca5-158">1 a 8</span><span class="sxs-lookup"><span data-stu-id="18ca5-158">1 to 8</span></span> | <span data-ttu-id="18ca5-159">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="18ca5-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="18ca5-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18ca5-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="18ca5-161">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="18ca5-161">**Header**</span></span> | <span data-ttu-id="18ca5-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="18ca5-162">directml.h</span></span> |