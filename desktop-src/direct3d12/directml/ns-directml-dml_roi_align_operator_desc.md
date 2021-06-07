---
UID: NS:directml.DML_ROI_ALIGN_OPERATOR_DESC
title: DML_ROI_ALIGN_OPERATOR_DESC
description: Executa uma operação de alinhamento de ROI, conforme descrito no [papel de máscara R-CNN](https://arxiv.org/abs/1703.06870). Em suma, a operação extrai aparas da imagem de entrada tensor e as redimensiona para um tamanho de saída comum especificado pelas duas últimas dimensões de *OutputTensor* usando o *interpolamode* especificado.
helpviewer_keywords:
- DML_ROI_ALIGN_OPERATOR_DESC
- DML_ROI_ALIGN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ROI_ALIGN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ROI_ALIGN_OPERATOR_DESC, DML_ROI_ALIGN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
- directml/DML_ROI_ALIGN_OPERATOR_DESC
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
- DML_ROI_ALIGN_OPERATOR_DESC
ms.openlocfilehash: b9004a77d3b325dd3394d1a3a6b596e94997e9fd
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416937"
---
# <a name="dml_roi_align_operator_desc-structure-directmlh"></a><span data-ttu-id="44fda-104">Estrutura de DML_ROI_ALIGN_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="44fda-104">DML_ROI_ALIGN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="44fda-105">Executa uma operação de alinhamento de ROI, conforme descrito no [papel de máscara R-CNN](https://arxiv.org/abs/1703.06870).</span><span class="sxs-lookup"><span data-stu-id="44fda-105">Performs an ROI Align operation, as described in the [Mask R-CNN paper](https://arxiv.org/abs/1703.06870).</span></span> <span data-ttu-id="44fda-106">Em suma, a operação extrai aparas da imagem de entrada tensor e as redimensiona para um tamanho de saída comum especificado pelas duas últimas dimensões de *OutputTensor* usando o *interpolamode* especificado.</span><span class="sxs-lookup"><span data-stu-id="44fda-106">In summary, the operation extracts crops from the input image tensor and resizes them to a common output size specified by the last 2 dimensions of *OutputTensor* using the specified *InterpolationMode*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44fda-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="44fda-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="44fda-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="44fda-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="44fda-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44fda-109">Syntax</span></span>

```cpp
struct DML_ROI_ALIGN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* ROITensor;
  const DML_TENSOR_DESC* BatchIndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  DML_REDUCE_FUNCTION ReductionFunction;
  DML_INTERPOLATION_MODE InterpolationMode;
  FLOAT SpatialScaleX;
  FLOAT SpatialScaleY;
  FLOAT OutOfBoundsInputValue;
  UINT MinimumSamplesPerOutput;
  UINT MaximumSamplesPerOutput;
};
```

## <a name="members"></a><span data-ttu-id="44fda-110">Membros</span><span class="sxs-lookup"><span data-stu-id="44fda-110">Members</span></span>

`InputTensor`

<span data-ttu-id="44fda-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44fda-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44fda-112">Um tensor que contém os dados de entrada com dimensões `{ BatchCount, ChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="44fda-112">A tensor containing the input data with dimensions `{ BatchCount, ChannelCount, InputHeight, InputWidth }`.</span></span>

`ROITensor`

<span data-ttu-id="44fda-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44fda-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44fda-114">Um tensor que contém os dados de ROI (regiões de interesse).</span><span class="sxs-lookup"><span data-stu-id="44fda-114">A tensor containing the regions of interest (ROI) data.</span></span> <span data-ttu-id="44fda-115">As dimensões permitidas do `ROITensor` são `{ NumROIs, 4 }` , `{ 1, NumROIs, 4 }` , ou `{ 1, 1, NumROIs, 4 }` .</span><span class="sxs-lookup"><span data-stu-id="44fda-115">The allowed dimensions of `ROITensor` are `{ NumROIs, 4 }`, `{ 1, NumROIs, 4 }`, or `{ 1, 1, NumROIs, 4 }`.</span></span> <span data-ttu-id="44fda-116">Para cada ROI, os valores serão as coordenadas de seus cantos superior esquerdo e inferior direito na ordem `[x1, y1, x2, y2]` .</span><span class="sxs-lookup"><span data-stu-id="44fda-116">For each ROI, the values will be the coordinates of its top-left and bottom-right corners in the order `[x1, y1, x2, y2]`.</span></span>

`BatchIndicesTensor`

<span data-ttu-id="44fda-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44fda-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44fda-118">Um tensor que contém os índices de lote para extrair o ROIs.</span><span class="sxs-lookup"><span data-stu-id="44fda-118">A tensor containing the batch indices to extract the ROIs from.</span></span> <span data-ttu-id="44fda-119">As dimensões permitidas `BatchIndicesTensor` são `{ NumROIs }` , `{ 1, NumROIs }` , `{ 1, 1, NumROIs }` ou `{ 1, 1, 1, NumROIs }` .</span><span class="sxs-lookup"><span data-stu-id="44fda-119">The allowed dimensions of `BatchIndicesTensor` are `{ NumROIs }`, `{ 1, NumROIs }`, `{ 1, 1, NumROIs }`, or `{ 1, 1, 1, NumROIs }`.</span></span> <span data-ttu-id="44fda-120">Cada valor é o índice de um lote de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="44fda-120">Each value is the index of a batch from *InputTensor*.</span></span> <span data-ttu-id="44fda-121">O comportamento será indefinido se os valores não estiverem no intervalo [0, BatchCount).</span><span class="sxs-lookup"><span data-stu-id="44fda-121">The behavior is undefined if the values are not in the range [0, BatchCount).</span></span>

`OutputTensor`

<span data-ttu-id="44fda-122">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="44fda-122">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="44fda-123">Um tensor que contém os dados de saída.</span><span class="sxs-lookup"><span data-stu-id="44fda-123">A tensor containing the output data.</span></span> <span data-ttu-id="44fda-124">As dimensões esperadas de *OutputTensor* são `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="44fda-124">The expected dimensions of *OutputTensor* are `{ NumROIs, ChannelCount, OutputHeight, OutputWidth }`.</span></span>

`ReductionFunction`

<span data-ttu-id="44fda-125">Tipo: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span><span class="sxs-lookup"><span data-stu-id="44fda-125">Type: **[DML_REDUCE_FUNCTION](/windows/win32/api/directml/ne-directml-dml_reduce_function)**</span></span>

<span data-ttu-id="44fda-126">A função de redução a ser usada ao reduzir em todos os exemplos de entrada que contribuem para um elemento de saída ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) ou **DML_REDUCE_FUNCTION_MAX**).</span><span class="sxs-lookup"><span data-stu-id="44fda-126">The reduction function to use when reducing across all input samples that contribute to an output element ([DML_REDUCE_FUNCTION_AVERAGE](/windows/win32/api/directml/ne-directml-dml_reduce_function) or **DML_REDUCE_FUNCTION_MAX**).</span></span> <span data-ttu-id="44fda-127">O número de amostras de entrada para reduzir em é limitado por *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="44fda-127">The number of input samples to reduce across is bounded by *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`InterpolationMode`

<span data-ttu-id="44fda-128">Tipo: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span><span class="sxs-lookup"><span data-stu-id="44fda-128">Type: **[DML_INTERPOLATION_MODE](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)**</span></span>

<span data-ttu-id="44fda-129">O modo de interpolação a ser usado ao redimensionar as regiões.</span><span class="sxs-lookup"><span data-stu-id="44fda-129">The interpolation mode to use when resizing the regions.</span></span>

- <span data-ttu-id="44fda-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span><span class="sxs-lookup"><span data-stu-id="44fda-130">[DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/win32/api/directml/ne-directml-dml_interpolation_mode).</span></span> <span data-ttu-id="44fda-131">Usa o algoritmo de *vizinho mais próximo* , que escolhe o elemento de entrada mais próximo ao pixel Center correspondente para cada elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="44fda-131">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>
- <span data-ttu-id="44fda-132">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="44fda-132">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="44fda-133">Usa o algoritmo *biline* , que computa o elemento Output, fazendo a média ponderada dos 2 elementos de entrada vizinhos mais próximos por dimensão.</span><span class="sxs-lookup"><span data-stu-id="44fda-133">Uses the *Bilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="44fda-134">Como apenas 2 dimensões são redimensionadas, a média ponderada é calculada em um total de 4 elementos de entrada para cada elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="44fda-134">Since only 2 dimensions are resized, the weighted average is computed on a total of 4 input elements for each output element.</span></span>

`SpatialScaleX`

<span data-ttu-id="44fda-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="44fda-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="44fda-136">O componente X (ou largura) do fator de dimensionamento para multiplicar as coordenadas *ROITensor* por a fim de torná-las proporcionais a *InputHeight* e *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="44fda-136">The X (or width) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="44fda-137">Por exemplo, se *ROITensor* contiver coordenadas normalizadas (valores no intervalo [0.. 1]), *SpatialScaleX* normalmente teria o mesmo valor que *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="44fda-137">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), then *SpatialScaleX* would usually have the same value as *InputWidth*.</span></span>

`SpatialScaleY`

<span data-ttu-id="44fda-138">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="44fda-138">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="44fda-139">O componente Y (ou Height) do fator de dimensionamento para multiplicar as coordenadas *ROITensor* por a fim de torná-las proporcionais a *InputHeight* e *InputWidth*.</span><span class="sxs-lookup"><span data-stu-id="44fda-139">The Y (or height) component of the scaling factor to multiply the *ROITensor* coordinates by in order to make them proportionate to *InputHeight* and *InputWidth*.</span></span> <span data-ttu-id="44fda-140">Por exemplo, se *ROITensor* contiver coordenadas normalizadas (valores no intervalo [0.. 1]), *SpatialScaleY* normalmente teria o mesmo valor que *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="44fda-140">For example, if *ROITensor* contains normalized coordinates (values in the range [0..1]), *SpatialScaleY* would usually have the same value as *InputHeight*.</span></span>

`OutOfBoundsInputValue`

<span data-ttu-id="44fda-141">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="44fda-141">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="44fda-142">O valor a ser lido de *InputTensor* quando Rois estão fora dos limites de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="44fda-142">The value to read from *InputTensor* when the ROIs are outside the bounds of *InputTensor*.</span></span> <span data-ttu-id="44fda-143">Isso pode acontecer quando os valores obtidos após o dimensionamento de *ROITensor* por *SpatialScaleX* e *SpatialScaleY* são maiores que *InputWidth* e *InputHeight*.</span><span class="sxs-lookup"><span data-stu-id="44fda-143">This can happen when the values obtained after scaling *ROITensor* by *SpatialScaleX* and *SpatialScaleY* are bigger than *InputWidth* and *InputHeight*.</span></span>

`MinimumSamplesPerOutput`

<span data-ttu-id="44fda-144">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="44fda-144">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="44fda-145">O número mínimo de amostras de entrada a serem usadas para cada elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="44fda-145">The minimum number of input samples to use for every output element.</span></span> <span data-ttu-id="44fda-146">O operador calculará o número de exemplos de entrada fazendo `ScaledCropSize / OutputSize` e, em seguida, fixe-o para *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="44fda-146">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

`MaximumSamplesPerOutput`

<span data-ttu-id="44fda-147">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="44fda-147">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="44fda-148">O número máximo de amostras de entrada a serem usadas para cada elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="44fda-148">The maximum number of input samples to use for every output element.</span></span> <span data-ttu-id="44fda-149">O operador calculará o número de exemplos de entrada fazendo `ScaledCropSize / OutputSize` e, em seguida, fixe-o para *MinimumSamplesPerOutput* e *MaximumSamplesPerOutput*.</span><span class="sxs-lookup"><span data-stu-id="44fda-149">The operator will calculate the number of input samples by doing `ScaledCropSize / OutputSize`, and then clamp it to *MinimumSamplesPerOutput* and *MaximumSamplesPerOutput*.</span></span>

## <a name="availability"></a><span data-ttu-id="44fda-150">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="44fda-150">Availability</span></span>
<span data-ttu-id="44fda-151">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="44fda-151">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="44fda-152">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="44fda-152">Tensor constraints</span></span>
<span data-ttu-id="44fda-153">*InputTensor*, *OutputTensor* e *ROITensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="44fda-153">*InputTensor*, *OutputTensor*, and *ROITensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="44fda-154">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="44fda-154">Tensor support</span></span>
| <span data-ttu-id="44fda-155">Tensor</span><span class="sxs-lookup"><span data-stu-id="44fda-155">Tensor</span></span> | <span data-ttu-id="44fda-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="44fda-156">Kind</span></span> | <span data-ttu-id="44fda-157">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="44fda-157">Supported dimension counts</span></span> | <span data-ttu-id="44fda-158">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="44fda-158">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="44fda-159">InputTensor</span><span class="sxs-lookup"><span data-stu-id="44fda-159">InputTensor</span></span> | <span data-ttu-id="44fda-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="44fda-160">Input</span></span> | <span data-ttu-id="44fda-161">4</span><span class="sxs-lookup"><span data-stu-id="44fda-161">4</span></span> | <span data-ttu-id="44fda-162">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="44fda-162">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="44fda-163">ROITensor</span><span class="sxs-lookup"><span data-stu-id="44fda-163">ROITensor</span></span> | <span data-ttu-id="44fda-164">Entrada</span><span class="sxs-lookup"><span data-stu-id="44fda-164">Input</span></span> | <span data-ttu-id="44fda-165">2 a 4</span><span class="sxs-lookup"><span data-stu-id="44fda-165">2 to 4</span></span> | <span data-ttu-id="44fda-166">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="44fda-166">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="44fda-167">BatchIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="44fda-167">BatchIndicesTensor</span></span> | <span data-ttu-id="44fda-168">Entrada</span><span class="sxs-lookup"><span data-stu-id="44fda-168">Input</span></span> | <span data-ttu-id="44fda-169">1 a 4</span><span class="sxs-lookup"><span data-stu-id="44fda-169">1 to 4</span></span> | <span data-ttu-id="44fda-170">UINT32</span><span class="sxs-lookup"><span data-stu-id="44fda-170">UINT32</span></span> |
| <span data-ttu-id="44fda-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="44fda-171">OutputTensor</span></span> | <span data-ttu-id="44fda-172">Saída</span><span class="sxs-lookup"><span data-stu-id="44fda-172">Output</span></span> | <span data-ttu-id="44fda-173">4</span><span class="sxs-lookup"><span data-stu-id="44fda-173">4</span></span> | <span data-ttu-id="44fda-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="44fda-174">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="44fda-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44fda-175">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="44fda-176">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="44fda-176">**Header**</span></span> | <span data-ttu-id="44fda-177">directml. h</span><span class="sxs-lookup"><span data-stu-id="44fda-177">directml.h</span></span> |