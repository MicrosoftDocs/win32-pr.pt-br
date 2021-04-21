---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Gera os índices dos elementos com valor máximo em uma ou mais dimensões do tensor de entrada.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 0c466975ad3b88973f50bc06676f2197267c56a7
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803553"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a>Estrutura de DML_ARGMAX_OPERATOR_DESC (directml. h)

Gera os índices dos elementos com valor máximo em uma ou mais dimensões do tensor de entrada.

Cada elemento de saída é o resultado da aplicação de uma redução de *ARGMAX* em um subconjunto do tensor de entrada. A função *ARGMAX* gera o índice do elemento com valor máximo em um conjunto de elementos de entrada. Os elementos de entrada envolvidos em cada redução são determinados pelos eixos de entrada fornecidos. Da mesma forma, cada índice de saída é relativo aos eixos de entrada fornecidos. Se todos os eixos de entrada forem especificados, o operador aplicará uma única redução de *ARGMAX* e produzirá um único elemento de saída.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor do qual ler.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor para gravar os resultados. Cada elemento de saída é o resultado de uma redução de *ARGMAX* em um subconjunto de elementos do *InputTensor*. 

- *DimensionCount* deve corresponder a *InputTensor. DimensionCount* (a classificação da entrada tensor é preservada).
- Os *tamanhos* devem corresponder a *InputTensor. Sizes*, exceto as dimensões incluídas nos *eixos* reduzidos, que devem ser de tamanho 1.

`AxisCount`

Tipo: **[uint](/windows/win32/winprog/windows-data-types)**

O número de eixos a serem reduzidos. Este campo determina o tamanho da matriz de *eixos* .

`Axes`

Tipo: \_ Field_size \_ (AxisCount) **const [uint](/windows/win32/winprog/windows-data-types) \***

Os eixos ao longo do qual reduzir. Os valores devem estar no intervalo `[0, InputTensor.DimensionCount - 1]` .

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Determina qual índice deve ser selecionado quando vários elementos de entrada têm o mesmo valor.
- **DML_AXIS_DIRECTION_INCREASING** retorna o índice do primeiro elemento com valor máximo (por exemplo, `argmax({3,2,1,2,3}) = 0` )
- **DML_AXIS_DIRECTION_DECREASING** retorna o índice do último elemento com valor máximo (por exemplo, `argmax({3,2,1,2,3}) = 4` )

## <a name="examples"></a>Exemplos

Os exemplos nesta seção usam esse mesmo tensor de entrada bidimensional.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a>Exemplo 1. Aplicando *ARGMAX* a colunas

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a>Exemplo 2. Aplicando *ARGMAX* a linhas

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a>Exemplo 3. Aplicando *ARGMAX* a todos os eixos (toda a tensor)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Comentários
Os tamanhos de tensor de saída devem ser iguais aos tamanhos de tensor de entrada, exceto para os eixos reduzidos, que devem ser 1.

Quando *AxisDirection* é [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), essa API é equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) com [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).

Um subconjunto dessa funcionalidade é exposto por meio do operador de [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) e tem suporte em níveis de recursos de DirectML anteriores.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputTensor* e *OutputTensor* devem ter o mesmo *DimensionCount*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 1 a 8 | INT64, INT32, UINT64, UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |