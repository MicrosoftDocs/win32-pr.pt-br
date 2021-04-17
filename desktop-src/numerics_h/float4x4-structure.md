---
title: estrutura float4x4 (Windowsnumerics. h)
description: Uma matriz 4x4, usada para transformações 3D.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- estrutura float4x4
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790436"
---
# <a name="float4x4-structure"></a><span data-ttu-id="9d446-104">estrutura float4x4</span><span class="sxs-lookup"><span data-stu-id="9d446-104">float4x4 structure</span></span>

<span data-ttu-id="9d446-105">Uma matriz 4x4, usada para transformações 3D.</span><span class="sxs-lookup"><span data-stu-id="9d446-105">A 4x4 matrix, used for 3D transforms.</span></span>

<span data-ttu-id="9d446-106">Esse tipo de matriz usa um layout de vetor de linha.</span><span class="sxs-lookup"><span data-stu-id="9d446-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="9d446-107">O x, y e z do vetor de conversão dessa matriz correspondem aos campos M41, M42, M43.</span><span class="sxs-lookup"><span data-stu-id="9d446-107">The x, y, and z of this matrix's translation vector correspond to the fields m41, m42, m43.</span></span>

<span data-ttu-id="9d446-108">Esse tipo está disponível apenas em C++.</span><span class="sxs-lookup"><span data-stu-id="9d446-108">This type is available only in C++.</span></span> <span data-ttu-id="9d446-109">Seu equivalente em .NET é [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="9d446-109">Its .NET equivalent is [System.Numerics.Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="9d446-110">Construtores</span><span class="sxs-lookup"><span data-stu-id="9d446-110">Constructors</span></span>

| <span data-ttu-id="9d446-111">Nome</span><span class="sxs-lookup"><span data-stu-id="9d446-111">Name</span></span> | <span data-ttu-id="9d446-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d446-112">Description</span></span> |
|-|-|
| `float4x4()` | <span data-ttu-id="9d446-113">Cria um float4x4 não inicializado.</span><span class="sxs-lookup"><span data-stu-id="9d446-113">Creates an uninitialized float4x4.</span></span> |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | <span data-ttu-id="9d446-114">Cria um float4x4 com os valores especificados.</span><span class="sxs-lookup"><span data-stu-id="9d446-114">Creates a float4x4 with the specified values.</span></span> |
| `explicit float4x4(float3x2 value)` | <span data-ttu-id="9d446-115">Cria um float4x4 de um float3x2.</span><span class="sxs-lookup"><span data-stu-id="9d446-115">Creates a float4x4 from a float3x2.</span></span> |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | <span data-ttu-id="9d446-116">Converte um **Microsoft. Graphics. Canvas. Numerics. Matrix4x4** em um float4x4.</span><span class="sxs-lookup"><span data-stu-id="9d446-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** to a float4x4.</span></span> |

## <a name="functions"></a><span data-ttu-id="9d446-117">Funções</span><span class="sxs-lookup"><span data-stu-id="9d446-117">Functions</span></span>

| <span data-ttu-id="9d446-118">Nome</span><span class="sxs-lookup"><span data-stu-id="9d446-118">Name</span></span> | <span data-ttu-id="9d446-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d446-119">Description</span></span> |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | <span data-ttu-id="9d446-120">Cria um mural esférico que gira em volta de uma posição de objeto especificada, usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-120">Creates a spherical billboard that rotates around a specified object position, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | <span data-ttu-id="9d446-121">Cria um mural cilíndrico que gira em um eixo especificado, usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-121">Creates a cylindrical billboard that rotates around a specified axis, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_translation(float3 const& position)` | <span data-ttu-id="9d446-122">Cria uma matriz de translação.</span><span class="sxs-lookup"><span data-stu-id="9d446-122">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | <span data-ttu-id="9d446-123">Cria uma matriz de translação.</span><span class="sxs-lookup"><span data-stu-id="9d446-123">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | <span data-ttu-id="9d446-124">Cria uma matriz de dimensionamento, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="9d446-124">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | <span data-ttu-id="9d446-125">Cria uma matriz de dimensionamento, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d446-125">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales)` | <span data-ttu-id="9d446-126">Cria uma matriz de dimensionamento, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="9d446-126">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | <span data-ttu-id="9d446-127">Cria uma matriz de dimensionamento, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d446-127">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float scale)` | <span data-ttu-id="9d446-128">Cria uma matriz de dimensionamento, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="9d446-128">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | <span data-ttu-id="9d446-129">Cria uma matriz de dimensionamento, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d446-129">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians)` | <span data-ttu-id="9d446-130">Cria uma matriz de rotação do eixo x, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="9d446-130">Creates an x-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | <span data-ttu-id="9d446-131">Cria uma matriz de rotação do eixo x, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d446-131">Creates an x-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians)` | <span data-ttu-id="9d446-132">Cria uma matriz de rotação do eixo y, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="9d446-132">Creates a y-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | <span data-ttu-id="9d446-133">Cria uma matriz de rotação do eixo y, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d446-133">Creates a y-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians)` | <span data-ttu-id="9d446-134">Cria uma matriz de rotação do eixo z, centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="9d446-134">Creates a z-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | <span data-ttu-id="9d446-135">Cria uma matriz de rotação do eixo z, centralizada no ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="9d446-135">Creates a z-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="9d446-136">Cria uma matriz que gira em torno de um vetor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="9d446-136">Creates a matrix that rotates around an arbitrary vector.</span></span> |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="9d446-137">Cria uma matriz de projeção em perspectiva com base em um campo de exibição, usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-137">Creates a perspective projection matrix based on a field of view, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="9d446-138">Cria uma matriz de projeção em perspectiva, usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-138">Creates a perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="9d446-139">Cria uma matriz de projeção em perspectiva personalizada usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-139">Creates a customized perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | <span data-ttu-id="9d446-140">Cria uma matriz de projeção ortográfica usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-140">Creates an orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | <span data-ttu-id="9d446-141">Cria uma matriz de projeção ortográfica personalizada usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-141">Creates a customized orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | <span data-ttu-id="9d446-142">Cria uma matriz de exibição, usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-142">Creates a view matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | <span data-ttu-id="9d446-143">Cria uma matriz mundial, usando um sistema de coordenadas à direita.</span><span class="sxs-lookup"><span data-stu-id="9d446-143">Creates a world matrix, using a right handed coordinate system.</span></span> <span data-ttu-id="9d446-144">Isso pode ser usado para posicionar objetos no espaço 3D.</span><span class="sxs-lookup"><span data-stu-id="9d446-144">This can be used to position objects in 3D space.</span></span> |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | <span data-ttu-id="9d446-145">Cria uma matriz de rotação de um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="9d446-145">Creates a rotation matrix from a quaternion.</span></span> |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="9d446-146">Cria uma matriz de rotação a partir de uma guinada, pitch e roll especificados.</span><span class="sxs-lookup"><span data-stu-id="9d446-146">Creates a rotation matrix from a specified yaw, pitch, and roll.</span></span> |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | <span data-ttu-id="9d446-147">Cria uma matriz que nivela a geometria em um plano especificado como se projetando uma sombra de uma fonte de luz especificada.</span><span class="sxs-lookup"><span data-stu-id="9d446-147">Creates a matrix that flattens geometry into a specified plane as if casting a shadow from a specified light source.</span></span> |
| `float4x4 make_float4x4_reflection(plane const& value)` | <span data-ttu-id="9d446-148">Cria uma matriz que reflete o sistema de coordenadas sobre um plano especificado.</span><span class="sxs-lookup"><span data-stu-id="9d446-148">Creates a matrix that reflects the coordinate system about a specified plane.</span></span> |
| `bool is_identity(float4x4 const& value)` | <span data-ttu-id="9d446-149">Verifica se esta é uma matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="9d446-149">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float4x4 const& value)` | <span data-ttu-id="9d446-150">Calcula o determinante da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-150">Calculates the determinant of the matrix.</span></span> |
| `float3 translation(float4x4 const& value)` | <span data-ttu-id="9d446-151">Obtém o vetor de tradução da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-151">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | <span data-ttu-id="9d446-152">Calcula o inverso de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-152">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="9d446-153">Retornará true se a matriz puder ser invertida; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="9d446-153">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | <span data-ttu-id="9d446-154">Extrai os componentes escalares, de tradução e de rotação de uma matriz de SRT (escala/rotação/conversão) 3D.</span><span class="sxs-lookup"><span data-stu-id="9d446-154">Extracts the scalar, translation, and rotation components from a 3D scale/rotate/translate (SRT) matrix.</span></span> <span data-ttu-id="9d446-155">Retornará true se a matriz puder ser decomposta; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="9d446-155">Returns true if the matrix can be decomposed; false otherwise.</span></span> |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | <span data-ttu-id="9d446-156">Transforma uma matriz aplicando uma rotação de Quaternion.</span><span class="sxs-lookup"><span data-stu-id="9d446-156">Transforms a matrix by applying a quaternion rotation.</span></span> |
| `float4x4 transpose(float4x4 const& matrix)` | <span data-ttu-id="9d446-157">Transpõe os componentes de uma matriz ao longo de sua diagonal.</span><span class="sxs-lookup"><span data-stu-id="9d446-157">Transposes the components of a matrix along its diagonal.</span></span> |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | <span data-ttu-id="9d446-158">Interpola linearmente entre os valores correspondentes de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="9d446-158">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="9d446-159">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d446-159">Methods</span></span>

| <span data-ttu-id="9d446-160">Nome</span><span class="sxs-lookup"><span data-stu-id="9d446-160">Name</span></span> | <span data-ttu-id="9d446-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d446-161">Description</span></span> |
|-|-|
| `static float4x4 identity()` | <span data-ttu-id="9d446-162">Retorna uma instância da matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="9d446-162">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="9d446-163">Operadores</span><span class="sxs-lookup"><span data-stu-id="9d446-163">Operators</span></span>

| <span data-ttu-id="9d446-164">Nome</span><span class="sxs-lookup"><span data-stu-id="9d446-164">Name</span></span> | <span data-ttu-id="9d446-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d446-165">Description</span></span> |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-166">Adiciona cada componente de uma matriz a outra matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-166">Adds each component of a matrix to another matrix.</span></span> |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-167">Subtrai cada componente de uma matriz de outra matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-167">Subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-168">Multiplica uma matriz por outra matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-168">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="9d446-169">Isso tem o efeito de concatenar duas transformações.</span><span class="sxs-lookup"><span data-stu-id="9d446-169">This has the effect of concatenating two transforms.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float value2)` | <span data-ttu-id="9d446-170">Multiplica cada componente de uma matriz por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="9d446-170">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float4x4 operator- (float4x4 const& value)` | <span data-ttu-id="9d446-171">Nega cada componente de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-171">Negates each component of a matrix.</span></span> |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-172">In-loco adiciona cada componente de uma matriz a outra matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-172">In-place adds each component of a matrix to another matrix.</span></span> |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-173">O in-loco subtrai cada componente de uma matriz de outra matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-173">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-174">O in-loco multiplica uma matriz por outra matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-174">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="9d446-175">Isso tem o efeito de concatenar duas transformações.</span><span class="sxs-lookup"><span data-stu-id="9d446-175">This has the effect of concatenating two transforms.</span></span> |
| `float4x4& operator*= (float4x4& value1, float value2)` | <span data-ttu-id="9d446-176">O in-loco multiplica cada componente de uma matriz por um valor escalar.</span><span class="sxs-lookup"><span data-stu-id="9d446-176">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-177">Determina se duas instâncias de float4x4 são iguais.</span><span class="sxs-lookup"><span data-stu-id="9d446-177">Determines whether two instances of float4x4 are equal.</span></span> |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="9d446-178">Determina se duas instâncias de float4x4 não são iguais.</span><span class="sxs-lookup"><span data-stu-id="9d446-178">Determines whether two instances of float4x4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | <span data-ttu-id="9d446-179">Converte um float4x4 em um **Microsoft. Graphics. Canvas. Numerics. Matrix4x4**.</span><span class="sxs-lookup"><span data-stu-id="9d446-179">Converts a float4x4 to a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="9d446-180">Campos</span><span class="sxs-lookup"><span data-stu-id="9d446-180">Fields</span></span>

| <span data-ttu-id="9d446-181">Nome</span><span class="sxs-lookup"><span data-stu-id="9d446-181">Name</span></span> | <span data-ttu-id="9d446-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d446-182">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="9d446-183">Valor na linha 1, coluna 1 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-183">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="9d446-184">Valor na linha 1, coluna 2 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-184">Value at row 1 column 2 of the matrix.</span></span> |
| `float m13` | <span data-ttu-id="9d446-185">Valor na linha 1, coluna 3 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-185">Value at row 1 column 3 of the matrix.</span></span> |
| `float m14` | <span data-ttu-id="9d446-186">Valor na linha 1, coluna 4 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-186">Value at row 1 column 4 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="9d446-187">Valor na linha 2, coluna 1 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-187">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="9d446-188">Valor na linha 2, coluna 2 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-188">Value at row 2 column 2 of the matrix.</span></span> |
| `float m23` | <span data-ttu-id="9d446-189">Valor na linha 2, coluna 3 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-189">Value at row 2 column 3 of the matrix.</span></span> |
| `float m24` | <span data-ttu-id="9d446-190">Valor na linha 2, coluna 4 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-190">Value at row 2 column 4 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="9d446-191">Valor na linha 3, coluna 1 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-191">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="9d446-192">Valor na linha 3, coluna 2 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-192">Value at row 3 column 2 of the matrix.</span></span> |
| `float m33` | <span data-ttu-id="9d446-193">Valor na linha 3, coluna 3 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-193">Value at row 3 column 3 of the matrix.</span></span> |
| `float m34` | <span data-ttu-id="9d446-194">Valor na linha 3, coluna 4 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-194">Value at row 3 column 4 of the matrix.</span></span> |
| `float m41` | <span data-ttu-id="9d446-195">Valor na linha 4, coluna 1 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-195">Value at row 4 column 1 of the matrix.</span></span> |
| `float m42` | <span data-ttu-id="9d446-196">Valor na linha 4, coluna 2 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-196">Value at row 4 column 2 of the matrix.</span></span> |
| `float m43` | <span data-ttu-id="9d446-197">Valor na linha 4 coluna 3 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-197">Value at row 4 column 3 of the matrix.</span></span> |
| `float m44` | <span data-ttu-id="9d446-198">Valor na linha 4, coluna 4 da matriz.</span><span class="sxs-lookup"><span data-stu-id="9d446-198">Value at row 4 column 4 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="9d446-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d446-199">Requirements</span></span>

| <span data-ttu-id="9d446-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d446-200">Requirement</span></span> | <span data-ttu-id="9d446-201">Valor</span><span class="sxs-lookup"><span data-stu-id="9d446-201">Value</span></span> |
|-|-|
| <span data-ttu-id="9d446-202">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d446-202">Namespace</span></span> | <span data-ttu-id="9d446-203">Windows:: Foundation:: numéricos</span><span class="sxs-lookup"><span data-stu-id="9d446-203">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="9d446-204">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d446-204">Header</span></span> | <dl> <span data-ttu-id="9d446-205"><dt>Windowsnumerics. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d446-205"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="9d446-206">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d446-206">See also</span></span>

[<span data-ttu-id="9d446-207">APIs windowsnumerics. h</span><span class="sxs-lookup"><span data-stu-id="9d446-207">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
