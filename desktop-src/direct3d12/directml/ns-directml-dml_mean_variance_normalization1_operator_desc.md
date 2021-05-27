---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Executa uma função de normalização de variância média no tensor de entrada. Esse operador calculará a média e a variação do tensor de entrada para executar a normalização.
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
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549771"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="712b1-104">Estrutura de DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="712b1-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="712b1-105">Executa uma função de normalização de variância média no tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="712b1-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="712b1-106">Esse operador calculará a média e a variação do tensor de entrada para executar a normalização.</span><span class="sxs-lookup"><span data-stu-id="712b1-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="712b1-107">Esse operador executa a computação a seguir.</span><span class="sxs-lookup"><span data-stu-id="712b1-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="712b1-108">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="712b1-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="712b1-109">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="712b1-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="712b1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="712b1-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="712b1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="712b1-111">Members</span></span>

`InputTensor`

<span data-ttu-id="712b1-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="712b1-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="712b1-113">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="712b1-113">A tensor containing the Input data.</span></span> <span data-ttu-id="712b1-114">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="712b1-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="712b1-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="712b1-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="712b1-116">Um tensor opcional que contém os dados de escala.</span><span class="sxs-lookup"><span data-stu-id="712b1-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="712b1-117">Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="712b1-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="712b1-118">As dimensões ScaleBatchCount, AlturaDaEscala e LarguraDaEscala devem corresponder a *InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.</span><span class="sxs-lookup"><span data-stu-id="712b1-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="712b1-119">Se **DML_FEATURE_LEVEL** for maior ou igual a **DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e será difundida automaticamente para corresponder ao *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="712b1-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="712b1-120">Esse tensor será necessário se o *BiasTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="712b1-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="712b1-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="712b1-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="712b1-122">Um tensor opcional que contém os dados de tendência.</span><span class="sxs-lookup"><span data-stu-id="712b1-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="712b1-123">Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="712b1-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="712b1-124">As dimensões BiasBatchCount, BiasHeight e BiasWidth devem corresponder *a InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.</span><span class="sxs-lookup"><span data-stu-id="712b1-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="712b1-125">Se **DML_FEATURE_LEVEL** for maior ou igual **a DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e ser transmitida automaticamente para corresponder a *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="712b1-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="712b1-126">Esse tensor será necessário se o *ScaleTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="712b1-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="712b1-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="712b1-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="712b1-128">Um tensor no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="712b1-128">A tensor to write the results to.</span></span> <span data-ttu-id="712b1-129">As dimensões desse tensor são `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="712b1-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="712b1-130">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="712b1-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="712b1-131">O número de eixos.</span><span class="sxs-lookup"><span data-stu-id="712b1-131">The number of axes.</span></span> <span data-ttu-id="712b1-132">Esse campo determina o tamanho da matriz *Eixos.*</span><span class="sxs-lookup"><span data-stu-id="712b1-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="712b1-133">Tipo: \_ Tamanho do campo \_ \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="712b1-133">Type: \_Field\_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span> 

<span data-ttu-id="712b1-134">Os eixos ao longo dos quais calcular a Média e a Variação.</span><span class="sxs-lookup"><span data-stu-id="712b1-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="712b1-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="712b1-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="712b1-136">**TRUE** se a camada normalização incluir Variação no cálculo de normalização.</span><span class="sxs-lookup"><span data-stu-id="712b1-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="712b1-137">Caso contrário, **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="712b1-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="712b1-138">Se **FALSE**, a equação de normalização será `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="712b1-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="712b1-139">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="712b1-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="712b1-140">O valor de epsilon a ser usado para evitar a divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="712b1-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="712b1-141">Um valor de 0,00001 é recomendado como padrão.</span><span class="sxs-lookup"><span data-stu-id="712b1-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="712b1-142">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="712b1-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="712b1-143">Uma camada de ativação opcional mesclada a ser aplicada após a normalização.</span><span class="sxs-lookup"><span data-stu-id="712b1-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="712b1-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="712b1-144">Remarks</span></span>
<span data-ttu-id="712b1-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** é um superconjunto de funcionalidades do [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="712b1-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="712b1-146">Aqui, a definição da matriz de **eixos** como `{ 0, 2, 3 }` é o equivalente à definição de *CrossChannel* como **false** em **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; ao definir a matriz de **eixos** como `{ 1, 2, 3 }` equivalente à definição de *CrossChannel* como **true**.</span><span class="sxs-lookup"><span data-stu-id="712b1-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="712b1-147">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="712b1-147">Availability</span></span>
<span data-ttu-id="712b1-148">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="712b1-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="712b1-149">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="712b1-149">Tensor constraints</span></span>

<span data-ttu-id="712b1-150">*BiasTensor*, *InputTensor*, *OutputTensor* e *ScaleTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="712b1-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="712b1-151">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="712b1-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="712b1-152">DML_FEATURE_LEVEL_3_1 e acima</span><span class="sxs-lookup"><span data-stu-id="712b1-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="712b1-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="712b1-153">Tensor</span></span> | <span data-ttu-id="712b1-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="712b1-154">Kind</span></span> | <span data-ttu-id="712b1-155">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="712b1-155">Supported dimension counts</span></span> | <span data-ttu-id="712b1-156">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="712b1-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="712b1-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-157">InputTensor</span></span> | <span data-ttu-id="712b1-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="712b1-158">Input</span></span> | <span data-ttu-id="712b1-159">1 a 8</span><span class="sxs-lookup"><span data-stu-id="712b1-159">1 to 8</span></span> | <span data-ttu-id="712b1-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="712b1-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-161">ScaleTensor</span></span> | <span data-ttu-id="712b1-162">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="712b1-162">Optional input</span></span> | <span data-ttu-id="712b1-163">1 a 8</span><span class="sxs-lookup"><span data-stu-id="712b1-163">1 to 8</span></span> | <span data-ttu-id="712b1-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="712b1-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-165">BiasTensor</span></span> | <span data-ttu-id="712b1-166">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="712b1-166">Optional input</span></span> | <span data-ttu-id="712b1-167">1 a 8</span><span class="sxs-lookup"><span data-stu-id="712b1-167">1 to 8</span></span> | <span data-ttu-id="712b1-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="712b1-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-169">OutputTensor</span></span> | <span data-ttu-id="712b1-170">Saída</span><span class="sxs-lookup"><span data-stu-id="712b1-170">Output</span></span> | <span data-ttu-id="712b1-171">1 a 8</span><span class="sxs-lookup"><span data-stu-id="712b1-171">1 to 8</span></span> | <span data-ttu-id="712b1-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="712b1-173">DML_FEATURE_LEVEL_2_1 e superior</span><span class="sxs-lookup"><span data-stu-id="712b1-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="712b1-174">Tensor</span><span class="sxs-lookup"><span data-stu-id="712b1-174">Tensor</span></span> | <span data-ttu-id="712b1-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="712b1-175">Kind</span></span> | <span data-ttu-id="712b1-176">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="712b1-176">Supported dimension counts</span></span> | <span data-ttu-id="712b1-177">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="712b1-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="712b1-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-178">InputTensor</span></span> | <span data-ttu-id="712b1-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="712b1-179">Input</span></span> | <span data-ttu-id="712b1-180">4</span><span class="sxs-lookup"><span data-stu-id="712b1-180">4</span></span> | <span data-ttu-id="712b1-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="712b1-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-182">ScaleTensor</span></span> | <span data-ttu-id="712b1-183">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="712b1-183">Optional input</span></span> | <span data-ttu-id="712b1-184">4</span><span class="sxs-lookup"><span data-stu-id="712b1-184">4</span></span> | <span data-ttu-id="712b1-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="712b1-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-186">BiasTensor</span></span> | <span data-ttu-id="712b1-187">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="712b1-187">Optional input</span></span> | <span data-ttu-id="712b1-188">4</span><span class="sxs-lookup"><span data-stu-id="712b1-188">4</span></span> | <span data-ttu-id="712b1-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="712b1-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="712b1-190">OutputTensor</span></span> | <span data-ttu-id="712b1-191">Saída</span><span class="sxs-lookup"><span data-stu-id="712b1-191">Output</span></span> | <span data-ttu-id="712b1-192">4</span><span class="sxs-lookup"><span data-stu-id="712b1-192">4</span></span> | <span data-ttu-id="712b1-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="712b1-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="712b1-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="712b1-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="712b1-195">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="712b1-195">**Header**</span></span> | <span data-ttu-id="712b1-196">directml.h</span><span class="sxs-lookup"><span data-stu-id="712b1-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="712b1-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="712b1-197">See also</span></span>

[<span data-ttu-id="712b1-198">Usando operadores mesclados para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="712b1-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)