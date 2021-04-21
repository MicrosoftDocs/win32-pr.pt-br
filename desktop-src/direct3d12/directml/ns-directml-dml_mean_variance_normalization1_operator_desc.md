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
ms.openlocfilehash: 759bf25d4b6a97e70c6de7708a5c9fd0bccae439
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803394"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="5f2dc-104">Estrutura de DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5f2dc-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5f2dc-105">Executa uma função de normalização de variância média no tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="5f2dc-106">Esse operador calculará a média e a variação do tensor de entrada para executar a normalização.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="5f2dc-107">Esse operador executa a computação a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="5f2dc-108">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5f2dc-109">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5f2dc-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2dc-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f2dc-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="5f2dc-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5f2dc-111">Members</span></span>

`InputTensor`

<span data-ttu-id="5f2dc-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5f2dc-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5f2dc-113">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-113">A tensor containing the Input data.</span></span> <span data-ttu-id="5f2dc-114">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="5f2dc-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="5f2dc-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5f2dc-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5f2dc-116">Um tensor opcional que contém os dados de escala.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="5f2dc-117">Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5f2dc-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="5f2dc-118">As dimensões ScaleBatchCount, AlturaDaEscala e LarguraDaEscala devem corresponder a *InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="5f2dc-119">Se **DML_FEATURE_LEVEL** for maior ou igual a **DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e será difundida automaticamente para corresponder ao *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="5f2dc-120">Esse tensor será necessário se o *BiasTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="5f2dc-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5f2dc-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="5f2dc-122">Um tensor opcional que contém os dados de tendência.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="5f2dc-123">Se **DML_FEATURE_LEVEL** for menor que **DML_FEATURE_LEVEL_4_0**, as dimensões desse tensor deverão ser `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5f2dc-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="5f2dc-124">As dimensões BiasBatchCount, BiasHeight e BiasWidth devem corresponder a *InputTensor* ou ser definidas como 1 para transmitir automaticamente essas dimensões pela entrada.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="5f2dc-125">Se **DML_FEATURE_LEVEL** for maior ou igual a **DML_FEATURE_LEVEL_4_0**, qualquer dimensão poderá ser definida como 1 e será difundida automaticamente para corresponder ao *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="5f2dc-126">Esse tensor será necessário se o *ScaleTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="5f2dc-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5f2dc-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5f2dc-128">Um tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-128">A tensor to write the results to.</span></span> <span data-ttu-id="5f2dc-129">As dimensões de tensor são `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="5f2dc-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="5f2dc-130">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="5f2dc-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="5f2dc-131">O número de eixos.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-131">The number of axes.</span></span> <span data-ttu-id="5f2dc-132">Este campo determina o tamanho da matriz de *eixos* .</span><span class="sxs-lookup"><span data-stu-id="5f2dc-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="5f2dc-133">Tipo: \_ \_ tamanho \_ do campo (AxisCount) **const [uint](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5f2dc-133">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span> 

<span data-ttu-id="5f2dc-134">Os eixos ao longo do qual calcular a média e a variância.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="5f2dc-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="5f2dc-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="5f2dc-136">**True** se a camada de normalização incluir variância no cálculo de normalização.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="5f2dc-137">Caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="5f2dc-138">Se for **false**, a equação de normalização será `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="5f2dc-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="5f2dc-139">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="5f2dc-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="5f2dc-140">O valor de Épsilon a ser usado para evitar a divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="5f2dc-141">Um valor de 0, 1 é recomendado como padrão.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="5f2dc-142">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5f2dc-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="5f2dc-143">Uma camada de ativação com fusível opcional a ser aplicada após a normalização.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f2dc-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f2dc-144">Remarks</span></span>
<span data-ttu-id="5f2dc-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** é um superconjunto de funcionalidades do [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="5f2dc-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="5f2dc-146">Aqui, a definição da matriz de **eixos** como `{ 0, 2, 3 }` é o equivalente à definição de *CrossChannel* como **false** em **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; ao definir a matriz de **eixos** como `{ 1, 2, 3 }` equivalente à definição de *CrossChannel* como **true**.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="5f2dc-147">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="5f2dc-147">Availability</span></span>
<span data-ttu-id="5f2dc-148">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="5f2dc-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5f2dc-149">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-149">Tensor constraints</span></span>

<span data-ttu-id="5f2dc-150">*BiasTensor*, *InputTensor*, *OutputTensor* e *ScaleTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="5f2dc-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5f2dc-151">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="5f2dc-152">DML_FEATURE_LEVEL_3_1 e acima</span><span class="sxs-lookup"><span data-stu-id="5f2dc-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="5f2dc-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-153">Tensor</span></span> | <span data-ttu-id="5f2dc-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2dc-154">Kind</span></span> | <span data-ttu-id="5f2dc-155">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="5f2dc-155">Supported dimension counts</span></span> | <span data-ttu-id="5f2dc-156">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="5f2dc-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5f2dc-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-157">InputTensor</span></span> | <span data-ttu-id="5f2dc-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f2dc-158">Input</span></span> | <span data-ttu-id="5f2dc-159">1 a 8</span><span class="sxs-lookup"><span data-stu-id="5f2dc-159">1 to 8</span></span> | <span data-ttu-id="5f2dc-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5f2dc-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-161">ScaleTensor</span></span> | <span data-ttu-id="5f2dc-162">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5f2dc-162">Optional input</span></span> | <span data-ttu-id="5f2dc-163">1 a 8</span><span class="sxs-lookup"><span data-stu-id="5f2dc-163">1 to 8</span></span> | <span data-ttu-id="5f2dc-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5f2dc-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-165">BiasTensor</span></span> | <span data-ttu-id="5f2dc-166">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5f2dc-166">Optional input</span></span> | <span data-ttu-id="5f2dc-167">1 a 8</span><span class="sxs-lookup"><span data-stu-id="5f2dc-167">1 to 8</span></span> | <span data-ttu-id="5f2dc-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5f2dc-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-169">OutputTensor</span></span> | <span data-ttu-id="5f2dc-170">Saída</span><span class="sxs-lookup"><span data-stu-id="5f2dc-170">Output</span></span> | <span data-ttu-id="5f2dc-171">1 a 8</span><span class="sxs-lookup"><span data-stu-id="5f2dc-171">1 to 8</span></span> | <span data-ttu-id="5f2dc-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="5f2dc-173">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="5f2dc-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="5f2dc-174">Tensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-174">Tensor</span></span> | <span data-ttu-id="5f2dc-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f2dc-175">Kind</span></span> | <span data-ttu-id="5f2dc-176">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="5f2dc-176">Supported dimension counts</span></span> | <span data-ttu-id="5f2dc-177">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="5f2dc-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5f2dc-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-178">InputTensor</span></span> | <span data-ttu-id="5f2dc-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="5f2dc-179">Input</span></span> | <span data-ttu-id="5f2dc-180">4</span><span class="sxs-lookup"><span data-stu-id="5f2dc-180">4</span></span> | <span data-ttu-id="5f2dc-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5f2dc-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-182">ScaleTensor</span></span> | <span data-ttu-id="5f2dc-183">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5f2dc-183">Optional input</span></span> | <span data-ttu-id="5f2dc-184">4</span><span class="sxs-lookup"><span data-stu-id="5f2dc-184">4</span></span> | <span data-ttu-id="5f2dc-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5f2dc-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-186">BiasTensor</span></span> | <span data-ttu-id="5f2dc-187">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5f2dc-187">Optional input</span></span> | <span data-ttu-id="5f2dc-188">4</span><span class="sxs-lookup"><span data-stu-id="5f2dc-188">4</span></span> | <span data-ttu-id="5f2dc-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5f2dc-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5f2dc-190">OutputTensor</span></span> | <span data-ttu-id="5f2dc-191">Saída</span><span class="sxs-lookup"><span data-stu-id="5f2dc-191">Output</span></span> | <span data-ttu-id="5f2dc-192">4</span><span class="sxs-lookup"><span data-stu-id="5f2dc-192">4</span></span> | <span data-ttu-id="5f2dc-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5f2dc-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="5f2dc-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f2dc-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5f2dc-195">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="5f2dc-195">**Header**</span></span> | <span data-ttu-id="5f2dc-196">directml. h</span><span class="sxs-lookup"><span data-stu-id="5f2dc-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="5f2dc-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f2dc-197">See also</span></span>

[<span data-ttu-id="5f2dc-198">Usando operadores com fusível para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="5f2dc-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)
