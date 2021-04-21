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
ms.openlocfilehash: 461a7882e17d86b25cf27e0a28c05673f8899cea
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803056"
---
# <a name="dml_element_wise_modulus_truncate_operator_desc-structure-directmlh"></a><span data-ttu-id="c80d5-103">Estrutura de DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="c80d5-103">DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="c80d5-104">Computa o operador de módulo C para cada par de elementos correspondentes dos tempos de entrada, colocando o resultado no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="c80d5-104">Computes the C modulus operator for each pair of corresponding elements of the input tensors, placing the result into the corresponding element of *OutputTensor*.</span></span>

<span data-ttu-id="c80d5-105">Como o quociente é arredondado em direção a 0, o resultado terá o mesmo sinal que o dividendo.</span><span class="sxs-lookup"><span data-stu-id="c80d5-105">Because the quotient is rounded towards 0, the result will have the same sign as the dividend.</span></span>

```
f(a, b) = a - (b * trunc(a / b))
```

<span data-ttu-id="c80d5-106">Esse operador dá suporte à execução in-loco, o que significa que *OutputTensor* tem permissão para alias de um dos tempos de entrada durante a associação.</span><span class="sxs-lookup"><span data-stu-id="c80d5-106">This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c80d5-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c80d5-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="c80d5-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="c80d5-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c80d5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c80d5-109">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_MODULUS_TRUNCATE_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="c80d5-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c80d5-110">Members</span></span>

`ATensor`

<span data-ttu-id="c80d5-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c80d5-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c80d5-112">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="c80d5-112">A tensor containing the left-hand side inputs.</span></span>


`BTensor`

<span data-ttu-id="c80d5-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c80d5-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c80d5-114">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="c80d5-114">A tensor containing the right-hand side inputs.</span></span>


`OutputTensor`

<span data-ttu-id="c80d5-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="c80d5-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="c80d5-116">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="c80d5-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="c80d5-117">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="c80d5-117">Availability</span></span>
<span data-ttu-id="c80d5-118">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="c80d5-118">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="c80d5-119">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-119">Tensor constraints</span></span>
<span data-ttu-id="c80d5-120">*ATensor*, *BTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="c80d5-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="c80d5-121">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-121">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="c80d5-122">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="c80d5-122">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="c80d5-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-123">Tensor</span></span> | <span data-ttu-id="c80d5-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c80d5-124">Kind</span></span> | <span data-ttu-id="c80d5-125">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="c80d5-125">Supported dimension counts</span></span> | <span data-ttu-id="c80d5-126">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="c80d5-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c80d5-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-127">ATensor</span></span> | <span data-ttu-id="c80d5-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="c80d5-128">Input</span></span> | <span data-ttu-id="c80d5-129">1 a 8</span><span class="sxs-lookup"><span data-stu-id="c80d5-129">1 to 8</span></span> | <span data-ttu-id="c80d5-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c80d5-130">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c80d5-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-131">BTensor</span></span> | <span data-ttu-id="c80d5-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="c80d5-132">Input</span></span> | <span data-ttu-id="c80d5-133">1 a 8</span><span class="sxs-lookup"><span data-stu-id="c80d5-133">1 to 8</span></span> | <span data-ttu-id="c80d5-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c80d5-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c80d5-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-135">OutputTensor</span></span> | <span data-ttu-id="c80d5-136">Saída</span><span class="sxs-lookup"><span data-stu-id="c80d5-136">Output</span></span> | <span data-ttu-id="c80d5-137">1 a 8</span><span class="sxs-lookup"><span data-stu-id="c80d5-137">1 to 8</span></span> | <span data-ttu-id="c80d5-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c80d5-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="c80d5-139">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="c80d5-139">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="c80d5-140">Tensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-140">Tensor</span></span> | <span data-ttu-id="c80d5-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="c80d5-141">Kind</span></span> | <span data-ttu-id="c80d5-142">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="c80d5-142">Supported dimension counts</span></span> | <span data-ttu-id="c80d5-143">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="c80d5-143">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="c80d5-144">ATensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-144">ATensor</span></span> | <span data-ttu-id="c80d5-145">Entrada</span><span class="sxs-lookup"><span data-stu-id="c80d5-145">Input</span></span> | <span data-ttu-id="c80d5-146">4</span><span class="sxs-lookup"><span data-stu-id="c80d5-146">4</span></span> | <span data-ttu-id="c80d5-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c80d5-147">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c80d5-148">BTensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-148">BTensor</span></span> | <span data-ttu-id="c80d5-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="c80d5-149">Input</span></span> | <span data-ttu-id="c80d5-150">4</span><span class="sxs-lookup"><span data-stu-id="c80d5-150">4</span></span> | <span data-ttu-id="c80d5-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c80d5-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="c80d5-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="c80d5-152">OutputTensor</span></span> | <span data-ttu-id="c80d5-153">Saída</span><span class="sxs-lookup"><span data-stu-id="c80d5-153">Output</span></span> | <span data-ttu-id="c80d5-154">4</span><span class="sxs-lookup"><span data-stu-id="c80d5-154">4</span></span> | <span data-ttu-id="c80d5-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="c80d5-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="c80d5-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c80d5-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c80d5-157">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="c80d5-157">**Header**</span></span> | <span data-ttu-id="c80d5-158">directml. h</span><span class="sxs-lookup"><span data-stu-id="c80d5-158">directml.h</span></span> |