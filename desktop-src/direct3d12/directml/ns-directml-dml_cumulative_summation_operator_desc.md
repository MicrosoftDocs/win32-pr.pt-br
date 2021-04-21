---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Soma os elementos de um tensor ao longo de um eixo, gravando a contagem de execução da soma no tensor de saída.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803344"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="b41f1-103">Estrutura de DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b41f1-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b41f1-104">Soma os elementos de um tensor ao longo de um eixo, gravando a contagem de execução da soma no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="b41f1-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b41f1-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="b41f1-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b41f1-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b41f1-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b41f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b41f1-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a><span data-ttu-id="b41f1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b41f1-108">Members</span></span>

`InputTensor`

<span data-ttu-id="b41f1-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b41f1-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b41f1-110">O tensor de entrada que contém os elementos a serem somados.</span><span class="sxs-lookup"><span data-stu-id="b41f1-110">The input tensor containing elements to be summed.</span></span>

`OutputTensor`

<span data-ttu-id="b41f1-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b41f1-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b41f1-112">A saída tensor para gravar as somas cumulativas resultantes.</span><span class="sxs-lookup"><span data-stu-id="b41f1-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="b41f1-113">Esse tensor deve ter os mesmos tamanhos e tipo de dados que o *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b41f1-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="b41f1-114">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b41f1-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b41f1-115">O índice da dimensão à qual somar elementos.</span><span class="sxs-lookup"><span data-stu-id="b41f1-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="b41f1-116">Esse valor deve ser menor que o *DimensionCount* do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b41f1-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="b41f1-117">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="b41f1-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="b41f1-118">Um dos valores da enumeração [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="b41f1-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="b41f1-119">Se for definido como **DML_AXIS_DIRECTION_INCREASING**, a soma ocorrerá atravessando o tensor ao longo do eixo especificado por índice de elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="b41f1-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="b41f1-120">Se definido como **DML_AXIS_DIRECTION_DECREASING**, o inverso será true e a soma ocorrerá atravessando os elementos por índice decrescente.</span><span class="sxs-lookup"><span data-stu-id="b41f1-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>

`HasExclusiveSum`

<span data-ttu-id="b41f1-121">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="b41f1-121">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="b41f1-122">Se **for true**, o valor do elemento atual será excluído ao gravar a contagem em execução no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="b41f1-122">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="b41f1-123">Se **for false**, o valor do elemento atual será incluído na contagem em execução.</span><span class="sxs-lookup"><span data-stu-id="b41f1-123">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="b41f1-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b41f1-124">Examples</span></span>

<span data-ttu-id="b41f1-125">Os exemplos nesta seção usam um tensor de entrada com as propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="b41f1-125">The examples in this section all use an input tensor with the following properties.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a><span data-ttu-id="b41f1-126">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="b41f1-126">Example 1.</span></span> <span data-ttu-id="b41f1-127">Soma cumulativa entre slivers horizontais</span><span class="sxs-lookup"><span data-stu-id="b41f1-127">Cumulative summation across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a><span data-ttu-id="b41f1-128">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="b41f1-128">Example 2.</span></span> <span data-ttu-id="b41f1-129">Somas exclusivas</span><span class="sxs-lookup"><span data-stu-id="b41f1-129">Exclusive sums</span></span>

<span data-ttu-id="b41f1-130">Definir *HasExclusiveSum* como **true** tem o efeito de excluir o valor do elemento atual da contagem em execução ao gravar no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="b41f1-130">Setting *HasExclusiveSum* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="b41f1-131">Exemplo 3.</span><span class="sxs-lookup"><span data-stu-id="b41f1-131">Example 3.</span></span> <span data-ttu-id="b41f1-132">Direção do eixo</span><span class="sxs-lookup"><span data-stu-id="b41f1-132">Axis direction</span></span>

<span data-ttu-id="b41f1-133">Definir o *AxisDirection* como [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) tem o efeito de reverter a ordem de percurso dos elementos ao calcular a contagem em execução.</span><span class="sxs-lookup"><span data-stu-id="b41f1-133">Setting the *AxisDirection* to [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a><span data-ttu-id="b41f1-134">Exemplo 4.</span><span class="sxs-lookup"><span data-stu-id="b41f1-134">Example 4.</span></span> <span data-ttu-id="b41f1-135">Somando ao longo de um eixo diferente</span><span class="sxs-lookup"><span data-stu-id="b41f1-135">Summing along a different axis</span></span>

<span data-ttu-id="b41f1-136">Neste exemplo, a soma ocorre verticalmente, ao longo do eixo de altura (segunda dimensão).</span><span class="sxs-lookup"><span data-stu-id="b41f1-136">In this example, the summation occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a><span data-ttu-id="b41f1-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="b41f1-137">Remarks</span></span>
<span data-ttu-id="b41f1-138">Esse operador dá suporte à execução in-loco, o que significa que o *OutputTensor* tem permissão para alias do *InputTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="b41f1-138">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="b41f1-139">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="b41f1-139">Availability</span></span>
<span data-ttu-id="b41f1-140">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b41f1-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b41f1-141">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="b41f1-141">Tensor constraints</span></span>
<span data-ttu-id="b41f1-142">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="b41f1-142">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b41f1-143">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="b41f1-143">Tensor support</span></span>
| <span data-ttu-id="b41f1-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="b41f1-144">Tensor</span></span> | <span data-ttu-id="b41f1-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="b41f1-145">Kind</span></span> | <span data-ttu-id="b41f1-146">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="b41f1-146">Supported dimension counts</span></span> | <span data-ttu-id="b41f1-147">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b41f1-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b41f1-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b41f1-148">InputTensor</span></span> | <span data-ttu-id="b41f1-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="b41f1-149">Input</span></span> | <span data-ttu-id="b41f1-150">4</span><span class="sxs-lookup"><span data-stu-id="b41f1-150">4</span></span> | <span data-ttu-id="b41f1-151">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="b41f1-151">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="b41f1-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b41f1-152">OutputTensor</span></span> | <span data-ttu-id="b41f1-153">Saída</span><span class="sxs-lookup"><span data-stu-id="b41f1-153">Output</span></span> | <span data-ttu-id="b41f1-154">4</span><span class="sxs-lookup"><span data-stu-id="b41f1-154">4</span></span> | <span data-ttu-id="b41f1-155">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="b41f1-155">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b41f1-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b41f1-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b41f1-157">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="b41f1-157">**Header**</span></span> | <span data-ttu-id="b41f1-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="b41f1-158">directml.h</span></span> |
