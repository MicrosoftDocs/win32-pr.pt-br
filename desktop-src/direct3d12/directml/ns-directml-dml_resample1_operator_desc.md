---
UID: NS:directml.DML_RESAMPLE1_OPERATOR_DESC
title: DML_RESAMPLE1_OPERATOR_DESC
description: Reamostrar elementos da origem para o tensor de destino, usando os fatores de escala para calcular o tamanho do tensor de destino. Você pode usar um modo de interpolação de vizinho mais próximo ou linear.
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
- DML_RESAMPLE1_OPERATOR_DESC
f1_keywords:
- DML_RESAMPLE1_OPERATOR_DESC
- directml/DML_RESAMPLE1_OPERATOR_DESC
ms.openlocfilehash: 3cf5a49f5c92b835646e146b631abd18b4b19e6b
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417007"
---
# <a name="dml_resample1_operator_desc-structure-directmlh"></a>Estrutura de DML_RESAMPLE1_OPERATOR_DESC (directml. h)
Reamostrar elementos da origem para o tensor de destino, usando os fatores de escala para calcular o tamanho do tensor de destino. Você pode usar um modo de interpolação de vizinho mais próximo ou linear. O operador dá suporte à interpolação em várias dimensões, não apenas em 2D. Portanto, você pode manter o mesmo tamanho espacial, mas interpolar entre canais ou em lotes. A relação entre as coordenadas de entrada e saída é a seguinte.

`OutputTensorX = (InputTensorX + InputPixelOffset) * Scale + OutputPixelOffset`

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_RESAMPLE1_OPERATOR_DESC {
  const DML_TENSOR_DESC  *InputTensor;
  const DML_TENSOR_DESC  *OutputTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT                   DimensionCount;
  const FLOAT            *Scales;
  const FLOAT            *InputPixelOffsets;
  const FLOAT            *OutputPixelOffsets;
};
```



## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor que contém os dados de entrada.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor para gravar os dados de saída.


`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Este campo determina o tipo de interpolação usado para escolher pixels de saída.

- **DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR**. Usa o algoritmo de *vizinho mais próximo* , que escolhe o elemento de entrada mais próximo ao pixel Center correspondente para cada elemento de saída.

- **DML_INTERPOLATION_MODE_LINEAR**. Usa o algoritmo *Quadrilinear* , que computa o elemento Output, fazendo a média ponderada dos 2 elementos de entrada vizinhos mais próximos por dimensão. Como todas as quatro dimensões podem ser reamostradas, a média ponderada é calculada em um total de 16 elementos de entrada para cada elemento de saída.


`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de valores nas matrizes que *dimensionam*, *InputPixelOffsets* e *OutputPixelOffsets* apontam para. Esse valor deve corresponder à contagem de dimensões de *InputTensor* e *OutputTensor*, que deve ser 4.


`Scales`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

As escalas a serem aplicadas ao reamostrar a entrada, em que dimensiona > 1 escalar verticalmente a imagem e escalas < 1 reduzir verticalmente a imagem para essa dimensão. Observe que as escalas não precisam ser exatamente `OutputSize / InputSize` . Se a entrada após o dimensionamento for maior que o limite de saída, então, vamos cortá-lo para o tamanho de saída. Por outro lado, se a entrada após o dimensionamento for menor do que a saída associada, as bordas de saída serão clamped.


`InputPixelOffsets`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Os deslocamentos a serem aplicados aos pixels de entrada antes da reamostragem. Quando esse valor é `0` , o canto superior esquerdo do pixel é usado em vez de seu centro, o que normalmente não dará o resultado esperado. Para reamostrar a imagem usando o centro dos pixels e para obter o mesmo comportamento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), esse valor deve ser `0.5` .


`OutputPixelOffsets`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Os deslocamentos a serem aplicados aos pixels de saída após a reamostragem. Quando esse valor é `0` , o canto superior esquerdo do pixel é usado em vez de seu centro, o que normalmente não dará o resultado esperado. Para reamostrar a imagem usando o centro dos pixels e para obter o mesmo comportamento que [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc), esse valor deve ser `-0.5` .


## <a name="remarks"></a>Comentários
Quando *InputPixelOffsets* são definidos como 0,5 e *OutputPixelOffsets* são definidos como-0,5, esse operador é equivalente a [DML_RESAMPLE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample_operator_desc).

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |