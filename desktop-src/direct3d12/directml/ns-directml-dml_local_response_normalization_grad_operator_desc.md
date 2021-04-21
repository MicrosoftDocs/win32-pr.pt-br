---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para a [normalização de resposta local](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).
helpviewer_keywords:
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_local_response_normalization_grad_operator_desc
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: eecf849a06ee8e99ac9c015ecd4568496120b2d9
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804408"
---
# <a name="dml_local_response_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="f8e5d-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="f8e5d-103">DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="f8e5d-104">Computa gradientes de repropagação para a [normalização de resposta local](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f8e5d-104">Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).</span></span>

<span data-ttu-id="f8e5d-105">O tipo de dados e o tamanho de todos os dezenases devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-105">The data type and size of all tensors must be the same.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8e5d-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="f8e5d-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f8e5d-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e5d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8e5d-108">Syntax</span></span>
```cpp
struct DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    BOOL CrossChannel;
    UINT LocalSize;
    FLOAT Alpha;
    FLOAT Beta;
    FLOAT Bias;
};
```

## <a name="members"></a><span data-ttu-id="f8e5d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f8e5d-109">Members</span></span>

`InputTensor`

<span data-ttu-id="f8e5d-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f8e5d-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f8e5d-111">O tensor que contém os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-111">The tensor containing the input data.</span></span> <span data-ttu-id="f8e5d-112">Os *tamanhos* deste tensor devem ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="f8e5d-112">This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`InputGradientTensor`

<span data-ttu-id="f8e5d-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f8e5d-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f8e5d-114">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-114">The incoming gradient tensor.</span></span> <span data-ttu-id="f8e5d-115">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span>

`OutputGradientTensor`

<span data-ttu-id="f8e5d-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f8e5d-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f8e5d-117">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-117">An output tensor containing the backpropagated gradients.</span></span>

`CrossChannel`

<span data-ttu-id="f8e5d-118">Tipo: **[bool](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8e5d-118">Type: **[BOOL](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="f8e5d-119">**True** se a camada de LRN soma entre canais; **False** se a camada LRN soma entre dimensões espaciais.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-119">**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.</span></span>

`LocalSize`

<span data-ttu-id="f8e5d-120">Tipo: **[uint](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8e5d-120">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="f8e5d-121">O número máximo de elementos a serem somados por dimensão (a região local é recortada para que todos os elementos estejam dentro dos limites).</span><span class="sxs-lookup"><span data-stu-id="f8e5d-121">The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds).</span></span> <span data-ttu-id="f8e5d-122">Se *CrossChannel* for **true**, essa será a largura e a altura da região local.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-122">If *CrossChannel* is **TRUE**, then this is the width and height of the local region.</span></span> <span data-ttu-id="f8e5d-123">Se *CrossChannel* for **false**, esse será o número de elementos na região local.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-123">If *CrossChannel* is **FALSE**, then this is the number of elements in the local region.</span></span> <span data-ttu-id="f8e5d-124">Esse valor deve ser pelo menos 1.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-124">This value must be at least 1.</span></span>

`Alpha`

<span data-ttu-id="f8e5d-125">Tipo: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8e5d-125">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="f8e5d-126">O valor do parâmetro de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-126">The value of the scaling parameter.</span></span> <span data-ttu-id="f8e5d-127">É recomendável um valor de 0, 1 como padrão.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-127">We recommend a value of 0.0001 as default.</span></span>

`Beta`

<span data-ttu-id="f8e5d-128">Tipo: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8e5d-128">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="f8e5d-129">O valor do expoente.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-129">The value of the exponent.</span></span> <span data-ttu-id="f8e5d-130">É recomendável um valor de 0,75 como padrão.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-130">We recommend a value of 0.75 as default.</span></span>

`Bias`

<span data-ttu-id="f8e5d-131">Tipo: **[float](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8e5d-131">Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="f8e5d-132">O valor de bias.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-132">The value of bias.</span></span> <span data-ttu-id="f8e5d-133">Recomendamos um valor de 1 como padrão.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-133">We recommend a value of 1 as default.</span></span>

## <a name="availability"></a><span data-ttu-id="f8e5d-134">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="f8e5d-134">Availability</span></span>
<span data-ttu-id="f8e5d-135">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="f8e5d-135">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f8e5d-136">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="f8e5d-136">Tensor constraints</span></span>
<span data-ttu-id="f8e5d-137">*InputGradientTensor*, *InputTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="f8e5d-137">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f8e5d-138">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="f8e5d-138">Tensor support</span></span>
| <span data-ttu-id="f8e5d-139">Tensor</span><span class="sxs-lookup"><span data-stu-id="f8e5d-139">Tensor</span></span> | <span data-ttu-id="f8e5d-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8e5d-140">Kind</span></span> | <span data-ttu-id="f8e5d-141">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="f8e5d-141">Supported dimension counts</span></span> | <span data-ttu-id="f8e5d-142">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="f8e5d-142">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f8e5d-143">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f8e5d-143">InputTensor</span></span> | <span data-ttu-id="f8e5d-144">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8e5d-144">Input</span></span> | <span data-ttu-id="f8e5d-145">4</span><span class="sxs-lookup"><span data-stu-id="f8e5d-145">4</span></span> | <span data-ttu-id="f8e5d-146">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f8e5d-146">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f8e5d-147">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f8e5d-147">InputGradientTensor</span></span> | <span data-ttu-id="f8e5d-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8e5d-148">Input</span></span> | <span data-ttu-id="f8e5d-149">4</span><span class="sxs-lookup"><span data-stu-id="f8e5d-149">4</span></span> | <span data-ttu-id="f8e5d-150">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f8e5d-150">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f8e5d-151">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="f8e5d-151">OutputGradientTensor</span></span> | <span data-ttu-id="f8e5d-152">Saída</span><span class="sxs-lookup"><span data-stu-id="f8e5d-152">Output</span></span> | <span data-ttu-id="f8e5d-153">4</span><span class="sxs-lookup"><span data-stu-id="f8e5d-153">4</span></span> | <span data-ttu-id="f8e5d-154">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f8e5d-154">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="f8e5d-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8e5d-155">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f8e5d-156">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="f8e5d-156">**Header**</span></span> | <span data-ttu-id="f8e5d-157">directml. h</span><span class="sxs-lookup"><span data-stu-id="f8e5d-157">directml.h</span></span> |
