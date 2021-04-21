---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Verifica cada elemento de *InputTensor* para IEEE-754-inf, inf, ou ambos, dependendo do *InfinityMode* especificado e coloca o resultado (1 para true, 0 para false) no elemento correspondente de *OutputTensor*.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803095"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="871c2-103">Estrutura de DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="871c2-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="871c2-104">Verifica cada elemento de *InputTensor* para IEEE-754-inf, inf, ou ambos, dependendo do *InfinityMode* especificado e coloca o resultado (1 para true, 0 para false) no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="871c2-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="871c2-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="871c2-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="871c2-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="871c2-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="871c2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="871c2-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="871c2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="871c2-108">Members</span></span>

`InputTensor`

<span data-ttu-id="871c2-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="871c2-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="871c2-110">O tensor de entrada para leitura.</span><span class="sxs-lookup"><span data-stu-id="871c2-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="871c2-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="871c2-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="871c2-112">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="871c2-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="871c2-113">Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="871c2-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="871c2-114">Um [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determinando o sinal do infinito a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="871c2-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="871c2-115">Se **DML_IS_INFINITY_MODE_EITHER**, 1 será retornado se o elemento for-INF ou INF, caso contrário 0.</span><span class="sxs-lookup"><span data-stu-id="871c2-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="871c2-116">Se **DML_IS_INFINITY_MODE_POSITIVE**, 1 será retornado se o elemento for INF, caso contrário 0.</span><span class="sxs-lookup"><span data-stu-id="871c2-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="871c2-117">Se **DML_IS_INFINITY_MODE_NEGATIVE**', 1 será retornado se o elemento for-INF, caso contrário 0.</span><span class="sxs-lookup"><span data-stu-id="871c2-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="871c2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="871c2-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="871c2-119">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="871c2-119">Availability</span></span>
<span data-ttu-id="871c2-120">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="871c2-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="871c2-121">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="871c2-121">Tensor constraints</span></span>
<span data-ttu-id="871c2-122">*InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="871c2-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="871c2-123">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="871c2-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="871c2-124">DML_FEATURE_LEVEL_3_0 e acima</span><span class="sxs-lookup"><span data-stu-id="871c2-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="871c2-125">Tensor</span><span class="sxs-lookup"><span data-stu-id="871c2-125">Tensor</span></span> | <span data-ttu-id="871c2-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="871c2-126">Kind</span></span> | <span data-ttu-id="871c2-127">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="871c2-127">Supported dimension counts</span></span> | <span data-ttu-id="871c2-128">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="871c2-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="871c2-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="871c2-129">InputTensor</span></span> | <span data-ttu-id="871c2-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="871c2-130">Input</span></span> | <span data-ttu-id="871c2-131">1 a 8</span><span class="sxs-lookup"><span data-stu-id="871c2-131">1 to 8</span></span> | <span data-ttu-id="871c2-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="871c2-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="871c2-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="871c2-133">OutputTensor</span></span> | <span data-ttu-id="871c2-134">Saída</span><span class="sxs-lookup"><span data-stu-id="871c2-134">Output</span></span> | <span data-ttu-id="871c2-135">1 a 8</span><span class="sxs-lookup"><span data-stu-id="871c2-135">1 to 8</span></span> | <span data-ttu-id="871c2-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="871c2-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="871c2-137">DML_FEATURE_LEVEL_2_1 e acima</span><span class="sxs-lookup"><span data-stu-id="871c2-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="871c2-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="871c2-138">Tensor</span></span> | <span data-ttu-id="871c2-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="871c2-139">Kind</span></span> | <span data-ttu-id="871c2-140">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="871c2-140">Supported dimension counts</span></span> | <span data-ttu-id="871c2-141">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="871c2-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="871c2-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="871c2-142">InputTensor</span></span> | <span data-ttu-id="871c2-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="871c2-143">Input</span></span> | <span data-ttu-id="871c2-144">4</span><span class="sxs-lookup"><span data-stu-id="871c2-144">4</span></span> | <span data-ttu-id="871c2-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="871c2-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="871c2-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="871c2-146">OutputTensor</span></span> | <span data-ttu-id="871c2-147">Saída</span><span class="sxs-lookup"><span data-stu-id="871c2-147">Output</span></span> | <span data-ttu-id="871c2-148">4</span><span class="sxs-lookup"><span data-stu-id="871c2-148">4</span></span> | <span data-ttu-id="871c2-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="871c2-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="871c2-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="871c2-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="871c2-151">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="871c2-151">**Minimum supported client**</span></span> | <span data-ttu-id="871c2-152">Windows 10, versão 2004 (10,0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="871c2-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="871c2-153">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="871c2-153">**Minimum supported server**</span></span> | <span data-ttu-id="871c2-154">Windows Server, versão 2004 (10,0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="871c2-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="871c2-155">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="871c2-155">**Header**</span></span> | <span data-ttu-id="871c2-156">directml. h</span><span class="sxs-lookup"><span data-stu-id="871c2-156">directml.h</span></span> |