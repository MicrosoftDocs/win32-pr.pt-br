---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcula o valor máximo entre os elementos dentro da janela deslizante sobre a entrada tensor e, opcionalmente, retorna os índices dos valores máximos selecionados.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416954"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a><span data-ttu-id="4f3bd-103">Estrutura de DML_MAX_POOLING2_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="4f3bd-103">DML_MAX_POOLING2_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="4f3bd-104">Calcula o valor máximo entre os elementos dentro da janela deslizante sobre a entrada tensor e, opcionalmente, retorna os índices dos valores máximos selecionados.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-104">Computes the maximum value across the elements within the sliding window over the input tensor, and optionally returns the indices of the maximum values selected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f3bd-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="4f3bd-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="4f3bd-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f3bd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f3bd-107">Syntax</span></span>
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a><span data-ttu-id="4f3bd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4f3bd-108">Members</span></span>

`InputTensor`

<span data-ttu-id="4f3bd-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4f3bd-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4f3bd-110">Um tensor de entrada de *tamanhos* `{ BatchCount, ChannelCount, Height, Width }` se *InputTensor. DimensionCount* for 4 e `{ BatchCount, ChannelCount, Depth, Height, Weight } ` se *InputTensor. DimensionCount* for 5.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-110">An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` if *InputTensor.DimensionCount* is 4, and `{ BatchCount, ChannelCount, Depth, Height, Weight } `if *InputTensor.DimensionCount* is 5.</span></span>


`OutputTensor`

<span data-ttu-id="4f3bd-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4f3bd-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4f3bd-112">Um tensor de saída para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-112">An output tensor to write the results to.</span></span> <span data-ttu-id="4f3bd-113">Os tamanhos do tensor de saída podem ser computados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-113">The sizes of the output tensor can be computed as follows.</span></span>

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

<span data-ttu-id="4f3bd-114">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="4f3bd-114">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="4f3bd-115">Um tensor de saída opcional de índices para a entrada tensor *InputTensor* dos valores máximos produzidos e armazenados no *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-115">An optional output tensor of indices to the input tensor *InputTensor* of the maximum values produced and stored in the *OutputTensor*.</span></span> <span data-ttu-id="4f3bd-116">Esses valores de índice são baseados em zero e tratam o tensor de entrada como uma matriz unidimensional contígua.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-116">These index values are zero-based and treat the input tensor as a contiguous one-dimensional array.</span></span> <span data-ttu-id="4f3bd-117">Quando vários elementos dentro da janela deslizante têm o mesmo valor, os valores iguais posteriores são ignorados e o índice aponta para o primeiro valor encontrado.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-117">When multiple elements within the sliding window have the same value, the later equal values are ignored and the index points to the first value encountered.</span></span> <span data-ttu-id="4f3bd-118">*OutputTensor* e *OutputIndicesTensor* têm os mesmos tamanhos de tensor.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-118">Both the *OutputTensor* and *OutputIndicesTensor* have the same tensor sizes.</span></span>


`DimensionCount`

<span data-ttu-id="4f3bd-119">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="4f3bd-119">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="4f3bd-120">O número de dimensões espaciais da entrada tensor *InputTensor*, que também corresponde ao número de dimensões da janela deslizante *WindowSize*.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-120">The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*.</span></span> <span data-ttu-id="4f3bd-121">Esse valor também determina o tamanho das matrizes de *Preenchentes* *,* *StartPadding* e endpadding.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-121">This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="4f3bd-122">Ele deve ser definido como 2 quando *InputTensor* for 4D e 3 quando for um 5D tensor.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-122">It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.</span></span>


`Strides`

<span data-ttu-id="4f3bd-123">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4f3bd-123">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4f3bd-124">Os avanços para as dimensões de janela deslizante de tamanhos `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-124">The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`WindowSize`

<span data-ttu-id="4f3bd-125">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4f3bd-125">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4f3bd-126">As dimensões da janela deslizante em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-126">The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`StartPadding`

<span data-ttu-id="4f3bd-127">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4f3bd-127">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4f3bd-128">O número de elementos de preenchimento a serem aplicados ao início de cada dimensão espacial da entrada tensor *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-128">The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="4f3bd-129">Os valores estão em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-129">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`EndPadding`

<span data-ttu-id="4f3bd-130">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4f3bd-130">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4f3bd-131">O número de elementos de preenchimento a serem aplicados ao final de cada dimensão espacial da entrada tensor *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-131">The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*.</span></span> <span data-ttu-id="4f3bd-132">Os valores estão em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-132">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


`Dilations`

<span data-ttu-id="4f3bd-133">Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) \* </b></span><span class="sxs-lookup"><span data-stu-id="4f3bd-133">Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)\*</b></span></span>

<span data-ttu-id="4f3bd-134">Os valores para cada dimensão espacial da entrada tensor *InputTensor* pelo qual um elemento dentro da janela deslizante é selecionado para cada elemento desse valor.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-134">The values for each spatial dimension of the input tensor *InputTensor* by which an element within the sliding window is selected for every elements of that value.</span></span> <span data-ttu-id="4f3bd-135">Os valores estão em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-135">The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.</span></span>


## <a name="remarks"></a><span data-ttu-id="4f3bd-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f3bd-136">Remarks</span></span>
<span data-ttu-id="4f3bd-137">**DML_MAX_POOLING2_OPERATOR_DESC** substitui a versão anterior [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) com uma matriz constante adicional *Dilations*.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-137">**DML_MAX_POOLING2_OPERATOR_DESC** supersedes the earlier version [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) with an additional constant array *Dilations*.</span></span> <span data-ttu-id="4f3bd-138">As duas versões são equivalentes quando *Dilations* é definido como `{ 1,1 }` para entrada 4D ou `{ 1,1,1 }` para os recursos de entrada de 5D.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-138">The two versions are equivalent when *Dilations* is set to `{ 1,1 }` for 4D input, or `{ 1,1,1 }` for 5D input features.</span></span>

## <a name="availability"></a><span data-ttu-id="4f3bd-139">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4f3bd-139">Availability</span></span>
<span data-ttu-id="4f3bd-140">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="4f3bd-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="4f3bd-141">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-141">Tensor constraints</span></span>
* <span data-ttu-id="4f3bd-142">*InputTensor*, *OutputIndicesTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-142">*InputTensor*, *OutputIndicesTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="4f3bd-143">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="4f3bd-143">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="4f3bd-144">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-144">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="4f3bd-145">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="4f3bd-145">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="4f3bd-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-146">Tensor</span></span> | <span data-ttu-id="4f3bd-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f3bd-147">Kind</span></span> | <span data-ttu-id="4f3bd-148">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="4f3bd-148">Supported dimension counts</span></span> | <span data-ttu-id="4f3bd-149">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="4f3bd-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4f3bd-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-150">InputTensor</span></span> | <span data-ttu-id="4f3bd-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3bd-151">Input</span></span> | <span data-ttu-id="4f3bd-152">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4f3bd-152">4 to 5</span></span> | <span data-ttu-id="4f3bd-153">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4f3bd-153">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="4f3bd-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-154">OutputTensor</span></span> | <span data-ttu-id="4f3bd-155">Saída</span><span class="sxs-lookup"><span data-stu-id="4f3bd-155">Output</span></span> | <span data-ttu-id="4f3bd-156">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4f3bd-156">4 to 5</span></span> | <span data-ttu-id="4f3bd-157">FLOAT32, FLOAT16, INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="4f3bd-157">FLOAT32, FLOAT16, INT8, UINT8</span></span> |
| <span data-ttu-id="4f3bd-158">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-158">OutputIndicesTensor</span></span> | <span data-ttu-id="4f3bd-159">Saída opcional</span><span class="sxs-lookup"><span data-stu-id="4f3bd-159">Optional output</span></span> | <span data-ttu-id="4f3bd-160">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4f3bd-160">4 to 5</span></span> | <span data-ttu-id="4f3bd-161">UINT32</span><span class="sxs-lookup"><span data-stu-id="4f3bd-161">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="4f3bd-162">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="4f3bd-162">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="4f3bd-163">Tensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-163">Tensor</span></span> | <span data-ttu-id="4f3bd-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="4f3bd-164">Kind</span></span> | <span data-ttu-id="4f3bd-165">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="4f3bd-165">Supported dimension counts</span></span> | <span data-ttu-id="4f3bd-166">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="4f3bd-166">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="4f3bd-167">InputTensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-167">InputTensor</span></span> | <span data-ttu-id="4f3bd-168">Entrada</span><span class="sxs-lookup"><span data-stu-id="4f3bd-168">Input</span></span> | <span data-ttu-id="4f3bd-169">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4f3bd-169">4 to 5</span></span> | <span data-ttu-id="4f3bd-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4f3bd-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4f3bd-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-171">OutputTensor</span></span> | <span data-ttu-id="4f3bd-172">Saída</span><span class="sxs-lookup"><span data-stu-id="4f3bd-172">Output</span></span> | <span data-ttu-id="4f3bd-173">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4f3bd-173">4 to 5</span></span> | <span data-ttu-id="4f3bd-174">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="4f3bd-174">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="4f3bd-175">OutputIndicesTensor</span><span class="sxs-lookup"><span data-stu-id="4f3bd-175">OutputIndicesTensor</span></span> | <span data-ttu-id="4f3bd-176">Saída opcional</span><span class="sxs-lookup"><span data-stu-id="4f3bd-176">Optional output</span></span> | <span data-ttu-id="4f3bd-177">4 a 5</span><span class="sxs-lookup"><span data-stu-id="4f3bd-177">4 to 5</span></span> | <span data-ttu-id="4f3bd-178">UINT32</span><span class="sxs-lookup"><span data-stu-id="4f3bd-178">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="4f3bd-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f3bd-179">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4f3bd-180">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="4f3bd-180">**Minimum supported client**</span></span> | <span data-ttu-id="4f3bd-181">Windows 10, versão 2004 (10,0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="4f3bd-181">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="4f3bd-182">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="4f3bd-182">**Minimum supported server**</span></span> | <span data-ttu-id="4f3bd-183">Windows Server, versão 2004 (10,0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="4f3bd-183">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="4f3bd-184">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="4f3bd-184">**Header**</span></span> | <span data-ttu-id="4f3bd-185">directml. h</span><span class="sxs-lookup"><span data-stu-id="4f3bd-185">directml.h</span></span> |