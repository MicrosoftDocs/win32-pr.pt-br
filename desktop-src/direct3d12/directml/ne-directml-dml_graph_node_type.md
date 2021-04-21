---
UID: NE:directml.DML_GRAPH_NODE_TYPE
title: DML_GRAPH_NODE_TYPE
description: Define constantes que especificam um tipo de nó de gráfico. Consulte [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) para o uso dessa enumeração.
helpviewer_keywords:
- DML_GRAPH_NODE_TYPE
- DML_GRAPH_NODE_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_GRAPH_NODE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_TYPE, DML_GRAPH_NODE_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
- directml/DML_GRAPH_NODE_TYPE
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
- DML_GRAPH_NODE_TYPE
ms.openlocfilehash: 0bb0712370da35c4b8c9278ad7721d2ffc7d875d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803691"
---
# <a name="dml_graph_node_type-enumeration-directmlh"></a><span data-ttu-id="66223-104">Enumeração de DML_GRAPH_NODE_TYPE (directml. h)</span><span class="sxs-lookup"><span data-stu-id="66223-104">DML_GRAPH_NODE_TYPE enumeration (directml.h)</span></span>

<span data-ttu-id="66223-105">Define constantes que especificam um tipo de nó de gráfico.</span><span class="sxs-lookup"><span data-stu-id="66223-105">Defines constants that specify a type of graph node.</span></span> <span data-ttu-id="66223-106">Consulte [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) para o uso dessa enumeração.</span><span class="sxs-lookup"><span data-stu-id="66223-106">See [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) for the usage of this enumeration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66223-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="66223-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="66223-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="66223-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="66223-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66223-109">Syntax</span></span>
```cpp
typedef enum DML_GRAPH_NODE_TYPE {
  DML_GRAPH_NODE_TYPE_INVALID,
  DML_GRAPH_NODE_TYPE_OPERATOR
} ;
```

## <a name="constants"></a><span data-ttu-id="66223-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="66223-110">Constants</span></span>

| <span data-ttu-id="66223-111">Nome</span><span class="sxs-lookup"><span data-stu-id="66223-111">Name</span></span> | <span data-ttu-id="66223-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="66223-112">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="66223-113">DML_GRAPH_NODE_TYPE_INVALID</span><span class="sxs-lookup"><span data-stu-id="66223-113">DML_GRAPH_NODE_TYPE_INVALID</span></span> | <span data-ttu-id="66223-114">Especifica um tipo de borda de gráfico desconhecido e nunca é válido.</span><span class="sxs-lookup"><span data-stu-id="66223-114">Specifies an unknown graph edge type, and is never valid.</span></span> <span data-ttu-id="66223-115">O uso desse valor resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="66223-115">Using this value results in an error.</span></span> |
| <span data-ttu-id="66223-116">DML_GRAPH_NODE_TYPE_OPERATOR</span><span class="sxs-lookup"><span data-stu-id="66223-116">DML_GRAPH_NODE_TYPE_OPERATOR</span></span> | <span data-ttu-id="66223-117">Especifica que a borda do gráfico é descrita pela estrutura de [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) .</span><span class="sxs-lookup"><span data-stu-id="66223-117">Specifies that the graph edge is described by the [DML_OPERATOR_GRAPH_NODE_DESC](./ns-directml-dml_operator_graph_node_desc.md) structure.</span></span><br><br><span data-ttu-id="66223-118"># # Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="66223-118">## Availability</span></span><br><br><span data-ttu-id="66223-119">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="66223-119">This API was introduced in DirectML version `1.1.0`.</span></span> |


## <a name="requirements"></a><span data-ttu-id="66223-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66223-120">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="66223-121">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="66223-121">**Header**</span></span> | <span data-ttu-id="66223-122">directml. h</span><span class="sxs-lookup"><span data-stu-id="66223-122">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="66223-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="66223-123">See also</span></span>

* [<span data-ttu-id="66223-124">Método IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="66223-124">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="66223-125">Estrutura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="66223-125">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)     
* [<span data-ttu-id="66223-126">Estrutura de DML_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="66223-126">DML_GRAPH_NODE_DESC structure</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="66223-127">DML_OPERATOR_GRAPH_NODE_DESC</span><span class="sxs-lookup"><span data-stu-id="66223-127">DML_OPERATOR_GRAPH_NODE_DESC</span></span>](./ns-directml-dml_operator_graph_node_desc.md)