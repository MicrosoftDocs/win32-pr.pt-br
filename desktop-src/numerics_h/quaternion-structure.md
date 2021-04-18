---
title: estrutura Quaternion (Windowsnumerics. h)
description: Um vetor dimensional de quatro dimensões, usado para representar uma rotação.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- estrutura de Quaternion
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780738"
---
# <a name="quaternion-structure"></a>Estrutura de Quaternion

Um vetor dimensional de quatro dimensões, usado para representar uma rotação.

Um Quaternion pode girar com eficiência um objeto sobre o vetor (x, y, z) pelo ângulo teta, em que w = cos (teta/2). Os quaternions normalmente são usados para uma interpolação suave entre dois ângulos e para evitar o problema de bloqueio de gimbal que pode ocorrer com ângulos de Euler.

Esse tipo está disponível apenas em C++. Seu equivalente em .NET é [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).

## <a name="constructors"></a>Construtores

| Nome | Descrição |
|-|-|
| `quaternion()` | Cria um Quaternion não inicializado. |
| `quaternion(float x, float y, float z, float w)` | Cria um Quaternion com os valores especificados. |
| `quaternion(float3 vectorPart, float scalarPart)` | Cria um Quaternion a partir de um float3 e escalar. |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | Converte um **Microsoft. Graphics. Canvas. Numerics. Quaternion** em um Quaternion. |

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | Cria um quatérnio de um vetor e um ângulo a ser girado sobre o vetor. |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Cria um Quaternion com base nos ângulos de guinada, pitch e roll especificados. |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | Cria um Quaternion a partir de uma matriz de rotação. |
| `bool is_identity(quaternion const& value)` | Verifica se este é um Quaternion de identidade (sem rotação). |
| `float length(quaternion const& value)` | Calcula o comprimento de um Quaternion. |
| `float length_squared(quaternion const& value)` | Calcula o comprimento quadrado de um Quaternion. |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | Calcula o produto escalar de dois quatérnios. |
| `quaternion normalize(quaternion const& value)` | Divide cada componente de um Quaternion pelo comprimento do Quaternion. |
| `quaternion conjugate(quaternion const& value)` | Calcula o conjugado de um Quaternion. |
| `quaternion inverse(quaternion const& value)` | Calcula o inverso de um Quaternion. |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpola entre dois quatérnios usando interpolação linear esférica. |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | Interpola linearmente entre dois quaternions. |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | Concatena dois quaternions; o resultado representa a primeira rotação seguida pela segunda rotação. |

## <a name="methods"></a>Métodos

| Nome | Descrição |
|-|-|
| `static quaternion identity()` | Retorna uma instância da identidade Quaternion. |

## <a name="operators"></a>Operadores

| Nome | Descrição |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | Adiciona dois quaternions. |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | Subtrai um Quaternion de outro Quaternion. |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | Multiplica um Quaternion por outro Quaternion. |
| `quaternion operator* (quaternion const& value1, float value2)` | Multiplica um Quaternion por um valor escalar. |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | Divide um Quaternion por outro Quaternion. |
| `quaternion operator- (quaternion const& value)` | Inverte o sinal de cada componente do Quaternion. |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | O in-loco adiciona dois quaternions. |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | O in-loco subtrai um Quaternion de outro Quaternion. |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | O in-loco multiplica um Quaternion por outro Quaternion. |
| `quaternion& operator*= (quaternion& value1, float value2)` | O in-loco nultiplies um Quaternion por um valor escalar. |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | O in-loco divide um Quaternion por outro Quaternion. |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | Determina se duas instâncias de Quaternion são iguais. |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | Determina se duas instâncias de Quaternion não são iguais. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | Converte um Quaternion em um **Microsoft. Graphics. Canvas. Numerics. Quaternion**. |

## <a name="fields"></a>Campos

| Nome | Descrição |
|-|-|
| `float x` | Valor X do componente de vetor do Quaternion. |
| `float y` | Valor Y do componente de vetor do Quaternion. |
| `float z` | Valor Z do componente de vetor do Quaternion. |
| `float w` | Componente de rotação do Quaternion. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | Windows:: Foundation:: numéricos |
| parâmetro | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics. h](windowsnumerics-h-apis-portal.md)
