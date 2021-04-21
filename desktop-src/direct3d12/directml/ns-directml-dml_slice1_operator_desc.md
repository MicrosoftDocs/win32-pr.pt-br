---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrai uma única subregião (uma "fatia") de um tensor de entrada.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: f34525865be9541da879e66e88c29d4a2ab74f00
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803949"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a><span data-ttu-id="41b46-103">Estrutura de DML_SLICE1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="41b46-103">DML_SLICE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="41b46-104">Extrai uma única subregião (uma "fatia") de um tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="41b46-104">Extracts a single subregion (a "slice") of an input tensor.</span></span>

<span data-ttu-id="41b46-105">A *janela de entrada* descreve os limites do tensor de entrada a ser considerado na fatia.</span><span class="sxs-lookup"><span data-stu-id="41b46-105">The *input window* describes the bounds of the input tensor to consider in the slice.</span></span> <span data-ttu-id="41b46-106">A janela é definida usando três valores para cada dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-106">The window is defined using three values for each dimension.</span></span>

- <span data-ttu-id="41b46-107">O *deslocamento* marca o *início da janela* em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-107">The *offset* marks the *beginning of the window* in a dimension.</span></span>
- <span data-ttu-id="41b46-108">O *tamanho* marca a extensão da janela em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-108">The *size* marks the extent of the window in a dimension.</span></span> <span data-ttu-id="41b46-109">O *final da janela* em uma dimensão é `offset + size - 1` .</span><span class="sxs-lookup"><span data-stu-id="41b46-109">The *end of the window* in a dimension is `offset + size - 1`.</span></span>
- <span data-ttu-id="41b46-110">O *Stride* indica como atravessar os elementos em uma dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-110">The *stride* indicates how to traverse the elements in a dimension.</span></span>
  - <span data-ttu-id="41b46-111">A magnitude do Stride indica a quantidade de elementos a serem adiantados ao copiar dentro da janela.</span><span class="sxs-lookup"><span data-stu-id="41b46-111">The magnitude of the stride indicates how many elements to advance when copying within the window.</span></span>
  - <span data-ttu-id="41b46-112">Se um stride for positivo, os elementos serão copiados começando no *início* da janela na dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-112">If a stride is positive, elements are copied starting at the *beginning* of the window in the dimension.</span></span>
  - <span data-ttu-id="41b46-113">Se um stride for negativo, os elementos serão copiados começando no *final* da janela na dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-113">If a stride is negative, elements are copied starting at the *end* of the window in the dimension.</span></span>

<span data-ttu-id="41b46-114">O pseudocódigo a seguir ilustra como os elementos são copiados usando a janela de entrada.</span><span class="sxs-lookup"><span data-stu-id="41b46-114">The following pseudo-code illustrates how elements are copied using the input window.</span></span> <span data-ttu-id="41b46-115">Observe como os elementos em uma dimensão são copiados do início ao fim com um stride positivo e copiados de end para Start com um stride negativo.</span><span class="sxs-lookup"><span data-stu-id="41b46-115">Note how elements in a dimension are copied from start to end with a positive stride, and copied from end to start with a negative stride.</span></span>

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

<span data-ttu-id="41b46-116">A janela de entrada não deve estar vazia em qualquer dimensão e a janela não deve se estende além das dimensões da entrada tensor (as leituras fora de limites não são permitidas).</span><span class="sxs-lookup"><span data-stu-id="41b46-116">The input window mustn't be empty in any dimension, and the window mustn't extend beyond the dimensions of the input tensor (out-of-bounds reads aren't permitted).</span></span> <span data-ttu-id="41b46-117">O tamanho da janela e os passos limitam efetivamente o número de elementos que podem ser copiados de cada dimensão `i` do tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="41b46-117">The window's size and strides effectively limit the number of elements that may be copied from each dimension `i` of the input tensor.</span></span>

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

<span data-ttu-id="41b46-118">O tensor de saída não é necessário para copiar todos os elementos acessíveis dentro da janela.</span><span class="sxs-lookup"><span data-stu-id="41b46-118">The output tensor isn't required to copy all reachable elements within the window.</span></span> <span data-ttu-id="41b46-119">A fatia é válida desde que `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .</span><span class="sxs-lookup"><span data-stu-id="41b46-119">The slice is valid so long as `1 <= OutputSizes[i] <= MaxCopiedElements[i]`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41b46-120">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="41b46-120">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="41b46-121">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="41b46-121">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41b46-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41b46-122">Syntax</span></span>
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a><span data-ttu-id="41b46-123">Membros</span><span class="sxs-lookup"><span data-stu-id="41b46-123">Members</span></span>

`InputTensor`

<span data-ttu-id="41b46-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41b46-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41b46-125">O tensor para extrair fatias.</span><span class="sxs-lookup"><span data-stu-id="41b46-125">The tensor to extract slices from.</span></span>


`OutputTensor`

<span data-ttu-id="41b46-126">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="41b46-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="41b46-127">O tensor para gravar os resultados de dados na segmentação.</span><span class="sxs-lookup"><span data-stu-id="41b46-127">The tensor to write the sliced data results to.</span></span>


`DimensionCount`

<span data-ttu-id="41b46-128">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="41b46-128">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="41b46-129">O número de dimensões.</span><span class="sxs-lookup"><span data-stu-id="41b46-129">The number of dimensions.</span></span> <span data-ttu-id="41b46-130">Este campo determina o tamanho das matrizes *InputWindowOffsets*, *InputWindowSizes* e *InputWindowStrides* .</span><span class="sxs-lookup"><span data-stu-id="41b46-130">This field determines the size of the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="41b46-131">Esse valor deve corresponder ao *DimensionCount* dos tempos de entrada e de saída.</span><span class="sxs-lookup"><span data-stu-id="41b46-131">This value must match the *DimensionCount* of the input and output tensors.</span></span> <span data-ttu-id="41b46-132">Esse valor deve estar entre 1 e 8, inclusivamente, a partir de `DML_FEATURE_LEVEL_3_0` ; os níveis de recursos anteriores exigem um valor de 4 ou 5.</span><span class="sxs-lookup"><span data-stu-id="41b46-132">This value must be between 1 and 8, inclusively, starting from `DML_FEATURE_LEVEL_3_0`; earlier feature levels require a value of either 4 or 5.</span></span>


`InputWindowOffsets`

<span data-ttu-id="41b46-133">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="41b46-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="41b46-134">Uma matriz que contém o início (em elementos) da janela de entrada em cada dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-134">An array containing the beginning (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="41b46-135">Os valores na matriz devem atender à restrição `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="41b46-135">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowSizes`

<span data-ttu-id="41b46-136">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="41b46-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="41b46-137">Uma matriz que contém a extensão (em elementos) da janela de entrada em cada dimensão.</span><span class="sxs-lookup"><span data-stu-id="41b46-137">An array containing the extent (in elements) of the input window in each dimension.</span></span> <span data-ttu-id="41b46-138">Os valores na matriz devem atender à restrição `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span><span class="sxs-lookup"><span data-stu-id="41b46-138">Values in the array must satisfy the constraint `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`</span></span>


`InputWindowStrides`

<span data-ttu-id="41b46-139">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="41b46-139">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="41b46-140">Uma matriz que contém a distância da fatia ao longo de cada dimensão da entrada tensor, em elementos.</span><span class="sxs-lookup"><span data-stu-id="41b46-140">An array containing the slice's stride along each dimension of the input tensor, in elements.</span></span> <span data-ttu-id="41b46-141">A magnitude do Stride indica a quantidade de elementos a serem adiantados ao copiar dentro da janela de entrada.</span><span class="sxs-lookup"><span data-stu-id="41b46-141">The magnitude of the stride indicates how many elements to advance when copying within the input window.</span></span> <span data-ttu-id="41b46-142">O sinal do Stride determina se os elementos são copiados começando no início da janela (STRIDE positivo) ou no final da janela (STRIDE negativo).</span><span class="sxs-lookup"><span data-stu-id="41b46-142">The sign of the stride determines if elements are copied starting at the beginning of the window (positive stride) or end of the window (negative stride).</span></span> <span data-ttu-id="41b46-143">Os progressos não podem ser 0.</span><span class="sxs-lookup"><span data-stu-id="41b46-143">Strides may not be 0.</span></span>

## <a name="examples"></a><span data-ttu-id="41b46-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41b46-144">Examples</span></span>

<span data-ttu-id="41b46-145">Os exemplos a seguir usam esse mesmo tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="41b46-145">The following examples use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a><span data-ttu-id="41b46-146">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="41b46-146">Example 1.</span></span> <span data-ttu-id="41b46-147">Fatias encorridas com progressos positivos</span><span class="sxs-lookup"><span data-stu-id="41b46-147">Strided slice with positive strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

<span data-ttu-id="41b46-148">Os elementos copiados são calculados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="41b46-148">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a><span data-ttu-id="41b46-149">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="41b46-149">Example 2.</span></span> <span data-ttu-id="41b46-150">Fatia em um intervalo com avanços negativos</span><span class="sxs-lookup"><span data-stu-id="41b46-150">Strided slice with negative strides</span></span>

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

<span data-ttu-id="41b46-151">Lembre-se de que as dimensões com os passos negativos da janela começam a copiar no final da janela de entrada para essa dimensão; Isso é feito adicionando `InputWindowSize[i] - 1` ao deslocamento da janela.</span><span class="sxs-lookup"><span data-stu-id="41b46-151">Recall that dimensions with negative window strides start copying at the end of the input window for that dimension; this is done by adding `InputWindowSize[i] - 1` to the window offset.</span></span> <span data-ttu-id="41b46-152">As dimensões com um stride positivo simplesmente começam em `InputWindowOffset[i]` .</span><span class="sxs-lookup"><span data-stu-id="41b46-152">Dimensions with a positive stride simply start at `InputWindowOffset[i]`.</span></span>
- <span data-ttu-id="41b46-153">O eixo 0 ( `+1` Stride da janela) começa a copiar em `InputWindowOffsets[0] = 0` .</span><span class="sxs-lookup"><span data-stu-id="41b46-153">Axis 0 (`+1` window stride) starts copying at `InputWindowOffsets[0] = 0`.</span></span> 
- <span data-ttu-id="41b46-154">O eixo 1 ( `+1` Stride da janela) começa a copiar em `InputWindowOffsets[1] = 0` .</span><span class="sxs-lookup"><span data-stu-id="41b46-154">Axis 1 (`+1` window stride) starts copying at `InputWindowOffsets[1] = 0`.</span></span> 
- <span data-ttu-id="41b46-155">O eixo 2 ( `-2` Stride da janela) começa a copiar em `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` .</span><span class="sxs-lookup"><span data-stu-id="41b46-155">Axis 2 (`-2` window stride) starts copying at `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3`.</span></span> 
- <span data-ttu-id="41b46-156">O eixo 3 ( `+2` Stride da janela) começa a copiar em `InputWindowOffsets[3] = 1` .</span><span class="sxs-lookup"><span data-stu-id="41b46-156">Axis 3 (`+2` window stride) starts copying at `InputWindowOffsets[3] = 1`.</span></span> 

<span data-ttu-id="41b46-157">Os elementos copiados são calculados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="41b46-157">The copied elements are calculated as follows.</span></span> 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a><span data-ttu-id="41b46-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="41b46-158">Remarks</span></span>
<span data-ttu-id="41b46-159">Esse operador é semelhante a [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), mas difere de duas maneiras importantes.</span><span class="sxs-lookup"><span data-stu-id="41b46-159">This operator is similar to [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), but it differs in two important ways.</span></span>

- <span data-ttu-id="41b46-160">As sobremedidas de fatias podem ser negativas, o que permite reverter valores ao longo de dimensões.</span><span class="sxs-lookup"><span data-stu-id="41b46-160">Slice strides may be negative, which allows reversing values along dimensions.</span></span>
- <span data-ttu-id="41b46-161">Os tamanhos de janela de entrada não são necessariamente os mesmos que os tamanhos de tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="41b46-161">The input window sizes are not necessarily the same as the output tensor sizes.</span></span>

## <a name="availability"></a><span data-ttu-id="41b46-162">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="41b46-162">Availability</span></span>
<span data-ttu-id="41b46-163">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="41b46-163">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="41b46-164">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="41b46-164">Tensor constraints</span></span>
<span data-ttu-id="41b46-165">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="41b46-165">*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="41b46-166">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="41b46-166">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="41b46-167">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="41b46-167">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="41b46-168">Tensor</span><span class="sxs-lookup"><span data-stu-id="41b46-168">Tensor</span></span> | <span data-ttu-id="41b46-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b46-169">Kind</span></span> | <span data-ttu-id="41b46-170">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="41b46-170">Supported dimension counts</span></span> | <span data-ttu-id="41b46-171">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="41b46-171">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="41b46-172">InputTensor</span><span class="sxs-lookup"><span data-stu-id="41b46-172">InputTensor</span></span> | <span data-ttu-id="41b46-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="41b46-173">Input</span></span> | <span data-ttu-id="41b46-174">1 a 8</span><span class="sxs-lookup"><span data-stu-id="41b46-174">1 to 8</span></span> | <span data-ttu-id="41b46-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="41b46-175">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="41b46-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="41b46-176">OutputTensor</span></span> | <span data-ttu-id="41b46-177">Saída</span><span class="sxs-lookup"><span data-stu-id="41b46-177">Output</span></span> | <span data-ttu-id="41b46-178">1 a 8</span><span class="sxs-lookup"><span data-stu-id="41b46-178">1 to 8</span></span> | <span data-ttu-id="41b46-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="41b46-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="41b46-180">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="41b46-180">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="41b46-181">Tensor</span><span class="sxs-lookup"><span data-stu-id="41b46-181">Tensor</span></span> | <span data-ttu-id="41b46-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="41b46-182">Kind</span></span> | <span data-ttu-id="41b46-183">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="41b46-183">Supported dimension counts</span></span> | <span data-ttu-id="41b46-184">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="41b46-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="41b46-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="41b46-185">InputTensor</span></span> | <span data-ttu-id="41b46-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="41b46-186">Input</span></span> | <span data-ttu-id="41b46-187">4 a 5</span><span class="sxs-lookup"><span data-stu-id="41b46-187">4 to 5</span></span> | <span data-ttu-id="41b46-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="41b46-188">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="41b46-189">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="41b46-189">OutputTensor</span></span> | <span data-ttu-id="41b46-190">Saída</span><span class="sxs-lookup"><span data-stu-id="41b46-190">Output</span></span> | <span data-ttu-id="41b46-191">4 a 5</span><span class="sxs-lookup"><span data-stu-id="41b46-191">4 to 5</span></span> | <span data-ttu-id="41b46-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="41b46-192">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="41b46-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41b46-193">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="41b46-194">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="41b46-194">**Header**</span></span> | <span data-ttu-id="41b46-195">directml. h</span><span class="sxs-lookup"><span data-stu-id="41b46-195">directml.h</span></span> |