---
UID: NS:directml.DML_CONVOLUTION_INTEGER_OPERATOR_DESC
title: DML_CONVOLUTION_INTEGER_OPERATOR_DESC
description: Executa uma convolução do *FilterTensor* com *o InputTensor.* Esse operador executa a convolução de avanço em dados inteiros.
helpviewer_keywords:
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CONVOLUTION_INTEGER_OPERATOR_DESC, DML_CONVOLUTION_INTEGER_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
- directml/DML_CONVOLUTION_INTEGER_OPERATOR_DESC
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
- DML_CONVOLUTION_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f4045598dd1aa050479fec8e5732fe5c0a4e77ee
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416984"
---
# <a name="dml_convolution_integer_operator_desc-structure-directmlh"></a>DML_CONVOLUTION_INTEGER_OPERATOR_DESC estrutura (directml.h)

Executa uma convolução do *FilterTensor* com *o InputTensor.* Esse operador executa a convolução de avanço em dados inteiros. Tensores de ponto zero opcionais também podem ser usados para subtrair valores de ponto zero do tensor de entrada e filtro.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_CONVOLUTION_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
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

Um tensor que contém os dados de entrada. As dimensões esperadas do *InputTensor* são `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`InputZeroPointTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero de entrada. As dimensões esperadas do *InputZeroPointTensor* são `{ 1, 1, 1, 1 }` .


`FilterTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados do filtro. As dimensões esperadas do *FilterTensor* são `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .


`FilterZeroPointTensor`

Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero do filtro. As dimensões esperadas do *FilterZeroPointTensor* serão se a quantização por tensor for necessária ou se a `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` quantização por canal for necessária.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor no que gravar os resultados. As dimensões esperadas do *OutputTensor* são `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .


`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de dimensões espaciais para a operação de convolução. Dimensões espaciais são as dimensões inferiores do *FilterTensor* de convolução. Esse valor também determina o tamanho das *matrizes Strides,* *Quedas,* *StartPadding* e *EndPadding.* Há suporte apenas para um valor de 2.


`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Uma matriz que contém os passos da operação de convolução. Esses passos são aplicados ao filtro de convolução. Eles são separados dos passos tensores incluídos [no DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).


`Dilations`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Uma matriz que contém as barreiras da operação de convolução. As estruturas são passadas aplicadas aos elementos do kernel de filtro. Isso tem o efeito de simular um kernel de filtro maior ao preenchimento dos elementos do kernel de filtro interno com zeros.


`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Uma matriz que contém os valores de preenchimento a serem aplicados ao início de cada dimensão espacial do filtro e do tensor de entrada da operação de convolução.


`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Uma matriz que contém os valores de preenchimento a serem aplicados ao final de cada dimensão espacial do filtro e do tensor de entrada da operação de convolução.


`GroupCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de grupos nos quais dividir a operação de convolução. *GroupCount* pode ser usado para obter a convolução de profundidade definindo *GroupCount* igual à contagem de canais de entrada. Isso divide a convolução em uma convolução separada por canal de entrada.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições do Tensor
* *FilterTensor* e *FilterZeroPointTensor* devem ter o mesmo *DataType*.
* *InputTensor* e *InputZeroPointTensor* devem ter o mesmo *DataType*.

## <a name="tensor-support"></a>Suporte do Tensor
| Tensor | Tipo | Dimensões | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | INT8, UINT8 |
| InputZeroPointTensor | Entrada opcional | { 1, 1, 1, 1 } | 4 | INT8, UINT8 |
| FilterTensor | Entrada | { FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth } | 4 | INT8, UINT8 |
| FilterZeroPointTensor | Entrada opcional | { 1, FilterZeroPointChannelCount, 1, 1 } | 4 | INT8, UINT8 |
| OutputTensor | Saída | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | INT32 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |