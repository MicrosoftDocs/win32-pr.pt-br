---
title: estrutura Quaternion (Windowsnumerics. h)
description: Um vetor dimensional de quatro dimensões, usado para representar uma rotação.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- estrutura de Quaternion
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780738"
---
# <a name="quaternion-structure"></a><span data-ttu-id="d0002-104">Estrutura de Quaternion</span><span class="sxs-lookup"><span data-stu-id="d0002-104">quaternion Structure</span></span>

<span data-ttu-id="d0002-105">Um vetor dimensional de quatro dimensões, usado para representar uma rotação.</span><span class="sxs-lookup"><span data-stu-id="d0002-105">A four dimensional vector, used to represent a rotation.</span></span>

<span data-ttu-id="d0002-106">Um Quaternion pode girar com eficiência um objeto sobre o vetor (x, y, z) pelo ângulo teta, em que w = cos (teta/2).</span><span class="sxs-lookup"><span data-stu-id="d0002-106">A quaternion can efficiently rotate an object about the (x, y, z) vector by the angle theta, where w = cos(theta/2).</span></span> <span data-ttu-id="d0002-107">Os quaternions normalmente são usados para uma interpolação suave entre dois ângulos e para evitar o problema de bloqueio de gimbal que pode ocorrer com ângulos de Euler.</span><span class="sxs-lookup"><span data-stu-id="d0002-107">Quaternions are typically used for smooth interpolation between two angles, and for avoiding the gimbal lock problem that can occur with Euler angles.</span></span>

<span data-ttu-id="d0002-108">Esse tipo está disponível apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="d0002-108">This type is available only in C++.</span></span> <span data-ttu-id="d0002-109">Seu equivalente em .NET é [System. Numerics. Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="d0002-109">Its .NET equivalent is [System.Numerics.Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="d0002-110">Construtores</span><span class="sxs-lookup"><span data-stu-id="d0002-110">Constructors</span></span>

| <span data-ttu-id="d0002-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d0002-111">Name</span></span> | <span data-ttu-id="d0002-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0002-112">Description</span></span> |
|-|-|
| `quaternion()` | <span data-ttu-id="d0002-113">Cria um Quaternion não inicializado.</span><span class="sxs-lookup"><span data-stu-id="d0002-113">Creates an uninitialized quaternion.</span></span> |
| `quaternion(float x, float y, float z, float w)` | <span data-ttu-id="d0002-114">Cria um Quaternion com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="d0002-114">Creates a quaternion with the specified values.</span></span> |
| `quaternion(float3 vectorPart, float scalarPart)` | <span data-ttu-id="d0002-115">Cria um Quaternion a partir de um float3 e escalar.</span><span class="sxs-lookup"><span data-stu-id="d0002-115">Creates a quaternion from a float3 and scalar.</span></span> |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | <span data-ttu-id="d0002-116">Converte um **Microsoft. Graphics. Canvas. Numerics. Quaternion** em um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Quaternion** to a quaternion.</span></span> |

## <a name="functions"></a><span data-ttu-id="d0002-117">Funções</span><span class="sxs-lookup"><span data-stu-id="d0002-117">Functions</span></span>

| <span data-ttu-id="d0002-118">Nome</span><span class="sxs-lookup"><span data-stu-id="d0002-118">Name</span></span> | <span data-ttu-id="d0002-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0002-119">Description</span></span> |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="d0002-120">Cria um quatérnio de um vetor e um ângulo a ser girado sobre o vetor.</span><span class="sxs-lookup"><span data-stu-id="d0002-120">Creates a quaternion from a vector and an angle to rotate about the vector.</span></span> |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="d0002-121">Cria um Quaternion com base nos ângulos de guinada, pitch e roll especificados.</span><span class="sxs-lookup"><span data-stu-id="d0002-121">Creates a quaternion from specified yaw, pitch, and roll angles.</span></span> |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | <span data-ttu-id="d0002-122">Cria um Quaternion a partir de uma matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="d0002-122">Creates a quaternion from a rotation matrix.</span></span> |
| `bool is_identity(quaternion const& value)` | <span data-ttu-id="d0002-123">Verifica se este é um Quaternion de identidade (sem rotação).</span><span class="sxs-lookup"><span data-stu-id="d0002-123">Checks whether this is an identity (no rotation) quaternion.</span></span> |
| `float length(quaternion const& value)` | <span data-ttu-id="d0002-124">Calcula o comprimento de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-124">Calculates the length of a quaternion.</span></span> |
| `float length_squared(quaternion const& value)` | <span data-ttu-id="d0002-125">Calcula o comprimento quadrado de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-125">Calculates the length squared of a quaternion.</span></span> |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | <span data-ttu-id="d0002-126">Calcula o produto escalar de dois quatérnios.</span><span class="sxs-lookup"><span data-stu-id="d0002-126">Calculates the dot product of two quaternions.</span></span> |
| `quaternion normalize(quaternion const& value)` | <span data-ttu-id="d0002-127">Divide cada componente de um Quaternion pelo comprimento do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-127">Divides each component of a quaternion by the length of the quaternion.</span></span> |
| `quaternion conjugate(quaternion const& value)` | <span data-ttu-id="d0002-128">Calcula o conjugado de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-128">Calculates the conjugate of a quaternion.</span></span> |
| `quaternion inverse(quaternion const& value)` | <span data-ttu-id="d0002-129">Calcula o inverso de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-129">Calculates the inverse of a quaternion.</span></span> |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="d0002-130">Interpola entre dois quatérnios usando interpolação linear esférica.</span><span class="sxs-lookup"><span data-stu-id="d0002-130">Interpolates between two quaternions, using spherical linear interpolation.</span></span> |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="d0002-131">Interpola linearmente entre dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="d0002-131">Linearly interpolates between two quaternions.</span></span> |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="d0002-132">Concatena dois quaternions; o resultado representa a primeira rotação seguida pela segunda rotação.</span><span class="sxs-lookup"><span data-stu-id="d0002-132">Concatenates two quaternions; the result represents the first rotation followed by the second rotation.</span></span> |

## <a name="methods"></a><span data-ttu-id="d0002-133">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0002-133">Methods</span></span>

| <span data-ttu-id="d0002-134">Nome</span><span class="sxs-lookup"><span data-stu-id="d0002-134">Name</span></span> | <span data-ttu-id="d0002-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0002-135">Description</span></span> |
|-|-|
| `static quaternion identity()` | <span data-ttu-id="d0002-136">Retorna uma instância da identidade Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-136">Returns an instance of the identity quaternion.</span></span> |

## <a name="operators"></a><span data-ttu-id="d0002-137">Operadores</span><span class="sxs-lookup"><span data-stu-id="d0002-137">Operators</span></span>

| <span data-ttu-id="d0002-138">Nome</span><span class="sxs-lookup"><span data-stu-id="d0002-138">Name</span></span> | <span data-ttu-id="d0002-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0002-139">Description</span></span> |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="d0002-140">Adiciona dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="d0002-140">Adds two quaternions.</span></span> |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="d0002-141">Subtrai um Quaternion de outro Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-141">Subtracts a quaternion from another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="d0002-142">Multiplica um Quaternion por outro Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-142">Multiplies a quaternion by another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, float value2)` | <span data-ttu-id="d0002-143">Multiplica um Quaternion por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="d0002-143">Multiplies a quaternion by a scalar value.</span></span> |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="d0002-144">Divide um Quaternion por outro Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-144">Divides a quaternion by another quaternion.</span></span> |
| `quaternion operator- (quaternion const& value)` | <span data-ttu-id="d0002-145">Inverte o sinal de cada componente do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-145">Flips the sign of each component of the quaternion.</span></span> |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="d0002-146">O in-loco adiciona dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="d0002-146">In-place adds two quaternions.</span></span> |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="d0002-147">O in-loco subtrai um Quaternion de outro Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-147">In-place subtracts a quaternion from another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="d0002-148">O in-loco multiplica um Quaternion por outro Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-148">In-place multiplies a quaternion by another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, float value2)` | <span data-ttu-id="d0002-149">O in-loco nultiplies um Quaternion por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="d0002-149">In-place nultiplies a quaternion by a scalar value.</span></span> |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="d0002-150">O in-loco divide um Quaternion por outro Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-150">In-place divides a quaternion by another quaternion.</span></span> |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="d0002-151">Determina se duas instâncias de Quaternion são iguais.</span><span class="sxs-lookup"><span data-stu-id="d0002-151">Determines whether two instances of quaternion are equal.</span></span> |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="d0002-152">Determina se duas instâncias de Quaternion não são iguais.</span><span class="sxs-lookup"><span data-stu-id="d0002-152">Determines whether two instances of quaternion are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | <span data-ttu-id="d0002-153">Converte um Quaternion em um **Microsoft. Graphics. Canvas. Numerics. Quaternion**.</span><span class="sxs-lookup"><span data-stu-id="d0002-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span></span> |

## <a name="fields"></a><span data-ttu-id="d0002-154">Campos</span><span class="sxs-lookup"><span data-stu-id="d0002-154">Fields</span></span>

| <span data-ttu-id="d0002-155">Nome</span><span class="sxs-lookup"><span data-stu-id="d0002-155">Name</span></span> | <span data-ttu-id="d0002-156">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0002-156">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="d0002-157">Valor X do componente de vetor do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-157">X value of the vector component of the quaternion.</span></span> |
| `float y` | <span data-ttu-id="d0002-158">Valor Y do componente de vetor do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-158">Y value of the vector component of the quaternion.</span></span> |
| `float z` | <span data-ttu-id="d0002-159">Valor Z do componente de vetor do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-159">Z value of the vector component of the quaternion.</span></span> |
| `float w` | <span data-ttu-id="d0002-160">Componente de rotação do Quaternion.</span><span class="sxs-lookup"><span data-stu-id="d0002-160">Rotation component of the quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d0002-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0002-161">Requirements</span></span>

| <span data-ttu-id="d0002-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0002-162">Requirement</span></span> | <span data-ttu-id="d0002-163">Valor</span><span class="sxs-lookup"><span data-stu-id="d0002-163">Value</span></span> |
|-|-|
| <span data-ttu-id="d0002-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0002-164">Namespace</span></span> | <span data-ttu-id="d0002-165">Windows:: Foundation:: numéricos</span><span class="sxs-lookup"><span data-stu-id="d0002-165">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="d0002-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0002-166">Header</span></span> | <dl> <span data-ttu-id="d0002-167"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0002-167"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="d0002-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0002-168">See also</span></span>

[<span data-ttu-id="d0002-169">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="d0002-169">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
