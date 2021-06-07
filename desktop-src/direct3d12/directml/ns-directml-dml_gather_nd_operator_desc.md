---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Coleta elementos do tensor de entrada, usando o tensor de índices para remapear índices para subbloqueios inteiros da entrada. | DML_GATHER_ND_OPERATOR_DESC
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
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416957"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>DML_GATHER_ND_OPERATOR_DESC estrutura (directml.h)

Coleta elementos do tensor de entrada, usando o tensor de índices para remapear índices para subbloqueios inteiros da entrada. Esse operador executa o seguinte pseudocódigo, em que "..." representa uma série de coordenadas, com o comportamento exato dependente da contagem de dimensões de entrada e índices.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

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

O tensor do o que ler.


`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor que contém os índices. O *DimensionCount* desse tensor deve corresponder *a InputTensor.DimensionCount.* A última dimensão do *IndicesTensor* é, na verdade, o número de coordenadas por tupla de índice e não pode exceder *InputTensor.DimensionCount.* Por exemplo, um tensor de índices de *Tamanhos* com `{1,4,5,2}` *IndicesDimensionCount* = 3 significa uma matriz 4x5 de tuplas de duas coordenadas que são indexadas em *InputTensor*.

Começando com `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral com sinal com esse tensor. Índices negativos são interpretados como sendo relativos ao final da respectiva dimensão. Por exemplo, um índice de -1 refere-se ao último elemento ao longo dessa dimensão.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor no que gravar os resultados. O *DimensionCount* e *o DataType* desse tensor devem corresponder *a InputTensor.DimensionCount.* O *OutputTensor.Sizes* esperado é a concatenação dos segmentos à frente *DedicesTensor.Sizes* e *InputTensor.Sizes* à frente para produzir:

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

As dimensões de saída são alinhadas à direita, com 1 valores à direita pré-anexados, se necessário, para atender a *OutputTensor.DimensionCount.*

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

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de entrada reais no *InputTensor* depois de ignorar quaisquer dimensões à frente irrelevantes, variando `[1, *InputTensor.DimensionCount*]` . Por exemplo, dado *InputTensor.Sizes*  =  `{1,1,4,6}` e = `InputDimensionCount` 3, os índices significativos reais são `{1,4,6}` .


`IndicesDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de índice reais dentro do *IndicesTensor* depois de ignorar quaisquer dimensões principais irrelevantes, variando [1, *IndicesTensor.DimensionCount*]. Por exemplo, dado *IndicesTensor.Sizes*  =  `{1,1,4,6}` e *IndicesDimensionCount* = 3, os índices significativos reais são `{1,4,6}` .

## <a name="examples"></a>Exemplos

### <a name="example-1-1d-remapping"></a>Exemplo 1. Remapeamento 1D

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

### <a name="example-2-2d-remapping"></a>Exemplo 2. Remapeamento 2D

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

## <a name="tensor-constraints"></a>Restrições do Tensor
* *IndicesTensor,* *InputTensor* e *OutputTensor* devem ter o *mesmo DimensionCount*.
* *InputTensor* e *OutputTensor* devem ter o mesmo *DataType*.

## <a name="tensor-support"></a>Suporte do Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e superior
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e superior
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 4 | UINT32 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |
