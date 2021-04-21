---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: 'Descreve uma conexão em um grafo de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Essa estrutura é usada para definir uma conexão entre nós internos.'
helpviewer_keywords:
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- DML_INTERMEDIATE_GRAPH_EDGE_DESC structure
- direct3d12.dml_intermediate_graph_edge_desc
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INTERMEDIATE_GRAPH_EDGE_DESC, DML_INTERMEDIATE_GRAPH_EDGE_DESC structure, direct3d12.dml_intermediate_graph_edge_desc, directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.openlocfilehash: 17cf62def075e84ba86e97a5adfa48fb452f475e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802851"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="40fab-104">Estrutura de DML_INTERMEDIATE_GRAPH_EDGE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="40fab-104">DML_INTERMEDIATE_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="40fab-105">Descreve uma conexão em um grafo de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="40fab-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="40fab-106">Essa estrutura é usada para definir uma conexão entre nós internos.</span><span class="sxs-lookup"><span data-stu-id="40fab-106">This structure is used to define a connection between internal nodes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40fab-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="40fab-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="40fab-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="40fab-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40fab-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40fab-109">Syntax</span></span>
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="40fab-110">Membros</span><span class="sxs-lookup"><span data-stu-id="40fab-110">Members</span></span>

`FromNodeIndex`

<span data-ttu-id="40fab-111">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40fab-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="40fab-112">O índice do nó do grafo do qual uma conexão com outro nó é especificada.</span><span class="sxs-lookup"><span data-stu-id="40fab-112">The index of the graph node from which a connection to another node is specified.</span></span>


`FromNodeOutputIndex`

<span data-ttu-id="40fab-113">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40fab-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="40fab-114">O índice da saída no nó no índice *FromNodeIndex* em que a conexão é especificada.</span><span class="sxs-lookup"><span data-stu-id="40fab-114">The index of the output on the node at index *FromNodeIndex* where the connection is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="40fab-115">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40fab-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="40fab-116">O índice do nó do grafo no qual uma conexão de outro nó é especificada.</span><span class="sxs-lookup"><span data-stu-id="40fab-116">The index of the graph node into which a connection from another node is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="40fab-117">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="40fab-117">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="40fab-118">O índice da entrada no nó no índice *ToNodeIndex* em que a conexão é especificada.</span><span class="sxs-lookup"><span data-stu-id="40fab-118">The index of the input on the node at index *ToNodeIndex* where the connection is specified.</span></span>


`Name`

<span data-ttu-id="40fab-119">Tipo: \_ campo \_ z \_ \_ \_ **Maybenull const \***</span><span class="sxs-lookup"><span data-stu-id="40fab-119">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="40fab-120">Um nome opcional para a conexão do grafo.</span><span class="sxs-lookup"><span data-stu-id="40fab-120">An optional name for the graph connection.</span></span> <span data-ttu-id="40fab-121">Se fornecido, isso pode ser usado em determinadas mensagens de erro emitidas pela camada de depuração DirectML.</span><span class="sxs-lookup"><span data-stu-id="40fab-121">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="40fab-122">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="40fab-122">Availability</span></span>

<span data-ttu-id="40fab-123">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="40fab-123">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="40fab-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40fab-124">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="40fab-125">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="40fab-125">**Header**</span></span> | <span data-ttu-id="40fab-126">directml. h</span><span class="sxs-lookup"><span data-stu-id="40fab-126">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="40fab-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="40fab-127">See also</span></span>

* [<span data-ttu-id="40fab-128">Método IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="40fab-128">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="40fab-129">Estrutura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="40fab-129">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="40fab-130">Estrutura de DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="40fab-130">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)