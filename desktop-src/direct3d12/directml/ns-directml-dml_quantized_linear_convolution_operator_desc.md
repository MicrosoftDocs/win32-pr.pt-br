---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Executa uma convolução do *FilterTensor* com o *InputTensor*. Esse operador executa a convolução progressiva em dados quantificados. Esse operador é matematicamente equivalente a desquantificar as entradas, convolving e, em seguida, quantificar a saída.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416941"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="eb228-105">Estrutura de DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="eb228-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="eb228-106">Executa uma convolução do *FilterTensor* com o *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="eb228-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="eb228-107">Esse operador executa a convolução progressiva em dados quantificados.</span><span class="sxs-lookup"><span data-stu-id="eb228-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="eb228-108">Esse operador é matematicamente equivalente a desquantificar as entradas, convolving e, em seguida, quantificar a saída.</span><span class="sxs-lookup"><span data-stu-id="eb228-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="eb228-109">As funções lineares Quantize usadas por este operador são as funções de quantificação linear</span><span class="sxs-lookup"><span data-stu-id="eb228-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="eb228-110">Função de desquantificação</span><span class="sxs-lookup"><span data-stu-id="eb228-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="eb228-111">Função Quantize</span><span class="sxs-lookup"><span data-stu-id="eb228-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="eb228-112">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="eb228-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="eb228-113">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="eb228-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb228-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb228-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a><span data-ttu-id="eb228-115">Membros</span><span class="sxs-lookup"><span data-stu-id="eb228-115">Members</span></span>

`InputTensor`

<span data-ttu-id="eb228-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-117">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb228-117">A tensor containing the input data.</span></span> <span data-ttu-id="eb228-118">As dimensões esperadas do *InputTensor* são `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="eb228-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="eb228-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-120">Um tensor que contém os dados de escala de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb228-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="eb228-121">As dimensões esperadas do `InputScaleTensor` são `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="eb228-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="eb228-122">Esse valor de escala é usado para desquantificar os valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb228-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="eb228-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-124">Um tensor opcional que contém os dados de ponto zero de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb228-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="eb228-125">As dimensões esperadas do *InputZeroPointTensor* são `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="eb228-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="eb228-126">Esse valor de ponto zero é usado para desquantificar os valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb228-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="eb228-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-128">Um tensor que contém os dados de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb228-128">A tensor containing the filter data.</span></span> <span data-ttu-id="eb228-129">As dimensões esperadas do *FilterTensor* são `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="eb228-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="eb228-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-131">Um tensor que contém os dados de escala de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb228-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="eb228-132">As dimensões esperadas do `FilterScaleTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, OutputChannelCount, 1, 1 }` se a quantificação por canal for necessária.</span><span class="sxs-lookup"><span data-stu-id="eb228-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="eb228-133">Esse valor de escala é usado para desquantificar os valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb228-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="eb228-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-135">Um tensor opcional que contém os dados de ponto zero de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb228-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="eb228-136">As dimensões esperadas de *FilterZeroPointTensor* são `{ 1, 1, 1, 1 }` se a quantificação por tensor for necessária ou `{ 1, OutputChannelCount, 1, 1 }` se a quantificação por canal for necessária.</span><span class="sxs-lookup"><span data-stu-id="eb228-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="eb228-137">Esse valor de ponto zero é usado para desquantificar os valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb228-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="eb228-138">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-139">Um tensor que contém os dados de tendência.</span><span class="sxs-lookup"><span data-stu-id="eb228-139">A tensor containing the bias data.</span></span> <span data-ttu-id="eb228-140">O tensor de tendência é um tensor que contém dados que são transmitidos pelo tensor de saída no final da convolução que é adicionada ao resultado.</span><span class="sxs-lookup"><span data-stu-id="eb228-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="eb228-141">As dimensões esperadas do BiasTensor são `{ 1, OutputChannelCount, 1, 1 }` para 4D.</span><span class="sxs-lookup"><span data-stu-id="eb228-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="eb228-142">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-143">Um tensor que contém os dados de escala de saída.</span><span class="sxs-lookup"><span data-stu-id="eb228-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="eb228-144">As dimensões esperadas do OutputScaleTensor são `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="eb228-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="eb228-145">Esse valor de escala de entrada é usado para quantificar os valores de saída de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="eb228-146">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-147">Um tensor opcional que contém os dados de ponto zero de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb228-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="eb228-148">As dimensões esperadas do OutputZeroPointTensor são `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="eb228-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="eb228-149">Esse valor de ponto zero de entrada é usado para quantificar a convolução dos valores de saída.</span><span class="sxs-lookup"><span data-stu-id="eb228-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="eb228-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="eb228-151">Um tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="eb228-151">A tensor to write the results to.</span></span> <span data-ttu-id="eb228-152">As dimensões esperadas do OutputTensor são `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="eb228-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="eb228-153">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="eb228-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="eb228-154">O número de dimensões espaciais para a operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="eb228-155">Dimensões espaciais são as dimensões inferiores do filtro de convolução tensor *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="eb228-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="eb228-156">Esse valor também determina o tamanho das matrizes de *prerides*, *Dilations*, *StartPadding* e *endpadding* .</span><span class="sxs-lookup"><span data-stu-id="eb228-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="eb228-157">Há suporte apenas para um valor de 2.</span><span class="sxs-lookup"><span data-stu-id="eb228-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="eb228-158">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-158">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eb228-159">Os passos da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-159">The strides of the convolution operation.</span></span> <span data-ttu-id="eb228-160">Esses passos são aplicados ao filtro de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="eb228-161">Eles são separados dos avanços do tensor incluídos no [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="eb228-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="eb228-162">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-162">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eb228-163">O Dilations da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="eb228-164">Dilations são preparadas aplicadas aos elementos do kernel de filtro.</span><span class="sxs-lookup"><span data-stu-id="eb228-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="eb228-165">Isso tem o efeito de simular um kernel de filtro maior preenchendo os elementos do kernel de filtro interno com zeros.</span><span class="sxs-lookup"><span data-stu-id="eb228-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="eb228-166">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-166">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eb228-167">Os valores de preenchimento a serem aplicados ao início de cada dimensão espacial do filtro e tensor de entrada da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="eb228-168">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb228-168">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="eb228-169">Os valores de preenchimento a serem aplicados ao final de cada dimensão espacial do filtro e tensor de entrada da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="eb228-170">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="eb228-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="eb228-171">O número de grupos nos quais dividir a operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="eb228-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="eb228-172">*GroupCount* pode ser usado para obter convolução com profundidade, definindo o *GroupCount* igual à contagem de canais de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb228-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="eb228-173">Isso divide a convolução em uma convolução separada por canal de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb228-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="eb228-174">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="eb228-174">Availability</span></span>
<span data-ttu-id="eb228-175">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="eb228-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="eb228-176">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="eb228-176">Tensor constraints</span></span>
* <span data-ttu-id="eb228-177">*FilterTensor* e *FilterZeroPointTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="eb228-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="eb228-178">*InputTensor* e *InputZeroPointTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="eb228-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="eb228-179">*OutputTensor* e `OutputZeroPointTensor` deve ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="eb228-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="eb228-180">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="eb228-180">Tensor support</span></span>
| <span data-ttu-id="eb228-181">Tensor</span><span class="sxs-lookup"><span data-stu-id="eb228-181">Tensor</span></span> | <span data-ttu-id="eb228-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb228-182">Kind</span></span> | <span data-ttu-id="eb228-183">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="eb228-183">Supported dimension counts</span></span> | <span data-ttu-id="eb228-184">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="eb228-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="eb228-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-185">InputTensor</span></span> | <span data-ttu-id="eb228-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb228-186">Input</span></span> | <span data-ttu-id="eb228-187">4</span><span class="sxs-lookup"><span data-stu-id="eb228-187">4</span></span> | <span data-ttu-id="eb228-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="eb228-188">INT8, UINT8</span></span> |
| <span data-ttu-id="eb228-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-189">InputScaleTensor</span></span> | <span data-ttu-id="eb228-190">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb228-190">Input</span></span> | <span data-ttu-id="eb228-191">4</span><span class="sxs-lookup"><span data-stu-id="eb228-191">4</span></span> | <span data-ttu-id="eb228-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="eb228-192">FLOAT32</span></span> |
| <span data-ttu-id="eb228-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-193">InputZeroPointTensor</span></span> | <span data-ttu-id="eb228-194">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="eb228-194">Optional input</span></span> | <span data-ttu-id="eb228-195">4</span><span class="sxs-lookup"><span data-stu-id="eb228-195">4</span></span> | <span data-ttu-id="eb228-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="eb228-196">INT8, UINT8</span></span> |
| <span data-ttu-id="eb228-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-197">FilterTensor</span></span> | <span data-ttu-id="eb228-198">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb228-198">Input</span></span> | <span data-ttu-id="eb228-199">4</span><span class="sxs-lookup"><span data-stu-id="eb228-199">4</span></span> | <span data-ttu-id="eb228-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="eb228-200">INT8, UINT8</span></span> |
| <span data-ttu-id="eb228-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-201">FilterScaleTensor</span></span> | <span data-ttu-id="eb228-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb228-202">Input</span></span> | <span data-ttu-id="eb228-203">4</span><span class="sxs-lookup"><span data-stu-id="eb228-203">4</span></span> | <span data-ttu-id="eb228-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="eb228-204">FLOAT32</span></span> |
| <span data-ttu-id="eb228-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="eb228-206">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="eb228-206">Optional input</span></span> | <span data-ttu-id="eb228-207">4</span><span class="sxs-lookup"><span data-stu-id="eb228-207">4</span></span> | <span data-ttu-id="eb228-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="eb228-208">INT8, UINT8</span></span> |
| <span data-ttu-id="eb228-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-209">BiasTensor</span></span> | <span data-ttu-id="eb228-210">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="eb228-210">Optional input</span></span> | <span data-ttu-id="eb228-211">4</span><span class="sxs-lookup"><span data-stu-id="eb228-211">4</span></span> | <span data-ttu-id="eb228-212">INT32</span><span class="sxs-lookup"><span data-stu-id="eb228-212">INT32</span></span> |
| <span data-ttu-id="eb228-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-213">OutputScaleTensor</span></span> | <span data-ttu-id="eb228-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="eb228-214">Input</span></span> | <span data-ttu-id="eb228-215">4</span><span class="sxs-lookup"><span data-stu-id="eb228-215">4</span></span> | <span data-ttu-id="eb228-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="eb228-216">FLOAT32</span></span> |
| <span data-ttu-id="eb228-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="eb228-218">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="eb228-218">Optional input</span></span> | <span data-ttu-id="eb228-219">4</span><span class="sxs-lookup"><span data-stu-id="eb228-219">4</span></span> | <span data-ttu-id="eb228-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="eb228-220">INT8, UINT8</span></span> |
| <span data-ttu-id="eb228-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="eb228-221">OutputTensor</span></span> | <span data-ttu-id="eb228-222">Saída</span><span class="sxs-lookup"><span data-stu-id="eb228-222">Output</span></span> | <span data-ttu-id="eb228-223">4</span><span class="sxs-lookup"><span data-stu-id="eb228-223">4</span></span> | <span data-ttu-id="eb228-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="eb228-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="eb228-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb228-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="eb228-226">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="eb228-226">**Header**</span></span> | <span data-ttu-id="eb228-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="eb228-227">directml.h</span></span> |