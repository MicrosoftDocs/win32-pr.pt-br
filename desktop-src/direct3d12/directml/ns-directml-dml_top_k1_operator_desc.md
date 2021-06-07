---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Seleciona os maiores ou menores elementos *K* de cada sequência ao longo de um eixo de *InputTensor* e retorna os valores e índices desses elementos em *OutputValueTensor* e *OutputIndexTensor*, respectivamente.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416963"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>Estrutura de DML_TOP_K1_OPERATOR_DESC (directml. h)
Seleciona os maiores ou menores elementos *K* de cada sequência ao longo de um eixo de *InputTensor* e retorna os valores e índices desses elementos em *OutputValueTensor* e *OutputIndexTensor*, respectivamente. Uma *sequência* refere-se a um dos conjuntos de elementos que existem ao longo da dimensão de *eixo* do *InputTensor*.

A escolha de se deseja selecionar os maiores elementos K ou os menores K podem ser controlados usando *AxisDirection*.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de entrada que contém os elementos a serem selecionados.

`OutputValueTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de saída para gravar os valores dos primeiros *K* elementos em. Os primeiros elementos *K* são selecionados com base no fato de serem os maiores ou menores, dependendo do valor de *AxisDirection*. Esse tensor deve ter tamanhos iguais a *InputTensor*, *exceto* para a dimensão especificada pelo parâmetro *Axis* , que deve ter um tamanho igual a *K*.

Os valores *K* selecionados de cada sequência de entrada têm a garantia de serem classificados como decrescentes (maior do que o menor) se *AxisDirection* for [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md). Caso contrário, o oposto é verdadeiro e os valores selecionados têm a garantia de serem classificados em ordem crescente (menor para o maior).

`OutputIndexTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de saída para gravar os índices dos primeiros *K* elementos em. Esse tensor deve ter tamanhos iguais a *InputTensor*, *exceto* para a dimensão especificada pelo parâmetro *Axis* , que deve ter um tamanho igual a *K*.

Os índices retornados neste tensor são medidos em relação ao início de sua sequência (em oposição ao início do tensor). Por exemplo, um índice de 0 sempre se refere ao primeiro elemento para todas as sequências em um eixo.

Nos casos em que dois ou mais elementos de Top-K têm o mesmo valor (ou seja, quando há um empate), os índices de ambos os elementos são incluídos e têm a garantia de serem ordenados por índice de elemento crescente. Observe que isso é verdadeiro independentemente do valor de *AxisDirection*.

`Axis`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O índice da dimensão na qual selecionar elementos. Esse valor deve ser menor que o *DimensionCount* do *InputTensor*.

`K`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de elementos a serem selecionados. *K* deve ser maior que 0, mas menor que o número de elementos no *InputTensor* ao longo da dimensão especificada por *Axis*.

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Um valor da enumeração de [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) . Se definido como **DML_AXIS_DIRECTION_INCREASING**, esse operador retornará os *menores* elementos *K* na ordem de aumento do valor. Caso contrário, retornará os *maiores* elementos *K* em ordem decrescente.

## <a name="examples"></a>Exemplos

### <a name="example-1"></a>Exemplo 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a>Exemplo 2. Usando um eixo diferente

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a>Exemplo 3. Valores vinculados

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a>Exemplo 4. Aumentando a direção do eixo

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a>Comentários
Quando *AxisDirection* é definido como [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), esse operador é equivalente a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor

* *InputTensor*, *OutputIndexTensor* e *OutputValueTensor* devem ter o mesmo *DimensionCount*.
* *InputTensor* e *OutputValueTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 e acima

| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Saída | 1 a 8 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e acima

| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Saída | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Saída | 4 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |
