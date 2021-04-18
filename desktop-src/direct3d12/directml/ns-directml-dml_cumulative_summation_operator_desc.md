---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Soma os elementos de um tensor ao longo de um eixo, gravando a contagem de execução da soma no tensor de saída.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 955e70a8cfbb57995d77d73567238d082b96999b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105764335"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="1ef97-103">Estrutura de DML_CUMULATIVE_SUMMATION_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="1ef97-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="1ef97-104">Soma os elementos de um tensor ao longo de um eixo, gravando a contagem de execução da soma no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="1ef97-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ef97-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="1ef97-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="1ef97-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="1ef97-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef97-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ef97-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```



## <a name="members"></a><span data-ttu-id="1ef97-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1ef97-108">Members</span></span>

`InputTensor`

<span data-ttu-id="1ef97-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1ef97-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1ef97-110">O tensor de entrada que contém os elementos a serem somados.</span><span class="sxs-lookup"><span data-stu-id="1ef97-110">The input tensor containing elements to be summed.</span></span>


`OutputTensor`

<span data-ttu-id="1ef97-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1ef97-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="1ef97-112">A saída tensor para gravar as somas cumulativas resultantes.</span><span class="sxs-lookup"><span data-stu-id="1ef97-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="1ef97-113">Esse tensor deve ter os mesmos tamanhos e tipo de dados que o *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="1ef97-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="1ef97-114">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="1ef97-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="1ef97-115">O índice da dimensão à qual somar elementos.</span><span class="sxs-lookup"><span data-stu-id="1ef97-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="1ef97-116">Esse valor deve ser menor que o *DimensionCount* do *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="1ef97-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`AxisDirection`

<span data-ttu-id="1ef97-117">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="1ef97-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="1ef97-118">Um dos valores da enumeração [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef97-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="1ef97-119">Se for definido como **DML_AXIS_DIRECTION_INCREASING**, a soma ocorrerá atravessando o tensor ao longo do eixo especificado por índice de elemento crescente.</span><span class="sxs-lookup"><span data-stu-id="1ef97-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="1ef97-120">Se definido como **DML_AXIS_DIRECTION_DECREASING**, o inverso será true e a soma ocorrerá atravessando os elementos por índice decrescente.</span><span class="sxs-lookup"><span data-stu-id="1ef97-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>


`HasExclusiveSum`




## <a name="remarks"></a><span data-ttu-id="1ef97-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ef97-121">Remarks</span></span>
<span data-ttu-id="1ef97-122">Esse operador dá suporte à execução in-loco, o que significa que o *OutputTensor* tem permissão para alias do *InputTensor* durante a associação.</span><span class="sxs-lookup"><span data-stu-id="1ef97-122">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="1ef97-123">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="1ef97-123">Availability</span></span>
<span data-ttu-id="1ef97-124">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="1ef97-124">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="1ef97-125">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="1ef97-125">Tensor constraints</span></span>
<span data-ttu-id="1ef97-126">*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="1ef97-126">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="1ef97-127">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="1ef97-127">Tensor support</span></span>
| <span data-ttu-id="1ef97-128">Tensor</span><span class="sxs-lookup"><span data-stu-id="1ef97-128">Tensor</span></span> | <span data-ttu-id="1ef97-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ef97-129">Kind</span></span> | <span data-ttu-id="1ef97-130">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="1ef97-130">Supported dimension counts</span></span> | <span data-ttu-id="1ef97-131">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="1ef97-131">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="1ef97-132">InputTensor</span><span class="sxs-lookup"><span data-stu-id="1ef97-132">InputTensor</span></span> | <span data-ttu-id="1ef97-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="1ef97-133">Input</span></span> | <span data-ttu-id="1ef97-134">4</span><span class="sxs-lookup"><span data-stu-id="1ef97-134">4</span></span> | <span data-ttu-id="1ef97-135">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="1ef97-135">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="1ef97-136">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="1ef97-136">OutputTensor</span></span> | <span data-ttu-id="1ef97-137">Saída</span><span class="sxs-lookup"><span data-stu-id="1ef97-137">Output</span></span> | <span data-ttu-id="1ef97-138">4</span><span class="sxs-lookup"><span data-stu-id="1ef97-138">4</span></span> | <span data-ttu-id="1ef97-139">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="1ef97-139">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="1ef97-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ef97-140">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="1ef97-141">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="1ef97-141">**Header**</span></span> | <span data-ttu-id="1ef97-142">directml. h</span><span class="sxs-lookup"><span data-stu-id="1ef97-142">directml.h</span></span> |