---
UID: NS:directml.DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
description: Computa a operação OR de or entre cada elemento correspondente dos tempos de entrada e grava o resultado no tensor de saída.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.openlocfilehash: 7138c6647e1bd4df5d8957468ca67f103f4a3f5a
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803214"
---
# <a name="dml_element_wise_bit_or_operator_desc-structure-directmlh"></a><span data-ttu-id="d477a-103">Estrutura de DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="d477a-103">DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d477a-104">Computa a operação OR de or entre cada elemento correspondente dos tempos de entrada e grava o resultado no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="d477a-104">Computes the bitwise OR between each corresponding element of the input tensors, and writes the result into the output tensor.</span></span>

<span data-ttu-id="d477a-105">O tensor de entrada e saída deve ter o mesmo *DimensionCount*, *tamanhos* e *tipo de dados*.</span><span class="sxs-lookup"><span data-stu-id="d477a-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="d477a-106">Esse operador dá suporte à execução in-loco, o que significa que o tensor de saída é permitido para alias de um ou mais dos tempos de entrada durante a associação.</span><span class="sxs-lookup"><span data-stu-id="d477a-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias one or more of the input tensors during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d477a-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d477a-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d477a-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="d477a-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d477a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d477a-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="d477a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="d477a-110">Members</span></span>

`ATensor`

<span data-ttu-id="d477a-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d477a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d477a-112">Um tensor que contém as entradas do lado esquerdo.</span><span class="sxs-lookup"><span data-stu-id="d477a-112">A tensor containing the left-hand side inputs.</span></span>

`BTensor`

<span data-ttu-id="d477a-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d477a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d477a-114">Um tensor que contém as entradas do lado direito.</span><span class="sxs-lookup"><span data-stu-id="d477a-114">A tensor containing the right-hand side inputs.</span></span>

`OutputTensor`

<span data-ttu-id="d477a-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d477a-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d477a-116">A saída tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="d477a-116">The output tensor to write the results to.</span></span>

## <a name="availability"></a><span data-ttu-id="d477a-117">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d477a-117">Availability</span></span>
<span data-ttu-id="d477a-118">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="d477a-118">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d477a-119">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="d477a-119">Tensor constraints</span></span>
<span data-ttu-id="d477a-120">*ATensor*, *BTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="d477a-120">*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d477a-121">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="d477a-121">Tensor support</span></span>
| <span data-ttu-id="d477a-122">Tensor</span><span class="sxs-lookup"><span data-stu-id="d477a-122">Tensor</span></span> | <span data-ttu-id="d477a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d477a-123">Kind</span></span> | <span data-ttu-id="d477a-124">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="d477a-124">Supported dimension counts</span></span> | <span data-ttu-id="d477a-125">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="d477a-125">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d477a-126">ATensor</span><span class="sxs-lookup"><span data-stu-id="d477a-126">ATensor</span></span> | <span data-ttu-id="d477a-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="d477a-127">Input</span></span> | <span data-ttu-id="d477a-128">1 a 8</span><span class="sxs-lookup"><span data-stu-id="d477a-128">1 to 8</span></span> | <span data-ttu-id="d477a-129">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d477a-129">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d477a-130">BTensor</span><span class="sxs-lookup"><span data-stu-id="d477a-130">BTensor</span></span> | <span data-ttu-id="d477a-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="d477a-131">Input</span></span> | <span data-ttu-id="d477a-132">1 a 8</span><span class="sxs-lookup"><span data-stu-id="d477a-132">1 to 8</span></span> | <span data-ttu-id="d477a-133">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d477a-133">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d477a-134">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d477a-134">OutputTensor</span></span> | <span data-ttu-id="d477a-135">Saída</span><span class="sxs-lookup"><span data-stu-id="d477a-135">Output</span></span> | <span data-ttu-id="d477a-136">1 a 8</span><span class="sxs-lookup"><span data-stu-id="d477a-136">1 to 8</span></span> | <span data-ttu-id="d477a-137">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d477a-137">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="d477a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d477a-138">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d477a-139">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="d477a-139">**Header**</span></span> | <span data-ttu-id="d477a-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="d477a-140">directml.h</span></span> |