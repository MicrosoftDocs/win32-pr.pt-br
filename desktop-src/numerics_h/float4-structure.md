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
# <a name="float4-structure"></a><span data-ttu-id="d3083-104">estrutura FLOAT4</span><span class="sxs-lookup"><span data-stu-id="d3083-104">float4 structure</span></span>

<span data-ttu-id="d3083-105">Um vetor com quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="d3083-105">A vector with four components.</span></span>

<span data-ttu-id="d3083-106">Esse tipo está disponível apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="d3083-106">This type is available only in C++.</span></span> <span data-ttu-id="d3083-107">Seu equivalente em .NET é [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="d3083-107">Its .NET equivalent is [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="d3083-108">Construtores</span><span class="sxs-lookup"><span data-stu-id="d3083-108">Constructors</span></span>

| <span data-ttu-id="d3083-109">Nome</span><span class="sxs-lookup"><span data-stu-id="d3083-109">Name</span></span> | <span data-ttu-id="d3083-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3083-110">Description</span></span> |
|-|-|
| `float4()` | <span data-ttu-id="d3083-111">Cria um FLOAT4 não inicializado.</span><span class="sxs-lookup"><span data-stu-id="d3083-111">Creates an uninitialized float4.</span></span> |
| `float4(float x, float y, float z, float w)` | <span data-ttu-id="d3083-112">Cria um FLOAT4 com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="d3083-112">Creates a float4 with the specified values.</span></span> |
| `float4(float2 value, float z, float w)` | <span data-ttu-id="d3083-113">Cria um FLOAT4 com x e y copiados de um float2 mais os valores z e w especificados.</span><span class="sxs-lookup"><span data-stu-id="d3083-113">Creates a float4 with x and y copied from a float2 plus the specified z and w values.</span></span> |
| `float4(float3 value, float w)` | <span data-ttu-id="d3083-114">Cria um FLOAT4 com x, y e z copiados de um float3 mais o valor w especificado.</span><span class="sxs-lookup"><span data-stu-id="d3083-114">Creates a float4 with x, y and z copied from a float3 plus the specified w value.</span></span> |
| `explicit float4(float value)` | <span data-ttu-id="d3083-115">Cria um FLOAT4 com todos os com. gentes definidos com o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="d3083-115">Creates a float4 with all com.ents set to the specified value.</span></span> |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | <span data-ttu-id="d3083-116">Converte um **Microsoft. Graphics. Canvas. Numerics. Vector4** em um FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d3083-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector4** to a float4.</span></span> |

## <a name="functions"></a><span data-ttu-id="d3083-117">Funções</span><span class="sxs-lookup"><span data-stu-id="d3083-117">Functions</span></span>

| <span data-ttu-id="d3083-118">Nome</span><span class="sxs-lookup"><span data-stu-id="d3083-118">Name</span></span> | <span data-ttu-id="d3083-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3083-119">Description</span></span> |
|-|-|
| `float length(float4 const& value)` | <span data-ttu-id="d3083-120">Calcula o comprimento ou a distância euclidiana do vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float4 const& value)` | <span data-ttu-id="d3083-121">Calcula o comprimento ou a distância euclidiana do vetor ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="d3083-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-122">Calcula a distância euclidiana entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="d3083-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-123">Calcula a distância euclidiana entre dois vetores ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="d3083-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float4 const& vector1, float4 const& vector2)` | <span data-ttu-id="d3083-124">Calcula o produto de ponto de dois vetores.</span><span class="sxs-lookup"><span data-stu-id="d3083-124">Calculates the dot product of two vectors.</span></span> |
| `float4 normalize(float4 const& vector)` | <span data-ttu-id="d3083-125">Cria um vetor de unidade a partir do vetor especificado.</span><span class="sxs-lookup"><span data-stu-id="d3083-125">Creates a unit vector from the specified vector.</span></span> |
| `float4 min(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-126">Retorna um vetor que contém o valor mais baixo de cada par de componentes correspondente.</span><span class="sxs-lookup"><span data-stu-id="d3083-126">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float4 max(float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-127">Retorna um vetor que contém o valor mais alto de cada par de componentes correspondente.</span><span class="sxs-lookup"><span data-stu-id="d3083-127">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | <span data-ttu-id="d3083-128">Restringe um valor a estar dentro de um intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="d3083-128">Restricts a value to be within a specified range.</span></span> |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | <span data-ttu-id="d3083-129">Executa uma interpolação linear entre dois vetores.</span><span class="sxs-lookup"><span data-stu-id="d3083-129">Performs a linear interpolation between two vectors.</span></span> |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | <span data-ttu-id="d3083-130">Transforma um FLOAT4 pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="d3083-130">Transforms a float4 by the given matrix.</span></span> |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="d3083-131">Transforma um float3 pela matriz especificada, retornando um FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d3083-131">Transforms a float3 by the given matrix, returning a float4.</span></span> |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="d3083-132">Transforma um float2 pela matriz especificada, retornando um FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d3083-132">Transforms a float2 by the given matrix, returning a float4.</span></span> |
| `float4 transform(float4 const& value, quaternion const& rotation)` | <span data-ttu-id="d3083-133">Transforma um FLOAT4 pelo Quaternion especificado.</span><span class="sxs-lookup"><span data-stu-id="d3083-133">Transforms a float4 by the given quaternion.</span></span> |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="d3083-134">Transforma um float3 pelo Quaternion fornecido, retornando um FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d3083-134">Transforms a float3 by the given quaternion, returning a float4.</span></span> |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="d3083-135">Transforma um float2 pelo Quaternion fornecido, retornando um FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="d3083-135">Transforms a float2 by the given quaternion, returning a float4.</span></span> |

## <a name="methods"></a><span data-ttu-id="d3083-136">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3083-136">Methods</span></span>

| <span data-ttu-id="d3083-137">Nome</span><span class="sxs-lookup"><span data-stu-id="d3083-137">Name</span></span> | <span data-ttu-id="d3083-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3083-138">Description</span></span> |
|-|-|
| `static float4 zero()` | <span data-ttu-id="d3083-139">Retorna um FLOAT4 com todos os seus componentes definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="d3083-139">Returns a float4 with all of its components set to zero.</span></span> |
| `static float4 one()` | <span data-ttu-id="d3083-140">Retorna um FLOAT4 com todos os seus componentes definidos como um.</span><span class="sxs-lookup"><span data-stu-id="d3083-140">Returns a float4 with all of its components set to one.</span></span> |
| `static float4 unit_x()` | <span data-ttu-id="d3083-141">Retorna o FLOAT4 (1, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d3083-141">Returns the float4 (1, 0, 0, 0).</span></span> |
| `static float4 unit_y()` | <span data-ttu-id="d3083-142">Retorna o FLOAT4 (0, 1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="d3083-142">Returns the float4 (0, 1, 0, 0).</span></span> |
| `static float4 unit_z()` | <span data-ttu-id="d3083-143">Retorna o FLOAT4 (0, 0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="d3083-143">Returns the float4 (0, 0, 1, 0).</span></span> |
| `static float4 unit_w()` | <span data-ttu-id="d3083-144">Retorna o FLOAT4 (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="d3083-144">Returns the float4 (0, 0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="d3083-145">Operadores</span><span class="sxs-lookup"><span data-stu-id="d3083-145">Operators</span></span>

| <span data-ttu-id="d3083-146">Nome</span><span class="sxs-lookup"><span data-stu-id="d3083-146">Name</span></span> | <span data-ttu-id="d3083-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3083-147">Description</span></span> |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-148">Adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="d3083-148">Adds two vectors.</span></span> |
| `float4 operator- (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-149">Subtrai um vetor de um vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-149">Subtracts a vector from a vector.</span></span> |
| `float4 operator* (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-150">Multiplica os componentes de dois vetores entre si.</span><span class="sxs-lookup"><span data-stu-id="d3083-150">Multiplies the components of two vectors by each other.</span></span> |
| `float4 operator* (float4 const& value1, float value2)` | <span data-ttu-id="d3083-151">Multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="d3083-151">Multiplies a vector by a scalar.</span></span> |
| `float4 operator* (float value1, float4 const& value2)` | <span data-ttu-id="d3083-152">Multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="d3083-152">Multiplies a vector by a scalar.</span></span> |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-153">Divide os componentes de um vetor pelos componentes de outro vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float4 operator/ (float4 const& value1, float value2)` | <span data-ttu-id="d3083-154">Divide um vetor por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="d3083-154">Divides a vector by a scalar value.</span></span> |
| `float4 operator- (float4 const& value)` | <span data-ttu-id="d3083-155">Retorna um ponto de vetor na direção oposta.</span><span class="sxs-lookup"><span data-stu-id="d3083-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float4& operator+= (float4& value1, float4 const& value2)` | <span data-ttu-id="d3083-156">O in-loco adiciona dois vetores.</span><span class="sxs-lookup"><span data-stu-id="d3083-156">In-place adds two vectors.</span></span> |
| `float4& operator-= (float4& value1, float4 const& value2)` | <span data-ttu-id="d3083-157">O in-loco subtrai um vetor de um vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-157">In-place subtracts a vector from a vector.</span></span> |
| `float4& operator*= (float4& value1, float4 const& value2)` | <span data-ttu-id="d3083-158">O in-loco multiplica os componentes de dois vetores entre si.</span><span class="sxs-lookup"><span data-stu-id="d3083-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float4& operator*= (float4& value1, float value2)` | <span data-ttu-id="d3083-159">O in-loco multiplica um vetor por um escalar.</span><span class="sxs-lookup"><span data-stu-id="d3083-159">In-place multiplies a vector by a scalar.</span></span> |
| `float4& operator/= (float4& value1, float4 const& value2)` | <span data-ttu-id="d3083-160">O in-loco divide os componentes de um vetor pelos componentes de outro vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float4& operator/= (float4& value1, float value2)` | <span data-ttu-id="d3083-161">O in-loco divide um vetor por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="d3083-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-162">Determina se duas instâncias de FLOAT4 são iguais.</span><span class="sxs-lookup"><span data-stu-id="d3083-162">Determines whether two instances of float4 are equal.</span></span> |
| `bool operator!= (float4 const& value1, float4 const& value2)` | <span data-ttu-id="d3083-163">Determina se duas instâncias de FLOAT4 não são iguais.</span><span class="sxs-lookup"><span data-stu-id="d3083-163">Determines whether two instances of float4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | <span data-ttu-id="d3083-164">Converte um FLOAT4 em um **Microsoft. Graphics. Canvas. Numerics. Vector4**.</span><span class="sxs-lookup"><span data-stu-id="d3083-164">Converts a float4 to a **Microsoft.Graphics.Canvas.Numerics.Vector4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="d3083-165">Campos</span><span class="sxs-lookup"><span data-stu-id="d3083-165">Fields</span></span>

| <span data-ttu-id="d3083-166">Nome</span><span class="sxs-lookup"><span data-stu-id="d3083-166">Name</span></span> | <span data-ttu-id="d3083-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3083-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="d3083-168">Componente X do vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="d3083-169">Componente Y do vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-169">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="d3083-170">Componente Z do vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-170">Z component of the vector.</span></span> |
| `float w` | <span data-ttu-id="d3083-171">Componente W do vetor.</span><span class="sxs-lookup"><span data-stu-id="d3083-171">W component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d3083-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3083-172">Requirements</span></span>

| <span data-ttu-id="d3083-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3083-173">Requirement</span></span> | <span data-ttu-id="d3083-174">Valor</span><span class="sxs-lookup"><span data-stu-id="d3083-174">Value</span></span> |
|-|-|
| <span data-ttu-id="d3083-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3083-175">Namespace</span></span> | <span data-ttu-id="d3083-176">Windows:: Foundation:: numéricos</span><span class="sxs-lookup"><span data-stu-id="d3083-176">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="d3083-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3083-177">Header</span></span> | <dl> <span data-ttu-id="d3083-178"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3083-178"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d3083-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3083-179">See also</span></span>

[<span data-ttu-id="d3083-180">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="d3083-180">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
