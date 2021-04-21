---
UID: NS:directml.DML_SLICE_GRAD_OPERATOR_DESC
title: DML_SLICE_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para a fatia (consulte [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).
helpviewer_keywords:
- DML_SLICE_GRAD_OPERATOR_DESC
- DML_SLICE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_SLICE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_SLICE_GRAD_OPERATOR_DESC, DML_SLICE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
- directml/DML_SLICE_GRAD_OPERATOR_DESC
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
- DML_SLICE_GRAD_OPERATOR_DESC
ms.openlocfilehash: a22efe9b0b74f5fdc7b498b97784086f40f243b9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803964"
---
# <a name="dml_slice_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="b900f-103">Estrutura de DML_SLICE_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b900f-103">DML_SLICE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b900f-104">Computa gradientes de repropagação para a fatia (consulte [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="b900f-104">Computes backpropagation gradients for Slice (see [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc)).</span></span>

<span data-ttu-id="b900f-105">Lembre-se de que [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extrai uma sub-região de um tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="b900f-105">Recall that [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) extracts a subregion of an input tensor.</span></span> <span data-ttu-id="b900f-106">Dado um *InputGradientTensor* com os mesmos tamanhos da *saída* de um **DML_SLICE1_OPERATOR_DESC** equivalente, esse operador produz um *OutputGradientTensor* com os mesmos tamanhos da *entrada* de **DML_SLICE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="b900f-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_SLICE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of **DML_SLICE1_OPERATOR_DESC**.</span></span> <span data-ttu-id="b900f-107">Os elementos fatiados são propagados para a saída e todos os outros elementos são definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="b900f-107">The sliced elements are propagated to the output, and all other elements are set to 0.</span></span>

<span data-ttu-id="b900f-108">Como exemplo, considere um **DML_SLICE1_OPERATOR_DESC** que extrai os seguintes elementos de um tensor:</span><span class="sxs-lookup"><span data-stu-id="b900f-108">As an example, consider a **DML_SLICE1_OPERATOR_DESC** that extracts the following elements from a tensor:</span></span>

```
InputTensor            OutputTensor
[[a, b, c, d],
 [e, f, g, h],   Slice   [[a, c],
 [i, j, k, l],    -->     [i, k]]
 [m, n, o, p]]
```

<span data-ttu-id="b900f-109">Se forem fornecidos os mesmos tamanhos de *InputWindowOffsets* /  /  como no exemplo acima, esse operador executaria a transformação a seguir.</span><span class="sxs-lookup"><span data-stu-id="b900f-109">If provided the same *InputWindowOffsets*/*Sizes*/*Strides* as in the above example, this operator would then perform the following transform.</span></span>

```
InputGradientTensor       OutputGradientTensor
                             [[a, 0, c, 0],
      [[a, c],   SliceGrad    [0, 0, 0, 0],
       [i, k]]      -->       [i, 0, k, 0],
                              [0, 0, 0, 0]]
```

> [!IMPORTANT]
> <span data-ttu-id="b900f-110">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="b900f-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b900f-111">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b900f-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b900f-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b900f-112">Syntax</span></span>

```cpp
struct DML_SLICE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* InputWindowOffsets;
  _Field_size_(DimensionCount) const UINT* InputWindowSizes;
  _Field_size_(DimensionCount) const INT* InputWindowStrides;
};
```

## <a name="members"></a><span data-ttu-id="b900f-113">Membros</span><span class="sxs-lookup"><span data-stu-id="b900f-113">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="b900f-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b900f-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b900f-115">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="b900f-115">The incoming gradient tensor.</span></span> <span data-ttu-id="b900f-116">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="b900f-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="b900f-117">Normalmente, esse tensor teria os mesmos tamanhos da *saída* do [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="b900f-117">Typically, this tensor would have the same sizes as the *output* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="b900f-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b900f-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b900f-119">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="b900f-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="b900f-120">Normalmente, esse tensor teria os mesmos tamanhos da *entrada* das [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) correspondentes na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="b900f-120">Typically, this tensor would have the same sizes as the *input* of the corresponding [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc) in the forward pass.</span></span>

`DimensionCount`

<span data-ttu-id="b900f-121">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b900f-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b900f-122">O número de elementos nas matrizes *InputWindowOffsets*, *InputWindowSizes* e *InputWindowStrides* .</span><span class="sxs-lookup"><span data-stu-id="b900f-122">The number of elements in the *InputWindowOffsets*, *InputWindowSizes*, and *InputWindowStrides* arrays.</span></span> <span data-ttu-id="b900f-123">Esse valor deve ser igual ao *DimensionCount* fornecido em *InputGradientTensor* e *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="b900f-123">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`InputWindowOffsets`

<span data-ttu-id="b900f-124">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="b900f-124">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="b900f-125">Consulte *InputWindowOffsets* em [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b900f-125">See *InputWindowOffsets* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowSizes`

<span data-ttu-id="b900f-126">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="b900f-126">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="b900f-127">Consulte *InputWindowSizes* em [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b900f-127">See *InputWindowSizes* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

`InputWindowStrides`

<span data-ttu-id="b900f-128">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="b900f-128">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="b900f-129">Consulte *InputWindowStrides* em [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b900f-129">See *InputWindowStrides* in [DML_SLICE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice1_operator_desc).</span></span>

<span data-ttu-id="b900f-130">Observe que, ao contrário de **DML_SLICE1_OPERATOR_DESC**, esse operador requer sobrecorreções diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="b900f-130">Note that unlike **DML_SLICE1_OPERATOR_DESC**, this operator requires non-zero strides.</span></span> <span data-ttu-id="b900f-131">Isso ocorre porque, com um stride zero, ele é ambíguo com o qual o elemento de entrada deve ser mapeado para cada elemento de saída e, portanto, a propropagação não pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="b900f-131">That's because with a zero stride, it's ambiguous as to which input element should map to each output element, and therefore backpropagation can't be performed.</span></span> <span data-ttu-id="b900f-132">Assim como **DML_SLICE1_OPERATOR_DESC**, os avanços negativos invertem a direção da janela de entrada ao longo desse eixo.</span><span class="sxs-lookup"><span data-stu-id="b900f-132">Like **DML_SLICE1_OPERATOR_DESC**, negative strides flip the input window direction along that axis.</span></span>

## <a name="availability"></a><span data-ttu-id="b900f-133">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="b900f-133">Availability</span></span>
<span data-ttu-id="b900f-134">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="b900f-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b900f-135">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="b900f-135">Tensor constraints</span></span>
<span data-ttu-id="b900f-136">*InputGradientTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b900f-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b900f-137">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="b900f-137">Tensor support</span></span>
| <span data-ttu-id="b900f-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="b900f-138">Tensor</span></span> | <span data-ttu-id="b900f-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="b900f-139">Kind</span></span> | <span data-ttu-id="b900f-140">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="b900f-140">Supported dimension counts</span></span> | <span data-ttu-id="b900f-141">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b900f-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b900f-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b900f-142">InputGradientTensor</span></span> | <span data-ttu-id="b900f-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="b900f-143">Input</span></span> | <span data-ttu-id="b900f-144">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b900f-144">1 to 8</span></span> | <span data-ttu-id="b900f-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b900f-145">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b900f-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="b900f-146">OutputGradientTensor</span></span> | <span data-ttu-id="b900f-147">Saída</span><span class="sxs-lookup"><span data-stu-id="b900f-147">Output</span></span> | <span data-ttu-id="b900f-148">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b900f-148">1 to 8</span></span> | <span data-ttu-id="b900f-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b900f-149">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="b900f-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b900f-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b900f-151">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="b900f-151">**Header**</span></span> | <span data-ttu-id="b900f-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="b900f-152">directml.h</span></span> |