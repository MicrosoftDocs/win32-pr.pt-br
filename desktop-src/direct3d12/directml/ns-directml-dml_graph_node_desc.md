---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: Um contêiner genérico para um nó dentro de um grafo de operadores DirectML definidos [por DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passados para [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
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
ms.openlocfilehash: 5f59978f6b62572000a95ee3be5a3b8a685c8231
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417003"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a>DML_GRAPH_NODE_DESC estrutura (directml.h)
Um contêiner genérico para um nó dentro de um grafo de operadores DirectML definidos [por DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) e passados para [IDMLDevice1::CompileGraph.](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_GRAPH_NODE_DESC {
  DML_GRAPH_NODE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>Membros

`Type`

Tipo: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**

O tipo de nó de grafo. Consulte [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) para ver os tipos disponíveis.


`Desc`

Tipo: \_ Tamanho do campo ( \_ \_ \_ Inexpressível \_ ("Dependente do tipo de nó")) **const void \***

Um ponteiro para a descrição do nó do grafo. O tipo do struct apontado deve corresponder ao valor especificado em *Tipo*.

## <a name="availability"></a>Disponibilidade

Essa API foi introduzida na versão do `1.1.0` DirectML.



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |

## <a name="see-also"></a>Confira também

* [Método IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC estrutura](./ns-directml-dml_graph_desc.md)