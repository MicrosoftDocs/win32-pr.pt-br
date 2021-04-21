---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Coleta elementos do tensor de entrada, usando os índices tensor para remapear índices para subblocos inteiros da entrada. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802898"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>Estrutura de DML_GATHER_ND_OPERATOR_DESC (directml. h)

Coleta elementos do tensor de entrada, usando os índices tensor para remapear índices para subblocos inteiros da entrada. Esse operador executa o pseudocódigo a seguir, onde "..." representa uma série de coordenadas, com o comportamento exato dependente da contagem de dimensões de entrada e de índices.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
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

O tensor para gravar os resultados. O *DimensionCount* e o *tipo de dados* desse tensor devem corresponder a *InputTensor. DimensionCount*. Os tamanhos esperados *OutputTensor* são a concatenação do *IndicesTensor. tamanhos* principais segmentos e *InputTensor. tamanhos* segmento à direita para produzir:

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

As dimensões de saída são alinhadas à direita, com os 1 valores iniciais precedidos, se necessário, para atender a *OutputTensor. DimensionCount*.

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

## <a name="examples"></a>Exemplos

### <a name="example-1-1d-remapping"></a>Exemplo 1. remapeamento 1D

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a>Exemplo 2. remapeamento de 2D

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a>Comentários
Uma versão mais recente desse operador, `DML_OPERATOR_GATHER_ND1` , foi introduzida no `DML_FEATURE_LEVEL_3_0` .

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *IndicesTensor*, *InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.
* *InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 4 | UINT32 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |
