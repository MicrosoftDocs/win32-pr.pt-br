---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para a média de Pooling (consulte [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5c2803fc300ca862d54a74aee1c864e9097e3d8e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803358"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="4734b-103">Estrutura de DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="4734b-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="4734b-104">Computa gradientes de repropagação para a média de Pooling (consulte [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="4734b-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="4734b-105">Considere um **DML_AVERAGE_POOLING_OPERATOR_DESC** 2x2, sem preenchimento e um stride de 1, que realiza o seguinte.</span><span class="sxs-lookup"><span data-stu-id="4734b-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="4734b-106">Cada janela 2x2 no tensor de entrada é calculada para produzir um elemento da saída (lendo zeros para elementos além da borda).</span><span class="sxs-lookup"><span data-stu-id="4734b-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="4734b-107">Aqui está um exemplo da saída de **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** dadas parâmetros semelhantes.</span><span class="sxs-lookup"><span data-stu-id="4734b-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="4734b-108">Observe que os valores no *OutputGradientTensor* representam as contribuições ponderadas desse elemento para o *OutputTensor* durante o operador de [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) original.</span><span class="sxs-lookup"><span data-stu-id="4734b-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4734b-109">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="4734b-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4734b-110">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="4734b-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4734b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4734b-111">Syntax</span></span>

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a><span data-ttu-id="4734b-112">Membros</span><span class="sxs-lookup"><span data-stu-id="4734b-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="4734b-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4734b-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4734b-114">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="4734b-114">The incoming gradient tensor.</span></span> <span data-ttu-id="4734b-115">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="4734b-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="4734b-116">Normalmente, esse tensor teria os mesmos tamanhos da *saída* do [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4734b-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="4734b-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4734b-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4734b-118">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="4734b-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="4734b-119">Normalmente, esse tensor teria os mesmos tamanhos que a *entrada* do [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="4734b-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="4734b-120">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4734b-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4734b-121">O número de elementos nas matrizes de *prerides*, *WindowSize*, *StartPadding* e *endpadding* .</span><span class="sxs-lookup"><span data-stu-id="4734b-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="4734b-122">Esse valor deve ser igual à contagem espacial da dimensão.</span><span class="sxs-lookup"><span data-stu-id="4734b-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="4734b-123">A contagem de dimensões espaciais será 2 se os dezenasais de 4D forem fornecidos ou 3 se forem fornecidos mais de dezenas.</span><span class="sxs-lookup"><span data-stu-id="4734b-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="4734b-124">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4734b-124">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="4734b-125">Veja os *avanços* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4734b-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="4734b-126">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4734b-126">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="4734b-127">Consulte *WindowSize* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4734b-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="4734b-128">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4734b-128">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="4734b-129">Consulte *StartPadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4734b-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="4734b-130">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="4734b-130">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="4734b-131">Consulte *endpadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4734b-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="4734b-132">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="4734b-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="4734b-133">Consulte *IncludePadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="4734b-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="4734b-134">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4734b-134">Availability</span></span>
<span data-ttu-id="4734b-135">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="4734b-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4734b-136">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="4734b-136">Tensor constraints</span></span>
<span data-ttu-id="4734b-137">*InputGradientTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4734b-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4734b-138">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="4734b-138">Tensor support</span></span>
| <span data-ttu-id="4734b-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="4734b-139">Tensor</span></span> | <span data-ttu-id="4734b-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="4734b-140">Kind</span></span> | <span data-ttu-id="4734b-141">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="4734b-141">Supported dimension counts</span></span> | <span data-ttu-id="4734b-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="4734b-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4734b-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4734b-143">InputGradientTensor</span></span> | <span data-ttu-id="4734b-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="4734b-144">Input</span></span> | <span data-ttu-id="4734b-145">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4734b-145">4 to 5</span></span> | <span data-ttu-id="4734b-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4734b-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4734b-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="4734b-147">OutputGradientTensor</span></span> | <span data-ttu-id="4734b-148">Saída</span><span class="sxs-lookup"><span data-stu-id="4734b-148">Output</span></span> | <span data-ttu-id="4734b-149">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4734b-149">4 to 5</span></span> | <span data-ttu-id="4734b-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4734b-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="4734b-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4734b-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4734b-152">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="4734b-152">**Header**</span></span> | <span data-ttu-id="4734b-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="4734b-153">directml.h</span></span> |