---
title: estrutura float3x2 (Windowsnumerics. h)
description: Uma matriz 3x2, usada para transformações 2D.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- estrutura float3x2
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d403446fa3544bdb001c065e9874f812a829680e19a5e6b526ed12276fd6e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971755"
---
# <a name="float3x2-structure"></a>estrutura float3x2

Uma matriz 3x2, usada para transformações 2D.

Esse tipo de matriz usa um layout de vetor de linha. O x e y do vetor de conversão desta matriz correspondem aos campos M31, M32.

Esse tipo está disponível apenas em C++. Seu equivalente em .NET é [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).

## <a name="constructors"></a>Construtores

| Nome | Descrição |
|-|-|
| `float3x2()` | Cria um float3x2 não inicializado. |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | Cria um float3x2 com os valores especificados. |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | Converte um **Microsoft. Graphics. Canvas. Numerics. Matrix3x2** em um float3x2. |

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | Cria uma matriz de translação. |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | Cria uma matriz de translação. |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | Cria uma matriz de dimensionamento, centralizada na origem. |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | Cria uma matriz de dimensionamento, centralizada no ponto especificado. |
| `float3x2 make_float3x2_scale(float2 const& scales)` | Cria uma matriz de dimensionamento, centralizada na origem. |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | Cria uma matriz de dimensionamento, centralizada no ponto especificado. |
| `float3x2 make_float3x2_scale(float scale)` | Cria uma matriz de dimensionamento, centralizada na origem. |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | Cria uma matriz de dimensionamento, centralizada no ponto especificado. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | Cria uma matriz de distorção, centralizada na origem. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | Cria uma matriz de distorção, centralizada no ponto especificado. |
| `float3x2 make_float3x2_rotation(float radians)` | Cria uma matriz de rotação, centralizada na origem. |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | Cria uma matriz de rotação, centralizada no ponto especificado. |
| `bool is_identity(float3x2 const& value)` | Verifica se esta é uma matriz de identidade. |
| `float determinant(float3x2 const& value)` | Calcula o determinante da matriz. |
| `float2 translation(float3x2 const& value)` | Obtém o vetor de tradução da matriz. |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | Calcula o inverso de uma matriz. Retornará true se a matriz puder ser invertida; caso contrário, false. |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | Interpola linearmente entre os valores correspondentes de duas matrizes. |

## <a name="methods"></a>Métodos

| Nome | Descrição |
|-|-|
| `static float3x2 identity()` | Retorna uma instância da matriz de identidade. |

## <a name="operators"></a>Operadores

| Nome | Descrição |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | Adiciona cada componente de uma matriz a outra matriz. |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | Subtrai cada componente de uma matriz de outra matriz. |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | Multiplica uma matriz por outra matriz. Isso tem o efeito de concatenar duas transformações. |
| `float3x2 operator* (float3x2 const& value1, float value2)` | Multiplica cada componente de uma matriz por um valor escalar. |
| `float3x2 operator- (float3x2 const& value)` | Nega cada componente de uma matriz. |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | In-loco adiciona cada componente de uma matriz a outra matriz. |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | O in-loco subtrai cada componente de uma matriz de outra matriz. |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | O in-loco multiplica uma matriz por outra matriz. Isso tem o efeito de concatenar duas transformações. |
| `float3x2& operator*= (float3x2& value1, float value2)` | O in-loco multiplica cada componente de uma matriz por um valor escalar. |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | Determina se duas instâncias de float3x2 são iguais. |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | Determina se duas instâncias de float3x2 não são iguais. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | Converte um float3x2 em um **Microsoft. Graphics. Canvas. Numerics. Matrix3x2**. |

## <a name="fields"></a>Campos

| Nome | Descrição |
|-|-|
| `float m11` | Valor na linha 1, coluna 1 da matriz. |
| `float m12` | Valor na linha 1, coluna 2 da matriz. |
| `float m21` | Valor na linha 2, coluna 1 da matriz. |
| `float m22` | Valor na linha 2, coluna 2 da matriz. |
| `float m31` | Valor na linha 3, coluna 1 da matriz. |
| `float m32` | Valor na linha 3, coluna 2 da matriz. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | Windows:: Foundation:: numéricos |
| Cabeçalho | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics. h](windowsnumerics-h-apis-portal.md)
