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
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417006"
---
# <a name="dml_graph_desc-structure-directmlh"></a>Estrutura de DML_GRAPH_DESC (directml. h)

Descreve um grafo de operadores DirectML usados para compilar um operador combinado e otimizado. Consulte [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
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



## <a name="members"></a>Membros

`InputCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de entradas do grafo geral. Cada entrada de grafo pode ser conectada a um número variável de nós internos, portanto, isso pode ser diferente de *InputEdgeCount*.


`OutputCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de saídas do grafo geral. Cada saída de grafo pode ser conectada a um número variável de nós internos, portanto, isso pode ser diferente de *OutputEdgeCount*.


`NodeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de nós internos no grafo.


`Nodes`

Tipo: \_ \_ \_ NodeCount (tamanho do campo) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Os nós internos no grafo.


`InputEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de conexões entre entradas de grafo e entradas de nós internos no grafo.


`InputEdges`

Tipo: \_ \_ \_ InputEdgeCount (tamanho do campo) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Uma matriz de conexões entre entradas de grafo e entradas de nós internos no grafo. O campo de *tipo* dentro de cada elemento deve ser definido como [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).


`OutputEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de conexões entre saídas de grafo e saídas de nós internos no grafo.


`OutputEdges`

Tipo: \_ \_ \_ OutputEdgeCount (tamanho do campo) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Uma matriz de conexões entre saídas de grafo e saídas de nós internos no grafo. O campo de *tipo* dentro de cada elemento deve ser definido como [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).


`IntermediateEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de conexões internas entre os nós no grafo.


`IntermediateEdges`

Tipo: \_ \_ \_ IntermediateEdgeCount (tamanho do campo) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Uma matriz de conexões entre entradas e saídas de nós internos no grafo. O campo de tipo dentro de cada elemento deve ser definido como [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Comentários
O grafo descrito por essa estrutura deve ser um grafo acíclico direcionado. Você deve definir uma conexão para a entrada e a saída de cada nó fornecido, exceto para entradas e saídas opcionais para o operador associado.

Os nós podem usar operadores que foram criados usando o sinalizador [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) para determinadas entradas. Qualquer entrada de operador que use esse sinalizador deve estar conectada a entradas de grafo. Todas as entradas de operador conectadas à mesma entrada de grafo devem usar ou omitir esse sinalizador de maneira equivalente.

É legal conectar operadores cujas entradas e saídas conectadas usem contagens de dimensão, tamanhos e tipos de dados diferentes. Isso implica que o blob de dados tensor é interpretado de forma diferente por cada operador. No entanto, o campo *TotalTensorSizeInBytes* de entradas e saídas de tensor conectadas deve ser idêntico. Os operadores só devem ler regiões de dezenases escritas por operadores anteriores. Não há garantia de que as regiões de preenchimento na saída de uma operação (resultantes do uso de progressos) sejam lidas como zero por operadores de fluxo inativos.

## <a name="availability"></a>Disponibilidade

Essa API foi introduzida na versão DirectML `1.1.0` .


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |

## <a name="see-also"></a>Confira também

* [Método IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_NODE_DESC struct](./ns-directml-dml_graph_node_desc.md)
* [DML_GRAPH_EDGE_DESC struct](./ns-directml-dml_graph_edge_desc.md)