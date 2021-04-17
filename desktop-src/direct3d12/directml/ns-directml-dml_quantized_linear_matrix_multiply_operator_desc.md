---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Executa uma função de multiplicação de matriz em dados quantificados. Esse operador é matematicamente equivalente a desquantificar as entradas, executar a matriz de multiplicação e, em seguida, quantificar a saída.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105791105"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="a9c41-104">Estrutura de DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="a9c41-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="a9c41-105">Executa uma função de multiplicação de matriz em dados quantificados.</span><span class="sxs-lookup"><span data-stu-id="a9c41-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="a9c41-106">Esse operador é matematicamente equivalente a desquantificar as entradas, executar a matriz de multiplicação e, em seguida, quantificar a saída.</span><span class="sxs-lookup"><span data-stu-id="a9c41-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="a9c41-107">Esse operador requer que a matriz multiplique os tempos de entrada para ser 4D, formatados como `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="a9c41-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="a9c41-108">O operador de multiplicação de matriz executará BatchCount \* ChannelCount número de multiplicações de matriz independentes.</span><span class="sxs-lookup"><span data-stu-id="a9c41-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="a9c41-109">Por exemplo, se *ATensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, K }` e *BTensor* tiver tamanhos  de `{ BatchCount, ChannelCount, K, N }` e *OutputTensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, N }` , o operador de multiplicação de matriz executará BatchCount \* ChannelCount multiplicações de matriz independentes de dimensões {M, K} x {K, n} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="a9c41-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="a9c41-110">Função de desquantificação</span><span class="sxs-lookup"><span data-stu-id="a9c41-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="a9c41-111">Função Quantize</span><span class="sxs-lookup"><span data-stu-id="a9c41-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="a9c41-112">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="a9c41-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="a9c41-113">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a9c41-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c41-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9c41-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="a9c41-115">Membros</span><span class="sxs-lookup"><span data-stu-id="a9c41-115">Members</span></span>

`ATensor`

<span data-ttu-id="a9c41-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-117">Um tensor que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="a9c41-117">A tensor containing the A data.</span></span> <span data-ttu-id="a9c41-118">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="a9c41-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="a9c41-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-120">Um tensor que contém os dados de escala ATensor.</span><span class="sxs-lookup"><span data-stu-id="a9c41-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="a9c41-121">As dimensões esperadas do `AScaleTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha.</span><span class="sxs-lookup"><span data-stu-id="a9c41-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="a9c41-122">Esses valores de escala são usados para desquantificar os valores.</span><span class="sxs-lookup"><span data-stu-id="a9c41-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="a9c41-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-124">Um tensor opcional que contém os dados de ponto de *ATensor* zero.</span><span class="sxs-lookup"><span data-stu-id="a9c41-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="a9c41-125">As dimensões esperadas de AZeroPointTensor são `{ 1, 1, 1, 1 }` se a quantificação por tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha.</span><span class="sxs-lookup"><span data-stu-id="a9c41-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="a9c41-126">Esses valores de ponto zero são usados para desquantificar os valores de ATensor.</span><span class="sxs-lookup"><span data-stu-id="a9c41-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="a9c41-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-128">Um tensor que contém os dados B.</span><span class="sxs-lookup"><span data-stu-id="a9c41-128">A tensor containing the B data.</span></span> <span data-ttu-id="a9c41-129">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="a9c41-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="a9c41-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-131">Um tensor que contém os dados de escala *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="a9c41-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="a9c41-132">As dimensões esperadas do `BScaleTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, 1, N }` se for necessária quantização por coluna.</span><span class="sxs-lookup"><span data-stu-id="a9c41-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="a9c41-133">Esses valores de escala são usados para desquantificar os valores de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="a9c41-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="a9c41-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-135">Um tensor opcional que contém os dados de ponto de *BTensor* zero.</span><span class="sxs-lookup"><span data-stu-id="a9c41-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="a9c41-136">As dimensões esperadas do `BZeroPointTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, 1, N }` se for necessária quantização por coluna.</span><span class="sxs-lookup"><span data-stu-id="a9c41-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="a9c41-137">Esses valores de ponto zero são usados para desquantificar os valores de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="a9c41-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="a9c41-138">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-139">Um tensor que contém os dados de escala de filtro.</span><span class="sxs-lookup"><span data-stu-id="a9c41-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="a9c41-140">As dimensões esperadas do `OutputScaleTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha.</span><span class="sxs-lookup"><span data-stu-id="a9c41-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="a9c41-141">Esse valor de escala é usado para desquantificar os valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="a9c41-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="a9c41-142">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-143">Um tensor opcional que contém os dados de ponto zero de filtro.</span><span class="sxs-lookup"><span data-stu-id="a9c41-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="a9c41-144">As dimensões esperadas do `OutputZeroPointTensor` são `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha.</span><span class="sxs-lookup"><span data-stu-id="a9c41-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="a9c41-145">Esse valor de ponto zero é usado para desquantificar os valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="a9c41-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="a9c41-146">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a9c41-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a9c41-147">Um tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a9c41-147">A tensor to write the results to.</span></span> <span data-ttu-id="a9c41-148">As dimensões de tensor são `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="a9c41-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="a9c41-149">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a9c41-149">Availability</span></span>
<span data-ttu-id="a9c41-150">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="a9c41-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a9c41-151">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-151">Tensor constraints</span></span>
* <span data-ttu-id="a9c41-152">*ATensor* e `AZeroPointTensor` deve ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="a9c41-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="a9c41-153">*BTensor* e `BZeroPointTensor` deve ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="a9c41-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="a9c41-154">*OutputTensor* e `OutputZeroPointTensor` deve ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="a9c41-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a9c41-155">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-155">Tensor support</span></span>
| <span data-ttu-id="a9c41-156">Tensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-156">Tensor</span></span> | <span data-ttu-id="a9c41-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9c41-157">Kind</span></span> | <span data-ttu-id="a9c41-158">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="a9c41-158">Supported dimension counts</span></span> | <span data-ttu-id="a9c41-159">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="a9c41-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a9c41-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-160">ATensor</span></span> | <span data-ttu-id="a9c41-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9c41-161">Input</span></span> | <span data-ttu-id="a9c41-162">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-162">4</span></span> | <span data-ttu-id="a9c41-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9c41-163">INT8, UINT8</span></span> |
| <span data-ttu-id="a9c41-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-164">AScaleTensor</span></span> | <span data-ttu-id="a9c41-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9c41-165">Input</span></span> | <span data-ttu-id="a9c41-166">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-166">4</span></span> | <span data-ttu-id="a9c41-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="a9c41-167">FLOAT32</span></span> |
| <span data-ttu-id="a9c41-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-168">AZeroPointTensor</span></span> | <span data-ttu-id="a9c41-169">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="a9c41-169">Optional input</span></span> | <span data-ttu-id="a9c41-170">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-170">4</span></span> | <span data-ttu-id="a9c41-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9c41-171">INT8, UINT8</span></span> |
| <span data-ttu-id="a9c41-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-172">BTensor</span></span> | <span data-ttu-id="a9c41-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9c41-173">Input</span></span> | <span data-ttu-id="a9c41-174">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-174">4</span></span> | <span data-ttu-id="a9c41-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9c41-175">INT8, UINT8</span></span> |
| <span data-ttu-id="a9c41-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-176">BScaleTensor</span></span> | <span data-ttu-id="a9c41-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9c41-177">Input</span></span> | <span data-ttu-id="a9c41-178">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-178">4</span></span> | <span data-ttu-id="a9c41-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="a9c41-179">FLOAT32</span></span> |
| <span data-ttu-id="a9c41-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-180">BZeroPointTensor</span></span> | <span data-ttu-id="a9c41-181">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="a9c41-181">Optional input</span></span> | <span data-ttu-id="a9c41-182">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-182">4</span></span> | <span data-ttu-id="a9c41-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9c41-183">INT8, UINT8</span></span> |
| <span data-ttu-id="a9c41-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-184">OutputScaleTensor</span></span> | <span data-ttu-id="a9c41-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="a9c41-185">Input</span></span> | <span data-ttu-id="a9c41-186">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-186">4</span></span> | <span data-ttu-id="a9c41-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="a9c41-187">FLOAT32</span></span> |
| <span data-ttu-id="a9c41-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="a9c41-189">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="a9c41-189">Optional input</span></span> | <span data-ttu-id="a9c41-190">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-190">4</span></span> | <span data-ttu-id="a9c41-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9c41-191">INT8, UINT8</span></span> |
| <span data-ttu-id="a9c41-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a9c41-192">OutputTensor</span></span> | <span data-ttu-id="a9c41-193">Saída</span><span class="sxs-lookup"><span data-stu-id="a9c41-193">Output</span></span> | <span data-ttu-id="a9c41-194">4</span><span class="sxs-lookup"><span data-stu-id="a9c41-194">4</span></span> | <span data-ttu-id="a9c41-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="a9c41-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="a9c41-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9c41-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a9c41-197">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a9c41-197">**Header**</span></span> | <span data-ttu-id="a9c41-198">directml. h</span><span class="sxs-lookup"><span data-stu-id="a9c41-198">directml.h</span></span> |