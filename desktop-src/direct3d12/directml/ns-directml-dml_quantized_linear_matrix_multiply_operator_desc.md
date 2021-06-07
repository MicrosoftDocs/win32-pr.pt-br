---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Executa uma função de multiplicação de matriz em dados quantificados. Esse operador é matematicamente equivalente a desquantificar as entradas, executar a matriz de multiplicação e, em seguida, quantificar a saída.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417009"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>Estrutura de DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC (directml. h)
Executa uma função de multiplicação de matriz em dados quantificados. Esse operador é matematicamente equivalente a desquantificar as entradas, executar a matriz de multiplicação e, em seguida, quantificar a saída.

Esse operador requer que a matriz multiplique os tempos de entrada para ser 4D, formatados como `{ BatchCount, ChannelCount, Height, Width }` . O operador de multiplicação de matriz executará BatchCount * ChannelCount número de multiplicações de matriz independentes. 

Por exemplo, se *ATensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, K }` e *BTensor* tiver tamanhos  de `{ BatchCount, ChannelCount, K, N }` e *OutputTensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, N }` , o operador de multiplicação de matriz executará BatchCount * ChannelCount multiplicações de matriz independentes de dimensões {M, K} x {K, n} = {m, n}. 

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
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Membros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados. As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de escala ATensor. As dimensões esperadas do `AScaleTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha. Esses valores de escala são usados para desquantificar os valores.


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto de *ATensor* zero. As dimensões esperadas de AZeroPointTensor são `{ 1, 1, 1, 1 }` se a quantificação por tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha. Esses valores de ponto zero são usados para desquantificar os valores de ATensor.


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados B. As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de escala *BTensor* . As dimensões esperadas do `BScaleTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, 1, N }` se for necessária quantização por coluna. Esses valores de escala são usados para desquantificar os valores de *BTensor* .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto de *BTensor* zero. As dimensões esperadas do `BZeroPointTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, 1, N }` se for necessária quantização por coluna. Esses valores de ponto zero são usados para desquantificar os valores de *BTensor* .


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de escala de filtro. As dimensões esperadas do `OutputScaleTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha. Esse valor de escala é usado para desquantificar os valores de filtro.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero de filtro. As dimensões esperadas do `OutputZeroPointTensor` são `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se for necessária quantização por linha. Esse valor de ponto zero é usado para desquantificar os valores de filtro.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor para gravar os resultados. As dimensões de tensor são `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *ATensor* e `AZeroPointTensor` deve ter o mesmo *tipo de dados*.
* *BTensor* e `BZeroPointTensor` deve ter o mesmo *tipo de dados*.
* *OutputTensor* e `OutputZeroPointTensor` deve ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | 4 | INT8, UINT8 |
| AScaleTensor | Entrada | 4 | FLOAT32 |
| AZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| BTensor | Entrada | 4 | INT8, UINT8 |
| BScaleTensor | Entrada | 4 | FLOAT32 |
| BZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputScaleTensor | Entrada | 4 | FLOAT32 |
| OutputZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputTensor | Saída | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |