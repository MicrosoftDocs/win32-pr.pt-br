---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcula gradientes de backpropagation para pooling médio [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
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
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416990"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="0bbf5-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="0bbf5-103">DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="0bbf5-104">Calcula gradientes de backpropagation para pooling médio [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-104">Computes backpropagation gradients for average pooling (see [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).</span></span>

<span data-ttu-id="0bbf5-105">Considere um 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, sem preenchimento e um passo de 1, que executa o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-105">Consider a 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, without padding and a stride of 1, that performs the following.</span></span>

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

<span data-ttu-id="0bbf5-106">Cada janela 2x2 no tensor de entrada é média para produzir um elemento da saída (lendo zeros para elementos além da borda).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-106">Each 2x2 window in the input tensor is averaged to produce one element of the output (reading zeros for elements beyond the edge).</span></span> <span data-ttu-id="0bbf5-107">Aqui está um exemplo da saída de **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** parâmetros semelhantes.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-107">Here's an example of the output of **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** given similar parameters.</span></span>

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

<span data-ttu-id="0bbf5-108">Observe que os valores no *OutputGradientTensor* representam as contribuições ponderadas desse elemento para *o OutputTensor* durante o operador [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) original.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-108">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bbf5-109">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-109">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="0bbf5-110">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="0bbf5-110">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbf5-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bbf5-111">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="0bbf5-112">Membros</span><span class="sxs-lookup"><span data-stu-id="0bbf5-112">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="0bbf5-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0bbf5-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0bbf5-114">O tensor de gradiente de entrada.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-114">The incoming gradient tensor.</span></span> <span data-ttu-id="0bbf5-115">Normalmente, isso é obtido da saída de backpropagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="0bbf5-116">Normalmente, esse tensor teria os  mesmos tamanhos que a saída do DML_AVERAGE_POOLING_OPERATOR_DESC [correspondente](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) na passagem de avanço.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-116">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="0bbf5-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0bbf5-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0bbf5-118">Um tensor de saída que contém os gradientes paxados.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="0bbf5-119">Normalmente, esse tensor teria os  mesmos tamanhos que a entrada do DML_AVERAGE_POOLING_OPERATOR_DESC [correspondente](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) na passagem de avanço.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-119">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="0bbf5-120">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="0bbf5-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="0bbf5-121">O número de elementos nas *matrizes Strides,* *WindowSize,* *StartPadding* e *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="0bbf5-121">The number of elements in the *Strides*, *WindowSize*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="0bbf5-122">Esse valor deve ser igual à contagem de dimensões espaciais.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-122">This value must equal the spatial dimension count.</span></span> <span data-ttu-id="0bbf5-123">A contagem de dimensões espaciais será 2 se tensores 4D são fornecidos ou 3 se tensores 5D são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-123">The spatial dimension count is 2 if 4D tensors are provided, or 3 if 5D tensors are provided.</span></span>

`Strides`

<span data-ttu-id="0bbf5-124">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bbf5-124">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bbf5-125">Consulte *Strides* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-125">See *Strides* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`WindowSize`

<span data-ttu-id="0bbf5-126">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bbf5-126">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bbf5-127">Consulte *WindowSize* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-127">See *WindowSize* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`StartPadding`

<span data-ttu-id="0bbf5-128">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bbf5-128">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bbf5-129">Consulte *StartPadding* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-129">See *StartPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`EndPadding`

<span data-ttu-id="0bbf5-130">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0bbf5-130">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0bbf5-131">Consulte *EndPadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-131">See *EndPadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

`IncludePadding`

<span data-ttu-id="0bbf5-132">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="0bbf5-132">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="0bbf5-133">Consulte *IncludePadding* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="0bbf5-133">See *IncludePadding* in [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="0bbf5-134">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="0bbf5-134">Availability</span></span>
<span data-ttu-id="0bbf5-135">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="0bbf5-135">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0bbf5-136">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="0bbf5-136">Tensor constraints</span></span>
<span data-ttu-id="0bbf5-137">*InputGradientTensor* *e OutputGradientTensor* devem ter o mesmo *DataType* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="0bbf5-137">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0bbf5-138">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="0bbf5-138">Tensor support</span></span>
| <span data-ttu-id="0bbf5-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="0bbf5-139">Tensor</span></span> | <span data-ttu-id="0bbf5-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="0bbf5-140">Kind</span></span> | <span data-ttu-id="0bbf5-141">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="0bbf5-141">Supported dimension counts</span></span> | <span data-ttu-id="0bbf5-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="0bbf5-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0bbf5-143">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="0bbf5-143">InputGradientTensor</span></span> | <span data-ttu-id="0bbf5-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="0bbf5-144">Input</span></span> | <span data-ttu-id="0bbf5-145">4 a 5</span><span class="sxs-lookup"><span data-stu-id="0bbf5-145">4 to 5</span></span> | <span data-ttu-id="0bbf5-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0bbf5-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0bbf5-147">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="0bbf5-147">OutputGradientTensor</span></span> | <span data-ttu-id="0bbf5-148">Saída</span><span class="sxs-lookup"><span data-stu-id="0bbf5-148">Output</span></span> | <span data-ttu-id="0bbf5-149">4 a 5</span><span class="sxs-lookup"><span data-stu-id="0bbf5-149">4 to 5</span></span> | <span data-ttu-id="0bbf5-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0bbf5-150">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="0bbf5-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bbf5-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0bbf5-152">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="0bbf5-152">**Header**</span></span> | <span data-ttu-id="0bbf5-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="0bbf5-153">directml.h</span></span> |