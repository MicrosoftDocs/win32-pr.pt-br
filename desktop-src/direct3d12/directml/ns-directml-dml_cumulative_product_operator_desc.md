---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multiplica os elementos de um tensor ao longo de um eixo, escrevendo a conta em execução do produto no tensor de saída.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 71a078ad0f47c19ad1964d8d21f22e06822b5d01
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550211"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="b9ca3-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b9ca3-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="b9ca3-104">Multiplica os elementos de um tensor ao longo de um eixo, escrevendo a conta em execução do produto no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9ca3-105">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.5 e posterior).</span><span class="sxs-lookup"><span data-stu-id="b9ca3-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="b9ca3-106">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b9ca3-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ca3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9ca3-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a><span data-ttu-id="b9ca3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b9ca3-108">Members</span></span>

`InputTensor`

<span data-ttu-id="b9ca3-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9ca3-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9ca3-110">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-110">A tensor containing the input data.</span></span> <span data-ttu-id="b9ca3-111">Normalmente, esse é o mesmo tensor que foi fornecido como *o InputTensor* para DML_BATCH_NORMALIZATION_OPERATOR_DESC [**na**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passagem de avanço.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="b9ca3-112">O tensor de entrada que contém elementos a serem multiplicados.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="b9ca3-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b9ca3-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b9ca3-114">O tensor de saída para gravar os produtos cumulativos resultantes.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="b9ca3-115">Esse tensor deve ter os mesmos tamanhos e tipo de dados *que InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="b9ca3-116">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b9ca3-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b9ca3-117">O índice da dimensão sobre a que multiplicar elementos.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="b9ca3-118">Esse valor deve ser menor que *DimensionCount* do *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="b9ca3-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="b9ca3-119">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="b9ca3-119">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="b9ca3-120">Um dos valores da [enumeração DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) dados.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-120">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="b9ca3-121">Se definido como **DML_AXIS_DIRECTION_INCREASING**, o produto ocorrerá atravessando o tensor ao longo do eixo especificado pelo índice de elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="b9ca3-122">Se definido como **DML_AXIS_DIRECTION_DECREASING**, o inverso será true e o produto ocorrerá atravessando elementos por índice decrescente.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="b9ca3-123">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="b9ca3-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="b9ca3-124">Se **for true**, o valor do elemento atual será excluído ao gravar a contagem em execução no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="b9ca3-125">Se **for false**, o valor do elemento atual será incluído na contagem em execução.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="b9ca3-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9ca3-126">Examples</span></span>

<span data-ttu-id="b9ca3-127">Todos os exemplos nesta seção usam esse mesmo tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="b9ca3-128">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-128">Example 1.</span></span> <span data-ttu-id="b9ca3-129">Produto cumulativo entre slivers horizontais</span><span class="sxs-lookup"><span data-stu-id="b9ca3-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="b9ca3-130">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-130">Example 2.</span></span> <span data-ttu-id="b9ca3-131">Produtos exclusivos</span><span class="sxs-lookup"><span data-stu-id="b9ca3-131">Exclusive products</span></span>

<span data-ttu-id="b9ca3-132">Definir *HasExclusiveProduct* como **true** tem o efeito de excluir o valor do elemento atual da contagem em execução ao gravar no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="b9ca3-133">Exemplo 3.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-133">Example 3.</span></span> <span data-ttu-id="b9ca3-134">Direção do eixo</span><span class="sxs-lookup"><span data-stu-id="b9ca3-134">Axis direction</span></span>

<span data-ttu-id="b9ca3-135">Definir o *AxisDirection* como [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) tem o efeito de reverter a ordem de percurso dos elementos ao calcular a contagem em execução.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="b9ca3-136">Exemplo 4.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-136">Example 4.</span></span> <span data-ttu-id="b9ca3-137">Multiplicação ao longo de um eixo diferente</span><span class="sxs-lookup"><span data-stu-id="b9ca3-137">Multiplying along a different axis</span></span>

<span data-ttu-id="b9ca3-138">Neste exemplo, o produto ocorre verticalmente, ao longo do eixo de altura (segunda dimensão).</span><span class="sxs-lookup"><span data-stu-id="b9ca3-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="b9ca3-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9ca3-139">Remarks</span></span>
<span data-ttu-id="b9ca3-140">Esse operador dá suporte à execução in-loco, o que significa que a saída tensor é permitida para o alias *InputTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="b9ca3-141">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="b9ca3-141">Availability</span></span>
<span data-ttu-id="b9ca3-142">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="b9ca3-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b9ca3-143">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="b9ca3-143">Tensor constraints</span></span>
<span data-ttu-id="b9ca3-144">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="b9ca3-144">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b9ca3-145">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="b9ca3-145">Tensor support</span></span>
| <span data-ttu-id="b9ca3-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="b9ca3-146">Tensor</span></span> | <span data-ttu-id="b9ca3-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9ca3-147">Kind</span></span> | <span data-ttu-id="b9ca3-148">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="b9ca3-148">Supported dimension counts</span></span> | <span data-ttu-id="b9ca3-149">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b9ca3-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b9ca3-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b9ca3-150">InputTensor</span></span> | <span data-ttu-id="b9ca3-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="b9ca3-151">Input</span></span> | <span data-ttu-id="b9ca3-152">4</span><span class="sxs-lookup"><span data-stu-id="b9ca3-152">4</span></span> | <span data-ttu-id="b9ca3-153">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="b9ca3-153">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="b9ca3-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b9ca3-154">OutputTensor</span></span> | <span data-ttu-id="b9ca3-155">Saída</span><span class="sxs-lookup"><span data-stu-id="b9ca3-155">Output</span></span> | <span data-ttu-id="b9ca3-156">4</span><span class="sxs-lookup"><span data-stu-id="b9ca3-156">4</span></span> | <span data-ttu-id="b9ca3-157">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="b9ca3-157">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b9ca3-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ca3-158">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b9ca3-159">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="b9ca3-159">**Header**</span></span> | <span data-ttu-id="b9ca3-160">directml.h</span><span class="sxs-lookup"><span data-stu-id="b9ca3-160">directml.h</span></span> |