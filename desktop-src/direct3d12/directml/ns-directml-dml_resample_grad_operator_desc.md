---
UID: NS:directml.DML_RESAMPLE_GRAD_OPERATOR_DESC
title: DML_RESAMPLE_GRAD_OPERATOR_DESC
description: Calcula gradientes de backpropagation para Resample (consulte [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).
helpviewer_keywords:
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- DML_RESAMPLE_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RESAMPLE_GRAD_OPERATOR_DESC, DML_RESAMPLE_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
- directml/DML_RESAMPLE_GRAD_OPERATOR_DESC
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
- DML_RESAMPLE_GRAD_OPERATOR_DESC
ms.openlocfilehash: ff2660257fa619edb72f10efb419f3c15f43fbde
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549721"
---
# <a name="dml_resample_grad_operator_desc-structure-directmlh"></a>DML_RESAMPLE_GRAD_OPERATOR_DESC estrutura (directml.h)

Calcula gradientes de backpropagation para Resample (consulte [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc)).

**DML_RESAMPLE1_OPERATOR_DESC** dimensiona dimensões arbitrárias do tensor de entrada usando amostragem de vizinho mais próximo ou interpolação bilinear. Dado um *InputGradientTensor* com os  mesmos tamanhos que a saída de um **DML_RESAMPLE1_OPERATOR_DESC** equivalente, esse operador produz  um *OutputGradientTensor* com os mesmos tamanhos que a entrada do **DML_RESAMPLE1_OPERATOR_DESC**.

Por exemplo, considere uma **DML_RESAMPLE1_OPERATOR_DESC** que executa um dimensionamento vizinho mais próximo de 1,5 x na largura e 0,5x na altura.

```
InputTensor           OutputTensor
[[1, 2],   Resample    [1, 1, 2]
 [3, 4]]      -->      
```

Observe como o 0º elemento do tensor de entrada (com o valor 1) contribui para dois elementos na saída, o 1º elemento (com o valor 2) contribui para um elemento na saída e os 2º e 3º elementos (com os valores 3 e 4) contribuem para nenhum elemento da saída.

O valor **DML_RESAMPLE_GRAD_OPERATOR_DESC** executaria o seguinte.

```
InputGradientTensor           OutputGradientTensor
    [4, 5, 6]      ResampleGrad    [[9, 6],
                       -->          [0, 0]]
```

Observe que os valores no *OutputGradientTensor* representam as contribuições ponderadas desse elemento para *o OutputTensor* durante o operador **DML_RESAMPLE1_OPERATOR_DESC** original.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_RESAMPLE_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  DML_INTERPOLATION_MODE InterpolationMode;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const FLOAT* Scales;
  _Field_size_(DimensionCount) const FLOAT* InputPixelOffsets;
  _Field_size_(DimensionCount) const FLOAT* OutputPixelOffsets;
};
```

## <a name="members"></a>Membros

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de gradiente de entrada. Normalmente, isso é obtido da saída de backpropagation de uma camada anterior. Normalmente, esse tensor teria os  mesmos tamanhos que a saída do DML_RESAMPLE1_OPERATOR_DESC [na](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) passagem de avanço.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém os gradientes paxados. Normalmente, esse tensor teria os mesmos tamanhos que a *entrada* do [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc) correspondente na passagem de encaminhamento.

`InterpolationMode`

Tipo: [ **DML_INTERPOLATION_MODE**](/windows/win32/api/directml/ne-directml-dml_interpolation_mode)

Consulte *interpolação* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`DimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

O número de elementos nas matrizes *Redimensions*, *InputPixelOffsets* e *OutputPixelOffsets* . Esse valor deve ser igual ao *DimensionCount* fornecido em *InputGradientTensor* e *OutputGradientTensor*.

`Scales`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Consulte *escalas* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`InputPixelOffsets`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Consulte *InputPixelOffsets* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

`OutputPixelOffsets`

Tipo: \_ \_ tamanho \_ do campo (DimensionCount) **const [float](../../winprog/windows-data-types.md) \***

Consulte *OutputPixelOffsets* em [DML_RESAMPLE1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_resample1_operator_desc).

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputGradientTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Saída | 4 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |