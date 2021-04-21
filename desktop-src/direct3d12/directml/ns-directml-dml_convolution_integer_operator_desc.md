---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Executa uma convolução do *FilterTensor* com o *InputTensor*. Esse operador executa a convolução progressiva nos dados inteiros.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: 07406155be9ae5f78fbf5f3b7fcd750aa4631dbc
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803376"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="3df51-104">Estrutura de DML_CONVOLUTION_INTEGER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="3df51-104">DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="3df51-105">Executa uma convolução do *FilterTensor* com o *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="3df51-105">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="3df51-106">Esse operador executa a convolução progressiva nos dados inteiros.</span><span class="sxs-lookup"><span data-stu-id="3df51-106">This operator performs forward convolution on integer data.</span></span> <span data-ttu-id="3df51-107">Também é possível usar zeros de ponto opcional para subtrair valores de ponto zero do tensor de entrada e de filtro.</span><span class="sxs-lookup"><span data-stu-id="3df51-107">Optional zero point tensors can also be used to subtract zero point values from the input and filter tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3df51-108">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3df51-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="3df51-109">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="3df51-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3df51-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3df51-110">Syntax</span></span>
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```

## <a name="members"></a><span data-ttu-id="3df51-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3df51-111">Members</span></span>

`InputTensor`

<span data-ttu-id="3df51-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3df51-113">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="3df51-113">A tensor containing the input data.</span></span> <span data-ttu-id="3df51-114">As dimensões esperadas do *InputTensor* são `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="3df51-114">The expected dimensions of the *InputTensor* are `{ BatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="3df51-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3df51-116">Um tensor opcional que contém os dados de ponto zero de entrada.</span><span class="sxs-lookup"><span data-stu-id="3df51-116">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="3df51-117">As dimensões esperadas do *InputZeroPointTensor* são `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="3df51-117">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span>


`FilterTensor`

<span data-ttu-id="3df51-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3df51-119">Um tensor que contém os dados de filtro.</span><span class="sxs-lookup"><span data-stu-id="3df51-119">A tensor containing the filter data.</span></span> <span data-ttu-id="3df51-120">As dimensões esperadas do *FilterTensor* são `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="3df51-120">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="3df51-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3df51-122">Um tensor opcional que contém os dados de ponto zero de filtro.</span><span class="sxs-lookup"><span data-stu-id="3df51-122">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="3df51-123">As dimensões esperadas de *FilterZeroPointTensor* são `{ 1, 1, 1, 1 }` se a quantificação por tensor for necessária ou `{ 1, OutputChannelCount, 1, 1 }` se a quantificação por canal for necessária.</span><span class="sxs-lookup"><span data-stu-id="3df51-123">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per-channel quantization is required.</span></span>


`OutputTensor`

<span data-ttu-id="3df51-124">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-124">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="3df51-125">O tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="3df51-125">The tensor to write the results to.</span></span> <span data-ttu-id="3df51-126">As dimensões esperadas do *OutputTensor* são `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="3df51-126">The expected dimensions of the *OutputTensor* are `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="3df51-127">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3df51-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="3df51-128">O número de dimensões espaciais para a operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-128">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="3df51-129">Dimensões espaciais são as dimensões inferiores do *FilterTensor* de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-129">Spatial dimensions are the lower dimensions of the convolution *FilterTensor*.</span></span> <span data-ttu-id="3df51-130">Esse valor também determina o tamanho das matrizes de *prerides*, *Dilations*, *StartPadding* e *endpadding* .</span><span class="sxs-lookup"><span data-stu-id="3df51-130">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="3df51-131">Há suporte apenas para um valor de 2.</span><span class="sxs-lookup"><span data-stu-id="3df51-131">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="3df51-132">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-132">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="3df51-133">Uma matriz que contém os passos da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-133">An array containing the strides of the convolution operation.</span></span> <span data-ttu-id="3df51-134">Esses passos são aplicados ao filtro de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-134">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="3df51-135">Eles são separados dos avanços do tensor incluídos no [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="3df51-135">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="3df51-136">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-136">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="3df51-137">Uma matriz que contém o dilations da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-137">An array containing the dilations of the convolution operation.</span></span> <span data-ttu-id="3df51-138">Dilations são preparadas aplicadas aos elementos do kernel de filtro.</span><span class="sxs-lookup"><span data-stu-id="3df51-138">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="3df51-139">Isso tem o efeito de simular um kernel de filtro maior preenchendo os elementos do kernel de filtro interno com zeros.</span><span class="sxs-lookup"><span data-stu-id="3df51-139">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="3df51-140">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-140">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="3df51-141">Uma matriz que contém os valores de preenchimento a serem aplicados ao início de cada dimensão espacial do filtro e tensor de entrada da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-141">An array containing the padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="3df51-142">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="3df51-142">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="3df51-143">Uma matriz que contém os valores de preenchimento a serem aplicados ao final de cada dimensão espacial do filtro e tensor de entrada da operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-143">An array containing the padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="3df51-144">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="3df51-144">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="3df51-145">O número de grupos nos quais dividir a operação de convolução.</span><span class="sxs-lookup"><span data-stu-id="3df51-145">The number of groups which to divide the convolution operation up into.</span></span> <span data-ttu-id="3df51-146">*GroupCount* pode ser usado para obter convolução com profundidade, definindo o *GroupCount* igual à contagem de canais de entrada.</span><span class="sxs-lookup"><span data-stu-id="3df51-146">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="3df51-147">Isso divide a convolução em uma convolução separada por canal de entrada.</span><span class="sxs-lookup"><span data-stu-id="3df51-147">This divides the convolution up into a separate convolution per input channel.</span></span>

## <a name="availability"></a><span data-ttu-id="3df51-148">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="3df51-148">Availability</span></span>
<span data-ttu-id="3df51-149">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="3df51-149">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="3df51-150">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="3df51-150">Tensor constraints</span></span>
* <span data-ttu-id="3df51-151">*FilterTensor* e *FilterZeroPointTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="3df51-151">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="3df51-152">*InputTensor* e *InputZeroPointTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="3df51-152">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="3df51-153">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="3df51-153">Tensor support</span></span>
| <span data-ttu-id="3df51-154">Tensor</span><span class="sxs-lookup"><span data-stu-id="3df51-154">Tensor</span></span> | <span data-ttu-id="3df51-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="3df51-155">Kind</span></span> | <span data-ttu-id="3df51-156">Dimensões</span><span class="sxs-lookup"><span data-stu-id="3df51-156">Dimensions</span></span> | <span data-ttu-id="3df51-157">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="3df51-157">Supported dimension counts</span></span> | <span data-ttu-id="3df51-158">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="3df51-158">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="3df51-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="3df51-159">InputTensor</span></span> | <span data-ttu-id="3df51-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="3df51-160">Input</span></span> | <span data-ttu-id="3df51-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="3df51-161">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="3df51-162">4</span><span class="sxs-lookup"><span data-stu-id="3df51-162">4</span></span> | <span data-ttu-id="3df51-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="3df51-163">INT8, UINT8</span></span> |
| <span data-ttu-id="3df51-164">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="3df51-164">InputZeroPointTensor</span></span> | <span data-ttu-id="3df51-165">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="3df51-165">Optional input</span></span> | <span data-ttu-id="3df51-166">{1, 1, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="3df51-166">{ 1, 1, 1, 1 }</span></span> | <span data-ttu-id="3df51-167">4</span><span class="sxs-lookup"><span data-stu-id="3df51-167">4</span></span> | <span data-ttu-id="3df51-168">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="3df51-168">INT8, UINT8</span></span> |
| <span data-ttu-id="3df51-169">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="3df51-169">FilterTensor</span></span> | <span data-ttu-id="3df51-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="3df51-170">Input</span></span> | <span data-ttu-id="3df51-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span><span class="sxs-lookup"><span data-stu-id="3df51-171">{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }</span></span> | <span data-ttu-id="3df51-172">4</span><span class="sxs-lookup"><span data-stu-id="3df51-172">4</span></span> | <span data-ttu-id="3df51-173">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="3df51-173">INT8, UINT8</span></span> |
| <span data-ttu-id="3df51-174">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="3df51-174">FilterZeroPointTensor</span></span> | <span data-ttu-id="3df51-175">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="3df51-175">Optional input</span></span> | <span data-ttu-id="3df51-176">{1, FilterZeroPointChannelCount, 1, 1}</span><span class="sxs-lookup"><span data-stu-id="3df51-176">{ 1, FilterZeroPointChannelCount, 1, 1 }</span></span> | <span data-ttu-id="3df51-177">4</span><span class="sxs-lookup"><span data-stu-id="3df51-177">4</span></span> | <span data-ttu-id="3df51-178">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="3df51-178">INT8, UINT8</span></span> |
| <span data-ttu-id="3df51-179">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="3df51-179">OutputTensor</span></span> | <span data-ttu-id="3df51-180">Saída</span><span class="sxs-lookup"><span data-stu-id="3df51-180">Output</span></span> | <span data-ttu-id="3df51-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="3df51-181">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="3df51-182">4</span><span class="sxs-lookup"><span data-stu-id="3df51-182">4</span></span> | <span data-ttu-id="3df51-183">INT32</span><span class="sxs-lookup"><span data-stu-id="3df51-183">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="3df51-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3df51-184">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3df51-185">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="3df51-185">**Header**</span></span> | <span data-ttu-id="3df51-186">directml. h</span><span class="sxs-lookup"><span data-stu-id="3df51-186">directml.h</span></span> |