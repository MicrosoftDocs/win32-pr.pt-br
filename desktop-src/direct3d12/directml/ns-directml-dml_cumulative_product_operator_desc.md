---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multiplica os elementos de um tensor ao longo de um eixo, escrevendo a conta em execução do produto no tensor de saída.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: cb4006a20dd25751c027ba97e63dcfc60c25faf6
ms.sourcegitcommit: 0b93de98c4afc79a6801a113bc91adbc89e835b9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/03/2021
ms.locfileid: "113282555"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a>DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)

Multiplica os elementos de um tensor ao longo de um eixo, escrevendo a conta em execução do produto no tensor de saída.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.5 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de entrada. Normalmente, esse é o mesmo tensor que foi fornecido como *o InputTensor* para DML_BATCH_NORMALIZATION_OPERATOR_DESC [**na**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passagem de avanço.

O tensor de entrada que contém elementos a serem multiplicados.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de saída para gravar os produtos cumulativos resultantes. Esse tensor deve ter os mesmos tamanhos e tipo de dados *que InputTensor*.

`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O índice da dimensão sobre a que multiplicar elementos. Esse valor deve ser menor que *DimensionCount* do *InputTensor.*

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Um dos valores da [enumeração DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction) dados. Se definido como **DML_AXIS_DIRECTION_INCREASING**, o produto ocorrerá atravessando o tensor ao longo do eixo especificado pelo índice de elemento crescente. Se definido como **DML_AXIS_DIRECTION_DECREASING**, o inverso será true e o produto ocorrerá atravessando elementos por índice decrescente.

`HasExclusiveProduct`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

Se **TRUE**, o valor do elemento atual será excluído ao escrever o tally em execução no tensor de saída. Se **FALSE**, o valor do elemento atual será incluído na lista em execução.

## <a name="examples"></a>Exemplos

Todos os exemplos nesta seção usam esse mesmo tensor de entrada.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>Exemplo 1. Produto cumulativo entre entregas horizontais

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a>Exemplo 2. Produtos exclusivos

Definir *HasExclusiveProduct* como **TRUE** tem o efeito de excluir o valor do elemento atual da tally em execução ao escrever no tensor de saída.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a>Exemplo 3. Direção do eixo

Definir *AxisDirection como* [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/api/directml/ne-directml-dml_axis_direction) tem o efeito de reverter a ordem de travessia dos elementos ao calcular a tally em execução.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>Exemplo 4. Multiplicando ao longo de um eixo diferente

Neste exemplo, o produto ocorre verticalmente, ao longo do eixo de altura (segunda dimensão).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a>Comentários
Esse operador dá suporte à execução in-loca, o que significa que o tensor de saída tem permissão para alias *InputTensor* durante a associação.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Restrições do Tensor
*InputTensor* e *OutputTensor* devem ter o mesmo *DataType,* *DimensionCount* e *tamanhos*.

## <a name="tensor-support"></a>Suporte do Tensor
### <a name="dml_feature_level_4_0-and-above"></a>DML_FEATURE_LEVEL_4_0 e superior
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, UINT32, UINT16 |

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 e superior
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |