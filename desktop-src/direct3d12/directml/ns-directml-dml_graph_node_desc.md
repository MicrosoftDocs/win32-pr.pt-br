---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: 'Um contêiner genérico para um nó dentro de um grafo de operadores DirectML definido por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_GRAPH_NODE_DESC
- DML_GRAPH_NODE_DESC structure
- direct3d12.dml_graph_node_desc
- directml/DML_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_DESC, DML_GRAPH_NODE_DESC structure, direct3d12.dml_graph_node_desc, directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
- directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
ms.openlocfilehash: 8c79719f51efb4a59f9459a28765d3442ed3f4ee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105808395"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a><span data-ttu-id="0362a-103">Estrutura de DML_GRAPH_NODE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="0362a-103">DML_GRAPH_NODE_DESC structure (directml.h)</span></span>
<span data-ttu-id="0362a-104">Um contêiner genérico para um nó dentro de um grafo de operadores DirectML definido por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="0362a-104">A generic container for a node within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0362a-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="0362a-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="0362a-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="0362a-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0362a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0362a-107">Syntax</span></span>
```cpp
struct DML_GRAPH_NODE_DESC {
  DML_GRAPH_NODE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="0362a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0362a-108">Members</span></span>

`Type`

<span data-ttu-id="0362a-109">Tipo: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**</span><span class="sxs-lookup"><span data-stu-id="0362a-109">Type: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**</span></span>

<span data-ttu-id="0362a-110">O tipo de nó do gráfico.</span><span class="sxs-lookup"><span data-stu-id="0362a-110">The type of graph node.</span></span> <span data-ttu-id="0362a-111">Consulte [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) para obter os tipos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0362a-111">See [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) for available types.</span></span>


`Desc`

<span data-ttu-id="0362a-112">Tipo: \_ \_ tamanho \_ do campo ( \_ Inexpressible \_ ("dependente do tipo de nó")) **const void \***</span><span class="sxs-lookup"><span data-stu-id="0362a-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on node type")) **const void\***</span></span>

<span data-ttu-id="0362a-113">Um ponteiro para a descrição do nó do gráfico.</span><span class="sxs-lookup"><span data-stu-id="0362a-113">A pointer to the graph node description.</span></span> <span data-ttu-id="0362a-114">O tipo de estrutura apontada deve corresponder ao valor especificado em *tipo*.</span><span class="sxs-lookup"><span data-stu-id="0362a-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="0362a-115">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="0362a-115">Availability</span></span>

<span data-ttu-id="0362a-116">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="0362a-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="0362a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0362a-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0362a-118">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="0362a-118">**Header**</span></span> | <span data-ttu-id="0362a-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="0362a-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="0362a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0362a-120">See also</span></span>

* [<span data-ttu-id="0362a-121">Método IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="0362a-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="0362a-122">Estrutura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="0362a-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)