---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para a [normalização em lotes](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).
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
ms.openlocfilehash: ba12541514c8121d483236afa2163a04bd991288
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804419"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="84b3f-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="84b3f-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="84b3f-104">Computa gradientes de repropagação para a [normalização em lotes](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="84b3f-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="84b3f-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** executa vários cálculos, que são detalhados nas descrições de saída separadas.</span><span class="sxs-lookup"><span data-stu-id="84b3f-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84b3f-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="84b3f-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="84b3f-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="84b3f-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84b3f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84b3f-108">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="84b3f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="84b3f-109">Members</span></span>

`InputTensor`

<span data-ttu-id="84b3f-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-111">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="84b3f-111">A tensor containing the input data.</span></span> <span data-ttu-id="84b3f-112">Normalmente, isso é o mesmo tensor que foi fornecido como o *InputTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="84b3f-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="84b3f-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-114">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="84b3f-114">The incoming gradient tensor.</span></span> <span data-ttu-id="84b3f-115">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="84b3f-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="84b3f-116">Este tensor deve ter os mesmos tamanhos de dimensão que *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="84b3f-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="84b3f-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-118">Um tensor que contém os dados médios.</span><span class="sxs-lookup"><span data-stu-id="84b3f-118">A tensor containing the mean data.</span></span> <span data-ttu-id="84b3f-119">Normalmente, isso é o mesmo tensor que foi fornecido como o *MeanTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="84b3f-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="84b3f-120">Todas as dimensões que não têm o mesmo tamanho que a dimensão correspondente de *InputTensor* devem ter um tamanho de 1 para que possam ser transmitidas para corresponder à entrada.</span><span class="sxs-lookup"><span data-stu-id="84b3f-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="84b3f-121">Por exemplo, os tamanhos a seguir são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="84b3f-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="84b3f-122">Veja a seguir um erro, pois, para que a difusão seja compatível, quaisquer dimensões que não correspondam devem ter o tamanho 1.</span><span class="sxs-lookup"><span data-stu-id="84b3f-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="84b3f-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-124">Um tensor que contém os dados de variação.</span><span class="sxs-lookup"><span data-stu-id="84b3f-124">A tensor containing the variance data.</span></span> <span data-ttu-id="84b3f-125">Normalmente, isso é o mesmo tensor que foi fornecido como o *VarianceTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="84b3f-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="84b3f-126">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor*.</span><span class="sxs-lookup"><span data-stu-id="84b3f-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="84b3f-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-128">Um tensor que contém os dados de escala.</span><span class="sxs-lookup"><span data-stu-id="84b3f-128">A tensor containing the scale data.</span></span> <span data-ttu-id="84b3f-129">Normalmente, isso é o mesmo tensor que foi fornecido como o *ScaleTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="84b3f-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="84b3f-130">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor*.</span><span class="sxs-lookup"><span data-stu-id="84b3f-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="84b3f-131">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-132">Para cada valor correspondente nas entradas, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="84b3f-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="84b3f-133">Este tensor deve ter os mesmos tamanhos de dimensão que *InputTensor* / *InputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="84b3f-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="84b3f-134">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-135">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor* / *VarianceTensor* / *ScaleTensor*.</span><span class="sxs-lookup"><span data-stu-id="84b3f-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="84b3f-136">A computação a seguir é feita ou cada valor correspondente nas entradas.</span><span class="sxs-lookup"><span data-stu-id="84b3f-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="84b3f-137">O `sum` é calculado em todas as dimensões que precisam ser transmitidas.</span><span class="sxs-lookup"><span data-stu-id="84b3f-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="84b3f-138">Se não houver nenhuma difusão necessária, nenhuma soma será necessária.</span><span class="sxs-lookup"><span data-stu-id="84b3f-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="84b3f-139">Veja um exemplo.</span><span class="sxs-lookup"><span data-stu-id="84b3f-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="84b3f-140">O elemento [0, **0**, 0, 0] de `OutputScaleGradientTensor` é a soma de `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` para todos os elementos 90 (3 \* 5 \* 6) [[0, 2], **0**, [0, 4], [0, 5]].</span><span class="sxs-lookup"><span data-stu-id="84b3f-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="84b3f-141">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="84b3f-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="84b3f-142">Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor* / *VarianceTensor* / *ScaleTensor*.</span><span class="sxs-lookup"><span data-stu-id="84b3f-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="84b3f-143">A computação a seguir é feita ou cada valor correspondente nas entradas.</span><span class="sxs-lookup"><span data-stu-id="84b3f-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="84b3f-144">O `sum` é calculado em todas as dimensões que precisam ser transmitidas (consulte o exemplo de *OutputScaleGradientTensor*).</span><span class="sxs-lookup"><span data-stu-id="84b3f-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="84b3f-145">Se não houver nenhuma difusão necessária, nenhuma soma será necessária.</span><span class="sxs-lookup"><span data-stu-id="84b3f-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="84b3f-146">Tipo: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="84b3f-146">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="84b3f-147">Um valor pequeno adicionado à variação para evitar Zero.</span><span class="sxs-lookup"><span data-stu-id="84b3f-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="84b3f-148">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="84b3f-148">Availability</span></span>
<span data-ttu-id="84b3f-149">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="84b3f-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="84b3f-150">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-150">Tensor constraints</span></span>
<span data-ttu-id="84b3f-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor* e *VarianceTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="84b3f-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="84b3f-152">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-152">Tensor support</span></span>
| <span data-ttu-id="84b3f-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-153">Tensor</span></span> | <span data-ttu-id="84b3f-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="84b3f-154">Kind</span></span> | <span data-ttu-id="84b3f-155">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="84b3f-155">Supported dimension counts</span></span> | <span data-ttu-id="84b3f-156">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="84b3f-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="84b3f-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-157">InputTensor</span></span> | <span data-ttu-id="84b3f-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="84b3f-158">Input</span></span> | <span data-ttu-id="84b3f-159">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-159">1 to 8</span></span> | <span data-ttu-id="84b3f-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="84b3f-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-161">InputGradientTensor</span></span> | <span data-ttu-id="84b3f-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="84b3f-162">Input</span></span> | <span data-ttu-id="84b3f-163">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-163">1 to 8</span></span> | <span data-ttu-id="84b3f-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="84b3f-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-165">MeanTensor</span></span> | <span data-ttu-id="84b3f-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="84b3f-166">Input</span></span> | <span data-ttu-id="84b3f-167">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-167">1 to 8</span></span> | <span data-ttu-id="84b3f-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="84b3f-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-169">VarianceTensor</span></span> | <span data-ttu-id="84b3f-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="84b3f-170">Input</span></span> | <span data-ttu-id="84b3f-171">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-171">1 to 8</span></span> | <span data-ttu-id="84b3f-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="84b3f-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-173">ScaleTensor</span></span> | <span data-ttu-id="84b3f-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="84b3f-174">Input</span></span> | <span data-ttu-id="84b3f-175">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-175">1 to 8</span></span> | <span data-ttu-id="84b3f-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="84b3f-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-177">OutputGradientTensor</span></span> | <span data-ttu-id="84b3f-178">Saída</span><span class="sxs-lookup"><span data-stu-id="84b3f-178">Output</span></span> | <span data-ttu-id="84b3f-179">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-179">1 to 8</span></span> | <span data-ttu-id="84b3f-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="84b3f-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="84b3f-182">Saída</span><span class="sxs-lookup"><span data-stu-id="84b3f-182">Output</span></span> | <span data-ttu-id="84b3f-183">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-183">1 to 8</span></span> | <span data-ttu-id="84b3f-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="84b3f-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="84b3f-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="84b3f-186">Saída</span><span class="sxs-lookup"><span data-stu-id="84b3f-186">Output</span></span> | <span data-ttu-id="84b3f-187">1 a 8</span><span class="sxs-lookup"><span data-stu-id="84b3f-187">1 to 8</span></span> | <span data-ttu-id="84b3f-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="84b3f-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="84b3f-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84b3f-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="84b3f-190">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="84b3f-190">**Header**</span></span> | <span data-ttu-id="84b3f-191">directml. h</span><span class="sxs-lookup"><span data-stu-id="84b3f-191">directml.h</span></span> |
