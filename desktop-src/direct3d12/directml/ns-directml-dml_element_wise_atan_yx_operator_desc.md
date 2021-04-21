---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Computa o arco tangente de dois argumentos para cada elemento de *ATensor* e *BTensor*, em que *ATensor* é *o eixo Y* e *BTensor* é o *eixo X*, colocando o resultado no elemento correspondente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804413"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a><span data-ttu-id="055b1-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="055b1-103">DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="055b1-104">Computa o arco tangente de dois argumentos para cada elemento de *ATensor* e *BTensor*, em que *ATensor* é *o eixo Y* e *BTensor* é o *eixo X*, colocando o resultado no elemento correspondente de *OutputTensor*.</span><span class="sxs-lookup"><span data-stu-id="055b1-104">Computes the 2-argument arctangent for each element of *ATensor* and *BTensor*, where *ATensor* is the *Y-axis* and *BTensor* is the *X-axis*, placing the result into the corresponding element of *OutputTensor*.</span></span> <span data-ttu-id="055b1-105">Esse operador é indefinido para a origem (ou seja, quando *ATensor* e *BTensor* são 0 para elementos correspondentes).</span><span class="sxs-lookup"><span data-stu-id="055b1-105">This operator is undefined for the origin (that is, when *ATensor* and *BTensor* are both 0 for corresponding elements).</span></span>

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

<span data-ttu-id="055b1-107">Esse operador dá suporte à execução in-loco, o que significa que a saída tensor é permitida para o alias *ATensor* ou *BTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="055b1-107">This operator supports in-place execution, meaning that the output tensor is permitted to alias *ATensor* or *BTensor* during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="055b1-108">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,5 e posterior.</span><span class="sxs-lookup"><span data-stu-id="055b1-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="055b1-109">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="055b1-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="055b1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="055b1-110">Syntax</span></span>
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="055b1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="055b1-111">Members</span></span>

`ATensor`

<span data-ttu-id="055b1-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="055b1-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="055b1-113">O tensor de entrada para o qual ler os valores do eixo Y.</span><span class="sxs-lookup"><span data-stu-id="055b1-113">The input tensor to read the Y-axis values from.</span></span>

`BTensor`

<span data-ttu-id="055b1-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="055b1-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="055b1-115">O tensor de entrada para ler os valores do eixo X.</span><span class="sxs-lookup"><span data-stu-id="055b1-115">The input tensor to read the X-axis values from.</span></span>

`OutputTensor`

<span data-ttu-id="055b1-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="055b1-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="055b1-117">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="055b1-117">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="055b1-118">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="055b1-118">Availability</span></span>
<span data-ttu-id="055b1-119">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="055b1-119">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="055b1-120">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="055b1-120">Tensor constraints</span></span>
<span data-ttu-id="055b1-121">*ATensor*, *BTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="055b1-121">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="055b1-122">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="055b1-122">Tensor support</span></span>
| <span data-ttu-id="055b1-123">Tensor</span><span class="sxs-lookup"><span data-stu-id="055b1-123">Tensor</span></span> | <span data-ttu-id="055b1-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="055b1-124">Kind</span></span> | <span data-ttu-id="055b1-125">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="055b1-125">Supported dimension counts</span></span> | <span data-ttu-id="055b1-126">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="055b1-126">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="055b1-127">ATensor</span><span class="sxs-lookup"><span data-stu-id="055b1-127">ATensor</span></span> | <span data-ttu-id="055b1-128">Entrada</span><span class="sxs-lookup"><span data-stu-id="055b1-128">Input</span></span> | <span data-ttu-id="055b1-129">1 a 8</span><span class="sxs-lookup"><span data-stu-id="055b1-129">1 to 8</span></span> | <span data-ttu-id="055b1-130">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="055b1-130">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="055b1-131">BTensor</span><span class="sxs-lookup"><span data-stu-id="055b1-131">BTensor</span></span> | <span data-ttu-id="055b1-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="055b1-132">Input</span></span> | <span data-ttu-id="055b1-133">1 a 8</span><span class="sxs-lookup"><span data-stu-id="055b1-133">1 to 8</span></span> | <span data-ttu-id="055b1-134">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="055b1-134">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="055b1-135">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="055b1-135">OutputTensor</span></span> | <span data-ttu-id="055b1-136">Saída</span><span class="sxs-lookup"><span data-stu-id="055b1-136">Output</span></span> | <span data-ttu-id="055b1-137">1 a 8</span><span class="sxs-lookup"><span data-stu-id="055b1-137">1 to 8</span></span> | <span data-ttu-id="055b1-138">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="055b1-138">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="055b1-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="055b1-139">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="055b1-140">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="055b1-140">**Header**</span></span> | <span data-ttu-id="055b1-141">directml. h</span><span class="sxs-lookup"><span data-stu-id="055b1-141">directml.h</span></span> |
