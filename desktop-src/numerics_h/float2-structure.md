---
title: estrutura float2 (Windowsnumerics. h)
description: Um vetor com dois componentes.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- estrutura float2
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793752"
---
# <a name="float2-structure"></a>estrutura float2

Um vetor com dois componentes.

Esse tipo está disponível apenas em C++. Seu equivalente em .NET é [System. Numerics. vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).

## <a name="constructors"></a>Construtores

| Nome | Descrição |
|-|-|
| `float2()` | Cria um float2 não inicializado. |
| `float2(float x, float y)` | Cria um float2 com os valores especificados. |
| `explicit float2(float value)` | Cria um float2 com todos os componentes definidos para o valor especificado. |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | Converte um **Microsoft. Graphics. Canvas. Numerics. vector2** em um float2. |
| `float2(Windows::Foundation::Point const& value)` | Converte um [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) em um float2. |
| `float2(Windows::Foundation::Size const& value)` | Converte um [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) em um float2. |

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `float length(float2 const& value)` | Calcula o comprimento ou a distância euclidiana do vetor. |
| `float length_squared(float2 const& value)` | Calcula o comprimento ou a distância euclidiana do vetor ao quadrado. |
| `float distance(float2 const& value1, float2 const& value2)` | Calcula a distância euclidiana entre dois vetores. |
| `float distance_squared(float2 const& value1, float2 const& value2)` | Calcula a distância euclidiana entre dois vetores ao quadrado. |
| `float dot(float2 const& value1, float2 const& value2)` | Calcula o produto de ponto de dois vetores. |
| `float2 normalize(float2 const& value)` | Cria um vetor de unidade a partir do vetor especificado. |
| `float2 reflect(float2 const& vector, float2 const& normal)` | Determina o vetor de reflexão do vetor e normal específico. |
| `float2 min(float2 const& value1, float2 const& value2)` | Retorna um vetor que contém o valor mais baixo de cada par de componentes correspondente. |
| `float2 max(float2 const& value1, float2 const& value2)` | Retorna um vetor que contém o valor mais alto de cada par de componentes correspondente. |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | Restringe um valor a estar dentro de um intervalo especificado. |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | Executa uma interpolação linear entre dois vetores. |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | Transforma o vetor (x, y, 0, 1) pela matriz especificada. |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | Transforma o vetor (x, y, 0, 1) pela matriz especificada. |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | Transforma o vetor normal (x, y, 0, 0) pela matriz especificada. |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | Transforma o vetor normal (x, y, 0, 0) pela matriz especificada. |
| `float2 transform(float2 const& value, quaternion const& rotation)` | Transforma um float2 pelo Quaternion especificado. |

## <a name="methods"></a>Métodos

| Nome | Descrição |
|-|-|
| `static float2 zero()` | Retorna um float2 com todos os seus componentes definidos como zero. |
| `static float2 one()` | Retorna um float2 com todos os seus componentes definidos como um. |
| `static float2 unit_x()` | Retorna o float2 (1, 0). |
| `static float2 unit_y()` | Retorna o float2 (0, 1). |

## <a name="operators"></a>Operadores

| Nome | Descrição |
|-|-|
| `operator Windows::Foundation::Point() const` | Converte um float2 em um [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point). |
| `operator Windows::Foundation::Size() const` | Converte um float2 em um [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size). |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | Adiciona dois vetores. |
| `float2 operator- (float2 const& value1, float2 const& value2)` | Subtrai um vetor de um vetor. |
| `float2 operator* (float2 const& value1, float2 const& value2)` | Multiplica os componentes de dois vetores entre si. |
| `float2 operator* (float2 const& value1, float value2)` | Multiplica um vetor por um escalar. |
| `float2 operator* (float value1, float2 const& value2)` | Multiplica um vetor por um escalar. |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | Divide os componentes de um vetor pelos componentes de outro vetor. |
| `float2 operator/ (float2 const& value1, float value2)` | Divide um vetor por um valor escalar. |
| `float2 operator- (float2 const& value)` | Retorna um ponto de vetor na direção oposta. |
| `float2& operator+= (float2& value1, float2 const& value2)` | O in-loco adiciona dois vetores. |
| `float2& operator-= (float2& value1, float2 const& value2)` | O in-loco subtrai um vetor de um vetor. |
| `float2& operator*= (float2& value1, float2 const& value2)` | O in-loco multiplica os componentes de dois vetores entre si. |
| `float2& operator*= (float2& value1, float value2)` | O in-loco multiplica um vetor por um escalar. |
| `float2& operator/= (float2& value1, float2 const& value2)` | O in-loco divide os componentes de um vetor pelos componentes de outro vetor. |
| `float2& operator/= (float2& value1, float value2)` | O in-loco divide um vetor por um valor escalar. |
| `bool operator== (float2 const& value1, float2 const& value2)` | Determina se duas instâncias de float2 são iguais. |
| `bool operator!= (float2 const& value1, float2 const& value2)` | Determina se duas instâncias de float2 não são iguais. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | Converte um float2 em um **Microsoft. Graphics. Canvas. Numerics. vector2**. |

## <a name="fields"></a>Campos

| Nome | Descrição |
|-|-|
| `float x` | Componente X do vetor. |
| `float y` | Componente Y do vetor. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | Windows:: Foundation:: numéricos |
| parâmetro | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics. h](windowsnumerics-h-apis-portal.md)
