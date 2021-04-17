---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Define constantes que especificam um tipo de borda de gráfico. Consulte [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para o uso dessa enumeração.
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: 19b11686f3741c386ca03e84af5a41af1ce5cb52
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105790665"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a><span data-ttu-id="aa55d-104">Enumeração de DML_GRAPH_EDGE_TYPE (directml. h)</span><span class="sxs-lookup"><span data-stu-id="aa55d-104">DML_GRAPH_EDGE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="aa55d-105">Define constantes que especificam um tipo de borda de gráfico.</span><span class="sxs-lookup"><span data-stu-id="aa55d-105">Defines constants that specify a type of graph edge.</span></span> <span data-ttu-id="aa55d-106">Consulte [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para o uso dessa enumeração.</span><span class="sxs-lookup"><span data-stu-id="aa55d-106">See [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa55d-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="aa55d-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="aa55d-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="aa55d-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa55d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa55d-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a><span data-ttu-id="aa55d-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="aa55d-110">Constants</span></span>

| <span data-ttu-id="aa55d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="aa55d-111">Name</span></span> | <span data-ttu-id="aa55d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa55d-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="aa55d-113">DML_GRAPH_EDGE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="aa55d-113">DML_GRAPH_EDGE_TYPE_INVALID</span></span> | <span data-ttu-id="aa55d-114">Especifica um tipo de borda de gráfico desconhecido e nunca é válido.</span><span class="sxs-lookup"><span data-stu-id="aa55d-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="aa55d-115">O uso desse valor resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="aa55d-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="aa55d-116">DML_GRAPH_EDGE_TYPE_INPUT</span><span class="sxs-lookup"><span data-stu-id="aa55d-116">DML_GRAPH_EDGE_TYPE_INPUT</span></span> | <span data-ttu-id="aa55d-117">Especifica que a borda do gráfico é descrita pela estrutura de [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="aa55d-117">Specifies that the graph edge is described by the [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="aa55d-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa55d-118">DML_GRAPH_EDGE_TYPE_OUTPUT</span></span> | <span data-ttu-id="aa55d-119">Especifica que a borda do gráfico é descrita pela estrutura de [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="aa55d-119">Specifies that the graph edge is described by the [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) structure.</span></span> |
| <span data-ttu-id="aa55d-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span><span class="sxs-lookup"><span data-stu-id="aa55d-120">DML_GRAPH_EDGE_TYPE_INTERMEDIATE</span></span> | <span data-ttu-id="aa55d-121">Especifica que a borda do gráfico é descrita pela estrutura de [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="aa55d-121">Specifies that the graph edge is described by the [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) structure.</span></span><br><br><span data-ttu-id="aa55d-122"># # Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="aa55d-122">## Availability</span></span><br><br><span data-ttu-id="aa55d-123">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="aa55d-123">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="aa55d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa55d-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="aa55d-125">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="aa55d-125">**Header**</span></span> | <span data-ttu-id="aa55d-126">directml. h</span><span class="sxs-lookup"><span data-stu-id="aa55d-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="aa55d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa55d-127">See also</span></span>

* [<span data-ttu-id="aa55d-128">Método IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="aa55d-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="aa55d-129">Estrutura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="aa55d-129">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="aa55d-130">Estrutura de DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="aa55d-130">DML_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_graph_edge_desc.md)
* [<span data-ttu-id="aa55d-131">Estrutura de DML_INPUT_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="aa55d-131">DML_INPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_input_graph_edge_desc.md)
* [<span data-ttu-id="aa55d-132">Estrutura de DML_OUTPUT_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="aa55d-132">DML_OUTPUT_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_output_graph_edge_desc.md)
* [<span data-ttu-id="aa55d-133">Estrutura de DML_INTERMEDIATE_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="aa55d-133">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure</span></span>](./ns-directml-dml_intermediate_graph_edge_desc.md)