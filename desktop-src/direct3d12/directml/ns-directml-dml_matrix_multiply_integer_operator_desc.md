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
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416956"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC estrutura (directml.h)
Executa uma função de multiplicação de matriz em dados inteiros.

Esse operador requer que os tensores de entrada de multiplicação de matriz sejam 4D, que são formatados como `{ BatchCount, ChannelCount, Height, Width }` . O operador de multiplicação de matriz executará BatchCount * ChannelCount número de multiplicações de matriz independentes.

Por exemplo, se *ATensor* tiver Tamanhos de e BTensor tiver Tamanhos de e  OutputTensor tiver Tamanhos de , o operador de multiplicação de matriz executará multiplicações de matriz independente BatchCount * ChannelCount de dimensões `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

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

Um tensor que contém os dados A. As dimensões desse tensor devem ser `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero do ATensor. As dimensões esperadas do são se a quantização por tensor for necessária ou se a quantização por `AZeroPointTensor` `{ 1, 1, 1, 1 }` linha for `{ 1, 1, M, 1 }` necessária. Esses valores de ponto zero são usados para rebaixar os *valores de ATensor.*


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados B. As dimensões desse tensor devem ser `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor opcional que contém os dados de ponto zero *do BTensor.* As dimensões esperadas do são se a quantização por tensor for necessária ou se a quantização por `BZeroPointTensor` coluna `{ 1, 1, 1, 1 }` for `{ 1, 1, 1, N }` necessária. Esses valores de ponto zero são usados para rebaixar os valores BTensor.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor no qual gravar os resultados. As dimensões desse tensor são `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições do Tensor
* *ATensor* `AZeroPointTensor` e devem ter o mesmo *DataType*.
* *BTensor* e `BZeroPointTensor` devem ter o mesmo *DataType*.

## <a name="tensor-support"></a>Suporte do Tensor
| Tensor | Tipo | Dimensões | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| Atensor | Entrada | { BatchCount, ChannelCount, M, K } | 4 | INT8, UINT8 |
| AZeroPointTensor | Entrada opcional | { 1, 1, AZeroPointCount, 1 } | 4 | INT8, UINT8 |
| BTensor | Entrada | { BatchCount, ChannelCount, K, N } | 4 | INT8, UINT8 |
| BZeroPointTensor | Entrada opcional | { 1, 1, 1, BZeroPointCount } | 4 | INT8, UINT8 |
| OutputTensor | Saída | { BatchCount, ChannelCount, M, N } | 4 | INT32 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |