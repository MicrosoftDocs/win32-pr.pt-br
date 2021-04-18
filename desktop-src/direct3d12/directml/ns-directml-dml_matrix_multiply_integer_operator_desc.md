---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Executa uma função de multiplicação de matriz em dados inteiros.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105793766"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a><span data-ttu-id="ac296-103">Estrutura de DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ac296-103">DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ac296-104">Executa uma função de multiplicação de matriz em dados inteiros.</span><span class="sxs-lookup"><span data-stu-id="ac296-104">Performs a matrix multiplication function on integer data.</span></span>

<span data-ttu-id="ac296-105">Esse operador requer que a matriz multiplique os tempos de entrada para ser 4D, que são formatados como `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="ac296-105">This operator requires the matrix multiply input tensors to be 4D, which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="ac296-106">O operador de multiplicação de matriz executará BatchCount \* ChannelCount número de multiplicações de matriz independentes.</span><span class="sxs-lookup"><span data-stu-id="ac296-106">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span>

<span data-ttu-id="ac296-107">Por exemplo, se *ATensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, K }` e *BTensor* tiver tamanhos  de `{ BatchCount, ChannelCount, K, N }` e *OutputTensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, N }` , o operador de multiplicação de matriz executará BatchCount \* ChannelCount multiplicações de matriz independentes de dimensões {M, K} x {K, n} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="ac296-107">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac296-108">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="ac296-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="ac296-109">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ac296-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac296-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac296-110">Syntax</span></span>
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="ac296-111">Membros</span><span class="sxs-lookup"><span data-stu-id="ac296-111">Members</span></span>

`ATensor`

<span data-ttu-id="ac296-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac296-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac296-113">Um tensor que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="ac296-113">A tensor containing the A data.</span></span> <span data-ttu-id="ac296-114">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="ac296-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AZeroPointTensor`

<span data-ttu-id="ac296-115">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac296-115">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac296-116">Um tensor opcional que contém os dados de ponto de ATensor zero.</span><span class="sxs-lookup"><span data-stu-id="ac296-116">An optional tensor containing the ATensor zero point data.</span></span> <span data-ttu-id="ac296-117">As dimensões esperadas do `AZeroPointTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se a quantificação por linha for necessária.</span><span class="sxs-lookup"><span data-stu-id="ac296-117">The expected dimensions of the `AZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per-row quantization is required.</span></span> <span data-ttu-id="ac296-118">Esses valores de ponto zero são usados para desquantificar os valores de *ATensor* .</span><span class="sxs-lookup"><span data-stu-id="ac296-118">These zero point values are used for dequantizing the *ATensor* values.</span></span>


`BTensor`

<span data-ttu-id="ac296-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac296-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac296-120">Um tensor que contém os dados B.</span><span class="sxs-lookup"><span data-stu-id="ac296-120">A tensor containing the B data.</span></span> <span data-ttu-id="ac296-121">As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="ac296-121">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BZeroPointTensor`

<span data-ttu-id="ac296-122">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac296-122">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac296-123">Um tensor opcional que contém os dados de ponto de *BTensor* zero.</span><span class="sxs-lookup"><span data-stu-id="ac296-123">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="ac296-124">As dimensões esperadas do `BZeroPointTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, 1, N }` se for necessária quantização por coluna.</span><span class="sxs-lookup"><span data-stu-id="ac296-124">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="ac296-125">Esses valores de ponto zero são usados para desquantificar os valores de BTensor.</span><span class="sxs-lookup"><span data-stu-id="ac296-125">These zero point values are used for dequantizing the BTensor values.</span></span>


`OutputTensor`

<span data-ttu-id="ac296-126">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ac296-126">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ac296-127">Um tensor com o qual gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="ac296-127">A tensor with which to write the results to.</span></span> <span data-ttu-id="ac296-128">As dimensões de tensor são `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="ac296-128">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="ac296-129">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="ac296-129">Availability</span></span>
<span data-ttu-id="ac296-130">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ac296-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ac296-131">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="ac296-131">Tensor constraints</span></span>
* <span data-ttu-id="ac296-132">*ATensor* e `AZeroPointTensor` deve ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="ac296-132">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="ac296-133">*BTensor* e `BZeroPointTensor` deve ter o mesmo *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="ac296-133">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ac296-134">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="ac296-134">Tensor support</span></span>
| <span data-ttu-id="ac296-135">Tensor</span><span class="sxs-lookup"><span data-stu-id="ac296-135">Tensor</span></span> | <span data-ttu-id="ac296-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac296-136">Kind</span></span> | <span data-ttu-id="ac296-137">Dimensões</span><span class="sxs-lookup"><span data-stu-id="ac296-137">Dimensions</span></span> | <span data-ttu-id="ac296-138">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="ac296-138">Supported dimension counts</span></span> | <span data-ttu-id="ac296-139">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="ac296-139">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="ac296-140">ATensor</span><span class="sxs-lookup"><span data-stu-id="ac296-140">ATensor</span></span> | <span data-ttu-id="ac296-141">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac296-141">Input</span></span> | <span data-ttu-id="ac296-142">{BatchCount, ChannelCount, M, K}</span><span class="sxs-lookup"><span data-stu-id="ac296-142">{ BatchCount, ChannelCount, M, K }</span></span> | <span data-ttu-id="ac296-143">4</span><span class="sxs-lookup"><span data-stu-id="ac296-143">4</span></span> | <span data-ttu-id="ac296-144">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ac296-144">INT8, UINT8</span></span> |
| <span data-ttu-id="ac296-145">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ac296-145">AZeroPointTensor</span></span> | <span data-ttu-id="ac296-146">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="ac296-146">Optional input</span></span> | <span data-ttu-id="ac296-147">{1, 1, AZeroPointCount, 1}</span><span class="sxs-lookup"><span data-stu-id="ac296-147">{ 1, 1, AZeroPointCount, 1 }</span></span> | <span data-ttu-id="ac296-148">4</span><span class="sxs-lookup"><span data-stu-id="ac296-148">4</span></span> | <span data-ttu-id="ac296-149">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ac296-149">INT8, UINT8</span></span> |
| <span data-ttu-id="ac296-150">BTensor</span><span class="sxs-lookup"><span data-stu-id="ac296-150">BTensor</span></span> | <span data-ttu-id="ac296-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="ac296-151">Input</span></span> | <span data-ttu-id="ac296-152">{BatchCount, ChannelCount, K, N}</span><span class="sxs-lookup"><span data-stu-id="ac296-152">{ BatchCount, ChannelCount, K, N }</span></span> | <span data-ttu-id="ac296-153">4</span><span class="sxs-lookup"><span data-stu-id="ac296-153">4</span></span> | <span data-ttu-id="ac296-154">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ac296-154">INT8, UINT8</span></span> |
| <span data-ttu-id="ac296-155">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ac296-155">BZeroPointTensor</span></span> | <span data-ttu-id="ac296-156">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="ac296-156">Optional input</span></span> | <span data-ttu-id="ac296-157">{1, 1, 1, BZeroPointCount}</span><span class="sxs-lookup"><span data-stu-id="ac296-157">{ 1, 1, 1, BZeroPointCount }</span></span> | <span data-ttu-id="ac296-158">4</span><span class="sxs-lookup"><span data-stu-id="ac296-158">4</span></span> | <span data-ttu-id="ac296-159">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ac296-159">INT8, UINT8</span></span> |
| <span data-ttu-id="ac296-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ac296-160">OutputTensor</span></span> | <span data-ttu-id="ac296-161">Saída</span><span class="sxs-lookup"><span data-stu-id="ac296-161">Output</span></span> | <span data-ttu-id="ac296-162">{BatchCount, ChannelCount, M, N}</span><span class="sxs-lookup"><span data-stu-id="ac296-162">{ BatchCount, ChannelCount, M, N }</span></span> | <span data-ttu-id="ac296-163">4</span><span class="sxs-lookup"><span data-stu-id="ac296-163">4</span></span> | <span data-ttu-id="ac296-164">INT32</span><span class="sxs-lookup"><span data-stu-id="ac296-164">INT32</span></span> |



## <a name="requirements"></a><span data-ttu-id="ac296-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac296-165">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ac296-166">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="ac296-166">**Header**</span></span> | <span data-ttu-id="ac296-167">directml. h</span><span class="sxs-lookup"><span data-stu-id="ac296-167">directml.h</span></span> |