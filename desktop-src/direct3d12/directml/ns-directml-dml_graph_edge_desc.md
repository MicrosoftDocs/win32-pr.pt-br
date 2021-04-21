---
UID: NS:directml.DML_GRAPH_EDGE_DESC
title: DML_GRAPH_EDGE_DESC
description: 'Um contêiner genérico para uma conexão em um grafo de operadores DirectML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_GRAPH_EDGE_DESC
- DML_GRAPH_EDGE_DESC structure
- direct3d12.dml_graph_edge_desc
- directml/DML_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_DESC, DML_GRAPH_EDGE_DESC structure, direct3d12.dml_graph_edge_desc, directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
- directml/DML_GRAPH_EDGE_DESC
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
- DML_GRAPH_EDGE_DESC
ms.openlocfilehash: 58cdf22dd85b1464d68cf1db75ff47a34817514c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802921"
---
# <a name="dml_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="ee9bf-103">Estrutura de DML_GRAPH_EDGE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="ee9bf-103">DML_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="ee9bf-104">Um contêiner genérico para uma conexão em um grafo de operadores DirectML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="ee9bf-104">A generic container for a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee9bf-105">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ee9bf-106">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="ee9bf-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9bf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee9bf-107">Syntax</span></span>
```cpp
struct DML_GRAPH_EDGE_DESC {
  DML_GRAPH_EDGE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a><span data-ttu-id="ee9bf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ee9bf-108">Members</span></span>

`Type`

<span data-ttu-id="ee9bf-109">Tipo: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-109">Type: **[DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md)**</span></span>

<span data-ttu-id="ee9bf-110">O tipo de borda do gráfico.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-110">The type of graph edge.</span></span> <span data-ttu-id="ee9bf-111">Consulte [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) para os tipos disponíveis e [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) para onde usar cada tipo.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-111">See [DML_GRAPH_EDGE_TYPE](./ne-directml-dml_graph_edge_type.md) for available types, and [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) for where to use each type.</span></span>


`Desc`

<span data-ttu-id="ee9bf-112">Tipo: \_ \_ tamanho \_ do campo ( \_ Inexpressible \_ ("dependente do tipo de borda")) **const void \***</span><span class="sxs-lookup"><span data-stu-id="ee9bf-112">Type: \_Field\_size\_(\_Inexpressible\_("Dependent on edge type")) **const void\***</span></span>

<span data-ttu-id="ee9bf-113">Um ponteiro para a descrição do gráfico de borda.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-113">A pointer to the graph edge description.</span></span> <span data-ttu-id="ee9bf-114">O tipo de estrutura apontada deve corresponder ao valor especificado em *tipo*.</span><span class="sxs-lookup"><span data-stu-id="ee9bf-114">The type of the pointed-to struct must match the value specified in *Type*.</span></span>

## <a name="availability"></a><span data-ttu-id="ee9bf-115">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="ee9bf-115">Availability</span></span>

<span data-ttu-id="ee9bf-116">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="ee9bf-116">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="ee9bf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee9bf-117">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ee9bf-118">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="ee9bf-118">**Header**</span></span> | <span data-ttu-id="ee9bf-119">directml. h</span><span class="sxs-lookup"><span data-stu-id="ee9bf-119">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="ee9bf-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee9bf-120">See also</span></span>

* [<span data-ttu-id="ee9bf-121">Método IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="ee9bf-121">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="ee9bf-122">Estrutura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="ee9bf-122">DML_GRAPH_DESC structure</span></span>](./ns-directml-dml_graph_desc.md)