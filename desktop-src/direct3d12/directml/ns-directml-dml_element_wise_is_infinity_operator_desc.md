---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Verifica cada elemento de *InputTensor* para IEEE-754 -inf, inf ou ambos, dependendo do *InfinityMode* determinado e coloca o resultado (1 para true, 0 para false) no elemento correspondente *de OutputTensor*.
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416987"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a><span data-ttu-id="28930-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="28930-103">DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="28930-104">Verifica cada elemento de *InputTensor* para IEEE-754 -inf, inf ou ambos, dependendo do *InfinityMode* determinado e coloca o resultado (1 para true, 0 para false) no elemento correspondente *de OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="28930-104">Checks each element of *InputTensor* for IEEE-754 -inf, inf, or both, depending on the given *InfinityMode*, and places the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> <span data-ttu-id="28930-105">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="28930-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="28930-106">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="28930-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="28930-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28930-107">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a><span data-ttu-id="28930-108">Membros</span><span class="sxs-lookup"><span data-stu-id="28930-108">Members</span></span>

`InputTensor`

<span data-ttu-id="28930-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="28930-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="28930-110">O tensor de entrada do que ler.</span><span class="sxs-lookup"><span data-stu-id="28930-110">The input tensor to read from.</span></span>


`OutputTensor`

<span data-ttu-id="28930-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="28930-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="28930-112">O tensor de saída no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="28930-112">The output tensor to write the results to.</span></span>


`InfinityMode`

<span data-ttu-id="28930-113">Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span><span class="sxs-lookup"><span data-stu-id="28930-113">Type: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**</span></span>

<span data-ttu-id="28930-114">Um [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determinando o sinal do infinito a ser determinado.</span><span class="sxs-lookup"><span data-stu-id="28930-114">A [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determining the sign of the infinity to check for.</span></span>

* <span data-ttu-id="28930-115">Se **DML_IS_INFINITY_MODE_EITHER**, 1 será retornado se o elemento for -inf ou inf, caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="28930-115">If **DML_IS_INFINITY_MODE_EITHER**, then 1 will be returned if the element is -inf or inf, otherwise 0.</span></span>
* <span data-ttu-id="28930-116">Se **DML_IS_INFINITY_MODE_POSITIVE**, 1 será retornado se o elemento for inf, caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="28930-116">If **DML_IS_INFINITY_MODE_POSITIVE**, then 1 will be returned if the element is inf, otherwise 0.</span></span>
* <span data-ttu-id="28930-117">Se **DML_IS_INFINITY_MODE_NEGATIVE**', 1 será retornado se o elemento for -inf, caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="28930-117">If **DML_IS_INFINITY_MODE_NEGATIVE**\`, then 1 will be returned if the element is -inf, otherwise 0.</span></span>


## <a name="remarks"></a><span data-ttu-id="28930-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="28930-118">Remarks</span></span>
## <a name="availability"></a><span data-ttu-id="28930-119">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="28930-119">Availability</span></span>
<span data-ttu-id="28930-120">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="28930-120">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="28930-121">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="28930-121">Tensor constraints</span></span>
<span data-ttu-id="28930-122">*InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount* e *Tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="28930-122">*InputTensor* and *OutputTensor* must have the same *DimensionCount* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="28930-123">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="28930-123">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="28930-124">DML_FEATURE_LEVEL_3_0 e superior</span><span class="sxs-lookup"><span data-stu-id="28930-124">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="28930-125">Tensor</span><span class="sxs-lookup"><span data-stu-id="28930-125">Tensor</span></span> | <span data-ttu-id="28930-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="28930-126">Kind</span></span> | <span data-ttu-id="28930-127">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="28930-127">Supported dimension counts</span></span> | <span data-ttu-id="28930-128">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="28930-128">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="28930-129">InputTensor</span><span class="sxs-lookup"><span data-stu-id="28930-129">InputTensor</span></span> | <span data-ttu-id="28930-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="28930-130">Input</span></span> | <span data-ttu-id="28930-131">1 a 8</span><span class="sxs-lookup"><span data-stu-id="28930-131">1 to 8</span></span> | <span data-ttu-id="28930-132">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="28930-132">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="28930-133">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="28930-133">OutputTensor</span></span> | <span data-ttu-id="28930-134">Saída</span><span class="sxs-lookup"><span data-stu-id="28930-134">Output</span></span> | <span data-ttu-id="28930-135">1 a 8</span><span class="sxs-lookup"><span data-stu-id="28930-135">1 to 8</span></span> | <span data-ttu-id="28930-136">UINT8</span><span class="sxs-lookup"><span data-stu-id="28930-136">UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="28930-137">DML_FEATURE_LEVEL_2_1 e superior</span><span class="sxs-lookup"><span data-stu-id="28930-137">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="28930-138">Tensor</span><span class="sxs-lookup"><span data-stu-id="28930-138">Tensor</span></span> | <span data-ttu-id="28930-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="28930-139">Kind</span></span> | <span data-ttu-id="28930-140">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="28930-140">Supported dimension counts</span></span> | <span data-ttu-id="28930-141">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="28930-141">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="28930-142">InputTensor</span><span class="sxs-lookup"><span data-stu-id="28930-142">InputTensor</span></span> | <span data-ttu-id="28930-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="28930-143">Input</span></span> | <span data-ttu-id="28930-144">4</span><span class="sxs-lookup"><span data-stu-id="28930-144">4</span></span> | <span data-ttu-id="28930-145">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="28930-145">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="28930-146">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="28930-146">OutputTensor</span></span> | <span data-ttu-id="28930-147">Saída</span><span class="sxs-lookup"><span data-stu-id="28930-147">Output</span></span> | <span data-ttu-id="28930-148">4</span><span class="sxs-lookup"><span data-stu-id="28930-148">4</span></span> | <span data-ttu-id="28930-149">UINT8</span><span class="sxs-lookup"><span data-stu-id="28930-149">UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="28930-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28930-150">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="28930-151">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="28930-151">**Minimum supported client**</span></span> | <span data-ttu-id="28930-152">Windows 10, versão 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="28930-152">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="28930-153">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="28930-153">**Minimum supported server**</span></span> | <span data-ttu-id="28930-154">Windows Server, versão 2004 (10.0; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="28930-154">Windows Server, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="28930-155">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="28930-155">**Header**</span></span> | <span data-ttu-id="28930-156">directml.h</span><span class="sxs-lookup"><span data-stu-id="28930-156">directml.h</span></span> |