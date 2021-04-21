---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Computa gradientes de repropagação para o [clipe com elemento](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).
helpviewer_keywords:
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure
- direct3d12.dml_element_wise_clip_grad_operator_desc
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
- DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
ms.openlocfilehash: 224fbacdb8816a6aed6a7779c5c8ff991736ee6c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804412"
---
# <a name="dml_element_wise_clip_grad_operator_desc-directmlh"></a>DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC (directml. h)

Computa gradientes de repropagação para o [clipe com elemento](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

Esse operador dá suporte à execução in-loco, o `OutputTensor` que significa que é permitido para alias *InputTensor* durante a associação.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,5 e posterior. Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* OutputGradientTensor;
    FLOAT Min;
    FLOAT Max;
};
```

## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O recurso de entrada tensor. Normalmente, isso é o mesmo tensor que foi fornecido como o *InputTensor* para [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) no passo de encaminhamento.

`InputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O gradiente de entrada tensor. Normalmente, isso é obtido a partir da saída de Propagation de uma camada anterior. Normalmente, esse tensor teria os mesmos tamanhos da *saída* do **DML_OPERATOR_ELEMENT_WISE_CLIP** correspondente na passagem de encaminhamento.

`OutputGradientTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor de saída que contém os gradientes propagados. Normalmente, esse tensor teria os mesmos tamanhos que a *entrada* do **DML_OPERATOR_ELEMENT_WISE_CLIP** correspondente na passagem de encaminhamento.

`Min`

Tipo: **[float](/windows/win32/winprog/windows-data-types)**

O valor mínimo. Se x estiver neste valor ou abaixo dele, o resultado do gradiente será 0.

`Max`

Tipo: **[float](/windows/win32/winprog/windows-data-types)**

O valor máximo. Se x estiver no valor ou acima dele, o resultado do gradiente será 0.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputGradientTensor*, *InputTensor* e *OutputGradientTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| InputGradientTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Saída | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |
