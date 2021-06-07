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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416917"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a>Estrutura de DML_INTERMEDIATE_GRAPH_EDGE_DESC (directml. h)
Descreve uma conexão em um grafo de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) e passado para [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Essa estrutura é usada para definir uma conexão entre nós internos.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Membros

`FromNodeIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

O índice do nó do grafo do qual uma conexão com outro nó é especificada.


`FromNodeOutputIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

O índice da saída no nó no índice *FromNodeIndex* em que a conexão é especificada.


`ToNodeIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

O índice do nó do grafo no qual uma conexão de outro nó é especificada.


`ToNodeInputIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

O índice da entrada no nó no índice *ToNodeIndex* em que a conexão é especificada.


`Name`

Tipo: \_ campo \_ z \_ \_ \_ **Maybenull const \***

Um nome opcional para a conexão do grafo. Se fornecido, isso pode ser usado em determinadas mensagens de erro emitidas pela camada de depuração DirectML.

## <a name="availability"></a>Disponibilidade

Essa API foi introduzida na versão DirectML `1.1.0` .



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |

## <a name="see-also"></a>Confira também

* [Método IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Estrutura de DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [Estrutura de DML_GRAPH_EDGE_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)