---
UID: NS:directml.DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
title: DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
description: Preenche um tensor com o Valor constante *determinado.*
helpviewer_keywords:
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure
- direct3d12.dml_fill_value_constant_operator_desc
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
- directml/DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
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
- DML_FILL_VALUE_CONSTANT_OPERATOR_DESC
ms.openlocfilehash: 4fe9f766fc48a4b1ca0d32082dcd8a5f67591195
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417015"
---
# <a name="dml_fill_value_constant_operator_desc-structure-directmlh"></a><span data-ttu-id="38afa-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="38afa-103">DML_FILL_VALUE_CONSTANT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="38afa-104">Preenche um tensor com o Valor constante *determinado.*</span><span class="sxs-lookup"><span data-stu-id="38afa-104">Fills a tensor with the given constant *Value*.</span></span> <span data-ttu-id="38afa-105">Esse operador executa o pseudocódigo a seguir.</span><span class="sxs-lookup"><span data-stu-id="38afa-105">This operator performs the following pseudocode.</span></span>

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
endfor
```

> [!IMPORTANT]
> <span data-ttu-id="38afa-106">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="38afa-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="38afa-107">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="38afa-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="38afa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38afa-108">Syntax</span></span>
```cpp
struct DML_FILL_VALUE_CONSTANT_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      Value;
};
```



## <a name="members"></a><span data-ttu-id="38afa-109">Membros</span><span class="sxs-lookup"><span data-stu-id="38afa-109">Members</span></span>

`OutputTensor`

<span data-ttu-id="38afa-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="38afa-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="38afa-111">O tensor no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="38afa-111">The tensor to write the results to.</span></span> <span data-ttu-id="38afa-112">Esse tensor pode ter qualquer tamanho.</span><span class="sxs-lookup"><span data-stu-id="38afa-112">This tensor may have any size.</span></span>


`ValueDataType`

<span data-ttu-id="38afa-113">Tipo: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span><span class="sxs-lookup"><span data-stu-id="38afa-113">Type: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**</span></span>

<span data-ttu-id="38afa-114">O tipo de dados do *campo Valor,* que deve corresponder *a OutputTensor.DataType.*</span><span class="sxs-lookup"><span data-stu-id="38afa-114">The data type of the *Value* field, which must match *OutputTensor.DataType*.</span></span>


`Value`

<span data-ttu-id="38afa-115">Tipo: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span><span class="sxs-lookup"><span data-stu-id="38afa-115">Type: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**</span></span>

<span data-ttu-id="38afa-116">Um valor constante para preencher a saída, com *ValueDataType* determinando como interpretar o campo.</span><span class="sxs-lookup"><span data-stu-id="38afa-116">A constant value to fill the output, with *ValueDataType* determining how to interpret the field.</span></span>

## <a name="examples"></a><span data-ttu-id="38afa-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="38afa-117">Examples</span></span>

```
Value = 13.0

OutputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
    [[[[13.0f, 13.0f, 13.0f, 13.0f],
       [13.0f, 13.0f, 13.0f, 13.0f]]]]
```

## <a name="availability"></a><span data-ttu-id="38afa-118">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="38afa-118">Availability</span></span>
<span data-ttu-id="38afa-119">Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="38afa-119">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="38afa-120">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="38afa-120">Tensor support</span></span>
| <span data-ttu-id="38afa-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="38afa-121">Tensor</span></span> | <span data-ttu-id="38afa-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="38afa-122">Kind</span></span> | <span data-ttu-id="38afa-123">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="38afa-123">Supported dimension counts</span></span> | <span data-ttu-id="38afa-124">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="38afa-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="38afa-125">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="38afa-125">OutputTensor</span></span> | <span data-ttu-id="38afa-126">Saída</span><span class="sxs-lookup"><span data-stu-id="38afa-126">Output</span></span> | <span data-ttu-id="38afa-127">4</span><span class="sxs-lookup"><span data-stu-id="38afa-127">4</span></span> | <span data-ttu-id="38afa-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="38afa-128">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="38afa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38afa-129">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="38afa-130">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="38afa-130">**Header**</span></span> | <span data-ttu-id="38afa-131">directml.h</span><span class="sxs-lookup"><span data-stu-id="38afa-131">directml.h</span></span> |