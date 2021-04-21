---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Seleciona os maiores ou menores elementos *K* de cada sequência ao longo de um eixo de *InputTensor* e retorna os valores e índices desses elementos em *OutputValueTensor* e *OutputIndexTensor*, respectivamente.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803818"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="44a9b-103">Estrutura de DML_TOP_K1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="44a9b-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="44a9b-104">Seleciona os maiores ou menores elementos *K* de cada sequência ao longo de um eixo de *InputTensor* e retorna os valores e índices desses elementos em *OutputValueTensor* e *OutputIndexTensor*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="44a9b-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="44a9b-105">Uma *sequência* refere-se a um dos conjuntos de elementos que existem ao longo da dimensão de *eixo* do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="44a9b-106">A escolha de se deseja selecionar os maiores elementos K ou os menores K podem ser controlados usando *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44a9b-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="44a9b-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="44a9b-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="44a9b-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44a9b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44a9b-109">Syntax</span></span>
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="44a9b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="44a9b-110">Members</span></span>

`InputTensor`

<span data-ttu-id="44a9b-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44a9b-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44a9b-112">O tensor de entrada que contém os elementos a serem selecionados.</span><span class="sxs-lookup"><span data-stu-id="44a9b-112">The input tensor containing elements to select.</span></span>

`OutputValueTensor`

<span data-ttu-id="44a9b-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44a9b-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44a9b-114">O tensor de saída para gravar os valores dos primeiros *K* elementos em.</span><span class="sxs-lookup"><span data-stu-id="44a9b-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="44a9b-115">Os primeiros elementos *K* são selecionados com base no fato de serem os maiores ou menores, dependendo do valor de *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="44a9b-116">Esse tensor deve ter tamanhos iguais a *InputTensor*, *exceto* para a dimensão especificada pelo parâmetro *Axis* , que deve ter um tamanho igual a *K*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="44a9b-117">Os valores *K* selecionados de cada sequência de entrada têm a garantia de serem classificados como decrescentes (maior do que o menor) se *AxisDirection* for [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span><span class="sxs-lookup"><span data-stu-id="44a9b-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="44a9b-118">Caso contrário, o oposto é verdadeiro e os valores selecionados têm a garantia de serem classificados em ordem crescente (menor para o maior).</span><span class="sxs-lookup"><span data-stu-id="44a9b-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>

`OutputIndexTensor`

<span data-ttu-id="44a9b-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44a9b-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44a9b-120">O tensor de saída para gravar os índices dos primeiros *K* elementos em.</span><span class="sxs-lookup"><span data-stu-id="44a9b-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="44a9b-121">Esse tensor deve ter tamanhos iguais a *InputTensor*, *exceto* para a dimensão especificada pelo parâmetro *Axis* , que deve ter um tamanho igual a *K*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="44a9b-122">Os índices retornados neste tensor são medidos em relação ao início de sua sequência (em oposição ao início do tensor).</span><span class="sxs-lookup"><span data-stu-id="44a9b-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="44a9b-123">Por exemplo, um índice de 0 sempre se refere ao primeiro elemento para todas as sequências em um eixo.</span><span class="sxs-lookup"><span data-stu-id="44a9b-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="44a9b-124">Nos casos em que dois ou mais elementos de Top-K têm o mesmo valor (ou seja, quando há um empate), os índices de ambos os elementos são incluídos e têm a garantia de serem ordenados por índice de elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="44a9b-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="44a9b-125">Observe que isso é verdadeiro independentemente do valor de *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>

`Axis`

<span data-ttu-id="44a9b-126">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="44a9b-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="44a9b-127">O índice da dimensão na qual selecionar elementos.</span><span class="sxs-lookup"><span data-stu-id="44a9b-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="44a9b-128">Esse valor deve ser menor que o *DimensionCount* do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`K`

<span data-ttu-id="44a9b-129">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="44a9b-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="44a9b-130">O número de elementos a serem selecionados.</span><span class="sxs-lookup"><span data-stu-id="44a9b-130">The number of elements to select.</span></span> <span data-ttu-id="44a9b-131">*K* deve ser maior que 0, mas menor que o número de elementos no *InputTensor* ao longo da dimensão especificada por *Axis*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>

`AxisDirection`

<span data-ttu-id="44a9b-132">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="44a9b-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="44a9b-133">Um valor da enumeração de [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="44a9b-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="44a9b-134">Se definido como **DML_AXIS_DIRECTION_INCREASING**, esse operador retornará os *menores* elementos *K* na ordem de aumento do valor.</span><span class="sxs-lookup"><span data-stu-id="44a9b-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="44a9b-135">Caso contrário, retornará os *maiores* elementos *K* em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="44a9b-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="44a9b-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44a9b-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="44a9b-137">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44a9b-137">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="44a9b-138">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="44a9b-138">Example 2.</span></span> <span data-ttu-id="44a9b-139">Usando um eixo diferente</span><span class="sxs-lookup"><span data-stu-id="44a9b-139">Using a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a><span data-ttu-id="44a9b-140">Exemplo 3.</span><span class="sxs-lookup"><span data-stu-id="44a9b-140">Example 3.</span></span> <span data-ttu-id="44a9b-141">Valores vinculados</span><span class="sxs-lookup"><span data-stu-id="44a9b-141">Tied values</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="44a9b-142">Exemplo 4.</span><span class="sxs-lookup"><span data-stu-id="44a9b-142">Example 4.</span></span> <span data-ttu-id="44a9b-143">Aumentando a direção do eixo</span><span class="sxs-lookup"><span data-stu-id="44a9b-143">Increasing axis direction</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a><span data-ttu-id="44a9b-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="44a9b-144">Remarks</span></span>
<span data-ttu-id="44a9b-145">Quando *AxisDirection* é definido como [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), esse operador é equivalente a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="44a9b-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="44a9b-146">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="44a9b-146">Availability</span></span>
<span data-ttu-id="44a9b-147">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="44a9b-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="44a9b-148">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-148">Tensor constraints</span></span>

* <span data-ttu-id="44a9b-149">*InputTensor*, *OutputIndexTensor* e *OutputValueTensor* devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-149">*InputTensor*, *OutputIndexTensor*, and *OutputValueTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="44a9b-150">*InputTensor* e *OutputValueTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="44a9b-150">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="44a9b-151">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="44a9b-152">DML_FEATURE_LEVEL_3_1 e acima</span><span class="sxs-lookup"><span data-stu-id="44a9b-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="44a9b-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-153">Tensor</span></span> | <span data-ttu-id="44a9b-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="44a9b-154">Kind</span></span> | <span data-ttu-id="44a9b-155">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="44a9b-155">Supported dimension counts</span></span> | <span data-ttu-id="44a9b-156">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="44a9b-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="44a9b-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-157">InputTensor</span></span> | <span data-ttu-id="44a9b-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="44a9b-158">Input</span></span> | <span data-ttu-id="44a9b-159">1 a 8</span><span class="sxs-lookup"><span data-stu-id="44a9b-159">1 to 8</span></span> | <span data-ttu-id="44a9b-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="44a9b-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="44a9b-161">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-161">OutputValueTensor</span></span> | <span data-ttu-id="44a9b-162">Saída</span><span class="sxs-lookup"><span data-stu-id="44a9b-162">Output</span></span> | <span data-ttu-id="44a9b-163">1 a 8</span><span class="sxs-lookup"><span data-stu-id="44a9b-163">1 to 8</span></span> | <span data-ttu-id="44a9b-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="44a9b-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="44a9b-165">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-165">OutputIndexTensor</span></span> | <span data-ttu-id="44a9b-166">Saída</span><span class="sxs-lookup"><span data-stu-id="44a9b-166">Output</span></span> | <span data-ttu-id="44a9b-167">1 a 8</span><span class="sxs-lookup"><span data-stu-id="44a9b-167">1 to 8</span></span> | <span data-ttu-id="44a9b-168">UINT32</span><span class="sxs-lookup"><span data-stu-id="44a9b-168">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="44a9b-169">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="44a9b-169">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="44a9b-170">Tensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-170">Tensor</span></span> | <span data-ttu-id="44a9b-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="44a9b-171">Kind</span></span> | <span data-ttu-id="44a9b-172">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="44a9b-172">Supported dimension counts</span></span> | <span data-ttu-id="44a9b-173">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="44a9b-173">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="44a9b-174">InputTensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-174">InputTensor</span></span> | <span data-ttu-id="44a9b-175">Entrada</span><span class="sxs-lookup"><span data-stu-id="44a9b-175">Input</span></span> | <span data-ttu-id="44a9b-176">4</span><span class="sxs-lookup"><span data-stu-id="44a9b-176">4</span></span> | <span data-ttu-id="44a9b-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="44a9b-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="44a9b-178">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-178">OutputValueTensor</span></span> | <span data-ttu-id="44a9b-179">Saída</span><span class="sxs-lookup"><span data-stu-id="44a9b-179">Output</span></span> | <span data-ttu-id="44a9b-180">4</span><span class="sxs-lookup"><span data-stu-id="44a9b-180">4</span></span> | <span data-ttu-id="44a9b-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="44a9b-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="44a9b-182">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="44a9b-182">OutputIndexTensor</span></span> | <span data-ttu-id="44a9b-183">Saída</span><span class="sxs-lookup"><span data-stu-id="44a9b-183">Output</span></span> | <span data-ttu-id="44a9b-184">4</span><span class="sxs-lookup"><span data-stu-id="44a9b-184">4</span></span> | <span data-ttu-id="44a9b-185">UINT32</span><span class="sxs-lookup"><span data-stu-id="44a9b-185">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="44a9b-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44a9b-186">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="44a9b-187">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="44a9b-187">**Header**</span></span> | <span data-ttu-id="44a9b-188">directml. h</span><span class="sxs-lookup"><span data-stu-id="44a9b-188">directml.h</span></span> |
