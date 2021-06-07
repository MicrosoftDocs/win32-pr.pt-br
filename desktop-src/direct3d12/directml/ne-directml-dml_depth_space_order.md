---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Define constantes que controlam a transformação aplicada nos operadores DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) e **DML_OPERATOR_SPACE_TO_DEPTH1**.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416935"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a><span data-ttu-id="64614-103">DML_DEPTH_SPACE_ORDER enumeração (directml.h)</span><span class="sxs-lookup"><span data-stu-id="64614-103">DML_DEPTH_SPACE_ORDER enumeration (directml.h)</span></span>

<span data-ttu-id="64614-104">Define constantes que controlam a transformação aplicada nos operadores DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) e **DML_OPERATOR_SPACE_TO_DEPTH1**.</span><span class="sxs-lookup"><span data-stu-id="64614-104">Defines constants controlling the transform applied in the DirectML operators [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) and **DML_OPERATOR_SPACE_TO_DEPTH1**.</span></span> <span data-ttu-id="64614-105">Eles são usados dentro das estruturas [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) dados.</span><span class="sxs-lookup"><span data-stu-id="64614-105">These are used within the [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) structures.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64614-106">Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior).</span><span class="sxs-lookup"><span data-stu-id="64614-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="64614-107">Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="64614-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="64614-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64614-108">Syntax</span></span>
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a><span data-ttu-id="64614-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="64614-109">Constants</span></span>

| <span data-ttu-id="64614-110">Nome</span><span class="sxs-lookup"><span data-stu-id="64614-110">Name</span></span> | <span data-ttu-id="64614-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="64614-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="64614-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span><span class="sxs-lookup"><span data-stu-id="64614-112">DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW</span></span> | <span data-ttu-id="64614-113">Faz com que tensores usados [em DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) sejam interpretados com os layouts a seguir, em que as dimensões entre parênteses são niveladas juntas.</span><span class="sxs-lookup"><span data-stu-id="64614-113">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="64614-114">- **Versão de** profundidade: [Lote, (BlockHeight, BlockWidth, Channels), Height, Width]</span><span class="sxs-lookup"><span data-stu-id="64614-114">- **Depth version**: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]</span></span><br><span data-ttu-id="64614-115">- **Versão do** espaço: [Lote, Canais, (Altura, BlockHeight), (Largura, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="64614-115">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |
| <span data-ttu-id="64614-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span><span class="sxs-lookup"><span data-stu-id="64614-116">DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH</span></span> | <span data-ttu-id="64614-117">Faz com que tensores usados [em DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) sejam interpretados com os layouts a seguir, em que as dimensões entre parênteses são niveladas juntas.</span><span class="sxs-lookup"><span data-stu-id="64614-117">Causes tensors used in [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) to be interpreted with the following layouts, where dimensions in parenthesis are flattened together.</span></span><br><br><span data-ttu-id="64614-118">- **Versão de** profundidade: [Lote, (Canais, BlockHeight, BlockWidth), Altura, Largura]</span><span class="sxs-lookup"><span data-stu-id="64614-118">- **Depth version**: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]</span></span><br><span data-ttu-id="64614-119">- **Versão do** espaço: [Lote, Canais, (Altura, BlockHeight), (Largura, BlockWidth)]</span><span class="sxs-lookup"><span data-stu-id="64614-119">- **Space version**: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)]</span></span> |

## <a name="remarks"></a><span data-ttu-id="64614-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="64614-120">Remarks</span></span>

<span data-ttu-id="64614-121">Consulte [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) e [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) para ver exemplos mostrando o efeito desses valores.</span><span class="sxs-lookup"><span data-stu-id="64614-121">See [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) and [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) documentation for examples showing the effect of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="64614-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64614-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="64614-123">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="64614-123">**Header**</span></span> | <span data-ttu-id="64614-124">directml.h</span><span class="sxs-lookup"><span data-stu-id="64614-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="64614-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="64614-125">See also</span></span>

* [<span data-ttu-id="64614-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="64614-126">DML_DEPTH_TO_SPACE1_OPERATOR_DESC</span></span>](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [<span data-ttu-id="64614-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span><span class="sxs-lookup"><span data-stu-id="64614-127">DML_SPACE_TO_DEPTH1_OPERATOR_DESC</span></span>](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a><span data-ttu-id="64614-128">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="64614-128">Availability</span></span>
<span data-ttu-id="64614-129">Essa enumeração foi introduzida em `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="64614-129">This enumeration was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>