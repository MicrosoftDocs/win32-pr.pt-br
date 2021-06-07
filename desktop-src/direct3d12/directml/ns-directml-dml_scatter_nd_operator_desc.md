---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia todo o tensor de entrada para a saída e, em seguida, substitui os índices selecionados com valores correspondentes do tensor de atualizações.
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
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416985"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>DML_SCATTER_ND_OPERATOR_DESC estrutura (directml.h)
Copia todo o tensor de entrada para a saída e, em seguida, substitui os índices selecionados com valores correspondentes do tensor de atualizações. Esse operador executa o seguinte pseudocódigo, em que "..." representa uma série de coordenadas, com o comportamento exato determinado pelo tamanho do eixo e dos índices.

```
output = input
output[indices[...]] = updates[...]
```

Se dois índices de elemento de saída se sobrepõem (o que é inválido), não há nenhuma garantia de qual última gravação vence.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

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

O tensor do o que ler.


`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os índices. O *DimensionCount* desse tensor deve corresponder *a InputTensor.DimensionCount.* A última dimensão do *IndicesTensor* é, na verdade, o número de coordenadas por tupla de índice e não deve exceder *InputTensor.DimensionCount*. Por exemplo, um tensor de índices de tamanho com `{1,4,5,2}` *IndicesDimensionCount* = 3 significa uma matriz 4x5 de tuplas de coordenadas de 2 valores que são indexadas em *InputTensor*.

Começando com `DML_FEATURE_LEVEL_3_0` , esse operador dá suporte a valores de índice negativos ao usar um tipo integral com sinal com esse tensor. Índices negativos são interpretados como sendo relativos ao final da respectiva dimensão. Por exemplo, um índice de -1 refere-se ao último elemento ao longo dessa dimensão.


`UpdatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os novos valores para substituir os valores de entrada existentes nos índices correspondentes. O *DimensionCount* desse tensor deve corresponder *a InputTensor.DimensionCount.* Os *updatesTensor.Sizes* esperados são a concatenação dos segmentos à frente *IndicesTensor.Sizes* e *InputTensor.Sizes* à frente para produzir o seguinte.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

As dimensões são alinhadas à direita, com os valores 1 à direita pré-anexados, se necessário, para atender *a UpdatesTensor.DimensionCount.*

Veja um exemplo.

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

O tensor no que gravar os resultados. Os *Tamanhos* e *o DataType* desse tensor devem corresponder *a InputTensor.Sizes.*


`InputDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de entrada reais dentro do *InputTensor* depois de ignorar quaisquer dimensões irrelevantes à frente, variando [1, *InputTensor.DimensionCount*). Por exemplo, dado *InputTensor.Sizes* = {1,1,4,6} e *InputDimensionCount* = 3, os índices significativos reais são {1,4,6} .


`IndicesDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de dimensões de índice reais dentro do *IndicesTensor* depois de ignorar quaisquer dimensões irrelevantes à frente, variando [1, *IndicesTensor.DimensionCount*). Por exemplo, dado *IndicesTensor.Sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, os índices significativos reais são {1,4,6} .

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

## <a name="tensor-constraints"></a>Restrições do Tensor
* *IndicesTensor*, *InputTensor,* *OutputTensor* e `UpdatesTensor` devem ter o mesmo *DimensionCount*.
* *InputTensor,* *OutputTensor* e `UpdatesTensor` devem ter o mesmo *DataType*.

## <a name="tensor-support"></a>Suporte do Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e superior
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 1 a 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e superior
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 4 | UINT32 |
| UpdatesTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |