---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Coleta elementos do tensor de entrada, usando os índices tensor para remapear índices para subblocos inteiros da entrada. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802854"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a>Estrutura de DML_GATHER_ND1_OPERATOR_DESC (directml. h)

Coleta elementos do tensor de entrada, usando os índices tensor para remapear índices para subblocos inteiros da entrada. Esse operador executa o pseudocódigo a seguir, onde "..." representa uma série de coordenadas, com o comportamento exato dependente da contagem de dimensões de lote, de entrada e de índices.

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor do qual ler.

`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor que contém os índices. O *DimensionCount* desse tensor deve corresponder a *InputTensor. DimensionCount*. A última dimensão de *IndicesTensor* é, na verdade, o número de coordenadas por tupla de índice e não pode exceder *InputTensor. DimensionCount*. Por exemplo, um tensor de índices de *tamanhos* `{1,4,5,2}` com *IndicesDimensionCount* = 3 significa uma matriz 4x5 de tuplas de duas coordenadas que são indexadas em *InputTensor*.

A partir do `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral assinado com este tensor. Os índices negativos são interpretados como sendo relativos ao final da respectiva dimensão. Por exemplo, um índice de-1 se refere ao último elemento ao longo dessa dimensão.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor para gravar os resultados. O *DimensionCount* e o *tipo de dados* desse tensor devem corresponder a *InputTensor. DimensionCount*. Os tamanhos esperados *OutputTensor* são a concatenação do *IndicesTensor. tamanhos* principais segmentos e *InputTensor. tamanhos* segmento à direita, o que resulta no seguinte.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

As dimensões são alinhadas à direita, com os 1 valores iniciais precedidos, se necessário, para atender a *OutputTensor. DimensionCount*.

Veja um exemplo.

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de entrada reais dentro do *InputTensor* depois de ignorar todas as irrelevantes, variando `[1, *InputTensor.DimensionCount*]` . Por exemplo, dado *InputTensor. Sizes*  =  `{1,1,4,6}` e `InputDimensionCount` = 3, os índices significativos reais são `{1,4,6}` .

`IndicesDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de índice reais dentro do *IndicesTensor* depois de ignorar qualquer ponto de entrelinha irrelevante, variando [1, *IndicesTensor. DimensionCount*]. Por exemplo, dado *IndicesTensor. Sizes*  =  `{1,1,4,6}` e *IndicesDimensionCount* = 3, os índices significativos reais são `{1,4,6}` .

`BatchDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões em cada tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) que são consideradas lotes independentes, variando entre [0, *InputTensor. DimensionCount*) e [0, *IndicesTensor. DimensionCount*). A contagem de lote pode ser 0, implicando um único lote. Por exemplo, dado *IndicesTensor. Sizes*  =  `{1,3,4,5,6,7}` e *IndicesDimensionCount* = 5 e `BatchDimensionCount` = 2, há lotes `{3,4}` e índices significativos `{5,6,7}` .

## <a name="remarks"></a>Comentários
**DML_GATHER_ND1_OPERATOR_DESC** adiciona *BatchDimensionCount* e é equivalente a [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) quando *BatchDimensionCount* = 0.

## <a name="examples"></a>Exemplos

### <a name="example-1-1d-remapping"></a>Exemplo 1. remapeamento 1D

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a>Exemplo 2. remapeamento de 2D com contagem de lote

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *IndicesTensor*, *InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.
* *InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |
