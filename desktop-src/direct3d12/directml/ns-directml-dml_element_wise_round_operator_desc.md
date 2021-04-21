---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Arredonda cada elemento de *InputTensor* para um valor inteiro, colocando o resultado no elemento correspondente de *OutputTensor*.
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
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803044"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a><span data-ttu-id="92d1f-103">Estrutura de DML_ELEMENT_WISE_ROUND_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="92d1f-103">DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="92d1f-104">Arredonda cada elemento de *InputTensor* para um valor inteiro, colocando o resultado no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="92d1f-104">Rounds each element of *InputTensor* to an integer value, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="92d1f-105">Esse operador dá suporte à execução in-loco, o que significa que *OutputTensor* é permitido para alias *InputTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="92d1f-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92d1f-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="92d1f-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="92d1f-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="92d1f-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="92d1f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92d1f-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a><span data-ttu-id="92d1f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="92d1f-109">Members</span></span>

`InputTensor`

<span data-ttu-id="92d1f-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92d1f-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92d1f-111">O tensor de entrada para leitura.</span><span class="sxs-lookup"><span data-stu-id="92d1f-111">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="92d1f-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="92d1f-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="92d1f-113">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="92d1f-113">The output tensor to write the results to.</span></span>


`RoundingMode`

<span data-ttu-id="92d1f-114">Tipo: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span><span class="sxs-lookup"><span data-stu-id="92d1f-114">Type: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**</span></span>

<span data-ttu-id="92d1f-115">Um [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determinando a direção para arredondar.</span><span class="sxs-lookup"><span data-stu-id="92d1f-115">A [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determining the direction to round towards.</span></span>

* <span data-ttu-id="92d1f-116">Se **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: os valores são arredondados para o número inteiro mais próximo, com valores intermediários (por exemplo, 0,5) sendo arredondados para o inteiro par mais próximo.</span><span class="sxs-lookup"><span data-stu-id="92d1f-116">If **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded toward the nearest even integer.</span></span>
* <span data-ttu-id="92d1f-117">Se **DML_ROUNDING_MODE_TOWARD_ZERO**: os valores são arredondados para zero.</span><span class="sxs-lookup"><span data-stu-id="92d1f-117">If **DML_ROUNDING_MODE_TOWARD_ZERO**: values are rounded toward zero.</span></span> <span data-ttu-id="92d1f-118">Isso efetivamente trunca a parte fracionária.</span><span class="sxs-lookup"><span data-stu-id="92d1f-118">This effectively truncates the fractional part.</span></span>
* <span data-ttu-id="92d1f-119">Se **DML_ROUNDING_MODE_TOWARD_INFINITY**: os valores são arredondados para o número inteiro mais próximo, com valores intermediários (por exemplo, 0,5) sendo arredondados para longe de zero (em direção ao infinito positivo ou negativo, dependendo do sinal do valor).</span><span class="sxs-lookup"><span data-stu-id="92d1f-119">If **DML_ROUNDING_MODE_TOWARD_INFINITY**: values are rounded to the nearest integer, with halfway values (for example, 0.5) being rounded away from zero (toward positive or negative infinity, depending on the sign of the value).</span></span>

## <a name="availability"></a><span data-ttu-id="92d1f-120">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="92d1f-120">Availability</span></span>
<span data-ttu-id="92d1f-121">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="92d1f-121">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="92d1f-122">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-122">Tensor constraints</span></span>
<span data-ttu-id="92d1f-123">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="92d1f-123">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="92d1f-124">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-124">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="92d1f-125">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="92d1f-125">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="92d1f-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-126">Tensor</span></span> | <span data-ttu-id="92d1f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="92d1f-127">Kind</span></span> | <span data-ttu-id="92d1f-128">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="92d1f-128">Supported dimension counts</span></span> | <span data-ttu-id="92d1f-129">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="92d1f-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="92d1f-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-130">InputTensor</span></span> | <span data-ttu-id="92d1f-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="92d1f-131">Input</span></span> | <span data-ttu-id="92d1f-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="92d1f-132">1 to 8</span></span> | <span data-ttu-id="92d1f-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92d1f-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92d1f-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-134">OutputTensor</span></span> | <span data-ttu-id="92d1f-135">Saída</span><span class="sxs-lookup"><span data-stu-id="92d1f-135">Output</span></span> | <span data-ttu-id="92d1f-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="92d1f-136">1 to 8</span></span> | <span data-ttu-id="92d1f-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92d1f-137">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="92d1f-138">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="92d1f-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="92d1f-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-139">Tensor</span></span> | <span data-ttu-id="92d1f-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="92d1f-140">Kind</span></span> | <span data-ttu-id="92d1f-141">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="92d1f-141">Supported dimension counts</span></span> | <span data-ttu-id="92d1f-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="92d1f-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="92d1f-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-143">InputTensor</span></span> | <span data-ttu-id="92d1f-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="92d1f-144">Input</span></span> | <span data-ttu-id="92d1f-145">4</span><span class="sxs-lookup"><span data-stu-id="92d1f-145">4</span></span> | <span data-ttu-id="92d1f-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92d1f-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="92d1f-147">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="92d1f-147">OutputTensor</span></span> | <span data-ttu-id="92d1f-148">Saída</span><span class="sxs-lookup"><span data-stu-id="92d1f-148">Output</span></span> | <span data-ttu-id="92d1f-149">4</span><span class="sxs-lookup"><span data-stu-id="92d1f-149">4</span></span> | <span data-ttu-id="92d1f-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="92d1f-150">FLOAT32, FLOAT16</span></span> |



## <a name="requirements"></a><span data-ttu-id="92d1f-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92d1f-151">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="92d1f-152">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="92d1f-152">**Header**</span></span> | <span data-ttu-id="92d1f-153">directml. h</span><span class="sxs-lookup"><span data-stu-id="92d1f-153">directml.h</span></span> |