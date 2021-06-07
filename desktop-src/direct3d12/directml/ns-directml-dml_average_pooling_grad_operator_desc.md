---
UID: NS:directml.DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
title: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
description: Calcula gradientes de backpropagation para pooling médio [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).
helpviewer_keywords:
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC, DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
- directml/DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
ms.openlocfilehash: aaa2b5d2becac421214afe7c643426c1c93cf899
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416990"
---
# <a name="dml_average_pooling_grad_operator_desc-structure-directmlh"></a>DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC estrutura (directml.h)

Calcula gradientes de backpropagation para pooling médio [(consulte DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc)).

Considere um 2x2 **DML_AVERAGE_POOLING_OPERATOR_DESC**, sem preenchimento e um passo de 1, que executa o seguinte.

```
InputTensor             OutputTensor
[[[[1, 2, 3],   AvgPool  [[[[3, 4],
   [4, 5, 6],     -->       [6, 7]]]]
   [7, 8, 9]]]]
```

Cada janela 2x2 no tensor de entrada é média para produzir um elemento da saída (lendo zeros para elementos além da borda). Aqui está um exemplo da saída de **DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC** parâmetros semelhantes.

```
InputGradientTensor            OutputGradientTensor
  [[[[1, 2],     AvgPoolGrad  [[[[0.25, 0.75, 0.5],
     [3, 4]]]]       -->         [   1,  2.5, 1.5],
                                 [0.75, 1.75,   1]]]]
```

Observe que os valores no *OutputGradientTensor* representam as contribuições ponderadas desse elemento para *o OutputTensor* durante o operador [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) original.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_AVERAGE_POOLING_GRAD_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputGradientTensor;
  const DML_TENSOR_DESC* OutputGradientTensor;
  UINT DimensionCount;
  _Field_size_(DimensionCount) const UINT* Strides;
  _Field_size_(DimensionCount) const UINT* WindowSize;
  _Field_size_(DimensionCount) const UINT* StartPadding;
  _Field_size_(DimensionCount) const UINT* EndPadding;
  BOOL IncludePadding;
};
```

## <a name="members"></a>Membros

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de gradiente de entrada. Normalmente, isso é obtido da saída de backpropagation de uma camada anterior. Normalmente, esse tensor teria os  mesmos tamanhos que a saída do DML_AVERAGE_POOLING_OPERATOR_DESC [correspondente](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) na passagem de avanço.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém os gradientes paxados. Normalmente, esse tensor teria os  mesmos tamanhos que a entrada do DML_AVERAGE_POOLING_OPERATOR_DESC [correspondente](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc) na passagem de avanço.

`DimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

O número de elementos nas *matrizes Strides,* *WindowSize,* *StartPadding* e *EndPadding.* Esse valor deve ser igual à contagem de dimensões espaciais. A contagem de dimensões espaciais será 2 se tensores 4D são fornecidos ou 3 se tensores 5D são fornecidos.

`Strides`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Consulte *Strides* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`WindowSize`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Consulte *WindowSize* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`StartPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Consulte *StartPadding* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`EndPadding`

Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***

Consulte *EndPadding* em [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

`IncludePadding`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

Consulte *IncludePadding* no [DML_AVERAGE_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_average_pooling_operator_desc).

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições do Tensor
*InputGradientTensor* *e OutputGradientTensor* devem ter o mesmo *DataType* e *DimensionCount*.

## <a name="tensor-support"></a>Suporte do Tensor
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputGradientTensor | Entrada | 4 a 5 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Saída | 4 a 5 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |