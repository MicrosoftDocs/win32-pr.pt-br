---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
description: Calcula o módulo, com os mesmos resultados que o módulo do Python, para cada par de elementos correspondentes dos tensores de entrada, colocando o resultado no elemento correspondente *de OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_floor_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC
ms.openlocfilehash: 8c70bd4649a57270807ac408802fe07edd36d98e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417025"
---
# <a name="dml_element_wise_modulus_floor_operator_desc-structure-directmlh"></a><span data-ttu-id="87f91-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="87f91-103">DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="87f91-104">Calcula o módulo, com os mesmos resultados que o módulo do Python, para cada par de elementos correspondentes dos tensores de entrada, colocando o resultado no elemento correspondente *de OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="87f91-104">Computes the modulus, with the same results as the Python modulus, for each pair of corresponding elements from the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="87f91-105">Como o quociente é arredondado para -inf, o resultado terá o mesmo sinal que o divisor.</span><span class="sxs-lookup"><span data-stu-id="87f91-105">Because the quotient is rounded towards -inf, the result will have the same sign as the divisor.</span></span>

```
f(a, b) = a - (b * floor(a / b))
```

<span data-ttu-id="87f91-106">Esse operador dá suporte à execução in-loca, o que significa que *OutputTensor* tem permissão para alias um dos tensores de entrada durante a associação.</span><span class="sxs-lookup"><span data-stu-id="87f91-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87f91-107">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="87f91-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="87f91-108">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="87f91-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="87f91-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87f91-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_FLOOR_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="87f91-110">Membros</span><span class="sxs-lookup"><span data-stu-id="87f91-110">Members</span></span>

`ATensor`

<span data-ttu-id="87f91-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87f91-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87f91-112">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="87f91-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="87f91-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87f91-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87f91-114">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="87f91-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="87f91-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="87f91-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="87f91-116">O tensor de saída no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="87f91-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="87f91-117">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="87f91-117">Availability</span></span>
<span data-ttu-id="87f91-118">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="87f91-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="87f91-119">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="87f91-119">Tensor constraints</span></span>
<span data-ttu-id="87f91-120">*ATensor,* *BTensor* e *OutputTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="87f91-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="87f91-121">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="87f91-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="87f91-122">DML_FEATURE_LEVEL_3_0 e superior</span><span class="sxs-lookup"><span data-stu-id="87f91-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="87f91-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="87f91-123">Tensor</span></span> | <span data-ttu-id="87f91-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="87f91-124">Kind</span></span> | <span data-ttu-id="87f91-125">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="87f91-125">Supported dimension counts</span></span> | <span data-ttu-id="87f91-126">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="87f91-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="87f91-127">Atensor</span><span class="sxs-lookup"><span data-stu-id="87f91-127">ATensor</span></span> | <span data-ttu-id="87f91-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="87f91-128">Input</span></span> | <span data-ttu-id="87f91-129">1 a 8</span><span class="sxs-lookup"><span data-stu-id="87f91-129">1 to 8</span></span> | <span data-ttu-id="87f91-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87f91-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87f91-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="87f91-131">BTensor</span></span> | <span data-ttu-id="87f91-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="87f91-132">Input</span></span> | <span data-ttu-id="87f91-133">1 a 8</span><span class="sxs-lookup"><span data-stu-id="87f91-133">1 to 8</span></span> | <span data-ttu-id="87f91-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87f91-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87f91-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="87f91-135">OutputTensor</span></span> | <span data-ttu-id="87f91-136">Saída</span><span class="sxs-lookup"><span data-stu-id="87f91-136">Output</span></span> | <span data-ttu-id="87f91-137">1 a 8</span><span class="sxs-lookup"><span data-stu-id="87f91-137">1 to 8</span></span> | <span data-ttu-id="87f91-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87f91-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="87f91-139">DML_FEATURE_LEVEL_2_1 e superior</span><span class="sxs-lookup"><span data-stu-id="87f91-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="87f91-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="87f91-140">Tensor</span></span> | <span data-ttu-id="87f91-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="87f91-141">Kind</span></span> | <span data-ttu-id="87f91-142">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="87f91-142">Supported dimension counts</span></span> | <span data-ttu-id="87f91-143">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="87f91-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="87f91-144">Atensor</span><span class="sxs-lookup"><span data-stu-id="87f91-144">ATensor</span></span> | <span data-ttu-id="87f91-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="87f91-145">Input</span></span> | <span data-ttu-id="87f91-146">4</span><span class="sxs-lookup"><span data-stu-id="87f91-146">4</span></span> | <span data-ttu-id="87f91-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87f91-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87f91-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="87f91-148">BTensor</span></span> | <span data-ttu-id="87f91-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="87f91-149">Input</span></span> | <span data-ttu-id="87f91-150">4</span><span class="sxs-lookup"><span data-stu-id="87f91-150">4</span></span> | <span data-ttu-id="87f91-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87f91-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="87f91-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="87f91-152">OutputTensor</span></span> | <span data-ttu-id="87f91-153">Saída</span><span class="sxs-lookup"><span data-stu-id="87f91-153">Output</span></span> | <span data-ttu-id="87f91-154">4</span><span class="sxs-lookup"><span data-stu-id="87f91-154">4</span></span> | <span data-ttu-id="87f91-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="87f91-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="87f91-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87f91-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="87f91-157">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="87f91-157">**Header**</span></span> | <span data-ttu-id="87f91-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="87f91-158">directml.h</span></span> |