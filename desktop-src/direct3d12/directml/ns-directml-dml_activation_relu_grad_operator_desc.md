---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para uma unidade linear corrigida (ReLU).
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
ms.openlocfilehash: 567a1de50c1c91de83a9fda2978f83af8daf1a6e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105766576"
---
# <a name="dml_activation_relu_grad_operator_desc-structure-directmlh"></a><span data-ttu-id="aa9f2-103">Estrutura de DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="aa9f2-103">DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="aa9f2-104">Computa gradientes de repropagação para uma unidade linear corrigida (ReLU).</span><span class="sxs-lookup"><span data-stu-id="aa9f2-104">Computes backpropagation gradients for a rectified linear unit (ReLU).</span></span> <span data-ttu-id="aa9f2-105">Esse operador executa a seguinte computação por elemento.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-105">This operator performs the following element-wise computation.</span></span>

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

<span data-ttu-id="aa9f2-106">O operador de passagem direta correspondente está [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="aa9f2-106">The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa9f2-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="aa9f2-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="aa9f2-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="aa9f2-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9f2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa9f2-109">Syntax</span></span>
```cpp
struct DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
};
```

## <a name="members"></a><span data-ttu-id="aa9f2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="aa9f2-110">Members</span></span>

`InputTensor`

<span data-ttu-id="aa9f2-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa9f2-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa9f2-112">A entrada (recurso) tensor.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-112">The input (feature) tensor.</span></span> <span data-ttu-id="aa9f2-113">Normalmente, essa é a mesma entrada fornecida durante a passagem de encaminhamento (consulte [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span><span class="sxs-lookup"><span data-stu-id="aa9f2-113">This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).</span></span>

`InputGradientTensor`

<span data-ttu-id="aa9f2-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa9f2-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa9f2-115">O gradiente de entrada tensor.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-115">The incoming gradient tensor.</span></span> <span data-ttu-id="aa9f2-116">Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-116">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="aa9f2-117">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-117">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

`OutputTensor`

<span data-ttu-id="aa9f2-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa9f2-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa9f2-119">Um tensor de saída que contém os gradientes propagados.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-119">An output tensor containing the backpropagated gradients.</span></span> <span data-ttu-id="aa9f2-120">Os *tamanhos* e o *tipo de dados* desse tensor devem corresponder exatamente aos do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-120">The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.</span></span>

## <a name="availability"></a><span data-ttu-id="aa9f2-121">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="aa9f2-121">Availability</span></span>
<span data-ttu-id="aa9f2-122">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="aa9f2-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="aa9f2-123">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="aa9f2-123">Tensor constraints</span></span>
<span data-ttu-id="aa9f2-124">*InputGradientTensor*, *InputTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="aa9f2-124">*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="aa9f2-125">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="aa9f2-125">Tensor support</span></span>
| <span data-ttu-id="aa9f2-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="aa9f2-126">Tensor</span></span> | <span data-ttu-id="aa9f2-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa9f2-127">Kind</span></span> | <span data-ttu-id="aa9f2-128">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="aa9f2-128">Supported dimension counts</span></span> | <span data-ttu-id="aa9f2-129">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="aa9f2-129">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="aa9f2-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="aa9f2-130">InputTensor</span></span> | <span data-ttu-id="aa9f2-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa9f2-131">Input</span></span> | <span data-ttu-id="aa9f2-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="aa9f2-132">1 to 8</span></span> | <span data-ttu-id="aa9f2-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="aa9f2-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="aa9f2-134">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="aa9f2-134">InputGradientTensor</span></span> | <span data-ttu-id="aa9f2-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa9f2-135">Input</span></span> | <span data-ttu-id="aa9f2-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="aa9f2-136">1 to 8</span></span> | <span data-ttu-id="aa9f2-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="aa9f2-137">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="aa9f2-138">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="aa9f2-138">OutputGradientTensor</span></span> | <span data-ttu-id="aa9f2-139">Saída</span><span class="sxs-lookup"><span data-stu-id="aa9f2-139">Output</span></span> | <span data-ttu-id="aa9f2-140">1 a 8</span><span class="sxs-lookup"><span data-stu-id="aa9f2-140">1 to 8</span></span> | <span data-ttu-id="aa9f2-141">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="aa9f2-141">FLOAT32, FLOAT16</span></span> |

## <a name="see-also"></a><span data-ttu-id="aa9f2-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa9f2-142">See also</span></span>
[<span data-ttu-id="aa9f2-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="aa9f2-143">DML_ACTIVATION_RELU_OPERATOR_DESC</span></span>](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

## <a name="requirements"></a><span data-ttu-id="aa9f2-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa9f2-144">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="aa9f2-145">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="aa9f2-145">**Header**</span></span> | <span data-ttu-id="aa9f2-146">directml. h</span><span class="sxs-lookup"><span data-stu-id="aa9f2-146">directml.h</span></span> |