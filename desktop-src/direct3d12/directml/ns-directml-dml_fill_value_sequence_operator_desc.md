---
UID: NS:directml.DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
title: DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
description: Preenche um tensor com uma sequência.
helpviewer_keywords:
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure
- direct3d12.dml_fill_value_sequence_operator_desc
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.openlocfilehash: 17b503630db2108dc4d9d2f5c2f32f7e324189d1
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803036"
---
# <a name="dml_fill_value_sequence_operator_desc-structure-directmlh"></a><span data-ttu-id="b254a-103">Estrutura de DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b254a-103">DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="b254a-104">Preenche um tensor com uma sequência.</span><span class="sxs-lookup"><span data-stu-id="b254a-104">Fills a tensor with a sequence.</span></span> <span data-ttu-id="b254a-105">Esse operador executa o pseudocódigo a seguir.</span><span class="sxs-lookup"><span data-stu-id="b254a-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
    Value += Delta
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="b254a-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="b254a-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="b254a-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b254a-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b254a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b254a-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      ValueStart;
  DML_SCALAR_UNION      ValueDelta;
};
```



## <a name="members"></a><span data-ttu-id="b254a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b254a-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="b254a-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b254a-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b254a-111">O tensor para gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="b254a-111">The tensor to write the results to.</span></span> <span data-ttu-id="b254a-112">Este tensor pode ter qualquer tamanho.</span><span class="sxs-lookup"><span data-stu-id="b254a-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="b254a-113">Tipo: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="b254a-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="b254a-114">O tipo de dados do campo de *valor* , que deve corresponder a *OutputTensor. DataType*.</span><span class="sxs-lookup"><span data-stu-id="b254a-114">The data type of *Value* field, which must match *OutputTensor.DataType*.</span></span>


`ValueStart`

<span data-ttu-id="b254a-115">Tipo: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="b254a-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="b254a-116">O valor inicial para preencher o primeiro elemento na saída, com *ValueDataType* determinando como interpretar o campo.</span><span class="sxs-lookup"><span data-stu-id="b254a-116">The initial value to fill the first element in the output, with *ValueDataType* determining how to interpret the field.</span></span>


`ValueDelta`

<span data-ttu-id="b254a-117">Tipo: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="b254a-117">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="b254a-118">Uma etapa para adicionar ao valor de cada elemento gravado, com *ValueDataType* determinando como interpretar o campo.</span><span class="sxs-lookup"><span data-stu-id="b254a-118">A step to add to the value for each element written, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="b254a-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b254a-119">Examples</span></span>

### <a name="example-1-1d-ascending-step"></a><span data-ttu-id="b254a-120">Exemplo 1.</span><span class="sxs-lookup"><span data-stu-id="b254a-120">Example 1.</span></span> <span data-ttu-id="b254a-121">etapa de crescente 1D</span><span class="sxs-lookup"><span data-stu-id="b254a-121">1D ascending step</span></span>

```
ValueStart = 3
ValueDelta = 2
ValueDataType = DML_TENSOR_DATA_TYPE_FLOAT32

OutputTensor: (Sizes:{1,1,1,3}, DataType:FLOAT32)
    [[[[3, 5, 7]]]]
```

### <a name="example-2-2d-ascending-step"></a><span data-ttu-id="b254a-122">Exemplo 2.</span><span class="sxs-lookup"><span data-stu-id="b254a-122">Example 2.</span></span> <span data-ttu-id="b254a-123">etapa 2D crescente</span><span class="sxs-lookup"><span data-stu-id="b254a-123">2D ascending step</span></span>

```
ValueStart = 10
ValueDelta = -2
ValueDataType = DML_TENSOR_DATA_TYPE_UINT8

OutputTensor: (Sizes:{1,1,2,2}, DataType:UINT8)
    [[[[10, 8],
       [ 6, 4]]]]
```

## <a name="availability"></a><span data-ttu-id="b254a-124">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="b254a-124">Availability</span></span>
<span data-ttu-id="b254a-125">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b254a-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b254a-126">Suporte do tensor</span><span class="sxs-lookup"><span data-stu-id="b254a-126">Tensor support</span></span>
| <span data-ttu-id="b254a-127">Tensor</span><span class="sxs-lookup"><span data-stu-id="b254a-127">Tensor</span></span> | <span data-ttu-id="b254a-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="b254a-128">Kind</span></span> | <span data-ttu-id="b254a-129">Contagens de dimensão com suporte</span><span class="sxs-lookup"><span data-stu-id="b254a-129">Supported dimension counts</span></span> | <span data-ttu-id="b254a-130">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="b254a-130">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b254a-131">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b254a-131">OutputTensor</span></span> | <span data-ttu-id="b254a-132">Saída</span><span class="sxs-lookup"><span data-stu-id="b254a-132">Output</span></span> | <span data-ttu-id="b254a-133">4</span><span class="sxs-lookup"><span data-stu-id="b254a-133">4</span></span> | <span data-ttu-id="b254a-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b254a-134">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="b254a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b254a-135">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b254a-136">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="b254a-136">**Header**</span></span> | <span data-ttu-id="b254a-137">directml. h</span><span class="sxs-lookup"><span data-stu-id="b254a-137">directml.h</span></span> |