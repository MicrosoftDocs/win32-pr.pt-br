---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Executa uma convolução do *FilterTensor* com o *InputTensor*. Esse operador executa a convolução progressiva em dados quantificados. Esse operador é matematicamente equivalente a desquantificar as entradas, convolving e, em seguida, quantificar a saída.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549774"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a>Estrutura de DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC (directml. h)
Executa uma convolução do *FilterTensor* com o *InputTensor*. Esse operador executa a convolução progressiva em dados quantificados. Esse operador é matematicamente equivalente a desquantificar as entradas, convolving e, em seguida, quantificar a saída. 

As funções lineares Quantize usadas por este operador são as funções de quantificação linear

### <a name="dequantize-function"></a>Função de desquantificação

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Função Quantize

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de entrada. As dimensões esperadas do *InputTensor* são `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de escala de entrada. As dimensões esperadas do `InputScaleTensor` são `{ 1, 1, 1, 1 }` . Esse valor de escala é usado para desquantificar os valores de entrada.


`InputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero de entrada. As dimensões esperadas do *InputZeroPointTensor* são `{ 1, 1, 1, 1 }` . Esse valor de ponto zero é usado para rebaixar os valores de entrada.


`FilterTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados do filtro. As dimensões esperadas do *FilterTensor* são `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de escala de filtro. As dimensões esperadas do são se a quantização por tensor for necessária ou se a `FilterScaleTensor` `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` quantização por canal for necessária. Esse valor de escala é usado para rebaixar os valores de filtro.


`FilterZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero do filtro. As dimensões esperadas do *FilterZeroPointTensor* serão se a quantização por tensor for necessária ou se a quantização por `{ 1, 1, 1, 1 }` canal for `{ 1, OutputChannelCount, 1, 1 }` necessária. Esse valor de ponto zero é usado para rebaixar os valores de filtro.


`BiasTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de desvio. O tensor de desvio é um tensor que contém dados que são transmitidos pelo tensor de saída no final da convolução, que é adicionado ao resultado. As dimensões esperadas do BiasTensor são `{ 1, OutputChannelCount, 1, 1 }` para 4D.


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de escala de saída. As dimensões esperadas do OutputScaleTensor são `{ 1, 1, 1, 1 }` . Esse valor de escala de entrada é usado para quantificar os valores de saída de convolução.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero de filtro. As dimensões esperadas do OutputZeroPointTensor são `{ 1, 1, 1, 1 }` . Esse valor de ponto zero de entrada é usado para quantificar a convolução dos valores de saída.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor para gravar os resultados. As dimensões esperadas do OutputTensor são `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de dimensões espaciais para a operação de convolução. Dimensões espaciais são as dimensões inferiores do filtro de convolução tensor *FilterTensor*. Esse valor também determina o tamanho das matrizes de *prerides*, *Dilations*, *StartPadding* e *endpadding* . Há suporte apenas para um valor de 2.


`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

Os passos da operação de convolução. Esses passos são aplicados ao filtro de convolução. Eles são separados dos avanços do tensor incluídos no [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Tipo: \_ Field_size \_ (DimensionCount) **const [uint](../../winprog/windows-data-types.md) \***

O Dilations da operação de convolução. As estruturas são passadas aplicadas aos elementos do kernel de filtro. Isso tem o efeito de simular um kernel de filtro maior ao preenchimento dos elementos do kernel de filtro interno com zeros.


`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Os valores de preenchimento a serem aplicados ao início de cada dimensão espacial do filtro e do tensor de entrada da operação de convolução.


`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Os valores de preenchimento a serem aplicados ao final de cada dimensão espacial do filtro e do tensor de entrada da operação de convolução.


`GroupCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de grupos nos quais dividir a operação de convolução. *GroupCount* pode ser usado para obter a convolução de profundidade definindo *GroupCount* igual à contagem de canais de entrada. Isso divide a convolução em uma convolução separada por canal de entrada. 

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições do Tensor
* *FilterTensor* e *FilterZeroPointTensor* devem ter o mesmo *DataType*.
* *InputTensor* e *InputZeroPointTensor* devem ter o mesmo *DataType*.
* *OutputTensor* `OutputZeroPointTensor` e devem ter o mesmo *DataType*.

## <a name="tensor-support"></a>Suporte do Tensor
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | INT8, UINT8 |
| InputScaleTensor | Entrada | 4 | FLOAT32 |
| InputZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| FilterTensor | Entrada | 4 | INT8, UINT8 |
| FilterScaleTensor | Entrada | 4 | FLOAT32 |
| FilterZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| BiasTensor | Entrada opcional | 4 | INT32 |
| OutputScaleTensor | Entrada | 4 | FLOAT32 |
| OutputZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputTensor | Saída | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |