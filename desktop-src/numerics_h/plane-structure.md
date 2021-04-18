---
title: estrutura do plano (Windowsnumerics. h)
description: Essa estrutura representa um plano usando um vetor 3D normal e um valor de distância.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- estrutura do plano
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105802160"
---
# <a name="plane-structure"></a>estrutura do plano

Essa estrutura representa um plano usando um vetor 3D normal e um valor de distância.

Esse tipo está disponível apenas em C++. Seu equivalente em .NET é [System. Numerics. avião](/dotnet/api/system.numerics.plane?view=netframework-4.8).

## <a name="constructors"></a>Construtores

| Nome | Descrição |
|-|-|
| `plane()` | Cria um plano não inicializado. |
| `plane(float x, float y, float z, float d)` | Cria um plano com os valores especificados. |
| `plane(float3 normal, float d)` | Cria um plano de um float3 e uma distância. |
| `explicit plane(float4 value)` | Cria um plano de um FLOAT4. |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Converte um **Microsoft. Graphics. Canvas. Numerics. avião** em um plano. |

## <a name="functions"></a>Funções

| Nome | Descrição |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | Cria um plano de um conjunto de três posições de vértice, que devem ser diferentes e não em uma linha reta. |
| `plane normalize(plane const& value)` | Altera os coeficientes do vetor normal de um plano para torná-lo do comprimento da unidade. |
| `plane transform(plane const& plane, float4x4 const& matrix)` | Transforma um plano normalizado por uma matriz. |
| `plane transform(plane const& plane, quaternion const& rotation)` | Transforma um plano normalizado por uma rotação de Quaternion. |
| `float dot(plane const& plane, float4 const& value)` | Calcula o produto de ponto de um plano com um vetor. |
| `float dot_coordinate(plane const& plane, float3 const& value)` | Calcula o produto de ponto de um plano com uma coordenada float3. Diferentemente \_ do ponto normal, essa computação inclui o valor do plano d. |
| `float dot_normal(plane const& plane, float3 const& value)` | Calcula o produto de ponto de um plano com um float3 normal. Ao contrário \_ da coordenada de ponto, essa computação ignora o valor de plano d. |

## <a name="operators"></a>Operadores

| Nome | Descrição |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | Determina se duas instâncias do plano são iguais. |
| `bool operator!= (plane const& value1, plane const& value2)` | Determina se duas instâncias do plano não são iguais. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | Converte um plano em um **Microsoft. Graphics. Canvas. Numerics. avião**. |

## <a name="fields"></a>Campos

| Nome | Descrição |
|-|-|
| `float3 normal` | Vetor normal do plano. |
| `float d` | Distância do plano ao longo do normal da origem. |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Namespace | Windows:: Foundation:: numéricos |
| parâmetro | <dl> <dt>Windowsnumerics. h</dt> </dl> |

## <a name="see-also"></a>Confira também

[APIs windowsnumerics. h](windowsnumerics-h-apis-portal.md)
