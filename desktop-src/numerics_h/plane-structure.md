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
# <a name="plane-structure"></a><span data-ttu-id="627b2-104">estrutura do plano</span><span class="sxs-lookup"><span data-stu-id="627b2-104">plane structure</span></span>

<span data-ttu-id="627b2-105">Essa estrutura representa um plano usando um vetor 3D normal e um valor de distância.</span><span class="sxs-lookup"><span data-stu-id="627b2-105">This structure represents a plane using a 3D vector normal and a distance value.</span></span>

<span data-ttu-id="627b2-106">Esse tipo está disponível apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="627b2-106">This type is available only in C++.</span></span> <span data-ttu-id="627b2-107">Seu equivalente em .NET é [System. Numerics. avião](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="627b2-107">Its .NET equivalent is [System.Numerics.Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="627b2-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="627b2-108">Constructors</span></span>

| <span data-ttu-id="627b2-109">Nome</span><span class="sxs-lookup"><span data-stu-id="627b2-109">Name</span></span> | <span data-ttu-id="627b2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="627b2-110">Description</span></span> |
|-|-|
| `plane()` | <span data-ttu-id="627b2-111">Cria um plano não inicializado.</span><span class="sxs-lookup"><span data-stu-id="627b2-111">Creates an uninitialized plane.</span></span> |
| `plane(float x, float y, float z, float d)` | <span data-ttu-id="627b2-112">Cria um plano com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="627b2-112">Creates a plane with the specified values.</span></span> |
| `plane(float3 normal, float d)` | <span data-ttu-id="627b2-113">Cria um plano de um float3 e uma distância.</span><span class="sxs-lookup"><span data-stu-id="627b2-113">Creates a plane from a float3 and a distance.</span></span> |
| `explicit plane(float4 value)` | <span data-ttu-id="627b2-114">Cria um plano de um FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="627b2-114">Creates a plane from a float4.</span></span> |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | <span data-ttu-id="627b2-115">Converte um **Microsoft. Graphics. Canvas. Numerics. avião** em um plano.</span><span class="sxs-lookup"><span data-stu-id="627b2-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span></span> |

## <a name="functions"></a><span data-ttu-id="627b2-116">Funções</span><span class="sxs-lookup"><span data-stu-id="627b2-116">Functions</span></span>

| <span data-ttu-id="627b2-117">Nome</span><span class="sxs-lookup"><span data-stu-id="627b2-117">Name</span></span> | <span data-ttu-id="627b2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="627b2-118">Description</span></span> |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | <span data-ttu-id="627b2-119">Cria um plano de um conjunto de três posições de vértice, que devem ser diferentes e não em uma linha reta.</span><span class="sxs-lookup"><span data-stu-id="627b2-119">Creates a plane from a set of three vertex positions, which must all be different and not in a straight line.</span></span> |
| `plane normalize(plane const& value)` | <span data-ttu-id="627b2-120">Altera os coeficientes do vetor normal de um plano para torná-lo do comprimento da unidade.</span><span class="sxs-lookup"><span data-stu-id="627b2-120">Changes the coefficients of the normal vector of a plane to make it of unit length.</span></span> |
| `plane transform(plane const& plane, float4x4 const& matrix)` | <span data-ttu-id="627b2-121">Transforma um plano normalizado por uma matriz.</span><span class="sxs-lookup"><span data-stu-id="627b2-121">Transforms a normalized plane by a matrix.</span></span> |
| `plane transform(plane const& plane, quaternion const& rotation)` | <span data-ttu-id="627b2-122">Transforma um plano normalizado por uma rotação de Quaternion.</span><span class="sxs-lookup"><span data-stu-id="627b2-122">Transforms a normalized plane by a quaternion rotation.</span></span> |
| `float dot(plane const& plane, float4 const& value)` | <span data-ttu-id="627b2-123">Calcula o produto de ponto de um plano com um vetor.</span><span class="sxs-lookup"><span data-stu-id="627b2-123">Calculates the dot product of a plane with a vector.</span></span> |
| `float dot_coordinate(plane const& plane, float3 const& value)` | <span data-ttu-id="627b2-124">Calcula o produto de ponto de um plano com uma coordenada float3.</span><span class="sxs-lookup"><span data-stu-id="627b2-124">Calculates the dot product of a plane with a float3 coordinate.</span></span> <span data-ttu-id="627b2-125">Diferentemente \_ do ponto normal, essa computação inclui o valor do plano d.</span><span class="sxs-lookup"><span data-stu-id="627b2-125">Unlike dot\_normal, this computation includes the plane d value.</span></span> |
| `float dot_normal(plane const& plane, float3 const& value)` | <span data-ttu-id="627b2-126">Calcula o produto de ponto de um plano com um float3 normal.</span><span class="sxs-lookup"><span data-stu-id="627b2-126">Calculates the dot product of a plane with a float3 normal.</span></span> <span data-ttu-id="627b2-127">Ao contrário \_ da coordenada de ponto, essa computação ignora o valor de plano d.</span><span class="sxs-lookup"><span data-stu-id="627b2-127">Unlike dot\_coordinate, this computation ignores the plane d value.</span></span> |

## <a name="operators"></a><span data-ttu-id="627b2-128">Operadores</span><span class="sxs-lookup"><span data-stu-id="627b2-128">Operators</span></span>

| <span data-ttu-id="627b2-129">Nome</span><span class="sxs-lookup"><span data-stu-id="627b2-129">Name</span></span> | <span data-ttu-id="627b2-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="627b2-130">Description</span></span> |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | <span data-ttu-id="627b2-131">Determina se duas instâncias do plano são iguais.</span><span class="sxs-lookup"><span data-stu-id="627b2-131">Determines whether two instances of plane are equal.</span></span> |
| `bool operator!= (plane const& value1, plane const& value2)` | <span data-ttu-id="627b2-132">Determina se duas instâncias do plano não são iguais.</span><span class="sxs-lookup"><span data-stu-id="627b2-132">Determines whether two instances of plane are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | <span data-ttu-id="627b2-133">Converte um plano em um **Microsoft. Graphics. Canvas. Numerics. avião**.</span><span class="sxs-lookup"><span data-stu-id="627b2-133">Converts a plane to a **Microsoft.Graphics.Canvas.Numerics.Plane**.</span></span> |

## <a name="fields"></a><span data-ttu-id="627b2-134">Campos</span><span class="sxs-lookup"><span data-stu-id="627b2-134">Fields</span></span>

| <span data-ttu-id="627b2-135">Nome</span><span class="sxs-lookup"><span data-stu-id="627b2-135">Name</span></span> | <span data-ttu-id="627b2-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="627b2-136">Description</span></span> |
|-|-|
| `float3 normal` | <span data-ttu-id="627b2-137">Vetor normal do plano.</span><span class="sxs-lookup"><span data-stu-id="627b2-137">Normal vector of the plane.</span></span> |
| `float d` | <span data-ttu-id="627b2-138">Distância do plano ao longo do normal da origem.</span><span class="sxs-lookup"><span data-stu-id="627b2-138">Distance of the plane along its normal from the origin.</span></span> |

## <a name="requirements"></a><span data-ttu-id="627b2-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="627b2-139">Requirements</span></span>

| <span data-ttu-id="627b2-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="627b2-140">Requirement</span></span> | <span data-ttu-id="627b2-141">Valor</span><span class="sxs-lookup"><span data-stu-id="627b2-141">Value</span></span> |
|-|-|
| <span data-ttu-id="627b2-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="627b2-142">Namespace</span></span> | <span data-ttu-id="627b2-143">Windows:: Foundation:: numéricos</span><span class="sxs-lookup"><span data-stu-id="627b2-143">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="627b2-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="627b2-144">Header</span></span> | <dl> <span data-ttu-id="627b2-145"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="627b2-145"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="627b2-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="627b2-146">See also</span></span>

[<span data-ttu-id="627b2-147">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="627b2-147">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
