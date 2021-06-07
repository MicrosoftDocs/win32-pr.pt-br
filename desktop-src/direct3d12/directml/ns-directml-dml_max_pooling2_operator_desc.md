---
UID: NS:directml.DML_MAX_POOLING2_OPERATOR_DESC
title: DML_MAX_POOLING2_OPERATOR_DESC
description: Calcula o valor máximo entre os elementos dentro da janela deslizante sobre a entrada tensor e, opcionalmente, retorna os índices dos valores máximos selecionados.
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
- DML_MAX_POOLING2_OPERATOR_DESC
f1_keywords:
- DML_MAX_POOLING2_OPERATOR_DESC
- directml/DML_MAX_POOLING2_OPERATOR_DESC
ms.openlocfilehash: 06e4d7eb01abab9c412238e353a73607df02b219
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416954"
---
# <a name="dml_max_pooling2_operator_desc-structure-directmlh"></a>Estrutura de DML_MAX_POOLING2_OPERATOR_DESC (directml. h)
Calcula o valor máximo entre os elementos dentro da janela deslizante sobre a entrada tensor e, opcionalmente, retorna os índices dos valores máximos selecionados.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_MAX_POOLING2_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  const DML_TENSOR_DESC *OutputIndicesTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *WindowSize;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  const UINT            *Dilations;
};
```



## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de entrada de *tamanhos* `{ BatchCount, ChannelCount, Height, Width }` se *InputTensor. DimensionCount* for 4 e `{ BatchCount, ChannelCount, Depth, Height, Weight } ` se *InputTensor. DimensionCount* for 5.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída para gravar os resultados. Os tamanhos do tensor de saída podem ser computados da seguinte maneira.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
  UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
  OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```


`OutputIndicesTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída opcional de índices para a entrada tensor *InputTensor* dos valores máximos produzidos e armazenados no *OutputTensor*. Esses valores de índice são baseados em zero e tratam o tensor de entrada como uma matriz unidimensional contígua. Quando vários elementos dentro da janela deslizante têm o mesmo valor, os valores iguais posteriores são ignorados e o índice aponta para o primeiro valor encontrado. *OutputTensor* e *OutputIndicesTensor* têm os mesmos tamanhos de tensor.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões espaciais da entrada tensor *InputTensor*, que também corresponde ao número de dimensões da janela deslizante *WindowSize*. Esse valor também determina o tamanho das matrizes de *Preenchentes* *,* *StartPadding* e endpadding. Ele deve ser definido como 2 quando *InputTensor* for 4D e 3 quando for um 5D tensor.


`Strides`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Os avanços para as dimensões de janela deslizante de tamanhos `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.


`WindowSize`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

As dimensões da janela deslizante em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.


`StartPadding`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

O número de elementos de preenchimento a serem aplicados ao início de cada dimensão espacial da entrada tensor *InputTensor*. Os valores estão em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.


`EndPadding`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

O número de elementos de preenchimento a serem aplicados ao final de cada dimensão espacial da entrada tensor *InputTensor*. Os valores estão em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.


`Dilations`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) <b>const [uint](/windows/desktop/winprog/windows-data-types) * </b>

Os valores para cada dimensão espacial da entrada tensor *InputTensor* pelo qual um elemento dentro da janela deslizante é selecionado para cada elemento desse valor. Os valores estão em `{ Height, Width }` quando *DimensionCount* é definido como 2 ou `{ Depth, Height, Width }` quando definido como 3.


## <a name="remarks"></a>Comentários
**DML_MAX_POOLING2_OPERATOR_DESC** substitui a versão anterior [DML_MAX_POOLING_OPERATOR1_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling1_operator_desc) com uma matriz constante adicional *Dilations*. As duas versões são equivalentes quando *Dilations* é definido como `{ 1,1 }` para entrada 4D ou `{ 1,1,1 }` para os recursos de entrada de 5D.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *InputTensor*, *OutputIndicesTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.
* *InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputTensor | Saída | 4 a 5 | FLOAT32, FLOAT16, INT8, UINT8 |
| OutputIndicesTensor | Saída opcional | 4 a 5 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 a 5 | FLOAT32, FLOAT16 |
| OutputTensor | Saída | 4 a 5 | FLOAT32, FLOAT16 |
| OutputIndicesTensor | Saída opcional | 4 a 5 | UINT32 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Windows 10, versão 2004 (10,0; Build 19041) |
| **Servidor mínimo com suporte** | Windows Server, versão 2004 (10,0; Build 19041) |
| **Cabeçalho** | directml. h |