---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcula gradientes de backpropagation para [normalização em lote.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550431"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="68735-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="68735-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="68735-104">Calcula gradientes de backpropagation para [normalização em lote.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="68735-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="68735-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** executa vários cálculos, que são detalhados nas descrições de saída separadas.</span><span class="sxs-lookup"><span data-stu-id="68735-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68735-106">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.5 e posterior).</span><span class="sxs-lookup"><span data-stu-id="68735-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="68735-107">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="68735-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68735-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68735-108">Syntax</span></span>
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="68735-109">Membros</span><span class="sxs-lookup"><span data-stu-id="68735-109">Members</span></span>

`InputTensor`

<span data-ttu-id="68735-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-111">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="68735-111">A tensor containing the input data.</span></span> <span data-ttu-id="68735-112">Normalmente, esse é o mesmo tensor que foi fornecido como *o InputTensor* para DML_BATCH_NORMALIZATION_OPERATOR_DESC [**na**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passagem de avanço.</span><span class="sxs-lookup"><span data-stu-id="68735-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="68735-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-114">O tensor de gradiente de entrada.</span><span class="sxs-lookup"><span data-stu-id="68735-114">The incoming gradient tensor.</span></span> <span data-ttu-id="68735-115">Normalmente, isso é obtido da saída de backpropagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="68735-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="68735-116">Esse tensor deve ter os mesmos tamanhos de dimensão *que InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="68735-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="68735-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-118">Um tensor que contém os dados de média.</span><span class="sxs-lookup"><span data-stu-id="68735-118">A tensor containing the mean data.</span></span> <span data-ttu-id="68735-119">Normalmente, esse é o mesmo tensor que foi fornecido como *o MeanTensor* para DML_BATCH_NORMALIZATION_OPERATOR_DESC [**na**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passagem de avanço.</span><span class="sxs-lookup"><span data-stu-id="68735-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="68735-120">Todas as dimensões que não têm o mesmo tamanho que a dimensão correspondente *de InputTensor* devem ter um tamanho de 1 para que possam ser transmitidas para corresponder à entrada.</span><span class="sxs-lookup"><span data-stu-id="68735-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="68735-121">Por exemplo, os tamanhos a seguir são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="68735-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="68735-122">A seguir está um erro, uma vez que, para ser compatível com difusão, todas as dimensões que não corresponderem devem ter o tamanho 1.</span><span class="sxs-lookup"><span data-stu-id="68735-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="68735-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-124">Um tensor que contém os dados de variação.</span><span class="sxs-lookup"><span data-stu-id="68735-124">A tensor containing the variance data.</span></span> <span data-ttu-id="68735-125">Normalmente, isso é o mesmo tensor que foi fornecido como o *VarianceTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="68735-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="68735-126">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor*.</span><span class="sxs-lookup"><span data-stu-id="68735-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="68735-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-128">Um tensor que contém os dados de escala.</span><span class="sxs-lookup"><span data-stu-id="68735-128">A tensor containing the scale data.</span></span> <span data-ttu-id="68735-129">Normalmente, isso é o mesmo tensor que foi fornecido como o *ScaleTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="68735-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="68735-130">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor*.</span><span class="sxs-lookup"><span data-stu-id="68735-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="68735-131">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-132">Para cada valor correspondente nas entradas, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="68735-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="68735-133">Este tensor deve ter os mesmos tamanhos de dimensão que *InputTensor* / *InputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="68735-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="68735-134">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-135">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor* / *VarianceTensor* / *ScaleTensor*.</span><span class="sxs-lookup"><span data-stu-id="68735-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="68735-136">A computação a seguir é feita ou cada valor correspondente nas entradas.</span><span class="sxs-lookup"><span data-stu-id="68735-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="68735-137">O `sum` é calculado em todas as dimensões que precisam ser transmitidas.</span><span class="sxs-lookup"><span data-stu-id="68735-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="68735-138">Se não houver nenhuma difusão necessária, nenhuma soma será necessária.</span><span class="sxs-lookup"><span data-stu-id="68735-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="68735-139">A seguir, um exemplo.</span><span class="sxs-lookup"><span data-stu-id="68735-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="68735-140">O elemento [0, **0**, 0, 0] de `OutputScaleGradientTensor` é a soma de `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` para todos os elementos 90 (3 \* 5 \* 6) [[0, 2], **0**, [0, 4], [0, 5]].</span><span class="sxs-lookup"><span data-stu-id="68735-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="68735-141">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="68735-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="68735-142">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor* / *VarianceTensor* / *ScaleTensor*.</span><span class="sxs-lookup"><span data-stu-id="68735-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="68735-143">A computação a seguir é feita ou cada valor correspondente nas entradas.</span><span class="sxs-lookup"><span data-stu-id="68735-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="68735-144">O `sum` é calculado em todas as dimensões que precisam ser transmitidas (consulte o exemplo de *OutputScaleGradientTensor*).</span><span class="sxs-lookup"><span data-stu-id="68735-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="68735-145">Se não houver nenhuma difusão necessária, nenhuma soma será necessária.</span><span class="sxs-lookup"><span data-stu-id="68735-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="68735-146">Tipo: **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68735-146">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68735-147">Um valor pequeno adicionado à variação para evitar zero.</span><span class="sxs-lookup"><span data-stu-id="68735-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="68735-148">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="68735-148">Availability</span></span>
<span data-ttu-id="68735-149">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="68735-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="68735-150">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="68735-150">Tensor constraints</span></span>
<span data-ttu-id="68735-151">*InputGradientTensor,* *InputTensor,* *MeanTensor,* *OutputBiasGradientTensor,* *OutputGradientTensor,* *OutputScaleGradientTensor,* *ScaleTensor* e *VarianceTensor* devem ter o mesmo *DataType* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="68735-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="68735-152">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="68735-152">Tensor support</span></span>
| <span data-ttu-id="68735-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="68735-153">Tensor</span></span> | <span data-ttu-id="68735-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="68735-154">Kind</span></span> | <span data-ttu-id="68735-155">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="68735-155">Supported dimension counts</span></span> | <span data-ttu-id="68735-156">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="68735-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="68735-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="68735-157">InputTensor</span></span> | <span data-ttu-id="68735-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="68735-158">Input</span></span> | <span data-ttu-id="68735-159">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-159">1 to 8</span></span> | <span data-ttu-id="68735-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68735-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="68735-161">InputGradientTensor</span></span> | <span data-ttu-id="68735-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="68735-162">Input</span></span> | <span data-ttu-id="68735-163">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-163">1 to 8</span></span> | <span data-ttu-id="68735-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68735-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="68735-165">MeanTensor</span></span> | <span data-ttu-id="68735-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="68735-166">Input</span></span> | <span data-ttu-id="68735-167">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-167">1 to 8</span></span> | <span data-ttu-id="68735-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68735-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="68735-169">VarianceTensor</span></span> | <span data-ttu-id="68735-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="68735-170">Input</span></span> | <span data-ttu-id="68735-171">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-171">1 to 8</span></span> | <span data-ttu-id="68735-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68735-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="68735-173">ScaleTensor</span></span> | <span data-ttu-id="68735-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="68735-174">Input</span></span> | <span data-ttu-id="68735-175">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-175">1 to 8</span></span> | <span data-ttu-id="68735-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68735-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="68735-177">OutputGradientTensor</span></span> | <span data-ttu-id="68735-178">Saída</span><span class="sxs-lookup"><span data-stu-id="68735-178">Output</span></span> | <span data-ttu-id="68735-179">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-179">1 to 8</span></span> | <span data-ttu-id="68735-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68735-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="68735-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="68735-182">Saída</span><span class="sxs-lookup"><span data-stu-id="68735-182">Output</span></span> | <span data-ttu-id="68735-183">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-183">1 to 8</span></span> | <span data-ttu-id="68735-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="68735-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="68735-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="68735-186">Saída</span><span class="sxs-lookup"><span data-stu-id="68735-186">Output</span></span> | <span data-ttu-id="68735-187">1 a 8</span><span class="sxs-lookup"><span data-stu-id="68735-187">1 to 8</span></span> | <span data-ttu-id="68735-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="68735-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="68735-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68735-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="68735-190">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="68735-190">**Header**</span></span> | <span data-ttu-id="68735-191">directml. h</span><span class="sxs-lookup"><span data-stu-id="68735-191">directml.h</span></span> |