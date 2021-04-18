---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para reamostragem (consulte [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: 5808381f2e812ac20399b46672e51acd063bc6a5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105766583"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="6e418-103">Estrutura de DML_RESAMPLE_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="6e418-103">DML_RESAMPLE_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="6e418-104">Computa gradientes de repropagação para reamostragem (consulte [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="6e418-104">Computes backpropagation gradients for Resample (see [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).</span></span>

<span data-ttu-id="6e418-105">**DML_RESAMPLE1_OPERATOR_DESC** redimensiona as dimensões arbitrárias do tensor de entrada usando a amostra de vizinho mais próximo ou a interpolação bilinear.</span><span class="sxs-lookup"><span data-stu-id="6e418-105">**DML_RESAMPLE1_OPERATOR_DESC** rescales arbitrary dimensions of the input tensor using either nearest-neighbor sampling or bilinear interpolation.</span></span> <span data-ttu-id="6e418-106">Dado um *InputGradientTensor* com os mesmos tamanhos da *saída* de um **DML_RESAMPLE1_OPERATOR_DESC** equivalente, esse operador produz um *OutputGradientTensor* com os mesmos tamanhos que a *entrada* do **DML_RESAMPLE1_OPERATOR_DESC**.</span><span class="sxs-lookup"><span data-stu-id="6e418-106">Given an *InputGradientTensor* with the same sizes as the *output* of an equivalent **DML_RESAMPLE1_OPERATOR_DESC**, this operator produces an *OutputGradientTensor* with the same sizes as the *input* of the **DML_RESAMPLE1_OPERATOR_DESC**.</span></span>

<span data-ttu-id="6e418-107">Como exemplo, considere um **DML_RESAMPLE1_OPERATOR_DESC** que executa um dimensionamento de um vizinho mais próximo de 1,5 x na largura e 0,5 x na altura.</span><span class="sxs-lookup"><span data-stu-id="6e418-107">As an example, consider a **DML_RESAMPLE1_OPERATOR_DESC** that performs a nearest-neighbor scaling of 1.5x in the width, and 0.5x in the height.</span></span>

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

<span data-ttu-id="6e418-108">Observe como o elemento 0º da tensor de entrada (com valor 1) contribui para dois elementos na saída, o primeiro elemento (com valor 2) contribui para um elemento na saída, e os 2ª e 3º elementos (com os valores 3 e 4) contribuem para não elementos da saída.</span><span class="sxs-lookup"><span data-stu-id="6e418-108">Notice how the 0th element of the input tensor (with value 1) contributes to two elements in the output, the 1st element (with value 2) contributes to one element in the output, and the 2nd and 3rd elements (with values 3 and 4) contribute to no elements of the output.</span></span>

<span data-ttu-id="6e418-109">O **DML_RESAMPLE_GRAD_OPERATOR_DESC** correspondente executaria o seguinte.</span><span class="sxs-lookup"><span data-stu-id="6e418-109">The corresponding **DML_RESAMPLE_GRAD_OPERATOR_DESC** would perform the following.</span></span>

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

<span data-ttu-id="6e418-110">Observe que os valores no *OutputGradientTensor* representam as contribuições ponderadas desse elemento para o *OutputTensor* durante o operador de **DML_RESAMPLE1_OPERATOR_DESC** original.</span><span class="sxs-lookup"><span data-stu-id="6e418-110">Notice that the values in the *OutputGradientTensor* represent the weighted contributions of that element to the *OutputTensor* during the original **DML_RESAMPLE1_OPERATOR_DESC** operator.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e418-111">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="6e418-111">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="6e418-112">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6e418-112">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e418-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e418-113">Syntax</span></span>

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a><span data-ttu-id="6e418-114">Membros</span><span class="sxs-lookup"><span data-stu-id="6e418-114">Members</span></span>

`InputGradientTensor`

<span data-ttu-id="6e418-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e418-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e418-116">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="6e418-116">The incoming gradient tensor.</span></span> <span data-ttu-id="6e418-117">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="6e418-117">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="6e418-118">Normalmente, esse tensor teria os mesmos tamanhos da *saída* do [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6e418-118">Typically this tensor would have the same sizes as the *output* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="6e418-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e418-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e418-120">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="6e418-120">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="6e418-121">Normalmente, esse tensor teria os mesmos tamanhos que a *entrada* do [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6e418-121">Typically this tensor would have the same sizes as the *input* of the corresponding [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) in the forward pass.</span></span>

`InterpolationMode`

<span data-ttu-id="6e418-122">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="6e418-122">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="6e418-123">Consulte *interpolação* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="6e418-123">See *InterpolationMode* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`DimensionCount`

<span data-ttu-id="6e418-124">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="6e418-124">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="6e418-125">O número de elementos nas matrizes *Redimensions*, *InputPixelOffsets* e *OutputPixelOffsets* .</span><span class="sxs-lookup"><span data-stu-id="6e418-125">The number of elements in the *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* arrays.</span></span> <span data-ttu-id="6e418-126">Esse valor deve ser igual ao *DimensionCount* fornecido em *InputGradientTensor* e *OutputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="6e418-126">This value must equal the *DimensionCount* provided in the *InputGradientTensor* and *OutputGradientTensor*.</span></span>

`Scales`

<span data-ttu-id="6e418-127">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="6e418-127">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6e418-128">Consulte *escalas* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="6e418-128">See *Scales* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`InputPixelOffsets`

<span data-ttu-id="6e418-129">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="6e418-129">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6e418-130">Consulte *InputPixelOffsets* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="6e418-130">See *InputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

`OutputPixelOffsets`

<span data-ttu-id="6e418-131">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="6e418-131">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="6e418-132">Consulte *OutputPixelOffsets* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="6e418-132">See *OutputPixelOffsets* in [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="6e418-133">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="6e418-133">Availability</span></span>
<span data-ttu-id="6e418-134">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="6e418-134">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6e418-135">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="6e418-135">Tensor constraints</span></span>
<span data-ttu-id="6e418-136">*InputGradientTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="6e418-136">*InputGradientTensor* and *OutputGradientTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6e418-137">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="6e418-137">Tensor support</span></span>
| <span data-ttu-id="6e418-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="6e418-138">Tensor</span></span> | <span data-ttu-id="6e418-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e418-139">Kind</span></span> | <span data-ttu-id="6e418-140">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="6e418-140">Supported dimension counts</span></span> | <span data-ttu-id="6e418-141">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="6e418-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6e418-142">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6e418-142">InputGradientTensor</span></span> | <span data-ttu-id="6e418-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e418-143">Input</span></span> | <span data-ttu-id="6e418-144">4</span><span class="sxs-lookup"><span data-stu-id="6e418-144">4</span></span> | <span data-ttu-id="6e418-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6e418-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="6e418-146">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6e418-146">OutputGradientTensor</span></span> | <span data-ttu-id="6e418-147">Saída</span><span class="sxs-lookup"><span data-stu-id="6e418-147">Output</span></span> | <span data-ttu-id="6e418-148">4</span><span class="sxs-lookup"><span data-stu-id="6e418-148">4</span></span> | <span data-ttu-id="6e418-149">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="6e418-149">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="6e418-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e418-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6e418-151">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="6e418-151">**Header**</span></span> | <span data-ttu-id="6e418-152">directml. h</span><span class="sxs-lookup"><span data-stu-id="6e418-152">directml.h</span></span> |