---
UID: NS:directml.DML_MAX_POOLING_GRAD_OPERATOR_DESC
title: DML_MAX_POOLING_GRAD_OPERATOR_DESC
description: Computa gradientes de inpropagação para o máximo de pools (consulte [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).
helpviewer_keywords:
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- DML_MAX_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_MAX_POOLING_GRAD_OPERATOR_DESC, DML_MAX_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
- directml/DML_MAX_POOLING_GRAD_OPERATOR_DESC
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
- DML_MAX_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: b7314cb6b9456d9ac9f99e90100085e86f88ffd9
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105808403"
---
# <a name="dml_max_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="4b7fd-103">Estrutura de DML_MAX_POOLING_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="4b7fd-103">DML_MAX_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4b7fd-104">Computa gradientes de inpropagação para o máximo de pools (consulte [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-104">Computes backpropagation gradients for max pooling (see [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md)).</span></span>

<span data-ttu-id="4b7fd-105">Considere um **DML_MAX_POOLING2_OPERATOR_DESC** 2x2 sem preenchimento nem dilations e um stride de 1, que realiza o seguinte.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-105">Consider a 2x2 **DML_MAX_POOLING2_OPERATOR_DESC** without padding nor dilations and a stride of 1, which performs the following.</span></span>

```
InputTensor             OutputTensor    IndicesTensor
[[1, 2, 3],   MaxPool    [[4, 4],        [[4, 4],
 [2, 4, 2],     -->       [6, 7]]         [7, 8]]
 [5, 6, 7]]
```

<span data-ttu-id="4b7fd-106">O maior elemento de cada janela 2x2 no tensor de entrada produz um elemento da saída.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-106">The largest element of each 2x2 window in the input tensor produces one element of the output.</span></span> <span data-ttu-id="4b7fd-107">Abaixo está um exemplo da saída de **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, dadas parâmetros semelhantes.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-107">Below is an example of the output of **DML_MAX_POOLING_GRAD_OPERATOR_DESC**, given similar parameters.</span></span>

```
InputTensor   InputGradientTensor            OutputGradientTensor
[[1, 2, 3],       [[1, 2],     MaxPoolGrad   [[0, 0, 0],
 [2, 4, 2],        [4, 5]]         -->        [0, 3, 0],
 [5, 6, 7]]                                   [0, 4, 5]]
```

<span data-ttu-id="4b7fd-108">Em vigor, esse operador usa o *InputTensor* para determinar o índice do maior elemento de cada janela e distribui os valores de *InputGradientTensor* para o *OutputGradientTensor* com base nesses índices.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-108">In effect, this operator uses the *InputTensor* to determine the index of the largest element from each window, and distributes the values of *InputGradientTensor* into the *OutputGradientTensor* based on these indices.</span></span> <span data-ttu-id="4b7fd-109">Em que os índices se sobrepõem, os valores são somados.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-109">Where indices overlap, the values are summed.</span></span> <span data-ttu-id="4b7fd-110">Todos os elementos de saída não referenciados são zerados.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-110">Any unreferenced output elements are zeroed.</span></span>

<span data-ttu-id="4b7fd-111">No caso de um empate (em que mais de um elemento em uma janela tem o mesmo valor máximo), o elemento com o índice de elemento lógico mais baixo é escolhido.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-111">In the case of a tie (where more than one element in a window has the same maximum value), the element with the lowest logical element index is chosen.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b7fd-112">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="4b7fd-113">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7fd-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b7fd-114">Syntax</span></span>

```cpp
struct DML_MAX_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  _Field_size_(DimensionCount) const UINT* Dilations;
};
```

## <a name="members"></a><span data-ttu-id="4b7fd-115">Membros</span><span class="sxs-lookup"><span data-stu-id="4b7fd-115">Members</span></span>

`InputTensor`

<span data-ttu-id="4b7fd-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4b7fd-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4b7fd-117">O recurso de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-117">The input feature tensor.</span></span> <span data-ttu-id="4b7fd-118">Normalmente, isso é o mesmo tensor que foi fornecido como o *InputTensor* para [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-118">This is typically the same tensor that was provided as the *InputTensor* to [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="4b7fd-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4b7fd-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4b7fd-120">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-120">The incoming gradient tensor.</span></span> <span data-ttu-id="4b7fd-121">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-121">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="4b7fd-122">Normalmente, esse tensor teria os mesmos tamanhos da *saída* do [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-122">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="4b7fd-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4b7fd-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4b7fd-124">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-124">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="4b7fd-125">Normalmente, esse tensor teria os mesmos tamanhos que a *entrada* do [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-125">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="4b7fd-126">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4b7fd-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4b7fd-127">O número de elementos nas matrizes de *progressos*, *WindowSize*, *StartPadding*, *endpadding* e *Dilations* .</span><span class="sxs-lookup"><span data-stu-id="4b7fd-127">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, *EndPadding*, and *Dilations* arrays.</span></span> <span data-ttu-id="4b7fd-128">Esse valor deve ser igual à contagem de dimensões espaciais (DimensionCount da InputTensor-2).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-128">This value must equal the spatial dimension count (InputTensor's DimensionCount - 2).</span></span> <span data-ttu-id="4b7fd-129">Como esse operador dá suporte apenas a dezenases de 4D, o único valor válido para esse parâmetro é 2.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-129">As this operator only supports 4D tensors, the only valid value for this parameter is 2.</span></span>

`Strides`

<span data-ttu-id="4b7fd-130">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4b7fd-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4b7fd-131">Veja os *avanços* no [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-131">See *Strides* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`WindowSize`

<span data-ttu-id="4b7fd-132">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4b7fd-132">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4b7fd-133">Consulte *WindowSize* em [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-133">See *WindowSize* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`StartPadding`

<span data-ttu-id="4b7fd-134">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4b7fd-134">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4b7fd-135">Consulte *StartPadding* em [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-135">See *StartPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`EndPadding`

<span data-ttu-id="4b7fd-136">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4b7fd-136">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4b7fd-137">Consulte *endpadding* em [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-137">See *EndPadding* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

`Dilations`

<span data-ttu-id="4b7fd-138">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4b7fd-138">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4b7fd-139">Consulte *Dilations* em [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="4b7fd-139">See *Dilations* in [DML_MAX_POOLING2_OPERATOR_DESC](./ns-directml-dml_max_pooling2_operator_desc.md).</span></span>

## <a name="availability"></a><span data-ttu-id="4b7fd-140">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4b7fd-140">Availability</span></span>
<span data-ttu-id="4b7fd-141">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="4b7fd-141">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4b7fd-142">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="4b7fd-142">Tensor constraints</span></span>
* <span data-ttu-id="4b7fd-143">*InputTensor* e *OutputGradientTensor* devem ter os mesmos *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-143">*InputTensor* and *OutputGradientTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="4b7fd-144">*InputGradientTensor*, *InputTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="4b7fd-144">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4b7fd-145">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="4b7fd-145">Tensor support</span></span>
| <span data-ttu-id="4b7fd-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="4b7fd-146">Tensor</span></span> | <span data-ttu-id="4b7fd-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b7fd-147">Kind</span></span> | <span data-ttu-id="4b7fd-148">Dimensões</span><span class="sxs-lookup"><span data-stu-id="4b7fd-148">Dimensions</span></span> | <span data-ttu-id="4b7fd-149">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="4b7fd-149">Supported dimension counts</span></span> | <span data-ttu-id="4b7fd-150">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="4b7fd-150">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="4b7fd-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4b7fd-151">InputTensor</span></span> | <span data-ttu-id="4b7fd-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b7fd-152">Input</span></span> | <span data-ttu-id="4b7fd-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="4b7fd-153">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="4b7fd-154">4</span><span class="sxs-lookup"><span data-stu-id="4b7fd-154">4</span></span> | <span data-ttu-id="4b7fd-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4b7fd-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4b7fd-156">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4b7fd-156">InputGradientTensor</span></span> | <span data-ttu-id="4b7fd-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="4b7fd-157">Input</span></span> | <span data-ttu-id="4b7fd-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="4b7fd-158">{ BatchCount, ChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="4b7fd-159">4</span><span class="sxs-lookup"><span data-stu-id="4b7fd-159">4</span></span> | <span data-ttu-id="4b7fd-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4b7fd-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4b7fd-161">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4b7fd-161">OutputGradientTensor</span></span> | <span data-ttu-id="4b7fd-162">Saída</span><span class="sxs-lookup"><span data-stu-id="4b7fd-162">Output</span></span> | <span data-ttu-id="4b7fd-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="4b7fd-163">{ BatchCount, ChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="4b7fd-164">4</span><span class="sxs-lookup"><span data-stu-id="4b7fd-164">4</span></span> | <span data-ttu-id="4b7fd-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4b7fd-165">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="4b7fd-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b7fd-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4b7fd-167">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="4b7fd-167">**Header**</span></span> | <span data-ttu-id="4b7fd-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="4b7fd-168">directml.h</span></span> |