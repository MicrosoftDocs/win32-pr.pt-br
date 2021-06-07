---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
description: Executa um lógico menor ou *igual* a em cada par de elementos correspondentes dos tensores de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente *de OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
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
- DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
ms.openlocfilehash: d1b8a282154b2b714daf061e2bb3f88b359209d4
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111416960"
---
# <a name="dml_element_wise_logical_less_than_or_equal_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC estrutura (directml.h)

Executa um lógico menor ou *igual* a em cada par de elementos correspondentes dos tensores de entrada, colocando o resultado (1 para true, 0 para false) no elemento correspondente *de OutputTensor*.

```
f(a, b) = (a <= b)
```

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível autônomo directML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1.4 e posterior). Consulte também [Histórico de versão do DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_ELEMENT_WISE_LOGICAL_LESS_THAN_OR_EQUAL_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Membros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém as entradas do lado esquerdo.

`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Um tensor que contém as entradas do lado direito.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

O tensor de saída no que gravar os resultados.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições do Tensor
* *ATensor* e *BTensor* devem ter o mesmo *DataType*.
* *ATensor,* *BTensor* e *OutputTensor* devem ter o mesmo *DimensionCount* e *Tamanhos*.

## <a name="tensor-support"></a>Suporte do Tensor
| Tensor | Tipo | Contagens de dimensões com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| Atensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| BTensor | Entrada | 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 1 a 8 | UINT32, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml.h |