---
title: Estrutura float4x4 (Windowsnumerics.h)
description: Uma matriz 4x4, usada para transformar em 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- Estrutura float4x4
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c918ee81ddac31d697ff3885e04e8cb530cd31a98f842c109f9d281786ee2539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825266"
---
# <a name="float4x4-structure"></a>Estrutura float4x4

Uma matriz 4x4, usada para transformar em 3D.

Esse tipo de matriz usa um layout de vetor de linha. Os x, y e z do vetor de tradução dessa matriz correspondem aos campos m41, m42, m43.

Esse tipo só está disponível no C++. Seu equivalente do .NET [é System.Numerics.Matrix4x4.](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8)

## <a name="constructors"></a>Construtores

| Nome | Descrição |
|-|-|
| `float4x4()` | Cria um float4x4 não reinicializado. |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | Cria um float4x4 com os valores especificados. |
| `explicit float4x4(float3x2 value)` | Cria um float4x4 de um float3x2. |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | Converte um **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** em um float4x4. |

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | Cria um giro esférico que gira em torno de uma posição de objeto especificada, usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | Cria um giro cilíndrico que gira em torno de um eixo especificado, usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_translation(float3 const& position)` | Cria uma matriz de translação. |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | Cria uma matriz de translação. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | Cria uma matriz de dimensionamento centralizada na origem. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | Cria uma matriz de dimensionamento centralizada no ponto especificado. |
| `float4x4 make_float4x4_scale(float3 const& scales)` | Cria uma matriz de dimensionamento centralizada na origem. |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | Cria uma matriz de dimensionamento centralizada no ponto especificado. |
| `float4x4 make_float4x4_scale(float scale)` | Cria uma matriz de dimensionamento centralizada na origem. |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | Cria uma matriz de dimensionamento centralizada no ponto especificado. |
| `float4x4 make_float4x4_rotation_x(float radians)` | Cria uma matriz de rotação do eixo x, centralizada na origem. |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | Cria uma matriz de rotação do eixo x, centralizada no ponto especificado. |
| `float4x4 make_float4x4_rotation_y(float radians)` | Cria uma matriz de rotação do eixo y, centralizada na origem. |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | Cria uma matriz de rotação do eixo y, centralizada no ponto especificado. |
| `float4x4 make_float4x4_rotation_z(float radians)` | Cria uma matriz de rotação do eixo z, centralizada na origem. |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | Cria uma matriz de rotação do eixo z, centralizada no ponto especificado. |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | Cria uma matriz que gira em torno de um vetor arbitrário. |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | Cria uma matriz de projeção de perspectiva com base em um campo de exibição, usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | Cria uma matriz de projeção de perspectiva usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | Cria uma matriz de projeção de perspectiva personalizada usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | Cria uma matriz de projeção ortográfica usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | Cria uma matriz de projeção ortográfica personalizada usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | Cria uma matriz de exibição usando um sistema de coordenadas à direita. |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | Cria uma matriz de mundo usando um sistema de coordenadas à direita. Isso pode ser usado para posicionar objetos no espaço 3D. |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | Cria uma matriz de rotação de um quaterão. |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Cria uma matriz de rotação com base em um yaw, pitch e roll especificados. |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | Cria uma matriz que nivela a geometria em um plano especificado como se projetando uma sombra de uma fonte de luz especificada. |
| `float4x4 make_float4x4_reflection(plane const& value)` | Cria uma matriz que reflete o sistema de coordenadas sobre um plano especificado. |
| `bool is_identity(float4x4 const& value)` | Verifica se esta é uma matriz de identidade. |
| `float determinant(float4x4 const& value)` | Calcula o determinante da matriz. |
| `float3 translation(float4x4 const& value)` | Obtém o vetor de tradução da matriz. |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | Calcula o inverso de uma matriz. Retornará true se a matriz puder ser invertida; false caso contrário, . |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | Extrai os componentes escalares, de conversão e de rotação de uma matriz SRT (escala/rotação/conversão)3D. Retornará true se a matriz puder ser decomposta; false caso contrário, . |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | Transforma uma matriz aplicando uma rotação de quaterna. |
| `float4x4 transpose(float4x4 const& matrix)` | Transpõe os componentes de uma matriz ao longo de sua diagonal. |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | Interpola linearmente entre os valores correspondentes de duas matrizes. |

## <a name="methods"></a>Métodos

| Nome | Descrição |
|-|-|
| `static float4x4 identity()` | Retorna uma instância da matriz de identidade. |

## <a name="operators"></a>Operadores

| Nome | Descrição |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | Adiciona cada componente de uma matriz a outra matriz. |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | Subtrai cada componente de uma matriz de outra matriz. |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | Multiplica uma matriz por outra matriz. Isso tem o efeito de concatenar duas transformaçãos. |
| `float4x4 operator* (float4x4 const& value1, float value2)` | Multiplica cada componente de uma matriz por um valor escalar. |
| `float4x4 operator- (float4x4 const& value)` | Nega cada componente de uma matriz. |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | In-locar adiciona cada componente de uma matriz a outra matriz. |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | No local, subtrai cada componente de uma matriz de outra matriz. |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | O in-place multiplica uma matriz por outra matriz. Isso tem o efeito de concatenar duas transformaçãos. |
| `float4x4& operator*= (float4x4& value1, float value2)` | O in-place multiplica cada componente de uma matriz por um valor escalar. |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | Determina se duas instâncias de float4x4 são iguais. |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | Determina se duas instâncias de float4x4 não são iguais. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | Converte um float4x4 em **um Microsoft.Graphics.Canvas.Numerics.Matrix4x4.** |

## <a name="fields"></a>Campos

| Nome | Descrição |
|-|-|
| `float m11` | Valor na linha 1 coluna 1 da matriz. |
| `float m12` | Valor na linha 1 coluna 2 da matriz. |
| `float m13` | Valor na linha 1 coluna 3 da matriz. |
| `float m14` | Valor na linha 1 coluna 4 da matriz. |
| `float m21` | Valor na linha 2 coluna 1 da matriz. |
| `float m22` | Valor na linha 2 coluna 2 da matriz. |
| `float m23` | Valor na linha 2 coluna 3 da matriz. |
| `float m24` | Valor na linha 2 coluna 4 da matriz. |
| `float m31` | Valor na linha 3 coluna 1 da matriz. |
| `float m32` | Valor na linha 3 coluna 2 da matriz. |
| `float m33` | Valor na linha 3 coluna 3 da matriz. |
| `float m34` | Valor na linha 3 coluna 4 da matriz. |
| `float m41` | Valor na linha 4 coluna 1 da matriz. |
| `float m42` | Valor na linha 4 coluna 2 da matriz. |
| `float m43` | Valor na linha 4 coluna 3 da matriz. |
| `float m44` | Valor na linha 4 coluna 4 da matriz. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | Windows:: Foundation:: numéricos |
| Cabeçalho | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics. h](windowsnumerics-h-apis-portal.md)
