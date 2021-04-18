---
UID: NS:directml.DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
title: DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
description: Computa o operador de módulo C para cada par de elementos correspondentes dos tempos de entrada, colocando o resultado no elemento correspondente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure
- direct3d12.dml_element_wise_modulus_truncate_operator_desc
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
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
- DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC
ms.openlocfilehash: f7cbfbf8613fb4309c6d336ccd807565d0dae53c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105790663"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="b8697-103">Estrutura de DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b8697-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b8697-104">Computa o operador de módulo C para cada par de elementos correspondentes dos tempos de entrada, colocando o resultado no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b8697-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="b8697-105">Como o quociente é arredondado em direção a 0, o resultado terá o mesmo sinal que o dividendo.</span><span class="sxs-lookup"><span data-stu-id="b8697-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="b8697-106">Esse operador dá suporte à execução in-loco, o que significa que *OutputTensor* tem permissão para alias de um dos tempos de entrada durante a associação.</span><span class="sxs-lookup"><span data-stu-id="b8697-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8697-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="b8697-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b8697-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b8697-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8697-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8697-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="b8697-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b8697-110">Members</span></span>

`ATensor`

<span data-ttu-id="b8697-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b8697-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b8697-112">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="b8697-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="b8697-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b8697-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b8697-114">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="b8697-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="b8697-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b8697-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b8697-116">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="b8697-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="b8697-117">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="b8697-117">Availability</span></span>
<span data-ttu-id="b8697-118">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b8697-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b8697-119">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="b8697-119">Tensor constraints</span></span>
<span data-ttu-id="b8697-120">*ATensor*, *BTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="b8697-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b8697-121">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="b8697-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="b8697-122">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="b8697-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="b8697-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="b8697-123">Tensor</span></span> | <span data-ttu-id="b8697-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8697-124">Kind</span></span> | <span data-ttu-id="b8697-125">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="b8697-125">Supported dimension counts</span></span> | <span data-ttu-id="b8697-126">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b8697-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b8697-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="b8697-127">ATensor</span></span> | <span data-ttu-id="b8697-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8697-128">Input</span></span> | <span data-ttu-id="b8697-129">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b8697-129">1 to 8</span></span> | <span data-ttu-id="b8697-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b8697-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b8697-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="b8697-131">BTensor</span></span> | <span data-ttu-id="b8697-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8697-132">Input</span></span> | <span data-ttu-id="b8697-133">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b8697-133">1 to 8</span></span> | <span data-ttu-id="b8697-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b8697-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b8697-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b8697-135">OutputTensor</span></span> | <span data-ttu-id="b8697-136">Saída</span><span class="sxs-lookup"><span data-stu-id="b8697-136">Output</span></span> | <span data-ttu-id="b8697-137">1 a 8</span><span class="sxs-lookup"><span data-stu-id="b8697-137">1 to 8</span></span> | <span data-ttu-id="b8697-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b8697-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="b8697-139">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="b8697-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="b8697-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="b8697-140">Tensor</span></span> | <span data-ttu-id="b8697-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8697-141">Kind</span></span> | <span data-ttu-id="b8697-142">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="b8697-142">Supported dimension counts</span></span> | <span data-ttu-id="b8697-143">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b8697-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b8697-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="b8697-144">ATensor</span></span> | <span data-ttu-id="b8697-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8697-145">Input</span></span> | <span data-ttu-id="b8697-146">4</span><span class="sxs-lookup"><span data-stu-id="b8697-146">4</span></span> | <span data-ttu-id="b8697-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b8697-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b8697-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="b8697-148">BTensor</span></span> | <span data-ttu-id="b8697-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="b8697-149">Input</span></span> | <span data-ttu-id="b8697-150">4</span><span class="sxs-lookup"><span data-stu-id="b8697-150">4</span></span> | <span data-ttu-id="b8697-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b8697-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b8697-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b8697-152">OutputTensor</span></span> | <span data-ttu-id="b8697-153">Saída</span><span class="sxs-lookup"><span data-stu-id="b8697-153">Output</span></span> | <span data-ttu-id="b8697-154">4</span><span class="sxs-lookup"><span data-stu-id="b8697-154">4</span></span> | <span data-ttu-id="b8697-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b8697-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="b8697-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8697-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b8697-157">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="b8697-157">**Header**</span></span> | <span data-ttu-id="b8697-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="b8697-158">directml.h</span></span> |