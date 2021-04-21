---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Computa as coordenadas N-dimensional de todos os elementos diferentes de zero do tensor de entrada.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803389"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>Estrutura de DML_NONZERO_COORDINATES_OPERATOR_DESC (directml. h)

Computa as coordenadas N-dimensional de todos os elementos diferentes de zero do tensor de entrada.

Esse operador produz uma matriz MxN de valores, em que cada linha M contém uma coordenada N-dimensional de um valor diferente de zero da entrada. Ao usar as entradas **FLOAT32** ou **FLOAT16** , ambos negativos e positivos 0 (0,0 f e-0,0 f) são tratados como zero para fins deste operador.

O operador requer que o *OutputCoordinatesTensor* tenha um tamanho grande o suficiente para acomodar um cenário de pior caso em que cada elemento da entrada é diferente de zero. Esse operador retorna a contagem de elementos diferentes de zero por meio do *OutputCountTensor*, que os chamadores podem inspecionar para determinar o número de coordenadas gravadas no *OutputCoordinatesTensor*.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de entrada.

`OutputCountTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém a contagem de elementos diferentes de zero no tensor de entrada. Esse tensor deve ser um escalar &mdash; ou seja, os tamanhos desse tensor devem ser 1. O tipo deste tensor deve ser **UINT32**.

`OutputCoordinatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém as coordenadas N-dimensional dos elementos Input que são diferentes de zero. 

Esse tensor deve ter *tamanhos* de `{1,1,M,N}` (se *DimensionCount* for 4) ou `{1,1,1,M,N}` (se *DimensionCount* for 5), em que M é o número total de elementos na *InputTensor* e N é maior ou igual à *classificação efetiva* de *InputTensor*, até o *DimensionCount* da entrada.

A classificação efetiva de um tensor é determinada pelo *DimensionCount* do tensor, excluindo as principais dimensões do tamanho 1. Por exemplo, um tensor com tamanhos de `{1,2,3,4}` tem a classificação efetiva 3, como faz um tensor com tamanhos de `{1,1,5,5,5}` . Um tensor com tamanhos `{1,1,1,1}` tem A classificação efetiva 0.

Considere um *InputTensor* com *tamanhos* de `{1,1,12,5}` . Este tensor de entrada contém 60 elementos e tem uma classificação efetiva de 2. Neste exemplo, todos os tamanhos válidos de *OutputCoordinatesTensor* são do formulário `{1,1,60,N}` , em que N >= 2, mas não maior que o *DimensionCount* (4 neste exemplo).

As coordenadas escritas nesse tensor têm garantia de serem ordenadas por índice de elemento crescente. Por exemplo, se o tensor de entrada tiver 3 valores diferentes de zero em coordenadas {1,0} , {1,2} e {0,5} os valores gravados em *OutputCoordinatesTensor* serão `[[0,5], [1,0], [1,2]]` .

Embora esse tensor exija que sua dimensão M seja igual ao número de elementos no tensor de entrada, esse operador gravará apenas um máximo de elementos de OutputCount para esse tensor. O OutputCount é retornado por meio do *OutputCountTensor* escalar.

> [!NOTE]
> Os elementos restantes desse tensor além do OutputCount são indefinidos quando esse operador é concluído. Você não deve contar com os valores desses elementos.

## <a name="example"></a>Exemplo

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputTensor*, *OutputCoordinatesTensor* e `OutputCountTensor` deve ter o mesmo *DimensionCount*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Dimensões | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | {[D0], D1, D2, D3, D4} | 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputCountTensor | Saída | {[1], 1, 1, 1, 1} | 4 a 5 | UINT32 |
| OutputCoordinatesTensor | Saída | {[1], 1, 1, M, N} | 4 a 5 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |