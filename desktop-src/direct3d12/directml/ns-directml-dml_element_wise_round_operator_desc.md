---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Arredoda cada *elemento de InputTensor* para um valor inteiro, colocando o resultado no elemento correspondente *de OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417020"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="482a0-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="482a0-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="482a0-104">Arredoda cada *elemento de InputTensor* para um valor inteiro, colocando o resultado no elemento correspondente *de OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="482a0-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="482a0-105">Esse operador dá suporte à execução in-loca, o que significa que *OutputTensor* tem permissão para alias *InputTensor durante* a associação.</span><span class="sxs-lookup"><span data-stu-id="482a0-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="482a0-106">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="482a0-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="482a0-107">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="482a0-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="482a0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="482a0-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="482a0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="482a0-109">Members</span></span>

`InputTensor`

<span data-ttu-id="482a0-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="482a0-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="482a0-111">O tensor de entrada do que ler.</span><span class="sxs-lookup"><span data-stu-id="482a0-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="482a0-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="482a0-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="482a0-113">O tensor de saída no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="482a0-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="482a0-114">Tipo: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="482a0-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="482a0-115">Um [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determinando a direção para a qual arredondar.</span><span class="sxs-lookup"><span data-stu-id="482a0-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="482a0-116">Se **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: os valores são arredondados para o inteiro mais próximo, com valores de metade (por exemplo, 0,5) arredondados para o inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="482a0-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="482a0-117">Se **DML_ROUNDING_MODE_TOWARD_ZERO**: os valores serão arredondados para zero.</span><span class="sxs-lookup"><span data-stu-id="482a0-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="482a0-118">Isso efetivamente trunca a parte fracionada.</span><span class="sxs-lookup"><span data-stu-id="482a0-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="482a0-119">Se **DML_ROUNDING_MODE_TOWARD_INFINITY**: os valores são arredondados para o inteiro mais próximo, com valores de metade (por exemplo, 0,5) sendo arredondados para fora de zero (em direção ao infinito positivo ou negativo, dependendo do sinal do valor).</span><span class="sxs-lookup"><span data-stu-id="482a0-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="482a0-120">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="482a0-120">Availability</span></span>
<span data-ttu-id="482a0-121">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="482a0-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="482a0-122">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="482a0-122">Tensor constraints</span></span>
<span data-ttu-id="482a0-123">*InputTensor* e *OutputTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="482a0-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="482a0-124">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="482a0-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="482a0-125">DML_FEATURE_LEVEL_3_0 e superior</span><span class="sxs-lookup"><span data-stu-id="482a0-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="482a0-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="482a0-126">Tensor</span></span> | <span data-ttu-id="482a0-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="482a0-127">Kind</span></span> | <span data-ttu-id="482a0-128">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="482a0-128">Supported dimension counts</span></span> | <span data-ttu-id="482a0-129">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="482a0-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="482a0-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="482a0-130">InputTensor</span></span> | <span data-ttu-id="482a0-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="482a0-131">Input</span></span> | <span data-ttu-id="482a0-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="482a0-132">1 to 8</span></span> | <span data-ttu-id="482a0-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="482a0-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="482a0-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="482a0-134">OutputTensor</span></span> | <span data-ttu-id="482a0-135">Saída</span><span class="sxs-lookup"><span data-stu-id="482a0-135">Output</span></span> | <span data-ttu-id="482a0-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="482a0-136">1 to 8</span></span> | <span data-ttu-id="482a0-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="482a0-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="482a0-138">DML_FEATURE_LEVEL_2_1 e superior</span><span class="sxs-lookup"><span data-stu-id="482a0-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="482a0-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="482a0-139">Tensor</span></span> | <span data-ttu-id="482a0-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="482a0-140">Kind</span></span> | <span data-ttu-id="482a0-141">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="482a0-141">Supported dimension counts</span></span> | <span data-ttu-id="482a0-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="482a0-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="482a0-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="482a0-143">InputTensor</span></span> | <span data-ttu-id="482a0-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="482a0-144">Input</span></span> | <span data-ttu-id="482a0-145">4</span><span class="sxs-lookup"><span data-stu-id="482a0-145">4</span></span> | <span data-ttu-id="482a0-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="482a0-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="482a0-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="482a0-147">OutputTensor</span></span> | <span data-ttu-id="482a0-148">Saída</span><span class="sxs-lookup"><span data-stu-id="482a0-148">Output</span></span> | <span data-ttu-id="482a0-149">4</span><span class="sxs-lookup"><span data-stu-id="482a0-149">4</span></span> | <span data-ttu-id="482a0-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="482a0-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="482a0-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="482a0-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="482a0-152">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="482a0-152">**Header**</span></span> | <span data-ttu-id="482a0-153">directml.h</span><span class="sxs-lookup"><span data-stu-id="482a0-153">directml.h</span></span> |