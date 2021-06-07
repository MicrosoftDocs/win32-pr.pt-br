---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Executa uma função de normalização de variação média no tensor de entrada. Esse operador calculará a média e a variação do tensor de entrada para executar a normalização.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416943"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="b5259-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="b5259-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b5259-105">Executa uma função de normalização de variação média no tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="b5259-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="b5259-106">Esse operador calculará a média e a variação do tensor de entrada para executar a normalização.</span><span class="sxs-lookup"><span data-stu-id="b5259-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="b5259-107">Esse operador executa a computação a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5259-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="b5259-108">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="b5259-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b5259-109">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="b5259-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5259-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5259-110">Syntax</span></span>
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a><span data-ttu-id="b5259-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b5259-111">Members</span></span>

`InputTensor`

<span data-ttu-id="b5259-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b5259-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b5259-113">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="b5259-113">A tensor containing the Input data.</span></span> <span data-ttu-id="b5259-114">As dimensões desse tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="b5259-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="b5259-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b5259-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b5259-116">Um tensor opcional que contém os dados de escala.</span><span class="sxs-lookup"><span data-stu-id="b5259-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="b5259-117">Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="b5259-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="b5259-118">As dimensões ScaleBatchCount, ScaleHeight e ScaleWidth devem corresponder *a InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.</span><span class="sxs-lookup"><span data-stu-id="b5259-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="b5259-119">Se **DML_FEATURE_LEVEL** for maior ou igual **a DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e ser transmitida automaticamente para corresponder a *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b5259-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="b5259-120">Esse tensor será necessário se *o BiasTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="b5259-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="b5259-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b5259-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="b5259-122">Um tensor opcional que contém os dados bias.</span><span class="sxs-lookup"><span data-stu-id="b5259-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="b5259-123">Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="b5259-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="b5259-124">As dimensões BiasBatchCount, BiasHeight e BiasWidth devem corresponder *a InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.</span><span class="sxs-lookup"><span data-stu-id="b5259-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="b5259-125">Se **DML_FEATURE_LEVEL** for maior ou igual **a DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e ser transmitida automaticamente para corresponder a *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b5259-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="b5259-126">Esse tensor será necessário se o *ScaleTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="b5259-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="b5259-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b5259-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b5259-128">Um tensor no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="b5259-128">A tensor to write the results to.</span></span> <span data-ttu-id="b5259-129">As dimensões desse tensor são `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="b5259-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="b5259-130">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="b5259-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="b5259-131">O número de eixos.</span><span class="sxs-lookup"><span data-stu-id="b5259-131">The number of axes.</span></span> <span data-ttu-id="b5259-132">Esse campo determina o tamanho da matriz *Eixos.*</span><span class="sxs-lookup"><span data-stu-id="b5259-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="b5259-133">Tipo: \_ Tamanho do campo \_ \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b5259-133">Type: \_Field\_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span> 

<span data-ttu-id="b5259-134">Os eixos ao longo dos quais calcular a Média e a Variação.</span><span class="sxs-lookup"><span data-stu-id="b5259-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="b5259-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="b5259-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="b5259-136">**TRUE** se a camada normalização incluir Variação no cálculo de normalização.</span><span class="sxs-lookup"><span data-stu-id="b5259-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="b5259-137">Caso contrário, **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b5259-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="b5259-138">Se **FALSE**, a equação de normalização será `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="b5259-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="b5259-139">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="b5259-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="b5259-140">O valor de epsilon a ser usado para evitar a divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="b5259-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="b5259-141">Um valor de 0,00001 é recomendado como padrão.</span><span class="sxs-lookup"><span data-stu-id="b5259-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="b5259-142">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b5259-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="b5259-143">Uma camada de ativação opcional mesclada a ser aplicada após a normalização.</span><span class="sxs-lookup"><span data-stu-id="b5259-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5259-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5259-144">Remarks</span></span>
<span data-ttu-id="b5259-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** é um superconjunto da funcionalidade [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="b5259-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="b5259-146">Aqui, definir a matriz **Eixos** como é o equivalente à definição de CrossChannel como FALSE no DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC ; enquanto definir a matriz Eixos como é equivalente à definição de `{ 0, 2, 3 }`     `{ 1, 2, 3 }` *CrossChannel* como **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="b5259-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="b5259-147">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="b5259-147">Availability</span></span>
<span data-ttu-id="b5259-148">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b5259-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b5259-149">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="b5259-149">Tensor constraints</span></span>

<span data-ttu-id="b5259-150">*BiasTensor,* *InputTensor,* *OutputTensor* e *ScaleTensor* devem ter o mesmo *DataType* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b5259-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b5259-151">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="b5259-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="b5259-152">DML_FEATURE_LEVEL_3_1 e superior</span><span class="sxs-lookup"><span data-stu-id="b5259-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="b5259-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="b5259-153">Tensor</span></span> | <span data-ttu-id="b5259-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5259-154">Kind</span></span> | <span data-ttu-id="b5259-155">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="b5259-155">Supported dimension counts</span></span> | <span data-ttu-id="b5259-156">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b5259-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b5259-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-157">InputTensor</span></span> | <span data-ttu-id="b5259-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5259-158">Input</span></span> | <span data-ttu-id="b5259-159">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b5259-159">1 to 8</span></span> | <span data-ttu-id="b5259-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b5259-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-161">ScaleTensor</span></span> | <span data-ttu-id="b5259-162">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-162">Optional input</span></span> | <span data-ttu-id="b5259-163">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b5259-163">1 to 8</span></span> | <span data-ttu-id="b5259-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b5259-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-165">BiasTensor</span></span> | <span data-ttu-id="b5259-166">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-166">Optional input</span></span> | <span data-ttu-id="b5259-167">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b5259-167">1 to 8</span></span> | <span data-ttu-id="b5259-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b5259-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-169">OutputTensor</span></span> | <span data-ttu-id="b5259-170">Saída</span><span class="sxs-lookup"><span data-stu-id="b5259-170">Output</span></span> | <span data-ttu-id="b5259-171">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b5259-171">1 to 8</span></span> | <span data-ttu-id="b5259-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="b5259-173">DML_FEATURE_LEVEL_2_1 e superior</span><span class="sxs-lookup"><span data-stu-id="b5259-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="b5259-174">Tensor</span><span class="sxs-lookup"><span data-stu-id="b5259-174">Tensor</span></span> | <span data-ttu-id="b5259-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5259-175">Kind</span></span> | <span data-ttu-id="b5259-176">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="b5259-176">Supported dimension counts</span></span> | <span data-ttu-id="b5259-177">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b5259-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b5259-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-178">InputTensor</span></span> | <span data-ttu-id="b5259-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="b5259-179">Input</span></span> | <span data-ttu-id="b5259-180">4</span><span class="sxs-lookup"><span data-stu-id="b5259-180">4</span></span> | <span data-ttu-id="b5259-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b5259-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-182">ScaleTensor</span></span> | <span data-ttu-id="b5259-183">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-183">Optional input</span></span> | <span data-ttu-id="b5259-184">4</span><span class="sxs-lookup"><span data-stu-id="b5259-184">4</span></span> | <span data-ttu-id="b5259-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b5259-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-186">BiasTensor</span></span> | <span data-ttu-id="b5259-187">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="b5259-187">Optional input</span></span> | <span data-ttu-id="b5259-188">4</span><span class="sxs-lookup"><span data-stu-id="b5259-188">4</span></span> | <span data-ttu-id="b5259-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="b5259-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b5259-190">OutputTensor</span></span> | <span data-ttu-id="b5259-191">Saída</span><span class="sxs-lookup"><span data-stu-id="b5259-191">Output</span></span> | <span data-ttu-id="b5259-192">4</span><span class="sxs-lookup"><span data-stu-id="b5259-192">4</span></span> | <span data-ttu-id="b5259-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="b5259-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="b5259-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5259-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b5259-195">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="b5259-195">**Header**</span></span> | <span data-ttu-id="b5259-196">directml.h</span><span class="sxs-lookup"><span data-stu-id="b5259-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="b5259-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5259-197">See also</span></span>

[<span data-ttu-id="b5259-198">Usando operadores mesclados para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="b5259-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)