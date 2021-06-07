---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: 'Descreve uma conexão em um grafo de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Essa estrutura é usada para definir uma conexão de uma entrada de grafo para uma entrada de um nó interno.'
helpviewer_keywords:
- DML_INPUT_GRAPH_EDGE_DESC
- DML_INPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_input_graph_edge_desc
- directml/DML_INPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
- directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 00fcece76f4cb7ac46589914df4d74321d957fbc
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416916"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="a5895-104">Estrutura de DML_INPUT_GRAPH_EDGE_DESC (directml. h)</span><span class="sxs-lookup"><span data-stu-id="a5895-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="a5895-105">Descreve uma conexão em um grafo de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="a5895-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="a5895-106">Essa estrutura é usada para definir uma conexão de uma entrada de grafo para uma entrada de um nó interno.</span><span class="sxs-lookup"><span data-stu-id="a5895-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5895-107">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a5895-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="a5895-108">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a5895-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5895-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5895-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="a5895-110">Membros</span><span class="sxs-lookup"><span data-stu-id="a5895-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="a5895-111">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5895-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="a5895-112">O índice da entrada do grafo do qual uma conexão com uma entrada de nó interno é especificada.</span><span class="sxs-lookup"><span data-stu-id="a5895-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="a5895-113">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5895-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="a5895-114">O índice do nó interno no qual a conexão da entrada do grafo é especificada.</span><span class="sxs-lookup"><span data-stu-id="a5895-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="a5895-115">Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a5895-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="a5895-116">O índice da entrada no nó interno onde a conexão é especificada.</span><span class="sxs-lookup"><span data-stu-id="a5895-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="a5895-117">Tipo: \_ campo \_ z \_ \_ \_ **Maybenull const \***</span><span class="sxs-lookup"><span data-stu-id="a5895-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="a5895-118">Um nome opcional para a conexão do grafo.</span><span class="sxs-lookup"><span data-stu-id="a5895-118">An optional name for the graph connection.</span></span> <span data-ttu-id="a5895-119">Se fornecido, isso pode ser usado em determinadas mensagens de erro emitidas pela camada de depuração DirectML.</span><span class="sxs-lookup"><span data-stu-id="a5895-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="a5895-120">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="a5895-120">Availability</span></span>

<span data-ttu-id="a5895-121">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="a5895-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="a5895-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5895-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a5895-123">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a5895-123">**Header**</span></span> | <span data-ttu-id="a5895-124">directml. h</span><span class="sxs-lookup"><span data-stu-id="a5895-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="a5895-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5895-125">See also</span></span>

* [<span data-ttu-id="a5895-126">Método IDMLDevice1:: CompileGraph</span><span class="sxs-lookup"><span data-stu-id="a5895-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="a5895-127">Estrutura de DML_GRAPH_DESC</span><span class="sxs-lookup"><span data-stu-id="a5895-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="a5895-128">Estrutura de DML_GRAPH_EDGE_DESC</span><span class="sxs-lookup"><span data-stu-id="a5895-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)