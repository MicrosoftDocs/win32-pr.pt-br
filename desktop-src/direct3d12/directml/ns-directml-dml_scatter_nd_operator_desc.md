---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia todo o tensor de entrada para a saída e, em seguida, substitui índices selecionados por valores correspondentes das atualizações tensor.
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105773939"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>Estrutura de DML_SCATTER_ND_OPERATOR_DESC (directml. h)
Copia todo o tensor de entrada para a saída e, em seguida, substitui índices selecionados por valores correspondentes das atualizações tensor. Esse operador executa o pseudocódigo a seguir, onde "..." representa uma série de coordenadas, com o comportamento exato determinado pelo eixo e pelo tamanho dos índices.

```
output = input
output[indices[...]] = updates[...]
```

Se dois índices de elementos de saída se sobrepõem (que é inválido), não há garantia de qual última gravação vence.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
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

Um tensor que contém os índices. O *DimensionCount* desse tensor deve corresponder a *InputTensor. DimensionCount*. A última dimensão de *IndicesTensor* é, na verdade, o número de coordenadas por tupla de índice e não deve excede *InputTensor. DimensionCount*. Por exemplo, um tensor de índices de tamanho `{1,4,5,2}` com *IndicesDimensionCount* = 3 significa uma matriz 4x5 de tuplas de coordenadas de 2 valores que são indexadas em *InputTensor*.

A partir do `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral assinado com este tensor. Os índices negativos são interpretados como sendo relativos ao final da respectiva dimensão. Por exemplo, um índice de-1 se refere ao último elemento ao longo dessa dimensão.


`UpdatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os novos valores para substituir os valores de entrada existentes nos índices correspondentes. O *DimensionCount* desse tensor deve corresponder a *InputTensor. DimensionCount*. Os tamanhos esperados *UpdatesTensor* são a concatenação do *IndicesTensor. tamanhos* principais segmentos e *InputTensor. tamanhos* segmento à direita para produzir o seguinte.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

As dimensões são alinhadas à direita, com os 1 valores iniciais precedidos, se necessário, para atender a *UpdatesTensor. DimensionCount*.

Aqui está um exemplo.

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor para gravar os resultados. Os *tamanhos* e o *tipo de dados* deste tensor devem corresponder a *InputTensor. Sizes*.


`InputDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de entrada reais dentro do *InputTensor* depois de ignorar qualquer ponto à esquerda irrelevante, variando [1, *InputTensor. DimensionCount*). Por exemplo, dado *InputTensor. Sizes* = {1,1,4,6} e *InputDimensionCount* = 3, os índices significativos reais são {1,4,6} .


`IndicesDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de índice reais dentro do *IndicesTensor* depois de ignorar qualquer ponto de entrelinha irrelevante, variando [1, *IndicesTensor. DimensionCount*). Por exemplo, dado *IndicesTensor. Sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, os índices significativos reais são {1,4,6} .

## <a name="examples"></a>Exemplos

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *IndicesTensor*, *InputTensor*, *OutputTensor* e `UpdatesTensor` devem ter o mesmo *DimensionCount*.
* *InputTensor*, *OutputTensor* e `UpdatesTensor` deve ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 1 a 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 4 | UINT32 |
| UpdatesTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |