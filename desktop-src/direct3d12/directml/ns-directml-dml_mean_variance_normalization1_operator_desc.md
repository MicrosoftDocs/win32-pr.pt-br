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
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105812140"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="cf65f-104">Estrutura de DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="cf65f-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="cf65f-105">Executa uma função de normalização de variância média no tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf65f-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="cf65f-106">Esse operador calculará a média e a variação do tensor de entrada para executar a normalização.</span><span class="sxs-lookup"><span data-stu-id="cf65f-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="cf65f-107">Esse operador executa a computação a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf65f-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="cf65f-108">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="cf65f-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="cf65f-109">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="cf65f-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf65f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf65f-110">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="cf65f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="cf65f-111">Members</span></span>

`InputTensor`

<span data-ttu-id="cf65f-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf65f-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cf65f-113">Um tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf65f-113">A tensor containing the Input data.</span></span> <span data-ttu-id="cf65f-114">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cf65f-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`ScaleTensor`

<span data-ttu-id="cf65f-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf65f-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cf65f-116">Um tensor opcional que contém os dados de escala.</span><span class="sxs-lookup"><span data-stu-id="cf65f-116">An optional tensor containing the Scale data.</span></span> <span data-ttu-id="cf65f-117">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cf65f-117">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="cf65f-118">Qualquer dimensão pode ser substituída por 1 para difundir nessa dimensão.</span><span class="sxs-lookup"><span data-stu-id="cf65f-118">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="cf65f-119">Esse tensor será necessário se o *BiasTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="cf65f-119">This tensor is required if the *BiasTensor* is used.</span></span>


`BiasTensor`

<span data-ttu-id="cf65f-120">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf65f-120">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cf65f-121">Um tensor opcional que contém os dados de tendência.</span><span class="sxs-lookup"><span data-stu-id="cf65f-121">An optional tensor containing the bias data.</span></span> <span data-ttu-id="cf65f-122">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cf65f-122">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="cf65f-123">Qualquer dimensão pode ser substituída por 1 para difundir nessa dimensão.</span><span class="sxs-lookup"><span data-stu-id="cf65f-123">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="cf65f-124">Esse tensor será necessário se o *ScaleTensor* for usado.</span><span class="sxs-lookup"><span data-stu-id="cf65f-124">This tensor is required if the *ScaleTensor* is used.</span></span>


`OutputTensor`

<span data-ttu-id="cf65f-125">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf65f-125">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cf65f-126">Um tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="cf65f-126">A tensor to write the results to.</span></span> <span data-ttu-id="cf65f-127">As dimensões de tensor são `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="cf65f-127">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`AxisCount`

<span data-ttu-id="cf65f-128">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="cf65f-128">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="cf65f-129">O número de eixos.</span><span class="sxs-lookup"><span data-stu-id="cf65f-129">The number of axes.</span></span> <span data-ttu-id="cf65f-130">Este campo determina o tamanho da matriz de *eixos* .</span><span class="sxs-lookup"><span data-stu-id="cf65f-130">This field determines the size of the *Axes* array.</span></span>


`Axes`

<span data-ttu-id="cf65f-131">Tipo: \_ \_ tamanho \_ do campo (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="cf65f-131">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span> 

<span data-ttu-id="cf65f-132">Os eixos ao longo do qual calcular a média e a variância.</span><span class="sxs-lookup"><span data-stu-id="cf65f-132">The axes along which to calculate the Mean and Variance.</span></span>


`NormalizeVariance`

<span data-ttu-id="cf65f-133">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="cf65f-133">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="cf65f-134">**True** se a camada de normalização incluir variância no cálculo de normalização.</span><span class="sxs-lookup"><span data-stu-id="cf65f-134">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="cf65f-135">Caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="cf65f-135">Otherwise, **FALSE**.</span></span> <span data-ttu-id="cf65f-136">Se for **false**, a equação de normalização será `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="cf65f-136">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>


`Epsilon`

<span data-ttu-id="cf65f-137">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="cf65f-137">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="cf65f-138">O valor de Épsilon a ser usado para evitar a divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="cf65f-138">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="cf65f-139">Um valor de 0, 1 é recomendado como padrão.</span><span class="sxs-lookup"><span data-stu-id="cf65f-139">A value of 0.00001 is recommended as default.</span></span>


`FusedActivation`

<span data-ttu-id="cf65f-140">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cf65f-140">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="cf65f-141">Uma camada de ativação com fusível opcional a ser aplicada após a normalização.</span><span class="sxs-lookup"><span data-stu-id="cf65f-141">An optional fused activation layer to apply after the normalization.</span></span>


## <a name="remarks"></a><span data-ttu-id="cf65f-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf65f-142">Remarks</span></span>
<span data-ttu-id="cf65f-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** é um superconjunto de funcionalidades do [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="cf65f-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="cf65f-144">Aqui, a definição da matriz de **eixos** como `{ 0, 2, 3 }` é o equivalente à definição de *CrossChannel* como **false** em **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; ao definir a matriz de **eixos** como `{ 1, 2, 3 }` equivalente à definição de *CrossChannel* como **true**.</span><span class="sxs-lookup"><span data-stu-id="cf65f-144">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="cf65f-145">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="cf65f-145">Availability</span></span>
<span data-ttu-id="cf65f-146">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="cf65f-146">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cf65f-147">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="cf65f-147">Tensor constraints</span></span>
* <span data-ttu-id="cf65f-148">*InputTensor* e *OutputTensor* devem ter os mesmos *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="cf65f-148">*InputTensor* and *OutputTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="cf65f-149">*BiasTensor*, *InputTensor*, *OutputTensor* e *ScaleTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="cf65f-149">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cf65f-150">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="cf65f-150">Tensor support</span></span>
| <span data-ttu-id="cf65f-151">Tensor</span><span class="sxs-lookup"><span data-stu-id="cf65f-151">Tensor</span></span> | <span data-ttu-id="cf65f-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf65f-152">Kind</span></span> | <span data-ttu-id="cf65f-153">Dimensões</span><span class="sxs-lookup"><span data-stu-id="cf65f-153">Dimensions</span></span> | <span data-ttu-id="cf65f-154">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="cf65f-154">Supported dimension counts</span></span> | <span data-ttu-id="cf65f-155">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="cf65f-155">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="cf65f-156">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cf65f-156">InputTensor</span></span> | <span data-ttu-id="cf65f-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="cf65f-157">Input</span></span> | <span data-ttu-id="cf65f-158">{BatchCount, ChannelCount, altura, largura}</span><span class="sxs-lookup"><span data-stu-id="cf65f-158">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="cf65f-159">4</span><span class="sxs-lookup"><span data-stu-id="cf65f-159">4</span></span> | <span data-ttu-id="cf65f-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cf65f-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cf65f-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="cf65f-161">ScaleTensor</span></span> | <span data-ttu-id="cf65f-162">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="cf65f-162">Optional input</span></span> | <span data-ttu-id="cf65f-163">{ScaleBatchCount, ScaleChannelCount, AlturaDaEscala, LarguraDaEscala}</span><span class="sxs-lookup"><span data-stu-id="cf65f-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span></span> | <span data-ttu-id="cf65f-164">4</span><span class="sxs-lookup"><span data-stu-id="cf65f-164">4</span></span> | <span data-ttu-id="cf65f-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cf65f-165">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cf65f-166">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="cf65f-166">BiasTensor</span></span> | <span data-ttu-id="cf65f-167">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="cf65f-167">Optional input</span></span> | <span data-ttu-id="cf65f-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span><span class="sxs-lookup"><span data-stu-id="cf65f-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span></span> | <span data-ttu-id="cf65f-169">4</span><span class="sxs-lookup"><span data-stu-id="cf65f-169">4</span></span> | <span data-ttu-id="cf65f-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cf65f-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="cf65f-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cf65f-171">OutputTensor</span></span> | <span data-ttu-id="cf65f-172">Saída</span><span class="sxs-lookup"><span data-stu-id="cf65f-172">Output</span></span> | <span data-ttu-id="cf65f-173">{BatchCount, ChannelCount, altura, largura}</span><span class="sxs-lookup"><span data-stu-id="cf65f-173">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="cf65f-174">4</span><span class="sxs-lookup"><span data-stu-id="cf65f-174">4</span></span> | <span data-ttu-id="cf65f-175">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cf65f-175">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="cf65f-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf65f-176">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cf65f-177">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="cf65f-177">**Header**</span></span> | <span data-ttu-id="cf65f-178">directml. h</span><span class="sxs-lookup"><span data-stu-id="cf65f-178">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="cf65f-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf65f-179">See also</span></span>

[<span data-ttu-id="cf65f-180">Usando operadores com fusível para melhorar o desempenho</span><span class="sxs-lookup"><span data-stu-id="cf65f-180">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)