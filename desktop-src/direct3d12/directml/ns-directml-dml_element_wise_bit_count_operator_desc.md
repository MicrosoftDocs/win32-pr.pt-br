---
UID: NS:directml.DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
description: Calcula o NOT bit a bit para cada elemento do tensor de entrada e grava o resultado no tensor de saída.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
ms.openlocfilehash: 070fc901c006ce1f18429e79eab635a5360c4af7
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416962"
---
# <a name="dml_element_wise_bit_not_operator_desc-structure-directmlh"></a><span data-ttu-id="aa71a-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC estrutura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="aa71a-103">DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="aa71a-104">Calcula o NOT bit a bit para cada elemento do tensor de entrada e grava o resultado no tensor de saída.</span><span class="sxs-lookup"><span data-stu-id="aa71a-104">Computes the bitwise NOT for each element of the input tensor, and writes the result into the output tensor.</span></span>

<span data-ttu-id="aa71a-105">O tensor de entrada e saída deve ter o mesmo *DimensionCount,* *Tamanhos* e *DataType*.</span><span class="sxs-lookup"><span data-stu-id="aa71a-105">The input and output tensor must have the same *DimensionCount*, *Sizes*, and *DataType*.</span></span>

<span data-ttu-id="aa71a-106">Esse operador dá suporte à execução in-loca, o que significa que o tensor de saída tem permissão para usar o tensor de entrada como alias durante a associação.</span><span class="sxs-lookup"><span data-stu-id="aa71a-106">This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa71a-107">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="aa71a-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="aa71a-108">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="aa71a-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa71a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa71a-109">Syntax</span></span>

```cpp
struct DML_ELEMENT_WISE_BIT_NOT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a><span data-ttu-id="aa71a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="aa71a-110">Members</span></span>

`InputTensor`

<span data-ttu-id="aa71a-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa71a-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa71a-112">O tensor de entrada do que ler.</span><span class="sxs-lookup"><span data-stu-id="aa71a-112">The input tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="aa71a-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="aa71a-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="aa71a-114">O tensor de saída no que gravar os resultados.</span><span class="sxs-lookup"><span data-stu-id="aa71a-114">The output tensor to write the results to.</span></span>

## <a name="example"></a><span data-ttu-id="aa71a-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="aa71a-115">Example</span></span>

```
InputTensor: (Sizes:{2,2}, DataType:UINT8)
[[0,  128], // 0b00000000, 0b10000000
 [42, 255]] // 0b00101010, 0b11111111

OutputTensor: (Sizes:{2,2}, DataType:UINT8)
[[255, 127], // 0b11111111, 0b01111111
 [213, 0  ]] // 0b11010101, 0b00000000
```

## <a name="availability"></a><span data-ttu-id="aa71a-116">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="aa71a-116">Availability</span></span>
<span data-ttu-id="aa71a-117">Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="aa71a-117">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="aa71a-118">Restrições do Tensor</span><span class="sxs-lookup"><span data-stu-id="aa71a-118">Tensor constraints</span></span>
<span data-ttu-id="aa71a-119">*InputTensor* e *OutputTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.</span><span class="sxs-lookup"><span data-stu-id="aa71a-119">*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="aa71a-120">Suporte do Tensor</span><span class="sxs-lookup"><span data-stu-id="aa71a-120">Tensor support</span></span>
| <span data-ttu-id="aa71a-121">Tensor</span><span class="sxs-lookup"><span data-stu-id="aa71a-121">Tensor</span></span> | <span data-ttu-id="aa71a-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa71a-122">Kind</span></span> | <span data-ttu-id="aa71a-123">Contagens de dimensões com suporte</span><span class="sxs-lookup"><span data-stu-id="aa71a-123">Supported dimension counts</span></span> | <span data-ttu-id="aa71a-124">Tipos de dados com suporte</span><span class="sxs-lookup"><span data-stu-id="aa71a-124">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="aa71a-125">InputTensor</span><span class="sxs-lookup"><span data-stu-id="aa71a-125">InputTensor</span></span> | <span data-ttu-id="aa71a-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71a-126">Input</span></span> | <span data-ttu-id="aa71a-127">1 a 8</span><span class="sxs-lookup"><span data-stu-id="aa71a-127">1 to 8</span></span> | <span data-ttu-id="aa71a-128">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="aa71a-128">UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="aa71a-129">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="aa71a-129">OutputTensor</span></span> | <span data-ttu-id="aa71a-130">Saída</span><span class="sxs-lookup"><span data-stu-id="aa71a-130">Output</span></span> | <span data-ttu-id="aa71a-131">1 a 8</span><span class="sxs-lookup"><span data-stu-id="aa71a-131">1 to 8</span></span> | <span data-ttu-id="aa71a-132">UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="aa71a-132">UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="aa71a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa71a-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="aa71a-134">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="aa71a-134">**Header**</span></span> | <span data-ttu-id="aa71a-135">directml.h</span><span class="sxs-lookup"><span data-stu-id="aa71a-135">directml.h</span></span> |