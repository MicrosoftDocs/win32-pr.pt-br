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
# <a name="float2-structure"></a><span data-ttu-id="998c0-104">estrutura float2</span><span class="sxs-lookup"><span data-stu-id="998c0-104">float2 structure</span></span>

<span data-ttu-id="998c0-105">Um vetor com dois componentes.</span><span class="sxs-lookup"><span data-stu-id="998c0-105">A vector with two components.</span></span>

<span data-ttu-id="998c0-106">Esse tipo está disponível apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="998c0-106">This type is available only in C++.</span></span> <span data-ttu-id="998c0-107">Seu equivalente em .NET é [System. Numerics. vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="998c0-107">Its .NET equivalent is [System.Numerics.Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="998c0-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="998c0-108">Constructors</span></span>

| <span data-ttu-id="998c0-109">Nome</span><span class="sxs-lookup"><span data-stu-id="998c0-109">Name</span></span> | <span data-ttu-id="998c0-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="998c0-110">Description</span></span> |
|-|-|
| `float2()` | <span data-ttu-id="998c0-111">Cria um float2 não inicializado.</span><span class="sxs-lookup"><span data-stu-id="998c0-111">Creates an uninitialized float2.</span></span> |
| `float2(float x, float y)` | <span data-ttu-id="998c0-112">Cria um float2 com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="998c0-112">Creates a float2 with the specified values.</span></span> |
| `explicit float2(float value)` | <span data-ttu-id="998c0-113">Cria um float2 com todos os componentes definidos para o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="998c0-113">Creates a float2 with all components set to the specified value.</span></span> |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | <span data-ttu-id="998c0-114">Converte um **Microsoft. Graphics. Canvas. Numerics. vector2** em um float2.</span><span class="sxs-lookup"><span data-stu-id="998c0-114">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector2** to a float2.</span></span> |
| `float2(Windows::Foundation::Point const& value)` | <span data-ttu-id="998c0-115">Converte um [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) em um float2.</span><span class="sxs-lookup"><span data-stu-id="998c0-115">Converts a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point) to a float2.</span></span> |
| `float2(Windows::Foundation::Size const& value)` | <span data-ttu-id="998c0-116">Converte um [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size) em um float2.</span><span class="sxs-lookup"><span data-stu-id="998c0-116">Converts a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size) to a float2.</span></span> |

## <a name="functions"></a><span data-ttu-id="998c0-117">Funções</span><span class="sxs-lookup"><span data-stu-id="998c0-117">Functions</span></span>

| <span data-ttu-id="998c0-118">Nome</span><span class="sxs-lookup"><span data-stu-id="998c0-118">Name</span></span> | <span data-ttu-id="998c0-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="998c0-119">Description</span></span> |
|-|-|
| `float length(float2 const& value)` | <span data-ttu-id="998c0-120">Calcula o comprimento ou a distância euclidiana do vetor.</span><span class="sxs-lookup"><span data-stu-id="998c0-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float2 const& value)` | <span data-ttu-id="998c0-121">Calcula o comprimento ou a distância euclidiana do vetor ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="998c0-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-122">Calcula a distância euclidiana entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="998c0-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-123">Calcula a distância euclidiana entre dois vetores ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="998c0-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-124">Calcula o produto de ponto de dois vetores.</span><span class="sxs-lookup"><span data-stu-id="998c0-124">Calculates the dot product of two vectors.</span></span> |
| `float2 normalize(float2 const& value)` | <span data-ttu-id="998c0-125">Cria um vetor de unidade a partir do vetor especificado.</span><span class="sxs-lookup"><span data-stu-id="998c0-125">Creates a unit vector from the specified vector.</span></span> |
| `float2 reflect(float2 const& vector, float2 const& normal)` | <span data-ttu-id="998c0-126">Determina o vetor de reflexão do vetor e normal específico.</span><span class="sxs-lookup"><span data-stu-id="998c0-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float2 min(float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-127">Retorna um vetor que contém o valor mais baixo de cada par de componentes correspondente.</span><span class="sxs-lookup"><span data-stu-id="998c0-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float2 max(float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-128">Retorna um vetor que contém o valor mais alto de cada par de componentes correspondente.</span><span class="sxs-lookup"><span data-stu-id="998c0-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | <span data-ttu-id="998c0-129">Restringe um valor a estar dentro de um intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="998c0-129">Restricts a value to be within a specified range.</span></span> |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | <span data-ttu-id="998c0-130">Executa uma interpolação linear entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="998c0-130">Performs a linear interpolation between two vectors.</span></span> |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | <span data-ttu-id="998c0-131">Transforma o vetor (x, y, 0, 1) pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="998c0-131">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="998c0-132">Transforma o vetor (x, y, 0, 1) pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="998c0-132">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | <span data-ttu-id="998c0-133">Transforma o vetor normal (x, y, 0, 0) pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="998c0-133">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | <span data-ttu-id="998c0-134">Transforma o vetor normal (x, y, 0, 0) pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="998c0-134">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="998c0-135">Transforma um float2 pelo Quaternion especificado.</span><span class="sxs-lookup"><span data-stu-id="998c0-135">Transforms a float2 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="998c0-136">Métodos</span><span class="sxs-lookup"><span data-stu-id="998c0-136">Methods</span></span>

| <span data-ttu-id="998c0-137">Nome</span><span class="sxs-lookup"><span data-stu-id="998c0-137">Name</span></span> | <span data-ttu-id="998c0-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="998c0-138">Description</span></span> |
|-|-|
| `static float2 zero()` | <span data-ttu-id="998c0-139">Retorna um float2 com todos os seus componentes definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="998c0-139">Returns a float2 with all of its components set to zero.</span></span> |
| `static float2 one()` | <span data-ttu-id="998c0-140">Retorna um float2 com todos os seus componentes definidos como um.</span><span class="sxs-lookup"><span data-stu-id="998c0-140">Returns a float2 with all of its components set to one.</span></span> |
| `static float2 unit_x()` | <span data-ttu-id="998c0-141">Retorna o float2 (1, 0).</span><span class="sxs-lookup"><span data-stu-id="998c0-141">Returns the float2 (1, 0).</span></span> |
| `static float2 unit_y()` | <span data-ttu-id="998c0-142">Retorna o float2 (0, 1).</span><span class="sxs-lookup"><span data-stu-id="998c0-142">Returns the float2 (0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="998c0-143">Operadores</span><span class="sxs-lookup"><span data-stu-id="998c0-143">Operators</span></span>

| <span data-ttu-id="998c0-144">Nome</span><span class="sxs-lookup"><span data-stu-id="998c0-144">Name</span></span> | <span data-ttu-id="998c0-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="998c0-145">Description</span></span> |
|-|-|
| `operator Windows::Foundation::Point() const` | <span data-ttu-id="998c0-146">Converte um float2 em um [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point).</span><span class="sxs-lookup"><span data-stu-id="998c0-146">Converts a float2 to a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point).</span></span> |
| `operator Windows::Foundation::Size() const` | <span data-ttu-id="998c0-147">Converte um float2 em um [**Windows. Foundation. Size**](/uwp/api/Windows.Foundation.Size).</span><span class="sxs-lookup"><span data-stu-id="998c0-147">Converts a float2 to a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size).</span></span> |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-148">Adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="998c0-148">Adds two vectors.</span></span> |
| `float2 operator- (float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-149">Subtrai um vetor de um vetor.</span><span class="sxs-lookup"><span data-stu-id="998c0-149">Subtracts a vector from a vector.</span></span> |
| `float2 operator* (float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-150">Multiplica os componentes de dois vetores entre si.</span><span class="sxs-lookup"><span data-stu-id="998c0-150">Multiplies the components of two vectors by each other.</span></span> |
| `float2 operator* (float2 const& value1, float value2)` | <span data-ttu-id="998c0-151">Multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="998c0-151">Multiplies a vector by a scalar.</span></span> |
| `float2 operator* (float value1, float2 const& value2)` | <span data-ttu-id="998c0-152">Multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="998c0-152">Multiplies a vector by a scalar.</span></span> |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-153">Divide os componentes de um vetor pelos componentes de outro vetor.</span><span class="sxs-lookup"><span data-stu-id="998c0-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float2 operator/ (float2 const& value1, float value2)` | <span data-ttu-id="998c0-154">Divide um vetor por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="998c0-154">Divides a vector by a scalar value.</span></span> |
| `float2 operator- (float2 const& value)` | <span data-ttu-id="998c0-155">Retorna um ponto de vetor na direção oposta.</span><span class="sxs-lookup"><span data-stu-id="998c0-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float2& operator+= (float2& value1, float2 const& value2)` | <span data-ttu-id="998c0-156">O in-loco adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="998c0-156">In-place adds two vectors.</span></span> |
| `float2& operator-= (float2& value1, float2 const& value2)` | <span data-ttu-id="998c0-157">O in-loco subtrai um vetor de um vetor.</span><span class="sxs-lookup"><span data-stu-id="998c0-157">In-place subtracts a vector from a vector.</span></span> |
| `float2& operator*= (float2& value1, float2 const& value2)` | <span data-ttu-id="998c0-158">O in-loco multiplica os componentes de dois vetores entre si.</span><span class="sxs-lookup"><span data-stu-id="998c0-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float2& operator*= (float2& value1, float value2)` | <span data-ttu-id="998c0-159">O in-loco multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="998c0-159">In-place multiplies a vector by a scalar.</span></span> |
| `float2& operator/= (float2& value1, float2 const& value2)` | <span data-ttu-id="998c0-160">O in-loco divide os componentes de um vetor pelos componentes de outro vetor.</span><span class="sxs-lookup"><span data-stu-id="998c0-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float2& operator/= (float2& value1, float value2)` | <span data-ttu-id="998c0-161">O in-loco divide um vetor por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="998c0-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-162">Determina se duas instâncias de float2 são iguais.</span><span class="sxs-lookup"><span data-stu-id="998c0-162">Determines whether two instances of float2 are equal.</span></span> |
| `bool operator!= (float2 const& value1, float2 const& value2)` | <span data-ttu-id="998c0-163">Determina se duas instâncias de float2 não são iguais.</span><span class="sxs-lookup"><span data-stu-id="998c0-163">Determines whether two instances of float2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | <span data-ttu-id="998c0-164">Converte um float2 em um **Microsoft. Graphics. Canvas. Numerics. vector2**.</span><span class="sxs-lookup"><span data-stu-id="998c0-164">Converts a float2 to a **Microsoft.Graphics.Canvas.Numerics.Vector2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="998c0-165">Campos</span><span class="sxs-lookup"><span data-stu-id="998c0-165">Fields</span></span>

| <span data-ttu-id="998c0-166">Nome</span><span class="sxs-lookup"><span data-stu-id="998c0-166">Name</span></span> | <span data-ttu-id="998c0-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="998c0-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="998c0-168">Componente X do vetor.</span><span class="sxs-lookup"><span data-stu-id="998c0-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="998c0-169">Componente Y do vetor.</span><span class="sxs-lookup"><span data-stu-id="998c0-169">Y component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="998c0-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="998c0-170">Requirements</span></span>

| <span data-ttu-id="998c0-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="998c0-171">Requirement</span></span> | <span data-ttu-id="998c0-172">Valor</span><span class="sxs-lookup"><span data-stu-id="998c0-172">Value</span></span> |
|-|-|
| <span data-ttu-id="998c0-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="998c0-173">Namespace</span></span> | <span data-ttu-id="998c0-174">Windows:: Foundation:: numéricos</span><span class="sxs-lookup"><span data-stu-id="998c0-174">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="998c0-175">parâmetro</span><span class="sxs-lookup"><span data-stu-id="998c0-175">Header</span></span> | <dl> <span data-ttu-id="998c0-176"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="998c0-176"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="998c0-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="998c0-177">See also</span></span>

[<span data-ttu-id="998c0-178">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="998c0-178">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
