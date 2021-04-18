---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Executa uma função de multiplicação de matriz em dados inteiros.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105793766"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>Estrutura de DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC (directml. h)
Executa uma função de multiplicação de matriz em dados inteiros.

Esse operador requer que a matriz multiplique os tempos de entrada para ser 4D, que são formatados como `{ BatchCount, ChannelCount, Height, Width }` . O operador de multiplicação de matriz executará BatchCount * ChannelCount número de multiplicações de matriz independentes.

Por exemplo, se *ATensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, K }` e *BTensor* tiver tamanhos  de `{ BatchCount, ChannelCount, K, N }` e *OutputTensor* tiver *tamanhos* de `{ BatchCount, ChannelCount, M, N }` , o operador de multiplicação de matriz executará BatchCount * ChannelCount multiplicações de matriz independentes de dimensões {M, K} x {K, n} = {m, n}.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Membros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados. As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto de ATensor zero. As dimensões esperadas do `AZeroPointTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, M, 1 }` se a quantificação por linha for necessária. Esses valores de ponto zero são usados para desquantificar os valores de *ATensor* .


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados B. As dimensões deste tensor devem ser `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto de *BTensor* zero. As dimensões esperadas do `BZeroPointTensor` serão `{ 1, 1, 1, 1 }` se a quantização de tensor for necessária ou `{ 1, 1, 1, N }` se for necessária quantização por coluna. Esses valores de ponto zero são usados para desquantificar os valores de BTensor.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor com o qual gravar os resultados. As dimensões de tensor são `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
* *ATensor* e `AZeroPointTensor` deve ter o mesmo *tipo de dados*.
* *BTensor* e `BZeroPointTensor` deve ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Dimensões | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Entrada | {BatchCount, ChannelCount, M, K} | 4 | INT8, UINT8 |
| AZeroPointTensor | Entrada opcional | {1, 1, AZeroPointCount, 1} | 4 | INT8, UINT8 |
| BTensor | Entrada | {BatchCount, ChannelCount, K, N} | 4 | INT8, UINT8 |
| BZeroPointTensor | Entrada opcional | {1, 1, 1, BZeroPointCount} | 4 | INT8, UINT8 |
| OutputTensor | Saída | {BatchCount, ChannelCount, M, N} | 4 | INT32 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |