---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Calcula gradientes de backpropagation para uma unidade linear retificada (ReLU).
helpviewer_keywords:
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC, DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
- directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
- DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
ms.openlocfilehash: dea89f0e3366a07ee98f47703f07e2f5a9d4009d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416924"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="bd92f-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="bd92f-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bd92f-104">Calcula gradientes de backpropagation para uma unidade linear retificada (ReLU).</span><span class="sxs-lookup"><span data-stu-id="bd92f-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="bd92f-105">Esse operador executa a computação elemento a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd92f-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="bd92f-106">O operador de passagem de avanço [correspondente é DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="bd92f-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd92f-107">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="bd92f-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="bd92f-108">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="bd92f-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd92f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd92f-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="bd92f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="bd92f-110">Members</span></span>

`InputTensor`

<span data-ttu-id="bd92f-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bd92f-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bd92f-112">O tensor de entrada (recurso).</span><span class="sxs-lookup"><span data-stu-id="bd92f-112">The input (feature) tensor.</span></span> <span data-ttu-id="bd92f-113">Normalmente, essa é a mesma entrada fornecida durante a passagem de avanço (consulte [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="bd92f-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="bd92f-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bd92f-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bd92f-115">O tensor de gradiente de entrada.</span><span class="sxs-lookup"><span data-stu-id="bd92f-115">The incoming gradient tensor.</span></span> <span data-ttu-id="bd92f-116">Normalmente, isso é obtido da saída de backpropagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="bd92f-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="bd92f-117">Os *Tamanhos* *e o DataType* desse tensor devem corresponder exatamente aos do *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="bd92f-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="bd92f-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bd92f-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bd92f-119">Um tensor de saída que contém os gradientes paxados.</span><span class="sxs-lookup"><span data-stu-id="bd92f-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="bd92f-120">Os *Tamanhos* *e o DataType* desse tensor devem corresponder exatamente aos do *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="bd92f-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="bd92f-121">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="bd92f-121">Availability</span></span>
<span data-ttu-id="bd92f-122">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="bd92f-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bd92f-123">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="bd92f-123">Tensor constraints</span></span>
<span data-ttu-id="bd92f-124">*InputGradientTensor,* *InputTensor* e *OutputGradientTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="bd92f-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bd92f-125">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="bd92f-125">Tensor support</span></span>
| <span data-ttu-id="bd92f-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="bd92f-126">Tensor</span></span> | <span data-ttu-id="bd92f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd92f-127">Kind</span></span> | <span data-ttu-id="bd92f-128">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="bd92f-128">Supported dimension counts</span></span> | <span data-ttu-id="bd92f-129">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="bd92f-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bd92f-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bd92f-130">InputTensor</span></span> | <span data-ttu-id="bd92f-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="bd92f-131">Input</span></span> | <span data-ttu-id="bd92f-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="bd92f-132">1 to 8</span></span> | <span data-ttu-id="bd92f-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="bd92f-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="bd92f-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="bd92f-134">InputGradientTensor</span></span> | <span data-ttu-id="bd92f-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="bd92f-135">Input</span></span> | <span data-ttu-id="bd92f-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="bd92f-136">1 to 8</span></span> | <span data-ttu-id="bd92f-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="bd92f-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="bd92f-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="bd92f-138">OutputGradientTensor</span></span> | <span data-ttu-id="bd92f-139">Saída</span><span class="sxs-lookup"><span data-stu-id="bd92f-139">Output</span></span> | <span data-ttu-id="bd92f-140">1 a 8</span><span class="sxs-lookup"><span data-stu-id="bd92f-140">1 to 8</span></span> | <span data-ttu-id="bd92f-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="bd92f-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="bd92f-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd92f-142">See also</span></span>
[<span data-ttu-id="bd92f-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="bd92f-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="bd92f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd92f-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bd92f-145">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="bd92f-145">**Header**</span></span> | <span data-ttu-id="bd92f-146">directml.h</span><span class="sxs-lookup"><span data-stu-id="bd92f-146">directml.h</span></span> |