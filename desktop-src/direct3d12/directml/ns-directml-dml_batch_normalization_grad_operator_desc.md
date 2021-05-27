---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcula gradientes de backpropagation para [normalização em lote.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
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
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550431"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a>DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)

Calcula gradientes de backpropagation para [normalização em lote.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) **DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** executa vários cálculos, que são detalhados nas descrições de saída separadas.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.5 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de entrada. Normalmente, esse é o mesmo tensor que foi fornecido como *o InputTensor* para DML_BATCH_NORMALIZATION_OPERATOR_DESC [**na**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passagem de avanço.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de gradiente de entrada. Normalmente, isso é obtido da saída de backpropagation de uma camada anterior. Esse tensor deve ter os mesmos tamanhos de dimensão *que InputTensor*.

`MeanTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de média. Normalmente, esse é o mesmo tensor que foi fornecido como *o MeanTensor* para DML_BATCH_NORMALIZATION_OPERATOR_DESC [**na**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) passagem de avanço.

Todas as dimensões que não têm o mesmo tamanho que a dimensão correspondente *de InputTensor* devem ter um tamanho de 1 para que possam ser transmitidas para corresponder à entrada.

Por exemplo, os tamanhos a seguir são aceitáveis.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

A seguir está um erro, uma vez que, para ser compatível com difusão, todas as dimensões que não corresponderem devem ter o tamanho 1.

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de variação. Normalmente, isso é o mesmo tensor que foi fornecido como o *VarianceTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento. Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor*.

`ScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém os dados de escala. Normalmente, isso é o mesmo tensor que foi fornecido como o *ScaleTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) no passo de encaminhamento. Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor*.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Para cada valor correspondente nas entradas, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .

Este tensor deve ter os mesmos tamanhos de dimensão que *InputTensor* / *InputGradientTensor*.

`OutputScaleGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor* / *VarianceTensor* / *ScaleTensor*.

A computação a seguir é feita ou cada valor correspondente nas entradas.

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

O `sum` é calculado em todas as dimensões que precisam ser transmitidas. Se não houver nenhuma difusão necessária, nenhuma soma será necessária.

A seguir, um exemplo.

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

O elemento [0, **0**, 0, 0] de `OutputScaleGradientTensor` é a soma de `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` para todos os elementos 90 (3 \* 5 \* 6) [[0, 2], **0**, [0, 4], [0, 5]].

`OutputBiasGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Este tensor deve ter os mesmos tamanhos de dimensão que *MeanTensor* / *VarianceTensor* / *ScaleTensor*.

A computação a seguir é feita ou cada valor correspondente nas entradas.

`OutputBiasGradient = sum(InputGradient)`  

O `sum` é calculado em todas as dimensões que precisam ser transmitidas (consulte o exemplo de *OutputScaleGradientTensor*). Se não houver nenhuma difusão necessária, nenhuma soma será necessária.

`Epsilon`

Tipo: **[FLOAT](../../winprog/windows-data-types.md)**

Um valor pequeno adicionado à variação para evitar zero.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Restrições do Tensor
*InputGradientTensor,* *InputTensor,* *MeanTensor,* *OutputBiasGradientTensor,* *OutputGradientTensor,* *OutputScaleGradientTensor,* *ScaleTensor* e *VarianceTensor* devem ter o mesmo *DataType* e *DimensionCount*.

## <a name="tensor-support"></a>Suporte do Tensor
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16 |
| MeanTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16 |
| VarianceTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Saída | 1 a 8 | FLOAT32, FLOAT16 |
| OutputScaleGradientTensor | Saída | 1 a 8 | FLOAT32, FLOAT16 |
| OutputBiasGradientTensor | Saída | 1 a 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |