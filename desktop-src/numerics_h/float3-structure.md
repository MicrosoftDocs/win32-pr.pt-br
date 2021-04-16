---
title: estrutura float3 (Windowsnumerics. h)
description: Um vetor com três componentes.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- estrutura float3
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
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772748"
---
# <a name="float3-structure"></a><span data-ttu-id="ea759-104">estrutura float3</span><span class="sxs-lookup"><span data-stu-id="ea759-104">float3 structure</span></span>

<span data-ttu-id="ea759-105">Um vetor com três componentes.</span><span class="sxs-lookup"><span data-stu-id="ea759-105">A vector with three components.</span></span>

<span data-ttu-id="ea759-106">Esse tipo está disponível apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="ea759-106">This type is available only in C++.</span></span> <span data-ttu-id="ea759-107">Seu equivalente em .NET é [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="ea759-107">Its .NET equivalent is [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="ea759-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="ea759-108">Constructors</span></span>

| <span data-ttu-id="ea759-109">Nome</span><span class="sxs-lookup"><span data-stu-id="ea759-109">Name</span></span> | <span data-ttu-id="ea759-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea759-110">Description</span></span> |
|-|-|
| `float3()` | <span data-ttu-id="ea759-111">Cria um float3 não inicializado.</span><span class="sxs-lookup"><span data-stu-id="ea759-111">Creates an uninitialized float3.</span></span> |
| `float3(float x, float y, float z)` | <span data-ttu-id="ea759-112">Cria um float3 com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="ea759-112">Creates a float3 with the specified values.</span></span> |
| `float3(float2 value, float z)` | <span data-ttu-id="ea759-113">Cria um float3 com x e y copiados de um float2 mais o valor z especificado.</span><span class="sxs-lookup"><span data-stu-id="ea759-113">Creates a float3 with x and y copied from a float2 plus the specified z value.</span></span> |
| `explicit float3(float value)` | <span data-ttu-id="ea759-114">Cria um float3 com todos os componentes definidos para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ea759-114">Creates a float3 with all components set to the specified value.</span></span> |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | <span data-ttu-id="ea759-115">Converte um **Microsoft. Graphics. Canvas. Numerics. Vector3** em um float3.</span><span class="sxs-lookup"><span data-stu-id="ea759-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector3** to a float3.</span></span> |

## <a name="functions"></a><span data-ttu-id="ea759-116">Funções</span><span class="sxs-lookup"><span data-stu-id="ea759-116">Functions</span></span>

| <span data-ttu-id="ea759-117">Nome</span><span class="sxs-lookup"><span data-stu-id="ea759-117">Name</span></span> | <span data-ttu-id="ea759-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea759-118">Description</span></span> |
|-|-|
| `float length(float3 const& value)` | <span data-ttu-id="ea759-119">Calcula o comprimento ou a distância euclidiana do vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-119">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float3 const& value)` | <span data-ttu-id="ea759-120">Calcula o comprimento ou a distância euclidiana do vetor ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="ea759-120">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-121">Calcula a distância euclidiana entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="ea759-121">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-122">Calcula a distância euclidiana entre dois vetores ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="ea759-122">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="ea759-123">Calcula o produto de ponto de dois vetores.</span><span class="sxs-lookup"><span data-stu-id="ea759-123">Calculates the dot product of two vectors.</span></span> |
| `float3 normalize(float3 const& value)` | <span data-ttu-id="ea759-124">Cria um vetor de unidade a partir do vetor especificado.</span><span class="sxs-lookup"><span data-stu-id="ea759-124">Creates a unit vector from the specified vector.</span></span> |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="ea759-125">Calcula o produto cruzado de dois vetores.</span><span class="sxs-lookup"><span data-stu-id="ea759-125">Calculates the cross product of two vectors.</span></span> |
| `float3 reflect(float3 const& vector, float3 const& normal)` | <span data-ttu-id="ea759-126">Determina o vetor de reflexão do vetor e normal específico.</span><span class="sxs-lookup"><span data-stu-id="ea759-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float3 min(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-127">Retorna um vetor que contém o valor mais baixo de cada par de componentes correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea759-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float3 max(float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-128">Retorna um vetor que contém o valor mais alto de cada par de componentes correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea759-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | <span data-ttu-id="ea759-129">Restringe um valor a estar dentro de um intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="ea759-129">Restricts a value to be within a specified range.</span></span> |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | <span data-ttu-id="ea759-130">Executa uma interpolação linear entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="ea759-130">Performs a linear interpolation between two vectors.</span></span> |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="ea759-131">Transforma o vetor (x, y, z, 1) pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="ea759-131">Transforms the vector (x, y, z, 1) by the specified matrix.</span></span> |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | <span data-ttu-id="ea759-132">Transforma o vetor normal (x, y, z, 0) pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="ea759-132">Transforms the normal vector (x, y, z, 0) by the specified matrix.</span></span> |
| `float3 transform(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="ea759-133">Transforma um float3 pelo Quaternion especificado.</span><span class="sxs-lookup"><span data-stu-id="ea759-133">Transforms a float3 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="ea759-134">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea759-134">Methods</span></span>

| <span data-ttu-id="ea759-135">Nome</span><span class="sxs-lookup"><span data-stu-id="ea759-135">Name</span></span> | <span data-ttu-id="ea759-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea759-136">Description</span></span> |
|-|-|
| `static float3 zero()` | <span data-ttu-id="ea759-137">Retorna um float3 com todos os seus componentes definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="ea759-137">Returns a float3 with all of its components set to zero.</span></span> |
| `static float3 one()` | <span data-ttu-id="ea759-138">Retorna um float3 com todos os seus componentes definidos como um.</span><span class="sxs-lookup"><span data-stu-id="ea759-138">Returns a float3 with all of its components set to one.</span></span> |
| `static float3 unit_x()` | <span data-ttu-id="ea759-139">Retorna o float3 (1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="ea759-139">Returns the float3 (1, 0, 0).</span></span> |
| `static float3 unit_y()` | <span data-ttu-id="ea759-140">Retorna o float3 (0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="ea759-140">Returns the float3 (0, 1, 0).</span></span> |
| `static float3 unit_z()` | <span data-ttu-id="ea759-141">Retorna o float3 (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="ea759-141">Returns the float3 (0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="ea759-142">Operadores</span><span class="sxs-lookup"><span data-stu-id="ea759-142">Operators</span></span>

| <span data-ttu-id="ea759-143">Nome</span><span class="sxs-lookup"><span data-stu-id="ea759-143">Name</span></span> | <span data-ttu-id="ea759-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea759-144">Description</span></span> |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-145">Adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="ea759-145">Adds two vectors.</span></span> |
| `float3 operator- (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-146">Subtrai um vetor de um vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-146">Subtracts a vector from a vector.</span></span> |
| `float3 operator* (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-147">Multiplica os componentes de dois vetores entre si.</span><span class="sxs-lookup"><span data-stu-id="ea759-147">Multiplies the components of two vectors by each other.</span></span> |
| `float3 operator* (float3 const& value1, float value2)` | <span data-ttu-id="ea759-148">Multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="ea759-148">Multiplies a vector by a scalar.</span></span> |
| `float3 operator* (float value1, float3 const& value2)` | <span data-ttu-id="ea759-149">Multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="ea759-149">Multiplies a vector by a scalar.</span></span> |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-150">Divide os componentes de um vetor pelos componentes de outro vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-150">Divides the components of a vector by the components of another vector.</span></span> |
| `float3 operator/ (float3 const& value1, float value2)` | <span data-ttu-id="ea759-151">Divide um vetor por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ea759-151">Divides a vector by a scalar value.</span></span> |
| `float3 operator- (float3 const& value)` | <span data-ttu-id="ea759-152">Retorna um ponto de vetor na direção oposta.</span><span class="sxs-lookup"><span data-stu-id="ea759-152">Returns a vector pointing in the opposite direction.</span></span> |
| `float3& operator+= (float3& value1, float3 const& value2)` | <span data-ttu-id="ea759-153">O in-loco adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="ea759-153">In-place adds two vectors.</span></span> |
| `float3& operator-= (float3& value1, float3 const& value2)` | <span data-ttu-id="ea759-154">O in-loco subtrai um vetor de um vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-154">In-place subtracts a vector from a vector.</span></span> |
| `float3& operator*= (float3& value1, float3 const& value2)` | <span data-ttu-id="ea759-155">O in-loco multiplica os componentes de dois vetores entre si.</span><span class="sxs-lookup"><span data-stu-id="ea759-155">In-place multiplies the components of two vectors by each other.</span></span> |
| `float3& operator*= (float3& value1, float value2)` | <span data-ttu-id="ea759-156">O in-loco multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="ea759-156">In-place multiplies a vector by a scalar.</span></span> |
| `float3& operator/= (float3& value1, float3 const& value2)` | <span data-ttu-id="ea759-157">O in-loco divide os componentes de um vetor pelos componentes de outro vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-157">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float3& operator/= (float3& value1, float value2)` | <span data-ttu-id="ea759-158">O in-loco divide um vetor por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="ea759-158">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-159">Determina se duas instâncias de float3 são iguais.</span><span class="sxs-lookup"><span data-stu-id="ea759-159">Determines whether two instances of float3 are equal.</span></span> |
| `bool operator!= (float3 const& value1, float3 const& value2)` | <span data-ttu-id="ea759-160">Determina se duas instâncias de float3 não são iguais.</span><span class="sxs-lookup"><span data-stu-id="ea759-160">Determines whether two instances of float3 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | <span data-ttu-id="ea759-161">Converte um float3 em um **Microsoft. Graphics. Canvas. Numerics. Vector3**.</span><span class="sxs-lookup"><span data-stu-id="ea759-161">Converts a float3 to a **Microsoft.Graphics.Canvas.Numerics.Vector3**.</span></span> |

## <a name="fields"></a><span data-ttu-id="ea759-162">Campos</span><span class="sxs-lookup"><span data-stu-id="ea759-162">Fields</span></span>

| <span data-ttu-id="ea759-163">Nome</span><span class="sxs-lookup"><span data-stu-id="ea759-163">Name</span></span> | <span data-ttu-id="ea759-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea759-164">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="ea759-165">Componente X do vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-165">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="ea759-166">Componente Y do vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-166">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="ea759-167">Componente Z do vetor.</span><span class="sxs-lookup"><span data-stu-id="ea759-167">Z component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="ea759-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea759-168">Requirements</span></span>

| <span data-ttu-id="ea759-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea759-169">Requirement</span></span> | <span data-ttu-id="ea759-170">Valor</span><span class="sxs-lookup"><span data-stu-id="ea759-170">Value</span></span> |
|-|-|
| <span data-ttu-id="ea759-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea759-171">Namespace</span></span> | <span data-ttu-id="ea759-172">Windows:: Foundation:: numéricos</span><span class="sxs-lookup"><span data-stu-id="ea759-172">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="ea759-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea759-173">Header</span></span> | <dl> <span data-ttu-id="ea759-174"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea759-174"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="ea759-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea759-175">See also</span></span>

[<span data-ttu-id="ea759-176">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="ea759-176">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
