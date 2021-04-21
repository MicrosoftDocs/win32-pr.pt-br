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
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803412"
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
