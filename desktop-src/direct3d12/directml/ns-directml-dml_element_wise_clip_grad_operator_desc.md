---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para o [clipe com elemento](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 3b993ca1c027119ae64157db2327a2836445bf43
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550201"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a><span data-ttu-id="6a717-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="6a717-103">DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="6a717-104">Computa gradientes de repropagação para o [clipe com elemento](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="6a717-104">Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).</span></span>

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

<span data-ttu-id="6a717-105">Esse operador dá suporte à execução in-loco, o `OutputTensor` que significa que é permitido para alias *InputTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="6a717-105">This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a717-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="6a717-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="6a717-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6a717-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a717-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a717-108">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a><span data-ttu-id="6a717-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6a717-109">Members</span></span>

`InputTensor`

<span data-ttu-id="6a717-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6a717-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6a717-111">O recurso de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="6a717-111">The input feature tensor.</span></span> <span data-ttu-id="6a717-112">Normalmente, isso é o mesmo tensor que foi fornecido como o *InputTensor* para [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) no passo de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6a717-112">This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="6a717-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6a717-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6a717-114">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="6a717-114">The incoming gradient tensor.</span></span> <span data-ttu-id="6a717-115">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="6a717-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="6a717-116">Normalmente, esse tensor teria os mesmos tamanhos da *saída* do **DML_OPERATOR_ELEMENT_WISE_CLIP** correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6a717-116">Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`OutputGradientTensor`

<span data-ttu-id="6a717-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6a717-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6a717-118">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="6a717-118">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="6a717-119">Normalmente, esse tensor teria os mesmos tamanhos que a *entrada* do **DML_OPERATOR_ELEMENT_WISE_CLIP** correspondente na passagem de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="6a717-119">Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.</span></span>

`Min`

<span data-ttu-id="6a717-120">Tipo: **[float](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a717-120">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a717-121">O valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="6a717-121">The minimum value.</span></span> <span data-ttu-id="6a717-122">Se x estiver neste valor ou abaixo dele, o resultado do gradiente será 0.</span><span class="sxs-lookup"><span data-stu-id="6a717-122">If x is at or below this value, then the gradient result is 0.</span></span>

`Max`

<span data-ttu-id="6a717-123">Tipo: **[float](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a717-123">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a717-124">O valor máximo.</span><span class="sxs-lookup"><span data-stu-id="6a717-124">The maximum value.</span></span> <span data-ttu-id="6a717-125">Se x estiver no valor ou acima dele, o resultado do gradiente será 0.</span><span class="sxs-lookup"><span data-stu-id="6a717-125">If x is at or above this value, then the gradient result is 0.</span></span>

## <a name="availability"></a><span data-ttu-id="6a717-126">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="6a717-126">Availability</span></span>
<span data-ttu-id="6a717-127">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="6a717-127">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6a717-128">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="6a717-128">Tensor constraints</span></span>
<span data-ttu-id="6a717-129">*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="6a717-129">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6a717-130">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="6a717-130">Tensor support</span></span>
| <span data-ttu-id="6a717-131">Tensor</span><span class="sxs-lookup"><span data-stu-id="6a717-131">Tensor</span></span> | <span data-ttu-id="6a717-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a717-132">Kind</span></span> | <span data-ttu-id="6a717-133">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="6a717-133">Supported dimension counts</span></span> | <span data-ttu-id="6a717-134">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="6a717-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6a717-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="6a717-135">InputTensor</span></span> | <span data-ttu-id="6a717-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a717-136">Input</span></span> | <span data-ttu-id="6a717-137">1 a 8</span><span class="sxs-lookup"><span data-stu-id="6a717-137">1 to 8</span></span> | <span data-ttu-id="6a717-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="6a717-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="6a717-139">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6a717-139">InputGradientTensor</span></span> | <span data-ttu-id="6a717-140">Entrada</span><span class="sxs-lookup"><span data-stu-id="6a717-140">Input</span></span> | <span data-ttu-id="6a717-141">1 a 8</span><span class="sxs-lookup"><span data-stu-id="6a717-141">1 to 8</span></span> | <span data-ttu-id="6a717-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="6a717-142">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="6a717-143">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="6a717-143">OutputGradientTensor</span></span> | <span data-ttu-id="6a717-144">Saída</span><span class="sxs-lookup"><span data-stu-id="6a717-144">Output</span></span> | <span data-ttu-id="6a717-145">1 a 8</span><span class="sxs-lookup"><span data-stu-id="6a717-145">1 to 8</span></span> | <span data-ttu-id="6a717-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="6a717-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="6a717-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a717-147">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6a717-148">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="6a717-148">**Header**</span></span> | <span data-ttu-id="6a717-149">directml.h</span><span class="sxs-lookup"><span data-stu-id="6a717-149">directml.h</span></span> |