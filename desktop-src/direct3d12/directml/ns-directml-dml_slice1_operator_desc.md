---
UID: NS:directml.DML_SLICE1_OPERATOR_DESC
title: DML_SLICE1_OPERATOR_DESC
description: Extrai uma única subregião (uma "fatia") de um tensor de entrada.
helpviewer_keywords:
- DML_SLICE1_OPERATOR_DESC
- DML_SLICE1_OPERATOR_DESC structure
- direct3d12.dml_slice1_operator_desc
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
- directml/DML_SLICE1_OPERATOR_DESC
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
- DML_SLICE1_OPERATOR_DESC
ms.openlocfilehash: 06721a7484426eb293494156a2ec23db6fbf0a6b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105808402"
---
# <a name="dml_slice1_operator_desc-structure-directmlh"></a>Estrutura de DML_SLICE1_OPERATOR_DESC (directml. h)
Extrai uma única subregião (uma "fatia") de um tensor de entrada.

A *janela de entrada* descreve os limites do tensor de entrada a ser considerado na fatia. A janela é definida usando três valores para cada dimensão.

- O *deslocamento* marca o *início da janela* em uma dimensão.
- O *tamanho* marca a extensão da janela em uma dimensão. O *final da janela* em uma dimensão é `offset + size - 1` .
- O *Stride* indica como atravessar os elementos em uma dimensão.
  - A magnitude do Stride indica a quantidade de elementos a serem adiantados ao copiar dentro da janela.
  - Se um stride for positivo, os elementos serão copiados começando no *início* da janela na dimensão.
  - Se um stride for negativo, os elementos serão copiados começando no *final* da janela na dimensão.

O pseudocódigo a seguir ilustra como os elementos são copiados usando a janela de entrada. Observe como os elementos em uma dimensão são copiados do início ao fim com um stride positivo e copiados de end para Start com um stride negativo.

```
CopyStart = InputWindowOffsets
for dimension i in [0, DimensionCount - 1]:
    if InputWindowStrides[i] < 0:
        CopyStart[i] += InputWindowSizes[i] - 1 // start at the end of the window in this dimension

OutputTensor[OutputCoordinates] = InputTensor[CopyStart + InputWindowStrides * OutputCoordinates]
```

A janela de entrada não deve estar vazia em qualquer dimensão e a janela não deve se estende além das dimensões da entrada tensor (as leituras fora de limites não são permitidas). O tamanho da janela e os passos limitam efetivamente o número de elementos que podem ser copiados de cada dimensão `i` do tensor de entrada.

```
MaxCopiedElements[i] = 1 + (InputWindowSize[i] - 1) / InputWindowStrides[i]
```

O tensor de saída não é necessário para copiar todos os elementos acessíveis dentro da janela. A fatia é válida desde que `1 <= OutputSizes[i] <= MaxCopiedElements[i]` .

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_SLICE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *InputWindowOffsets;
  const UINT            *InputWindowSizes;
  const INT             *InputWindowStrides;
};
```



## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor para extrair fatias.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor para gravar os resultados de dados na segmentação.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões. Este campo determina o tamanho das matrizes *InputWindowOffsets*, *InputWindowSizes* e *InputWindowStrides* . Esse valor deve corresponder ao *DimensionCount* dos tempos de entrada e de saída. Esse valor deve estar entre 1 e 8, inclusivamente, a partir de `DML_FEATURE_LEVEL_3_0` ; os níveis de recursos anteriores exigem um valor de 4 ou 5.


`InputWindowOffsets`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Uma matriz que contém o início (em elementos) da janela de entrada em cada dimensão. Os valores na matriz devem atender à restrição `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowSizes`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Uma matriz que contém a extensão (em elementos) da janela de entrada em cada dimensão. Os valores na matriz devem atender à restrição `InputWindowOffsets[i] + InputWindowSizes[i] <= InputTensor.Sizes[i]`


`InputWindowStrides`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Uma matriz que contém a distância da fatia ao longo de cada dimensão da entrada tensor, em elementos. A magnitude do Stride indica a quantidade de elementos a serem adiantados ao copiar dentro da janela de entrada. O sinal do Stride determina se os elementos são copiados começando no início da janela (STRIDE positivo) ou no final da janela (STRIDE negativo). Os progressos não podem ser 0.

## <a name="examples"></a>Exemplos

Os exemplos a seguir usam esse mesmo tensor de entrada.

```
InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[ 1,  2,  3,  4],
   [ 5,  6,  7,  8],
   [ 9, 10, 11, 12],
   [13, 14, 15, 16]]]]
```

### <a name="example-1-strided-slice-with-positive-strides"></a>Exemplo 1. Fatias encorridas com progressos positivos

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, 2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[ 2,  4],
   [10, 12]]]]
```

Os elementos copiados são calculados da seguinte maneira. 
```
Output[0,0,0,0] = {0,0,0,1} + {1,1,2,2} * {0,0,0,0} = Input[{0,0,0,1}] = 2
Output[0,0,0,1] = {0,0,0,1} + {1,1,2,2} * {0,0,0,1} = Input[{0,0,0,3}] = 4
Output[0,0,1,0] = {0,0,0,1} + {1,1,2,2} * {0,0,1,0} = Input[{0,0,2,1}] = 10
Output[0,0,1,1] = {0,0,0,1} + {1,1,2,2} * {0,0,1,1} = Input[{0,0,2,3}] = 12
```

### <a name="example-2-strided-slice-with-negative-strides"></a>Exemplo 2. Fatia em um intervalo com avanços negativos

```
InputWindowOffsets = {0, 0, 0, 1}
InputWindowSizes   = {1, 1, 4, 3}
InputWindowStrides = {1, 1, -2, 2}

OutputTensor: (Sizes:{1, 1, 2, 2}, DataType:FLOAT32)
[[[[14, 16],
   [ 6,  8]]]]
```

Lembre-se de que as dimensões com os passos negativos da janela começam a copiar no final da janela de entrada para essa dimensão; Isso é feito adicionando `InputWindowSize[i] - 1` ao deslocamento da janela. As dimensões com um stride positivo simplesmente começam em `InputWindowOffset[i]` .
- O eixo 0 ( `+1` Stride da janela) começa a copiar em `InputWindowOffsets[0] = 0` . 
- O eixo 1 ( `+1` Stride da janela) começa a copiar em `InputWindowOffsets[1] = 0` . 
- O eixo 2 ( `-2` Stride da janela) começa a copiar em `InputWindowOffsets[2] + InputWindowSizes[0] - 1 = 0 + 4 - 1 = 3` . 
- O eixo 3 ( `+2` Stride da janela) começa a copiar em `InputWindowOffsets[3] = 1` . 

Os elementos copiados são calculados da seguinte maneira. 
```
Output[0,0,0,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,0} = Input[{0,0,3,1}] = 14
Output[0,0,0,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,0,1} = Input[{0,0,3,3}] = 16
Output[0,0,1,0] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,0} = Input[{0,0,1,1}] = 6
Output[0,0,1,1] = {0,0,3,1} + {1,1,-2,2} * {0,0,1,1} = Input[{0,0,1,3}] = 8
```


## <a name="remarks"></a>Comentários
Esse operador é semelhante a [DML_SLICE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_slice_operator_desc), mas difere de duas maneiras importantes.

- As sobremedidas de fatias podem ser negativas, o que permite reverter valores ao longo de dimensões.
- Os tamanhos de janela de entrada não são necessariamente os mesmos que os tamanhos de tensor de saída.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados* e *DimensionCount*.

## <a name="tensor-support"></a>Suporte do tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |