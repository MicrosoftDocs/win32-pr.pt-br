---
UID: NS:directml.DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
description: Computa a bit e entre cada elemento correspondente dos tempos de entrada e grava o resultado no tensor de saída.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
ms.openlocfilehash: 9e8730eef1b2d98c2f3094fb2fa29ecfc571d877
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105762238"
---
# <a name="dml_element_wise_bit_and_operator_desc-structure-directmlh"></a>Estrutura de DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC (directml. h)

Computa a bit e entre cada elemento correspondente dos tempos de entrada e grava o resultado no tensor de saída.

O tensor de entrada e saída deve ter o mesmo *DimensionCount*, *tamanhos* e *tipo de dados*.

Esse operador dá suporte à execução in-loco, o que significa que o tensor de saída é permitido para alias de um ou mais dos tempos de entrada durante a associação.

> [!IMPORTANT]
> Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte também o [histórico de versão do DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxe

```cpp
struct DML_ELEMENT_WISE_BIT_AND_OPERATOR_DESC
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

A saída tensor para gravar os resultados.

## <a name="availability"></a>Disponibilidade
Esse operador foi introduzido no `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restrições de tensor
*ATensor*, *BTensor* e *OutputTensor* devem ter o mesmo *tipo de dados*, *DimensionCount* e *tamanhos*.

## <a name="tensor-support"></a>Suporte do tensor
| Tensor | Tipo | Contagens de dimensão com suporte | Tipos de dados com suporte |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | 1 a 8 | UINT32, UINT16, UINT8 |
| BTensor | Entrada | 1 a 8 | UINT32, UINT16, UINT8 |
| OutputTensor | Saída | 1 a 8 | UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cabeçalho** | directml. h |