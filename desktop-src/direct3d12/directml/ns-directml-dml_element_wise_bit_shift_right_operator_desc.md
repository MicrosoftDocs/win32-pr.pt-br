---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Executa um deslocamento lógico à direita de cada elemento de *ATensor* por um número de bits fornecido pelo elemento correspondente de *BTensor*, colocando o resultado no elemento correspondente de *OutputTensor*.
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
ms.openlocfilehash: 447b0f685b51bf8b146644de3b5f65390a492ffd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105762239"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a><span data-ttu-id="732bb-103">Estrutura de DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="732bb-103">DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="732bb-104">Executa um deslocamento lógico à direita de cada elemento de *ATensor* por um número de bits fornecido pelo elemento correspondente de *BTensor*, colocando o resultado no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="732bb-104">Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(a, b) = (a >> b)
```

<span data-ttu-id="732bb-105">Esse operador dá suporte à execução in-loco, o que significa que *OutputTensor* tem permissão para alias de um dos tempos de entrada durante a associação.</span><span class="sxs-lookup"><span data-stu-id="732bb-105">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="732bb-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="732bb-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="732bb-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="732bb-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="732bb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="732bb-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="732bb-109">Membros</span><span class="sxs-lookup"><span data-stu-id="732bb-109">Members</span></span>

`ATensor`

<span data-ttu-id="732bb-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="732bb-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="732bb-111">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="732bb-111">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="732bb-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="732bb-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="732bb-113">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="732bb-113">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="732bb-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="732bb-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="732bb-115">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="732bb-115">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="732bb-116">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="732bb-116">Availability</span></span>
<span data-ttu-id="732bb-117">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="732bb-117">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="732bb-118">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="732bb-118">Tensor constraints</span></span>
<span data-ttu-id="732bb-119">*ATensor*, *BTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="732bb-119">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="732bb-120">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="732bb-120">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="732bb-121">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="732bb-121">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="732bb-122">Tensor</span><span class="sxs-lookup"><span data-stu-id="732bb-122">Tensor</span></span> | <span data-ttu-id="732bb-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="732bb-123">Kind</span></span> | <span data-ttu-id="732bb-124">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="732bb-124">Supported dimension counts</span></span> | <span data-ttu-id="732bb-125">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="732bb-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="732bb-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="732bb-126">ATensor</span></span> | <span data-ttu-id="732bb-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="732bb-127">Input</span></span> | <span data-ttu-id="732bb-128">1 a 8</span><span class="sxs-lookup"><span data-stu-id="732bb-128">1 to 8</span></span> | <span data-ttu-id="732bb-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="732bb-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="732bb-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="732bb-130">BTensor</span></span> | <span data-ttu-id="732bb-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="732bb-131">Input</span></span> | <span data-ttu-id="732bb-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="732bb-132">1 to 8</span></span> | <span data-ttu-id="732bb-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="732bb-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="732bb-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="732bb-134">OutputTensor</span></span> | <span data-ttu-id="732bb-135">Saída</span><span class="sxs-lookup"><span data-stu-id="732bb-135">Output</span></span> | <span data-ttu-id="732bb-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="732bb-136">1 to 8</span></span> | <span data-ttu-id="732bb-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="732bb-137">UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="732bb-138">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="732bb-138">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="732bb-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="732bb-139">Tensor</span></span> | <span data-ttu-id="732bb-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="732bb-140">Kind</span></span> | <span data-ttu-id="732bb-141">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="732bb-141">Supported dimension counts</span></span> | <span data-ttu-id="732bb-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="732bb-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="732bb-143">ATensor</span><span class="sxs-lookup"><span data-stu-id="732bb-143">ATensor</span></span> | <span data-ttu-id="732bb-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="732bb-144">Input</span></span> | <span data-ttu-id="732bb-145">4</span><span class="sxs-lookup"><span data-stu-id="732bb-145">4</span></span> | <span data-ttu-id="732bb-146">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="732bb-146">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="732bb-147">BTensor</span><span class="sxs-lookup"><span data-stu-id="732bb-147">BTensor</span></span> | <span data-ttu-id="732bb-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="732bb-148">Input</span></span> | <span data-ttu-id="732bb-149">4</span><span class="sxs-lookup"><span data-stu-id="732bb-149">4</span></span> | <span data-ttu-id="732bb-150">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="732bb-150">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="732bb-151">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="732bb-151">OutputTensor</span></span> | <span data-ttu-id="732bb-152">Saída</span><span class="sxs-lookup"><span data-stu-id="732bb-152">Output</span></span> | <span data-ttu-id="732bb-153">4</span><span class="sxs-lookup"><span data-stu-id="732bb-153">4</span></span> | <span data-ttu-id="732bb-154">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="732bb-154">UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="732bb-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="732bb-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="732bb-156">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="732bb-156">**Header**</span></span> | <span data-ttu-id="732bb-157">directml. h</span><span class="sxs-lookup"><span data-stu-id="732bb-157">directml.h</span></span> |