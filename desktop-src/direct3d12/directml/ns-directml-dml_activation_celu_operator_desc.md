---
UID: NS:directml.DML_ACTIVATION_CELU_OPERATOR_DESC
title: DML_ACTIVATION_CELU_OPERATOR_DESC
description: Executa a função de ativação de CELU (unidade linear exponencial) continuamente diferenciável em todos os elementos no *InputTensor*, colocando o resultado no elemento correspondente de *OutputTensor*.
helpviewer_keywords:
- DML_ACTIVATION_CELU_OPERATOR_DESC
- DML_ACTIVATION_CELU_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ACTIVATION_CELU_OPERATOR_DESC, DML_ACTIVATION_CELU_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
- directml/DML_ACTIVATION_CELU_OPERATOR_DESC
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
- DML_ACTIVATION_CELU_OPERATOR_DESC
ms.openlocfilehash: d474bd44c8a830117bb62927f4bda954a753b612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105793764"
---
# <a name="dml_activation_celu_operator_desc-structure-directmlh"></a><span data-ttu-id="a7185-103">Estrutura de DML_ACTIVATION_CELU_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="a7185-103">DML_ACTIVATION_CELU_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a7185-104">Executa a função de ativação de CELU (unidade linear exponencial) continuamente diferenciável em todos os elementos no *InputTensor*, colocando o resultado no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="a7185-104">Performs the continuously differentiable exponential linear unit (CELU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.</span></span>

```
f(x) = max(0, x) + min(0, Alpha * (exp(x / Alpha) - 1));
```

<span data-ttu-id="a7185-105">Em que:</span><span class="sxs-lookup"><span data-stu-id="a7185-105">Where:</span></span>
* <span data-ttu-id="a7185-106">exp (x) é a função de exponenciação natural</span><span class="sxs-lookup"><span data-stu-id="a7185-106">exp(x) is the natural exponentiation function</span></span>
* <span data-ttu-id="a7185-107">Max (a, b) retorna o maior dos dois valores a, b</span><span class="sxs-lookup"><span data-stu-id="a7185-107">max(a,b) returns the larger of the two values a,b</span></span>
* <span data-ttu-id="a7185-108">mín (a, b) retorna o menor dos dois valores a, b</span><span class="sxs-lookup"><span data-stu-id="a7185-108">min(a,b) returns the smaller of the two values a,b</span></span>

<span data-ttu-id="a7185-109">Esse operador dá suporte à execução in-loco, o que significa que a saída tensor é permitida para o alias *InputTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="a7185-109">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7185-110">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="a7185-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="a7185-111">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a7185-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7185-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7185-112">Syntax</span></span>
```cpp
struct DML_ACTIVATION_CELU_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  FLOAT Alpha;
};
```

## <a name="members"></a><span data-ttu-id="a7185-113">Membros</span><span class="sxs-lookup"><span data-stu-id="a7185-113">Members</span></span>

`InputTensor`

<span data-ttu-id="a7185-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a7185-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a7185-115">O tensor de entrada para leitura.</span><span class="sxs-lookup"><span data-stu-id="a7185-115">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="a7185-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a7185-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a7185-117">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a7185-117">The output tensor to write the results to.</span></span>

`Alpha`

<span data-ttu-id="a7185-118">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="a7185-118">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="a7185-119">O coeficiente alfa.</span><span class="sxs-lookup"><span data-stu-id="a7185-119">The alpha coefficient.</span></span> <span data-ttu-id="a7185-120">Um padrão típico para esse valor é 1,0.</span><span class="sxs-lookup"><span data-stu-id="a7185-120">A typical default for this value is 1.0.</span></span>

## <a name="availability"></a><span data-ttu-id="a7185-121">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a7185-121">Availability</span></span>
<span data-ttu-id="a7185-122">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a7185-122">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a7185-123">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="a7185-123">Tensor constraints</span></span>
<span data-ttu-id="a7185-124">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="a7185-124">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a7185-125">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="a7185-125">Tensor support</span></span>
| <span data-ttu-id="a7185-126">Tensor</span><span class="sxs-lookup"><span data-stu-id="a7185-126">Tensor</span></span> | <span data-ttu-id="a7185-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7185-127">Kind</span></span> | <span data-ttu-id="a7185-128">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="a7185-128">Supported Dimension Counts</span></span> | <span data-ttu-id="a7185-129">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="a7185-129">Supported Data Types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a7185-130">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a7185-130">InputTensor</span></span> | <span data-ttu-id="a7185-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="a7185-131">Input</span></span> | <span data-ttu-id="a7185-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="a7185-132">1 to 8</span></span> | <span data-ttu-id="a7185-133">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a7185-133">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a7185-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a7185-134">OutputTensor</span></span> | <span data-ttu-id="a7185-135">Saída</span><span class="sxs-lookup"><span data-stu-id="a7185-135">Output</span></span> | <span data-ttu-id="a7185-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="a7185-136">1 to 8</span></span> | <span data-ttu-id="a7185-137">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a7185-137">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="a7185-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7185-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a7185-139">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a7185-139">**Header**</span></span> | <span data-ttu-id="a7185-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="a7185-140">directml.h</span></span> |