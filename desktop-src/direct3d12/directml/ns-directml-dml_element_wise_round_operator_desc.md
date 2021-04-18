---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Arredonda cada elemento de *InputTensor* para um valor inteiro, colocando o resultado no elemento correspondente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: f0964ae133c61b3a596b644630d363f902635585
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105795502"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a>Estrutura de DML_ELEMENT_WISE_ROUND_OPERATOR_DESC (directml. h)

Arredonda cada elemento de *InputTensor* para um valor inteiro, colocando o resultado no elemento correspondente de *OutputTensor*.

Esse operador dá suporte à execução in-loco, o que significa que *OutputTensor* é permitido para alias *InputTensor* durante a associação.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a>Membros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de entrada para leitura.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

A saída tensor para gravar os resultados.


`RoundingMode`

Tipo: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**

Um [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determinando a direção para arredondar.

* Se **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: os valores são arredondados para o número inteiro mais próximo, com valores intermediários (por exemplo, 0,5) sendo arredondados para o inteiro par mais próximo.
* Se **DML_ROUNDING_MODE_TOWARD_ZERO**: os valores são arredondados para zero. Isso efetivamente trunca a parte fracionária.
* Se **DML_ROUNDING_MODE_TOWARD_INFINITY**: os valores são arredondados para o número inteiro mais próximo, com valores intermediários (por exemplo, 0,5) sendo arredondados para longe de zero (em direção ao infinito positivo ou negativo, dependendo do sinal do valor).

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restrições de tensor
*InputTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.

## <a name="tensor-support"></a>Suporte do tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Saída | 1 a 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 e acima
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Saída | 4 | FLOAT32, FLOAT16 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |