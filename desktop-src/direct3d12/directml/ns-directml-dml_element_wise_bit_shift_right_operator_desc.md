---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Executa um deslocamento lógico para a direita de cada elemento *de ATensor* por um número de bits determinados pelo elemento correspondente *de BTensor*, colocando o resultado no elemento correspondente *de OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 5803b40520e3735d24d00eb7260eb527ab857c33
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416988"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="60877-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="60877-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="60877-104">Executa um deslocamento lógico para a direita de cada elemento *de ATensor* por um número de bits determinados pelo elemento correspondente *de BTensor*, colocando o resultado no elemento correspondente *de OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="60877-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="60877-105">Esse operador dá suporte à execução in-loca, o que significa que *OutputTensor* tem permissão para alias um dos tensores de entrada durante a associação.</span><span class="sxs-lookup"><span data-stu-id="60877-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60877-106">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="60877-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="60877-107">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="60877-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="60877-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60877-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="60877-109">Membros</span><span class="sxs-lookup"><span data-stu-id="60877-109">Members</span></span>

`ATensor`

<span data-ttu-id="60877-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="60877-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="60877-111">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="60877-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="60877-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="60877-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="60877-113">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="60877-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="60877-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="60877-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="60877-115">O tensor de saída no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="60877-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="60877-116">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="60877-116">Availability</span></span>
<span data-ttu-id="60877-117">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="60877-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="60877-118">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="60877-118">Tensor constraints</span></span>
<span data-ttu-id="60877-119">*ATensor,* *BTensor* e *OutputTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="60877-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="60877-120">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="60877-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="60877-121">DML_FEATURE_LEVEL_3_0 e superior</span><span class="sxs-lookup"><span data-stu-id="60877-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="60877-122">Tensor</span><span class="sxs-lookup"><span data-stu-id="60877-122">Tensor</span></span> | <span data-ttu-id="60877-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="60877-123">Kind</span></span> | <span data-ttu-id="60877-124">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="60877-124">Supported dimension counts</span></span> | <span data-ttu-id="60877-125">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="60877-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="60877-126">Atensor</span><span class="sxs-lookup"><span data-stu-id="60877-126">ATensor</span></span> | <span data-ttu-id="60877-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="60877-127">Input</span></span> | <span data-ttu-id="60877-128">1 a 8</span><span class="sxs-lookup"><span data-stu-id="60877-128">1 to 8</span></span> | <span data-ttu-id="60877-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="60877-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="60877-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="60877-130">BTensor</span></span> | <span data-ttu-id="60877-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="60877-131">Input</span></span> | <span data-ttu-id="60877-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="60877-132">1 to 8</span></span> | <span data-ttu-id="60877-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="60877-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="60877-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="60877-134">OutputTensor</span></span> | <span data-ttu-id="60877-135">Saída</span><span class="sxs-lookup"><span data-stu-id="60877-135">Output</span></span> | <span data-ttu-id="60877-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="60877-136">1 to 8</span></span> | <span data-ttu-id="60877-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="60877-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="60877-138">DML_FEATURE_LEVEL_2_1 e superior</span><span class="sxs-lookup"><span data-stu-id="60877-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="60877-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="60877-139">Tensor</span></span> | <span data-ttu-id="60877-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="60877-140">Kind</span></span> | <span data-ttu-id="60877-141">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="60877-141">Supported dimension counts</span></span> | <span data-ttu-id="60877-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="60877-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="60877-143">Atensor</span><span class="sxs-lookup"><span data-stu-id="60877-143">ATensor</span></span> | <span data-ttu-id="60877-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="60877-144">Input</span></span> | <span data-ttu-id="60877-145">4</span><span class="sxs-lookup"><span data-stu-id="60877-145">4</span></span> | <span data-ttu-id="60877-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="60877-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="60877-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="60877-147">BTensor</span></span> | <span data-ttu-id="60877-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="60877-148">Input</span></span> | <span data-ttu-id="60877-149">4</span><span class="sxs-lookup"><span data-stu-id="60877-149">4</span></span> | <span data-ttu-id="60877-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="60877-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="60877-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="60877-151">OutputTensor</span></span> | <span data-ttu-id="60877-152">Saída</span><span class="sxs-lookup"><span data-stu-id="60877-152">Output</span></span> | <span data-ttu-id="60877-153">4</span><span class="sxs-lookup"><span data-stu-id="60877-153">4</span></span> | <span data-ttu-id="60877-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="60877-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="60877-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60877-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="60877-156">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="60877-156">**Header**</span></span> | <span data-ttu-id="60877-157">directml.h</span><span class="sxs-lookup"><span data-stu-id="60877-157">directml.h</span></span> |