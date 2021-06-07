---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Computa as coordenadas N-dimensional de todos os elementos diferentes de zero do tensor de entrada.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416942"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a><span data-ttu-id="c4b1a-103">Estrutura de DML_NONZERO_COORDINATES_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c4b1a-103">DML_NONZERO_COORDINATES_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c4b1a-104">Computa as coordenadas N-dimensional de todos os elementos diferentes de zero do tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-104">Computes the N-dimensional coordinates of all non-zero elements of the input tensor.</span></span>

<span data-ttu-id="c4b1a-105">Esse operador produz uma matriz MxN de valores, em que cada linha M contém uma coordenada N-dimensional de um valor diferente de zero da entrada.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-105">This operator produces an MxN matrix of values, where each row M contains an N-dimensional coordinate of a non-zero value from the input.</span></span> <span data-ttu-id="c4b1a-106">Ao usar as entradas **FLOAT32** ou **FLOAT16** , ambos negativos e positivos 0 (0,0 f e-0,0 f) são tratados como zero para fins deste operador.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-106">When using **FLOAT32** or **FLOAT16** inputs, both negative and positive 0 (0.0f and -0.0f) are treated as zero for the purposes of this operator.</span></span>

<span data-ttu-id="c4b1a-107">O operador requer que o *OutputCoordinatesTensor* tenha um tamanho grande o suficiente para acomodar um cenário de pior caso em que cada elemento da entrada é diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-107">The operator requires that the *OutputCoordinatesTensor* has a size large enough to accommodate a worst-case scenario where every element of the input is non-zero.</span></span> <span data-ttu-id="c4b1a-108">Esse operador retorna a contagem de elementos diferentes de zero por meio do *OutputCountTensor*, que os chamadores podem inspecionar para determinar o número de coordenadas gravadas no *OutputCoordinatesTensor*.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-108">This operator returns the count of of non-zero elements via the *OutputCountTensor*, which callers can inspect to determine the number of coordinates written to the *OutputCoordinatesTensor*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4b1a-109">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c4b1a-110">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c4b1a-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b1a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4b1a-111">Syntax</span></span>

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a><span data-ttu-id="c4b1a-112">Membros</span><span class="sxs-lookup"><span data-stu-id="c4b1a-112">Members</span></span>

`InputTensor`

<span data-ttu-id="c4b1a-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c4b1a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c4b1a-114">Um tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-114">An input tensor.</span></span>

`OutputCountTensor`

<span data-ttu-id="c4b1a-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c4b1a-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c4b1a-116">Um tensor de saída que contém a contagem de elementos diferentes de zero no tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-116">An output tensor that holds the count of non-zero elements in the input tensor.</span></span> <span data-ttu-id="c4b1a-117">Esse tensor deve ser um escalar &mdash; ou seja, os tamanhos desse tensor devem ser 1.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-117">This tensor must be a scalar&mdash;that is, the Sizes of this tensor must all be 1.</span></span> <span data-ttu-id="c4b1a-118">O tipo deste tensor deve ser **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-118">The type of this tensor must be **UINT32**.</span></span>

`OutputCoordinatesTensor`

<span data-ttu-id="c4b1a-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c4b1a-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c4b1a-120">Um tensor de saída que contém as coordenadas N-dimensional dos elementos Input que são diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-120">An output tensor that holds the N-dimensional coordinates of the input elements which are non-zero.</span></span> 

<span data-ttu-id="c4b1a-121">Esse tensor deve ter *tamanhos* de `{1,1,M,N}` (se *DimensionCount* for 4) ou `{1,1,1,M,N}` (se *DimensionCount* for 5), em que M é o número total de elementos na *InputTensor* e N é maior ou igual à *classificação efetiva* de *InputTensor*, até o *DimensionCount* da entrada.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-121">This tensor must have *Sizes* of `{1,1,M,N}` (if *DimensionCount* is 4), or `{1,1,1,M,N}` (if *DimensionCount* is 5), where M is the total number of elements in the *InputTensor*, and N is greater or equal to the *effective rank* of *InputTensor*, up to the *DimensionCount* of the input.</span></span>

<span data-ttu-id="c4b1a-122">A classificação efetiva de um tensor é determinada pelo *DimensionCount* do tensor, excluindo as principais dimensões do tamanho 1.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-122">The effective rank of a tensor is determined by the *DimensionCount* of that tensor excluding leading dimensions of size 1.</span></span> <span data-ttu-id="c4b1a-123">Por exemplo, um tensor com tamanhos de `{1,2,3,4}` tem a classificação efetiva 3, como faz um tensor com tamanhos de `{1,1,5,5,5}` .</span><span class="sxs-lookup"><span data-stu-id="c4b1a-123">For example a tensor with sizes of `{1,2,3,4}` has effective rank 3, as does a tensor with sizes of `{1,1,5,5,5}`.</span></span> <span data-ttu-id="c4b1a-124">Um tensor com tamanhos `{1,1,1,1}` tem A classificação efetiva 0.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-124">A tensor with sizes `{1,1,1,1}` has effective rank 0.</span></span>

<span data-ttu-id="c4b1a-125">Considere um *InputTensor* com *tamanhos* de `{1,1,12,5}` .</span><span class="sxs-lookup"><span data-stu-id="c4b1a-125">Consider an *InputTensor* with *Sizes* of `{1,1,12,5}`.</span></span> <span data-ttu-id="c4b1a-126">Este tensor de entrada contém 60 elementos e tem uma classificação efetiva de 2.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-126">This input tensor contains 60 elements, and has an effective rank of 2.</span></span> <span data-ttu-id="c4b1a-127">Neste exemplo, todos os tamanhos válidos de *OutputCoordinatesTensor* são do formulário `{1,1,60,N}` , em que N >= 2, mas não maior que o *DimensionCount* (4 neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="c4b1a-127">In this example all valid sizes of *OutputCoordinatesTensor* are of the form `{1,1,60,N}`, where N >= 2 but no greater than the *DimensionCount* (4 in this example).</span></span>

<span data-ttu-id="c4b1a-128">As coordenadas escritas nesse tensor têm garantia de serem ordenadas por índice de elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-128">The coordinates written into this tensor are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="c4b1a-129">Por exemplo, se o tensor de entrada tiver 3 valores diferentes de zero em coordenadas {1,0} , {1,2} e {0,5} os valores gravados em *OutputCoordinatesTensor* serão `[[0,5], [1,0], [1,2]]` .</span><span class="sxs-lookup"><span data-stu-id="c4b1a-129">For example if the input tensor has 3 non-zero values at coordinates {1,0}, {1,2}, and {0,5}, the values written to the *OutputCoordinatesTensor* will be `[[0,5], [1,0], [1,2]]`.</span></span>

<span data-ttu-id="c4b1a-130">Embora esse tensor exija que sua dimensão M seja igual ao número de elementos no tensor de entrada, esse operador gravará apenas um máximo de elementos de OutputCount para esse tensor.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-130">While this tensor requires its dimension M to equal the number of elements in the input tensor, this operator will only write a maximum of OutputCount elements to this tensor.</span></span> <span data-ttu-id="c4b1a-131">O OutputCount é retornado por meio do *OutputCountTensor* escalar.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-131">The OutputCount is returned through the scalar *OutputCountTensor*.</span></span>

> [!NOTE]
> <span data-ttu-id="c4b1a-132">Os elementos restantes desse tensor além do OutputCount são indefinidos quando esse operador é concluído.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-132">The remaining elements of this tensor beyond the OutputCount are undefined once this operator completes.</span></span> <span data-ttu-id="c4b1a-133">Você não deve contar com os valores desses elementos.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-133">You shouldn't rely on the values of these elements.</span></span>

## <a name="example"></a><span data-ttu-id="c4b1a-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c4b1a-134">Example</span></span>

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a><span data-ttu-id="c4b1a-135">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="c4b1a-135">Availability</span></span>
<span data-ttu-id="c4b1a-136">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="c4b1a-136">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c4b1a-137">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="c4b1a-137">Tensor constraints</span></span>
<span data-ttu-id="c4b1a-138">*InputTensor*, *OutputCoordinatesTensor* e `OutputCountTensor` deve ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="c4b1a-138">*InputTensor*, *OutputCoordinatesTensor*, and `OutputCountTensor` must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c4b1a-139">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="c4b1a-139">Tensor support</span></span>
| <span data-ttu-id="c4b1a-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="c4b1a-140">Tensor</span></span> | <span data-ttu-id="c4b1a-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4b1a-141">Kind</span></span> | <span data-ttu-id="c4b1a-142">Dimensões</span><span class="sxs-lookup"><span data-stu-id="c4b1a-142">Dimensions</span></span> | <span data-ttu-id="c4b1a-143">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="c4b1a-143">Supported dimension counts</span></span> | <span data-ttu-id="c4b1a-144">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="c4b1a-144">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="c4b1a-145">InputTensor</span><span class="sxs-lookup"><span data-stu-id="c4b1a-145">InputTensor</span></span> | <span data-ttu-id="c4b1a-146">Entrada</span><span class="sxs-lookup"><span data-stu-id="c4b1a-146">Input</span></span> | <span data-ttu-id="c4b1a-147">{[D0], D1, D2, D3, D4}</span><span class="sxs-lookup"><span data-stu-id="c4b1a-147">{ [D0], D1, D2, D3, D4 }</span></span> | <span data-ttu-id="c4b1a-148">4 a 5</span><span class="sxs-lookup"><span data-stu-id="c4b1a-148">4 to 5</span></span> | <span data-ttu-id="c4b1a-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c4b1a-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c4b1a-150">OutputCountTensor</span><span class="sxs-lookup"><span data-stu-id="c4b1a-150">OutputCountTensor</span></span> | <span data-ttu-id="c4b1a-151">Saída</span><span class="sxs-lookup"><span data-stu-id="c4b1a-151">Output</span></span> | <span data-ttu-id="c4b1a-152">{[1], 1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="c4b1a-152">{ [1], 1, 1, 1, 1 }</span></span> | <span data-ttu-id="c4b1a-153">4 a 5</span><span class="sxs-lookup"><span data-stu-id="c4b1a-153">4 to 5</span></span> | <span data-ttu-id="c4b1a-154">UINT32</span><span class="sxs-lookup"><span data-stu-id="c4b1a-154">UINT32</span></span> |
| <span data-ttu-id="c4b1a-155">OutputCoordinatesTensor</span><span class="sxs-lookup"><span data-stu-id="c4b1a-155">OutputCoordinatesTensor</span></span> | <span data-ttu-id="c4b1a-156">Saída</span><span class="sxs-lookup"><span data-stu-id="c4b1a-156">Output</span></span> | <span data-ttu-id="c4b1a-157">{[1], 1, 1, M, N}</span><span class="sxs-lookup"><span data-stu-id="c4b1a-157">{ [1], 1, 1, M, N }</span></span> | <span data-ttu-id="c4b1a-158">4 a 5</span><span class="sxs-lookup"><span data-stu-id="c4b1a-158">4 to 5</span></span> | <span data-ttu-id="c4b1a-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="c4b1a-159">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="c4b1a-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4b1a-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c4b1a-161">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="c4b1a-161">**Header**</span></span> | <span data-ttu-id="c4b1a-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="c4b1a-162">directml.h</span></span> |