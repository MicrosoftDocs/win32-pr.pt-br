---
title: Estrutura float3 (Windowsnumerics.h)
description: Um vetor com três componentes.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- Estrutura float3
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521c63f99c35e68f18d9a6c0a81118f647ff131effb0f6528e2ef3882c43e234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939506"
---
# <a name="float3-structure"></a>Estrutura float3

Um vetor com três componentes.

Esse tipo só está disponível no C++. Seu equivalente do .NET [é System.Numerics.Vector3.](/dotnet/api/system.numerics.vector3?view=netframework-4.8)

## <a name="constructors"></a>Construtores

| Nome | Descrição |
|-|-|
| `float3()` | Cria um float3 não reinicializado. |
| `float3(float x, float y, float z)` | Cria um float3 com os valores especificados. |
| `float3(float2 value, float z)` | Cria um float3 com x e y copiados de um float2 mais o valor z especificado. |
| `explicit float3(float value)` | Cria um float3 com todos os componentes definidos para o valor especificado. |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | Converte um **Microsoft.Graphics.Canvas.Numerics.Vector3** em um float3. |

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `float length(float3 const& value)` | Calcula o comprimento ou a distância euclidiana do vetor. |
| `float length_squared(float3 const& value)` | Calcula o comprimento ou a distância euclidiana do vetor ao quadrado. |
| `float distance(float3 const& value1, float3 const& value2)` | Calcula a distância euclidiana entre dois vetores. |
| `float distance_squared(float3 const& value1, float3 const& value2)` | Calcula a distância euclidiana entre dois vetores ao quadrado. |
| `float dot(float3 const& vector1, float3 const& vector2)` | Calcula o produto de ponto de dois vetores. |
| `float3 normalize(float3 const& value)` | Cria um vetor de unidade do vetor especificado. |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | Calcula o produto cruzado de dois vetores. |
| `float3 reflect(float3 const& vector, float3 const& normal)` | Determina o vetor de reflexão do vetor determinado e normal. |
| `float3 min(float3 const& value1, float3 const& value2)` | Retorna um vetor que contém o valor mais baixo de cada par de componentes correspondente. |
| `float3 max(float3 const& value1, float3 const& value2)` | Retorna um vetor que contém o valor mais alto de cada par de componentes correspondente. |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | Restringe um valor a estar dentro de um intervalo especificado. |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | Executa uma interpolação linear entre dois vetores. |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | Transforma o vetor (x, y, z, 1) pela matriz especificada. |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | Transforma o vetor normal (x, y, z, 0) pela matriz especificada. |
| `float3 transform(float3 const& value, quaternion const& rotation)` | Transforma um float3 pelo quatternion determinado. |

## <a name="methods"></a>Métodos

| Nome | Descrição |
|-|-|
| `static float3 zero()` | Retorna um float3 com todos os seus componentes definidos como zero. |
| `static float3 one()` | Retorna um float3 com todos os seus componentes definidos como um. |
| `static float3 unit_x()` | Retorna o float3 (1, 0, 0). |
| `static float3 unit_y()` | Retorna o float3 (0, 1, 0). |
| `static float3 unit_z()` | Retorna o float3 (0, 0, 1). |

## <a name="operators"></a>Operadores

| Nome | Descrição |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | Adiciona dois vetores. |
| `float3 operator- (float3 const& value1, float3 const& value2)` | Subtrai um vetor de um vetor. |
| `float3 operator* (float3 const& value1, float3 const& value2)` | Multiplica os componentes de dois vetores uns pelos outros. |
| `float3 operator* (float3 const& value1, float value2)` | Multiplica um vetor por um escalar. |
| `float3 operator* (float value1, float3 const& value2)` | Multiplica um vetor por um escalar. |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | Divide os componentes de um vetor pelos componentes de outro vetor. |
| `float3 operator/ (float3 const& value1, float value2)` | Divide um vetor por um valor escalar. |
| `float3 operator- (float3 const& value)` | Retorna um vetor apontando na direção oposta. |
| `float3& operator+= (float3& value1, float3 const& value2)` | In-place adiciona dois vetores. |
| `float3& operator-= (float3& value1, float3 const& value2)` | No local, subtrai um vetor de um vetor. |
| `float3& operator*= (float3& value1, float3 const& value2)` | In-place multiplica os componentes de dois vetores uns pelos outros. |
| `float3& operator*= (float3& value1, float value2)` | In-place multiplica um vetor por um escalar. |
| `float3& operator/= (float3& value1, float3 const& value2)` | No local, divide os componentes de um vetor pelos componentes de outro vetor. |
| `float3& operator/= (float3& value1, float value2)` | In-loco divide um vetor por um valor escalar. |
| `bool operator== (float3 const& value1, float3 const& value2)` | Determina se duas instâncias de float3 são iguais. |
| `bool operator!= (float3 const& value1, float3 const& value2)` | Determina se duas instâncias de float3 não são iguais. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | Converte um float3 em **um Microsoft.Graphics.Canvas.Numerics.Vector3.** |

## <a name="fields"></a>Campos

| Nome | Descrição |
|-|-|
| `float x` | Componente X do vetor. |
| `float y` | Componente Y do vetor. |
| `float z` | Componente Z do vetor. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | Windows::Foundation::Numerics |
| Cabeçalho | <dl> <dt>Windowsnumerics.h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics.h](windowsnumerics-h-apis-portal.md)
