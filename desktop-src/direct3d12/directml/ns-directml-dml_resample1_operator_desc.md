---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Reamostrar elementos da origem para o tensor de destino, usando os fatores de escala para calcular o tamanho do tensor de destino. Você pode usar um modo de interpolação de vizinho mais próximo ou linear.
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 669e828c4d8376e081ef6638aba4a13d517afd88
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105794641"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a><span data-ttu-id="653c2-104">Estrutura de DML_RESAMPLE1_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="653c2-104">DML_RESAMPLE1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="653c2-105">Reamostrar elementos da origem para o tensor de destino, usando os fatores de escala para calcular o tamanho do tensor de destino.</span><span class="sxs-lookup"><span data-stu-id="653c2-105">Resamples elements from the source to the destination tensor, using the scale factors to compute the destination tensor size.</span></span> <span data-ttu-id="653c2-106">Você pode usar um modo de interpolação de vizinho mais próximo ou linear.</span><span class="sxs-lookup"><span data-stu-id="653c2-106">You can use a linear or nearest-neighbor interpolation mode.</span></span> <span data-ttu-id="653c2-107">O operador dá suporte à interpolação em várias dimensões, não apenas em 2D.</span><span class="sxs-lookup"><span data-stu-id="653c2-107">The operator supports interpolation across multiple dimensions, not just 2D.</span></span> <span data-ttu-id="653c2-108">Portanto, você pode manter o mesmo tamanho espacial, mas interpolar entre canais ou em lotes.</span><span class="sxs-lookup"><span data-stu-id="653c2-108">So you can keep the same spatial size, but interpolate across channels or across batches.</span></span> <span data-ttu-id="653c2-109">A relação entre as coordenadas de entrada e saída é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="653c2-109">The relationship between the input and output coordinates is the following.</span></span>

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> <span data-ttu-id="653c2-110">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="653c2-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="653c2-111">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="653c2-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="653c2-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="653c2-112">Syntax</span></span>
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a><span data-ttu-id="653c2-113">Membros</span><span class="sxs-lookup"><span data-stu-id="653c2-113">Members</span></span>

`InputTensor`

<span data-ttu-id="653c2-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="653c2-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="653c2-115">O tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="653c2-115">The tensor containing the input data.</span></span>


`OutputTensor`

<span data-ttu-id="653c2-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="653c2-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="653c2-117">O tensor para gravar os dados de saída.</span><span class="sxs-lookup"><span data-stu-id="653c2-117">The tensor to write the output data to.</span></span>


`InterpolationMode`

<span data-ttu-id="653c2-118">Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span><span class="sxs-lookup"><span data-stu-id="653c2-118">Type: [**DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)</span></span>

<span data-ttu-id="653c2-119">Este campo determina o tipo de interpolação usado para escolher pixels de saída.</span><span class="sxs-lookup"><span data-stu-id="653c2-119">This field determines the kind of interpolation used to choose output pixels.</span></span>

- <span data-ttu-id="653c2-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span><span class="sxs-lookup"><span data-stu-id="653c2-120">**DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**.</span></span> <span data-ttu-id="653c2-121">Usa o algoritmo de *vizinho mais próximo* , que escolhe o elemento de entrada mais próximo ao pixel Center correspondente para cada elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="653c2-121">Uses the *Nearest Neighbor* algorithm, which chooses the input element nearest to the corresponding pixel center for each output element.</span></span>

- <span data-ttu-id="653c2-122">**DML_INTERPOLATION_MODE_LINEAR**.</span><span class="sxs-lookup"><span data-stu-id="653c2-122">**DML_INTERPOLATION_MODE_LINEAR**.</span></span> <span data-ttu-id="653c2-123">Usa o algoritmo *Quadrilinear* , que computa o elemento Output, fazendo a média ponderada dos 2 elementos de entrada vizinhos mais próximos por dimensão.</span><span class="sxs-lookup"><span data-stu-id="653c2-123">Uses the *Quadrilinear* algorithm, which computes the output element by doing the weighted average of the 2 nearest neighboring input elements per dimension.</span></span> <span data-ttu-id="653c2-124">Como todas as quatro dimensões podem ser reamostradas, a média ponderada é calculada em um total de 16 elementos de entrada para cada elemento de saída.</span><span class="sxs-lookup"><span data-stu-id="653c2-124">Since all 4 dimensions can be resampled, the weighted average is computed on a total of 16 input elements for each output element.</span></span>


`DimensionCount`

<span data-ttu-id="653c2-125">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="653c2-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="653c2-126">O número de valores nas matrizes que *dimensionam*, *InputPixelOffsets* e *OutputPixelOffsets* apontam para.</span><span class="sxs-lookup"><span data-stu-id="653c2-126">The number of values in the arrays that *Scales*, *InputPixelOffsets*, and *OutputPixelOffsets* point to.</span></span> <span data-ttu-id="653c2-127">Esse valor deve corresponder à contagem de dimensões de *InputTensor* e *OutputTensor*, que deve ser 4.</span><span class="sxs-lookup"><span data-stu-id="653c2-127">This value must match the dimension count of *InputTensor* and *OutputTensor*, which has to be 4.</span></span>


`Scales`

<span data-ttu-id="653c2-128">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="653c2-128">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="653c2-129">As escalas a serem aplicadas ao reamostrar a entrada, em que dimensiona > 1 escalar verticalmente a imagem e escalas < 1 reduzir verticalmente a imagem para essa dimensão.</span><span class="sxs-lookup"><span data-stu-id="653c2-129">The scales to apply when resampling the input, where scales > 1 scale up the image and scales < 1 scale down the image for that dimension.</span></span> <span data-ttu-id="653c2-130">Observe que as escalas não precisam ser exatamente `OutputSize / InputSize` .</span><span class="sxs-lookup"><span data-stu-id="653c2-130">Note that the scales don't need to be exactly `OutputSize / InputSize`.</span></span> <span data-ttu-id="653c2-131">Se a entrada após o dimensionamento for maior que o limite de saída, então, vamos cortá-lo para o tamanho de saída.</span><span class="sxs-lookup"><span data-stu-id="653c2-131">If the input after scaling is larger than the output bound, then we crop it to the output size.</span></span> <span data-ttu-id="653c2-132">Por outro lado, se a entrada após o dimensionamento for menor do que a saída associada, as bordas de saída serão clamped.</span><span class="sxs-lookup"><span data-stu-id="653c2-132">On the other hand, if the input after scaling is smaller than the output bound, the output edges are clamped.</span></span>


`InputPixelOffsets`

<span data-ttu-id="653c2-133">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="653c2-133">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="653c2-134">Os deslocamentos a serem aplicados aos pixels de entrada antes da reamostragem.</span><span class="sxs-lookup"><span data-stu-id="653c2-134">The offsets to apply to the input pixels before resampling.</span></span> <span data-ttu-id="653c2-135">Quando esse valor é `0` , o canto superior esquerdo do pixel é usado em vez de seu centro, o que normalmente não dará o resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="653c2-135">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="653c2-136">Para reamostrar a imagem usando o centro dos pixels e para obter o mesmo comportamento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), esse valor deve ser `0.5` .</span><span class="sxs-lookup"><span data-stu-id="653c2-136">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `0.5`.</span></span>


`OutputPixelOffsets`

<span data-ttu-id="653c2-137">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="653c2-137">Type: \_Field\_size\_(DimensionCount) **const [FLOAT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="653c2-138">Os deslocamentos a serem aplicados aos pixels de saída após a reamostragem.</span><span class="sxs-lookup"><span data-stu-id="653c2-138">The offsets to apply to the output pixels after resampling.</span></span> <span data-ttu-id="653c2-139">Quando esse valor é `0` , o canto superior esquerdo do pixel é usado em vez de seu centro, o que normalmente não dará o resultado esperado.</span><span class="sxs-lookup"><span data-stu-id="653c2-139">When this value is `0`, the top left corner of the pixel is used instead of its center, which usually won't give the expected result.</span></span> <span data-ttu-id="653c2-140">Para reamostrar a imagem usando o centro dos pixels e para obter o mesmo comportamento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), esse valor deve ser `-0.5` .</span><span class="sxs-lookup"><span data-stu-id="653c2-140">To resample the image by using the center of the pixels and to get the same behavior as [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), this value must be `-0.5`.</span></span>


## <a name="remarks"></a><span data-ttu-id="653c2-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="653c2-141">Remarks</span></span>
<span data-ttu-id="653c2-142">Quando *InputPixelOffsets* são definidos como 0,5 e *OutputPixelOffsets* são definidos como-0,5, esse operador é equivalente a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="653c2-142">When the *InputPixelOffsets* are set to 0.5, and the *OutputPixelOffsets* are set to -0.5, this operator is equivalent to [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="653c2-143">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="653c2-143">Availability</span></span>
<span data-ttu-id="653c2-144">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="653c2-144">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="653c2-145">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="653c2-145">Tensor constraints</span></span>
<span data-ttu-id="653c2-146">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="653c2-146">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="653c2-147">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="653c2-147">Tensor support</span></span>
| <span data-ttu-id="653c2-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="653c2-148">Tensor</span></span> | <span data-ttu-id="653c2-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="653c2-149">Kind</span></span> | <span data-ttu-id="653c2-150">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="653c2-150">Supported dimension counts</span></span> | <span data-ttu-id="653c2-151">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="653c2-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="653c2-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="653c2-152">InputTensor</span></span> | <span data-ttu-id="653c2-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="653c2-153">Input</span></span> | <span data-ttu-id="653c2-154">4</span><span class="sxs-lookup"><span data-stu-id="653c2-154">4</span></span> | <span data-ttu-id="653c2-155">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="653c2-155">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="653c2-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="653c2-156">OutputTensor</span></span> | <span data-ttu-id="653c2-157">Saída</span><span class="sxs-lookup"><span data-stu-id="653c2-157">Output</span></span> | <span data-ttu-id="653c2-158">4</span><span class="sxs-lookup"><span data-stu-id="653c2-158">4</span></span> | <span data-ttu-id="653c2-159">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="653c2-159">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="653c2-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="653c2-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="653c2-161">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="653c2-161">**Header**</span></span> | <span data-ttu-id="653c2-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="653c2-162">directml.h</span></span> |