---
title: estrutura float3x2 (Windowsnumerics. h)
description: Uma matriz 3x2, usada para transformações 2D.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- estrutura float3x2
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790647"
---
# <a name="float3x2-structure"></a><span data-ttu-id="aca1d-104">estrutura float3x2</span><span class="sxs-lookup"><span data-stu-id="aca1d-104">float3x2 structure</span></span>

<span data-ttu-id="aca1d-105">Uma matriz 3x2, usada para transformações 2D.</span><span class="sxs-lookup"><span data-stu-id="aca1d-105">A 3x2 matrix, used for 2D transforms.</span></span>

<span data-ttu-id="aca1d-106">Esse tipo de matriz usa um layout de vetor de linha.</span><span class="sxs-lookup"><span data-stu-id="aca1d-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="aca1d-107">O x e y do vetor de conversão desta matriz correspondem aos campos M31, M32.</span><span class="sxs-lookup"><span data-stu-id="aca1d-107">The x and y of this matrix's translation vector correspond to the fields m31, m32.</span></span>

<span data-ttu-id="aca1d-108">Esse tipo está disponível apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="aca1d-108">This type is available only in C++.</span></span> <span data-ttu-id="aca1d-109">Seu equivalente em .NET é [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="aca1d-109">Its .NET equivalent is [System.Numerics.Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="aca1d-110">Construtores</span><span class="sxs-lookup"><span data-stu-id="aca1d-110">Constructors</span></span>

| <span data-ttu-id="aca1d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="aca1d-111">Name</span></span> | <span data-ttu-id="aca1d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="aca1d-112">Description</span></span> |
|-|-|
| `float3x2()` | <span data-ttu-id="aca1d-113">Cria um float3x2 não inicializado.</span><span class="sxs-lookup"><span data-stu-id="aca1d-113">Creates an uninitialized float3x2.</span></span> |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | <span data-ttu-id="aca1d-114">Cria um float3x2 com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="aca1d-114">Creates a float3x2 with the specified values.</span></span> |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | <span data-ttu-id="aca1d-115">Converte um **Microsoft. Graphics. Canvas. Numerics. Matrix3x2** em um float3x2.</span><span class="sxs-lookup"><span data-stu-id="aca1d-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** to a float3x2.</span></span> |

## <a name="functions"></a><span data-ttu-id="aca1d-116">Funções</span><span class="sxs-lookup"><span data-stu-id="aca1d-116">Functions</span></span>

| <span data-ttu-id="aca1d-117">Nome</span><span class="sxs-lookup"><span data-stu-id="aca1d-117">Name</span></span> | <span data-ttu-id="aca1d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="aca1d-118">Description</span></span> |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | <span data-ttu-id="aca1d-119">Cria uma matriz de translação.</span><span class="sxs-lookup"><span data-stu-id="aca1d-119">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | <span data-ttu-id="aca1d-120">Cria uma matriz de translação.</span><span class="sxs-lookup"><span data-stu-id="aca1d-120">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | <span data-ttu-id="aca1d-121">Cria uma matriz de dimensionamento, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="aca1d-121">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | <span data-ttu-id="aca1d-122">Cria uma matriz de dimensionamento, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="aca1d-122">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales)` | <span data-ttu-id="aca1d-123">Cria uma matriz de dimensionamento, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="aca1d-123">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | <span data-ttu-id="aca1d-124">Cria uma matriz de dimensionamento, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="aca1d-124">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float scale)` | <span data-ttu-id="aca1d-125">Cria uma matriz de dimensionamento, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="aca1d-125">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | <span data-ttu-id="aca1d-126">Cria uma matriz de dimensionamento, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="aca1d-126">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | <span data-ttu-id="aca1d-127">Cria uma matriz de distorção, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="aca1d-127">Creates a skew matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | <span data-ttu-id="aca1d-128">Cria uma matriz de distorção, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="aca1d-128">Creates a skew matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_rotation(float radians)` | <span data-ttu-id="aca1d-129">Cria uma matriz de rotação, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="aca1d-129">Creates a rotation matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | <span data-ttu-id="aca1d-130">Cria uma matriz de rotação, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="aca1d-130">Creates a rotation matrix, centered on the specified point.</span></span> |
| `bool is_identity(float3x2 const& value)` | <span data-ttu-id="aca1d-131">Verifica se esta é uma matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="aca1d-131">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float3x2 const& value)` | <span data-ttu-id="aca1d-132">Calcula o determinante da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-132">Calculates the determinant of the matrix.</span></span> |
| `float2 translation(float3x2 const& value)` | <span data-ttu-id="aca1d-133">Obtém o vetor de tradução da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-133">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | <span data-ttu-id="aca1d-134">Calcula o inverso de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-134">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="aca1d-135">Retornará true se a matriz puder ser invertida; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="aca1d-135">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | <span data-ttu-id="aca1d-136">Interpola linearmente entre os valores correspondentes de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="aca1d-136">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="aca1d-137">Métodos</span><span class="sxs-lookup"><span data-stu-id="aca1d-137">Methods</span></span>

| <span data-ttu-id="aca1d-138">Nome</span><span class="sxs-lookup"><span data-stu-id="aca1d-138">Name</span></span> | <span data-ttu-id="aca1d-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="aca1d-139">Description</span></span> |
|-|-|
| `static float3x2 identity()` | <span data-ttu-id="aca1d-140">Retorna uma instância da matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="aca1d-140">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="aca1d-141">Operadores</span><span class="sxs-lookup"><span data-stu-id="aca1d-141">Operators</span></span>

| <span data-ttu-id="aca1d-142">Nome</span><span class="sxs-lookup"><span data-stu-id="aca1d-142">Name</span></span> | <span data-ttu-id="aca1d-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="aca1d-143">Description</span></span> |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-144">Adiciona cada componente de uma matriz a outra matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-144">Adds each component of a matrix to another matrix.</span></span> |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-145">Subtrai cada componente de uma matriz de outra matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-145">Subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-146">Multiplica uma matriz por outra matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-146">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="aca1d-147">Isso tem o efeito de concatenar duas transformações.</span><span class="sxs-lookup"><span data-stu-id="aca1d-147">This has the effect of concatenating two transforms.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float value2)` | <span data-ttu-id="aca1d-148">Multiplica cada componente de uma matriz por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="aca1d-148">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float3x2 operator- (float3x2 const& value)` | <span data-ttu-id="aca1d-149">Nega cada componente de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-149">Negates each component of a matrix.</span></span> |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-150">In-loco adiciona cada componente de uma matriz a outra matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-150">In-place adds each component of a matrix to another matrix.</span></span> |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-151">O in-loco subtrai cada componente de uma matriz de outra matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-151">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-152">O in-loco multiplica uma matriz por outra matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-152">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="aca1d-153">Isso tem o efeito de concatenar duas transformações.</span><span class="sxs-lookup"><span data-stu-id="aca1d-153">This has the effect of concatenating two transforms.</span></span> |
| `float3x2& operator*= (float3x2& value1, float value2)` | <span data-ttu-id="aca1d-154">O in-loco multiplica cada componente de uma matriz por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="aca1d-154">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-155">Determina se duas instâncias de float3x2 são iguais.</span><span class="sxs-lookup"><span data-stu-id="aca1d-155">Determines whether two instances of float3x2 are equal.</span></span> |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="aca1d-156">Determina se duas instâncias de float3x2 não são iguais.</span><span class="sxs-lookup"><span data-stu-id="aca1d-156">Determines whether two instances of float3x2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | <span data-ttu-id="aca1d-157">Converte um float3x2 em um **Microsoft. Graphics. Canvas. Numerics. Matrix3x2**.</span><span class="sxs-lookup"><span data-stu-id="aca1d-157">Converts a float3x2 to a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="aca1d-158">Campos</span><span class="sxs-lookup"><span data-stu-id="aca1d-158">Fields</span></span>

| <span data-ttu-id="aca1d-159">Nome</span><span class="sxs-lookup"><span data-stu-id="aca1d-159">Name</span></span> | <span data-ttu-id="aca1d-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="aca1d-160">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="aca1d-161">Valor na linha 1, coluna 1 da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-161">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="aca1d-162">Valor na linha 1, coluna 2 da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-162">Value at row 1 column 2 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="aca1d-163">Valor na linha 2, coluna 1 da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-163">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="aca1d-164">Valor na linha 2, coluna 2 da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-164">Value at row 2 column 2 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="aca1d-165">Valor na linha 3, coluna 1 da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-165">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="aca1d-166">Valor na linha 3, coluna 2 da matriz.</span><span class="sxs-lookup"><span data-stu-id="aca1d-166">Value at row 3 column 2 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="aca1d-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aca1d-167">Requirements</span></span>

| <span data-ttu-id="aca1d-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="aca1d-168">Requirement</span></span> | <span data-ttu-id="aca1d-169">Valor</span><span class="sxs-lookup"><span data-stu-id="aca1d-169">Value</span></span> |
|-|-|
| <span data-ttu-id="aca1d-170">Namespace</span><span class="sxs-lookup"><span data-stu-id="aca1d-170">Namespace</span></span> | <span data-ttu-id="aca1d-171">Windows:: Foundation:: numéricos</span><span class="sxs-lookup"><span data-stu-id="aca1d-171">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="aca1d-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aca1d-172">Header</span></span> | <dl> <span data-ttu-id="aca1d-173"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca1d-173"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="aca1d-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="aca1d-174">See also</span></span>

[<span data-ttu-id="aca1d-175">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="aca1d-175">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
