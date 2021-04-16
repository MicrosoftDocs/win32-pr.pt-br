---
UID: NS:directml.DML_SPACE_TO_DEPTH1_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH1_OPERATOR_DESC
description: Reorganiza blocos de dados espaciais em profundidade. O operador gera uma cópia do tensor de entrada, onde os valores das dimensões de altura e largura são movidos para a dimensão de profundidade.
helpviewer_keywords:
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure
- direct3d12.dml_space_to_depth1_operator_desc
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.openlocfilehash: 9c5033440e65dacdcb815edd08994b79a5fae41a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105772763"
---
# <a name="dml_space_to_depth1_operator_desc-structure-directmlh"></a>Estrutura de DML_SPACE_TO_DEPTH1_OPERATOR_DESC (directml. h)
Reorganiza blocos de dados espaciais em profundidade. O operador gera uma cópia do tensor de entrada, onde os valores das dimensões de altura e largura são movidos para a dimensão de profundidade.

Esta é a transformação inversa de [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_SPACE_TO_DEPTH1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor do qual ler. As dimensões do tensor de entrada são `{ Batch, Channels, Height, Width }` .


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor para gravar os resultados. As dimensões de saída do tensor são `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }` .


`BlockSize`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

A largura e a altura dos blocos que são movidos.


`Order`

Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**

Consulte [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).

## <a name="examples"></a>Exemplos

### <a name="example-1-depth-column-row-order"></a>Exemplo 1. Profundidade-coluna-ordem de linha

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]

OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a>Exemplo 2. Ordem de profundidade de linha de coluna

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```


## <a name="remarks"></a>Comentários
Quando o parâmetro *Order* é definido como [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), esse operador é equivalente a [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Dimensões | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |