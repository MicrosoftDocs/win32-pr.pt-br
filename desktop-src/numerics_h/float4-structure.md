---
title: estrutura FLOAT4 (Windowsnumerics. h)
description: Um vetor com quatro componentes.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- estrutura FLOAT4
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4a2a4721e3ab7e5520545b42367d2432ba967f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765996"
---
# <a name="float4-structure"></a>estrutura FLOAT4

Um vetor com quatro componentes.

Esse tipo está disponível apenas em C++. Seu equivalente em .NET é [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).

## <a name="constructors"></a>Construtores

| Nome | Descrição |
|-|-|
| `float4()` | Cria um FLOAT4 não inicializado. |
| `float4(float x, float y, float z, float w)` | Cria um FLOAT4 com os valores especificados. |
| `float4(float2 value, float z, float w)` | Cria um FLOAT4 com x e y copiados de um float2 mais os valores z e w especificados. |
| `float4(float3 value, float w)` | Cria um FLOAT4 com x, y e z copiados de um float3 mais o valor w especificado. |
| `explicit float4(float value)` | Cria um FLOAT4 com todos os com. gentes definidos com o valor especificado. |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | Converte um **Microsoft. Graphics. Canvas. Numerics. Vector4** em um FLOAT4. |

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `float length(float4 const& value)` | Calcula o comprimento ou a distância euclidiana do vetor. |
| `float length_squared(float4 const& value)` | Calcula o comprimento ou a distância euclidiana do vetor ao quadrado. |
| `float distance(float4 const& value1, float4 const& value2)` | Calcula a distância euclidiana entre dois vetores. |
| `float distance_squared(float4 const& value1, float4 const& value2)` | Calcula a distância euclidiana entre dois vetores ao quadrado. |
| `float dot(float4 const& vector1, float4 const& vector2)` | Calcula o produto de ponto de dois vetores. |
| `float4 normalize(float4 const& vector)` | Cria um vetor de unidade a partir do vetor especificado. |
| `float4 min(float4 const& value1, float4 const& value2)` | Retorna um vetor que contém o valor mais baixo de cada par de componentes correspondente. |
| `float4 max(float4 const& value1, float4 const& value2)` | Retorna um vetor que contém o valor mais alto de cada par de componentes correspondente. |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | Restringe um valor a estar dentro de um intervalo especificado. |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | Executa uma interpolação linear entre dois vetores. |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | Transforma um FLOAT4 pela matriz especificada. |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | Transforma um float3 pela matriz especificada, retornando um FLOAT4. |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | Transforma um float2 pela matriz especificada, retornando um FLOAT4. |
| `float4 transform(float4 const& value, quaternion const& rotation)` | Transforma um FLOAT4 pelo Quaternion especificado. |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | Transforma um float3 pelo Quaternion fornecido, retornando um FLOAT4. |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | Transforma um float2 pelo Quaternion fornecido, retornando um FLOAT4. |

## <a name="methods"></a>Métodos

| Nome | Descrição |
|-|-|
| `static float4 zero()` | Retorna um FLOAT4 com todos os seus componentes definidos como zero. |
| `static float4 one()` | Retorna um FLOAT4 com todos os seus componentes definidos como um. |
| `static float4 unit_x()` | Retorna o FLOAT4 (1, 0, 0, 0). |
| `static float4 unit_y()` | Retorna o FLOAT4 (0, 1, 0, 0). |
| `static float4 unit_z()` | Retorna o FLOAT4 (0, 0, 1, 0). |
| `static float4 unit_w()` | Retorna o FLOAT4 (0, 0, 0, 1). |

## <a name="operators"></a>Operadores

| Nome | Descrição |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | Adiciona dois vetores. |
| `float4 operator- (float4 const& value1, float4 const& value2)` | Subtrai um vetor de um vetor. |
| `float4 operator* (float4 const& value1, float4 const& value2)` | Multiplica os componentes de dois vetores entre si. |
| `float4 operator* (float4 const& value1, float value2)` | Multiplica um vetor por um escalar. |
| `float4 operator* (float value1, float4 const& value2)` | Multiplica um vetor por um escalar. |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | Divide os componentes de um vetor pelos componentes de outro vetor. |
| `float4 operator/ (float4 const& value1, float value2)` | Divide um vetor por um valor escalar. |
| `float4 operator- (float4 const& value)` | Retorna um ponto de vetor na direção oposta. |
| `float4& operator+= (float4& value1, float4 const& value2)` | O in-loco adiciona dois vetores. |
| `float4& operator-= (float4& value1, float4 const& value2)` | O in-loco subtrai um vetor de um vetor. |
| `float4& operator*= (float4& value1, float4 const& value2)` | O in-loco multiplica os componentes de dois vetores entre si. |
| `float4& operator*= (float4& value1, float value2)` | O in-loco multiplica um vetor por um escalar. |
| `float4& operator/= (float4& value1, float4 const& value2)` | O in-loco divide os componentes de um vetor pelos componentes de outro vetor. |
| `float4& operator/= (float4& value1, float value2)` | O in-loco divide um vetor por um valor escalar. |
| `bool operator== (float4 const& value1, float4 const& value2)` | Determina se duas instâncias de FLOAT4 são iguais. |
| `bool operator!= (float4 const& value1, float4 const& value2)` | Determina se duas instâncias de FLOAT4 não são iguais. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | Converte um FLOAT4 em um **Microsoft. Graphics. Canvas. Numerics. Vector4**. |

## <a name="fields"></a>Campos

| Nome | Descrição |
|-|-|
| `float x` | Componente X do vetor. |
| `float y` | Componente Y do vetor. |
| `float z` | Componente Z do vetor. |
| `float w` | Componente W do vetor. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | Windows:: Foundation:: numéricos |
| parâmetro | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics. h](windowsnumerics-h-apis-portal.md)
