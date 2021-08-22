---
title: Constantes DirectML
description: As constantes a seguir são declaradas em `DirectML.h` .
keywords:
- Constantes
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5f2d95d0eef67309ef1e5902ed6b968616b38bc081bd259d77418e950e4e028f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989596"
---
# <a name="directml-constants"></a>Constantes DirectML

As constantes a seguir são declaradas em `DirectML.h` .

| Constante | Valor | Descrição |
|-|-|-|
| DML_TENSOR_DIMENSION_COUNT_MAX | 5 | Os dezenases de DirectML dão suporte a um máximo de 5 dimensões para DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0. |
| DML_TENSOR_DIMENSION_COUNT_MAX1 | 8 | Os dezenases de DirectML dão suporte a um máximo de 8 dimensões para DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0. |
| DML_TEMPORARY_BUFFER_ALIGNMENT | 256 | Os buffers temporários e persistentes devem ter um endereço base alinhado a 256 bytes. |
| DML_PERSISTENT_BUFFER_ALIGNMENT | 256 | Os buffers temporários e persistentes devem ter um endereço base alinhado a 256 bytes. |
| DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT | 16 | Os tempos de buffer têm um requisito mínimo de alinhamento de endereço base de 16 bytes. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | DirectML. h |

## <a name="see-also"></a>Confira também

* [Referência do DirectML](direct3d-directml-reference.md)
* [Referência de núcleo](direct3d-12-core-reference.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
