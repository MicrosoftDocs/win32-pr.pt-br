---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Coleta elementos do tensor de entrada ao longo do eixo fornecido usando os índices tensor para remapear para a entrada.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 89a4f2017f6adec8cce206e9261eb0fa6563e94c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803019"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="8d5cf-103">Estrutura de DML_GATHER_ELEMENTS_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="8d5cf-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="8d5cf-104">Coleta elementos do tensor de entrada ao longo do eixo fornecido usando os índices tensor para remapear para a entrada.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="8d5cf-105">Esse operador executa o pseudocódigo a seguir, com o comportamento exato dependente do eixo, a contagem de dimensões de entrada e a contagem de dimensões de índices.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="8d5cf-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="8d5cf-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="8d5cf-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d5cf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d5cf-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="8d5cf-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8d5cf-109">Members</span></span>

`InputTensor`

<span data-ttu-id="8d5cf-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8d5cf-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8d5cf-111">O tensor do qual ler.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="8d5cf-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8d5cf-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8d5cf-113">Os índices no tensor de entrada ao longo do eixo ativo.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="8d5cf-114">Os *tamanhos* devem corresponder a *InputTensor. Sizes* para cada dimensão, exceto *Axis*.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="8d5cf-115">A partir do `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral assinado com este tensor.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="8d5cf-116">Os índices negativos são interpretados como sendo relativos ao final da dimensão do eixo.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="8d5cf-117">Por exemplo, um índice de-1 se refere ao último elemento ao longo dessa dimensão.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="8d5cf-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="8d5cf-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="8d5cf-119">O tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-119">The tensor to write the results to.</span></span> <span data-ttu-id="8d5cf-120">Os *tamanhos* devem corresponder a *IndicesTensor. Sizes* e *DataType* deve corresponder a *InputTensor. DataType*.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="8d5cf-121">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="8d5cf-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="8d5cf-122">A dimensão do eixo de *InputTensor* a ser coletada, variando `[0, *InputTensor.DimensionCount*)` .</span><span class="sxs-lookup"><span data-stu-id="8d5cf-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="8d5cf-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d5cf-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="8d5cf-124">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="8d5cf-124">Availability</span></span>
<span data-ttu-id="8d5cf-125">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="8d5cf-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="8d5cf-126">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-126">Tensor constraints</span></span>
* <span data-ttu-id="8d5cf-127">`IndicesTensor`, *InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="8d5cf-128">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="8d5cf-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="8d5cf-129">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="8d5cf-130">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="8d5cf-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="8d5cf-131">Tensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-131">Tensor</span></span> | <span data-ttu-id="8d5cf-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d5cf-132">Kind</span></span> | <span data-ttu-id="8d5cf-133">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="8d5cf-133">Supported dimension counts</span></span> | <span data-ttu-id="8d5cf-134">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="8d5cf-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8d5cf-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-135">InputTensor</span></span> | <span data-ttu-id="8d5cf-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d5cf-136">Input</span></span> | <span data-ttu-id="8d5cf-137">1 a 8</span><span class="sxs-lookup"><span data-stu-id="8d5cf-137">1 to 8</span></span> | <span data-ttu-id="8d5cf-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8d5cf-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8d5cf-139">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-139">IndicesTensor</span></span> | <span data-ttu-id="8d5cf-140">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d5cf-140">Input</span></span> | <span data-ttu-id="8d5cf-141">1 a 8</span><span class="sxs-lookup"><span data-stu-id="8d5cf-141">1 to 8</span></span> | <span data-ttu-id="8d5cf-142">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="8d5cf-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="8d5cf-143">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-143">OutputTensor</span></span> | <span data-ttu-id="8d5cf-144">Saída</span><span class="sxs-lookup"><span data-stu-id="8d5cf-144">Output</span></span> | <span data-ttu-id="8d5cf-145">1 a 8</span><span class="sxs-lookup"><span data-stu-id="8d5cf-145">1 to 8</span></span> | <span data-ttu-id="8d5cf-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8d5cf-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="8d5cf-147">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="8d5cf-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="8d5cf-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-148">Tensor</span></span> | <span data-ttu-id="8d5cf-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d5cf-149">Kind</span></span> | <span data-ttu-id="8d5cf-150">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="8d5cf-150">Supported dimension counts</span></span> | <span data-ttu-id="8d5cf-151">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="8d5cf-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="8d5cf-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-152">InputTensor</span></span> | <span data-ttu-id="8d5cf-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d5cf-153">Input</span></span> | <span data-ttu-id="8d5cf-154">4</span><span class="sxs-lookup"><span data-stu-id="8d5cf-154">4</span></span> | <span data-ttu-id="8d5cf-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8d5cf-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="8d5cf-156">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-156">IndicesTensor</span></span> | <span data-ttu-id="8d5cf-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="8d5cf-157">Input</span></span> | <span data-ttu-id="8d5cf-158">4</span><span class="sxs-lookup"><span data-stu-id="8d5cf-158">4</span></span> | <span data-ttu-id="8d5cf-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="8d5cf-159">UINT32</span></span> |
| <span data-ttu-id="8d5cf-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="8d5cf-160">OutputTensor</span></span> | <span data-ttu-id="8d5cf-161">Saída</span><span class="sxs-lookup"><span data-stu-id="8d5cf-161">Output</span></span> | <span data-ttu-id="8d5cf-162">4</span><span class="sxs-lookup"><span data-stu-id="8d5cf-162">4</span></span> | <span data-ttu-id="8d5cf-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="8d5cf-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="8d5cf-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d5cf-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8d5cf-165">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="8d5cf-165">**Header**</span></span> | <span data-ttu-id="8d5cf-166">directml. h</span><span class="sxs-lookup"><span data-stu-id="8d5cf-166">directml.h</span></span> |