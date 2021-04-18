---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Descreve um grafo de operadores DirectML usados para compilar um operador combinado e otimizado.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105780759"
---
# <a name="dml_graph_desc-structure-directmlh"></a><span data-ttu-id="7dd81-103">Estrutura de DML_GRAPH_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="7dd81-103">DML_GRAPH_DESC structure (directml.h)</span></span>

<span data-ttu-id="7dd81-104">Descreve um grafo de operadores DirectML usados para compilar um operador combinado e otimizado.</span><span class="sxs-lookup"><span data-stu-id="7dd81-104">Describes a graph of DirectML operators used to compile a combined, optimized operator.</span></span> <span data-ttu-id="7dd81-105">Consulte [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="7dd81-105">See [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7dd81-106">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="7dd81-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="7dd81-107">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="7dd81-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd81-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7dd81-108">Syntax</span></span>
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a><span data-ttu-id="7dd81-109">Membros</span><span class="sxs-lookup"><span data-stu-id="7dd81-109">Members</span></span>

`InputCount`

<span data-ttu-id="7dd81-110">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7dd81-110">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7dd81-111">O número de entradas do grafo geral.</span><span class="sxs-lookup"><span data-stu-id="7dd81-111">The number of inputs of the overall graph.</span></span> <span data-ttu-id="7dd81-112">Cada entrada de grafo pode ser conectada a um número variável de nós internos, portanto, isso pode ser diferente de *InputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="7dd81-112">Each graph input may be connected to a variable number of internal nodes, therefore this may be different from *InputEdgeCount*.</span></span>


`OutputCount`

<span data-ttu-id="7dd81-113">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7dd81-113">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7dd81-114">O número de saídas do grafo geral.</span><span class="sxs-lookup"><span data-stu-id="7dd81-114">The number of outputs of the overall graph.</span></span> <span data-ttu-id="7dd81-115">Cada saída de grafo pode ser conectada a um número variável de nós internos, portanto, isso pode ser diferente de *OutputEdgeCount*.</span><span class="sxs-lookup"><span data-stu-id="7dd81-115">Each graph output may be connected to a variable number of internal nodes, therefore this may be different from *OutputEdgeCount*.</span></span>


`NodeCount`

<span data-ttu-id="7dd81-116">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7dd81-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7dd81-117">O número de nós internos no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-117">The number of internal nodes in the graph.</span></span>


`Nodes`

<span data-ttu-id="7dd81-118">Tipo: \_ \_ \_ NodeCount (tamanho do campo) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="7dd81-118">Type: \_Field\_size\_(NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md)\***</span></span>

<span data-ttu-id="7dd81-119">Os nós internos no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-119">The internal nodes in the graph.</span></span>


`InputEdgeCount`

<span data-ttu-id="7dd81-120">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7dd81-120">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7dd81-121">O número de conexões entre entradas de grafo e entradas de nós internos no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-121">The number of connections between graph inputs and inputs of internal nodes in the graph.</span></span>


`InputEdges`

<span data-ttu-id="7dd81-122">Tipo: \_ \_ \_ InputEdgeCount (tamanho do campo) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="7dd81-122">Type: \_Field\_size\_(InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="7dd81-123">Uma matriz de conexões entre entradas de grafo e entradas de nós internos no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-123">An array of connections between graph inputs and inputs of internal nodes in the graph.</span></span> <span data-ttu-id="7dd81-124">O campo de *tipo* dentro de cada elemento deve ser definido como [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="7dd81-124">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`OutputEdgeCount`

<span data-ttu-id="7dd81-125">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7dd81-125">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7dd81-126">O número de conexões entre saídas de grafo e saídas de nós internos no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-126">The number of connections between graph outputs and outputs of internal nodes in the graph.</span></span>


`OutputEdges`

<span data-ttu-id="7dd81-127">Tipo: \_ \_ \_ OutputEdgeCount (tamanho do campo) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="7dd81-127">Type: \_Field\_size\_(OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="7dd81-128">Uma matriz de conexões entre saídas de grafo e saídas de nós internos no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-128">An array of connections between graph outputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="7dd81-129">O campo de *tipo* dentro de cada elemento deve ser definido como [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span><span class="sxs-lookup"><span data-stu-id="7dd81-129">The *Type* field within each element should be set to [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).</span></span>


`IntermediateEdgeCount`

<span data-ttu-id="7dd81-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7dd81-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7dd81-131">O número de conexões internas entre os nós no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-131">The number of internal connections between nodes in the graph.</span></span>


`IntermediateEdges`

<span data-ttu-id="7dd81-132">Tipo: \_ \_ \_ IntermediateEdgeCount (tamanho do campo) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="7dd81-132">Type: \_Field\_size\_(IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)\***</span></span>

<span data-ttu-id="7dd81-133">Uma matriz de conexões entre entradas e saídas de nós internos no grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-133">An array of connections between inputs and outputs of internal nodes in the graph.</span></span> <span data-ttu-id="7dd81-134">O campo de tipo dentro de cada elemento deve ser definido como [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span><span class="sxs-lookup"><span data-stu-id="7dd81-134">The Type field within each element should be set to [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)</span></span>


## <a name="remarks"></a><span data-ttu-id="7dd81-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dd81-135">Remarks</span></span>
<span data-ttu-id="7dd81-136">O grafo descrito por essa estrutura deve ser um grafo acíclico direcionado.</span><span class="sxs-lookup"><span data-stu-id="7dd81-136">The graph described by this structure must be a directed acyclic graph.</span></span> <span data-ttu-id="7dd81-137">Você deve definir uma conexão para a entrada e a saída de cada nó fornecido, exceto para entradas e saídas opcionais para o operador associado.</span><span class="sxs-lookup"><span data-stu-id="7dd81-137">You must define a connection for the input and output of each supplied node, except for inputs and outputs that are optional for the associated operator.</span></span>

<span data-ttu-id="7dd81-138">Os nós podem usar operadores que foram criados usando o sinalizador [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) para determinadas entradas.</span><span class="sxs-lookup"><span data-stu-id="7dd81-138">Nodes may use operators that were created using the [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) flag for certain inputs.</span></span> <span data-ttu-id="7dd81-139">Qualquer entrada de operador que use esse sinalizador deve estar conectada a entradas de grafo.</span><span class="sxs-lookup"><span data-stu-id="7dd81-139">Any operator inputs using this flag must be connected to graph inputs.</span></span> <span data-ttu-id="7dd81-140">Todas as entradas de operador conectadas à mesma entrada de grafo devem usar ou omitir esse sinalizador de maneira equivalente.</span><span class="sxs-lookup"><span data-stu-id="7dd81-140">All operator inputs connected to the same graph input must use or omit this flag equivalently.</span></span>

<span data-ttu-id="7dd81-141">É legal conectar operadores cujas entradas e saídas conectadas usem contagens de dimensão, tamanhos e tipos de dados diferentes.</span><span class="sxs-lookup"><span data-stu-id="7dd81-141">It is legal to connect operators whose connected inputs and outputs use different dimension counts, sizes, and data types.</span></span> <span data-ttu-id="7dd81-142">Isso implica que o blob de dados tensor é interpretado de forma diferente por cada operador.</span><span class="sxs-lookup"><span data-stu-id="7dd81-142">This implies that the tensor data blob is interpreted differently by each operator.</span></span> <span data-ttu-id="7dd81-143">No entanto, o campo *TotalTensorSizeInBytes* de entradas e saídas de tensor conectadas deve ser idêntico.</span><span class="sxs-lookup"><span data-stu-id="7dd81-143">The *TotalTensorSizeInBytes* field of connected tensor inputs and outputs must be identical, though.</span></span> <span data-ttu-id="7dd81-144">Os operadores só devem ler regiões de dezenases escritas por operadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="7dd81-144">Operators should only read regions of tensors written by earlier operators.</span></span> <span data-ttu-id="7dd81-145">Não há garantia de que as regiões de preenchimento na saída de uma operação (resultantes do uso de progressos) sejam lidas como zero por operadores de fluxo inativos.</span><span class="sxs-lookup"><span data-stu-id="7dd81-145">Any padding regions in the output of an operation (resulting from the use of strides) are not guaranteed to be read as zero by down-stream operators.</span></span>

## <a name="availability"></a><span data-ttu-id="7dd81-146">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="7dd81-146">Availability</span></span>

<span data-ttu-id="7dd81-147">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="7dd81-147">This API was introduced in DirectML version `1.1.0`.</span></span>


## <a name="requirements"></a><span data-ttu-id="7dd81-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dd81-148">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7dd81-149">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="7dd81-149">**Header**</span></span> | <span data-ttu-id="7dd81-150">directml. h</span><span class="sxs-lookup"><span data-stu-id="7dd81-150">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="7dd81-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="7dd81-151">See also</span></span>

* [<span data-ttu-id="7dd81-152">Método IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="7dd81-152">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="7dd81-153">DML_GRAPH_NODE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="7dd81-153">DML_GRAPH_NODE_DESC struct</span></span>](./ns-directml-dml_graph_node_desc.md)
* [<span data-ttu-id="7dd81-154">DML_GRAPH_EDGE_DESC struct</span><span class="sxs-lookup"><span data-stu-id="7dd81-154">DML_GRAPH_EDGE_DESC struct</span></span>](./ns-directml-dml_graph_edge_desc.md)