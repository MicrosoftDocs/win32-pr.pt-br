---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Saída dos índices dos elementos com valor mínimo dentro de uma ou mais dimensões do tensor de entrada.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: da270ea5354e361067335ba1c789efe18310437a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416992"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="a5fa0-103">DML_ARGMIN_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a5fa0-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a5fa0-104">Saída dos índices dos elementos com valor mínimo dentro de uma ou mais dimensões do tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="a5fa0-105">Cada elemento de saída é o resultado da aplicação de uma *redução de argmin* em um subconjunto do tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="a5fa0-106">A *função argmin* saída o índice do elemento de valor mínimo dentro de um conjunto de elementos de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="a5fa0-107">Os elementos de entrada envolvidos em cada redução são determinados pelos eixos de entrada fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="a5fa0-108">Da mesma forma, cada índice de saída é em relação aos eixos de entrada fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="a5fa0-109">Se todos os eixos de entrada são especificados, o operador aplica uma única redução *de argmin* e produz um único elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5fa0-110">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="a5fa0-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a5fa0-111">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a5fa0-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fa0-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5fa0-112">Syntax</span></span>
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="a5fa0-113">Membros</span><span class="sxs-lookup"><span data-stu-id="a5fa0-113">Members</span></span>

`InputTensor`

<span data-ttu-id="a5fa0-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a5fa0-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a5fa0-115">O tensor do o que ler.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="a5fa0-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a5fa0-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a5fa0-117">O tensor no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-117">The tensor to write the results to.</span></span> <span data-ttu-id="a5fa0-118">Cada elemento de saída é o resultado de uma *redução de argmin* em um subconjunto de elementos do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="a5fa0-119">*DimensionCount* deve corresponder *a InputTensor.DimensionCount* (a classificação do tensor de entrada é preservada).</span><span class="sxs-lookup"><span data-stu-id="a5fa0-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="a5fa0-120">*Os* tamanhos *devem corresponder a InputTensor.Sizes,* exceto para dimensões incluídas nos *eixos reduzidos,* que devem ser de tamanho 1.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="a5fa0-121">Tipo: **[UINT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5fa0-121">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5fa0-122">O número de eixos a reduzir.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-122">The number of axes to reduce.</span></span> <span data-ttu-id="a5fa0-123">Esse campo determina o tamanho da matriz *Eixos.*</span><span class="sxs-lookup"><span data-stu-id="a5fa0-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="a5fa0-124">Tipo: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a5fa0-124">Type: \_Field_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a5fa0-125">Os eixos ao longo dos quais reduzir.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-125">The axes along which to reduce.</span></span> <span data-ttu-id="a5fa0-126">Os valores devem estar no intervalo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="a5fa0-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="a5fa0-127">DML_AXIS_DIRECTION AxisDirection;</span><span class="sxs-lookup"><span data-stu-id="a5fa0-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="a5fa0-128">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="a5fa0-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="a5fa0-129">Determina qual índice selecionar quando vários elementos de entrada têm o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="a5fa0-130">**DML_AXIS_DIRECTION_INCREASING** retorna o índice do primeiro elemento com valor mínimo (por exemplo, `argmin({1,2,3,2,1}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="a5fa0-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="a5fa0-131">**DML_AXIS_DIRECTION_DECREASING** retorna o índice do último elemento com valor mínimo (por exemplo, `argmin({1,2,3,2,1}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="a5fa0-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="a5fa0-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a5fa0-132">Examples</span></span>

<span data-ttu-id="a5fa0-133">Os exemplos nesta seção usam esse mesmo tensor de entrada bidimensional.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="a5fa0-134">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-134">Example 1.</span></span> <span data-ttu-id="a5fa0-135">Aplicando *argmin* a colunas</span><span class="sxs-lookup"><span data-stu-id="a5fa0-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="a5fa0-136">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-136">Example 2.</span></span> <span data-ttu-id="a5fa0-137">Aplicando *argmin* a linhas</span><span class="sxs-lookup"><span data-stu-id="a5fa0-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="a5fa0-138">Exemplo 3.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-138">Example 3.</span></span> <span data-ttu-id="a5fa0-139">Aplicando *argmin* a todos os eixos (o tensor inteiro)</span><span class="sxs-lookup"><span data-stu-id="a5fa0-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="a5fa0-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5fa0-140">Remarks</span></span>
<span data-ttu-id="a5fa0-141">Os tamanhos do tensor de saída devem ser iguais aos tamanhos do tensor de entrada, exceto pelos eixos reduzidos, que devem ser 1.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="a5fa0-142">Quando *AxisDirection é* [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), essa API é equivalente [a](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) DML_REDUCE_OPERATOR_DESC com [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="a5fa0-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="a5fa0-143">Um subconjunto dessa funcionalidade é exposto por meio [do operador DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) e tem suporte em níveis de recursos directML anteriores.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="a5fa0-144">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a5fa0-144">Availability</span></span>
<span data-ttu-id="a5fa0-145">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a5fa0-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a5fa0-146">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="a5fa0-146">Tensor constraints</span></span>
<span data-ttu-id="a5fa0-147">*InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="a5fa0-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a5fa0-148">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="a5fa0-148">Tensor support</span></span>
| <span data-ttu-id="a5fa0-149">Tensor</span><span class="sxs-lookup"><span data-stu-id="a5fa0-149">Tensor</span></span> | <span data-ttu-id="a5fa0-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5fa0-150">Kind</span></span> | <span data-ttu-id="a5fa0-151">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fa0-151">Supported dimension counts</span></span> | <span data-ttu-id="a5fa0-152">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="a5fa0-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a5fa0-153">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a5fa0-153">InputTensor</span></span> | <span data-ttu-id="a5fa0-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5fa0-154">Input</span></span> | <span data-ttu-id="a5fa0-155">1 a 8</span><span class="sxs-lookup"><span data-stu-id="a5fa0-155">1 to 8</span></span> | <span data-ttu-id="a5fa0-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a5fa0-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a5fa0-157">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a5fa0-157">OutputTensor</span></span> | <span data-ttu-id="a5fa0-158">Saída</span><span class="sxs-lookup"><span data-stu-id="a5fa0-158">Output</span></span> | <span data-ttu-id="a5fa0-159">1 a 8</span><span class="sxs-lookup"><span data-stu-id="a5fa0-159">1 to 8</span></span> | <span data-ttu-id="a5fa0-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="a5fa0-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="a5fa0-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5fa0-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a5fa0-162">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a5fa0-162">**Header**</span></span> | <span data-ttu-id="a5fa0-163">directml.h</span><span class="sxs-lookup"><span data-stu-id="a5fa0-163">directml.h</span></span> |