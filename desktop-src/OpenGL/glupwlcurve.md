---
title: função gluPwlCurve (Glu. h)
description: A função gluPwlCurve descreve uma curva de corte de B-spline (NURBS) não uniforme de piecewise linear.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- função gluPwlCurve OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751089"
---
# <a name="glupwlcurve-function"></a><span data-ttu-id="2f0b0-104">função gluPwlCurve</span><span class="sxs-lookup"><span data-stu-id="2f0b0-104">gluPwlCurve function</span></span>

<span data-ttu-id="2f0b0-105">A função **gluPwlCurve** descreve uma curva de corte de B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) não uniforme de piecewise linear.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-105">The **gluPwlCurve** function describes a piecewise linear Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f0b0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f0b0-106">Syntax</span></span>


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="2f0b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f0b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f0b0-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="2f0b0-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0b0-109">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="2f0b0-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2f0b0-110">*contagem*</span><span class="sxs-lookup"><span data-stu-id="2f0b0-110">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0b0-111">O número de pontos na curva.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-111">The number of points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="2f0b0-112">*array*</span><span class="sxs-lookup"><span data-stu-id="2f0b0-112">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0b0-113">Uma matriz que contém os pontos de curva.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-113">An array containing the curve points.</span></span>

</dd> <dt>

<span data-ttu-id="2f0b0-114">*Stride*</span><span class="sxs-lookup"><span data-stu-id="2f0b0-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0b0-115">O deslocamento (um número de valores de ponto flutuante de precisão simples) entre pontos na curva.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-115">The offset (a number of single-precision floating-point values) between points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="2f0b0-116">*tipo*</span><span class="sxs-lookup"><span data-stu-id="2f0b0-116">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0b0-117">O tipo de curva.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-117">The type of curve.</span></span> <span data-ttu-id="2f0b0-118">Deve ser GLU \_ MAP1 \_ Trim \_ 2 ou Glu \_ MAP1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-118">Must be either GLU\_MAP1\_TRIM\_2 or GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f0b0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f0b0-119">Return value</span></span>

<span data-ttu-id="2f0b0-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f0b0-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f0b0-121">Remarks</span></span>

<span data-ttu-id="2f0b0-122">A função **gluPwlCurve** descreve uma curva de corte linear piecewise para uma superfície NURBS.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-122">The **gluPwlCurve** function describes a piecewise linear trimming curve for a NURBS surface.</span></span> <span data-ttu-id="2f0b0-123">Uma curva linear piecewise consiste em uma lista de coordenadas de pontos no espaço de parâmetro para a superfície NURBS ser cortada.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-123">A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed.</span></span> <span data-ttu-id="2f0b0-124">Esses pontos são conectados com segmentos de linha para formar uma curva.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-124">These points are connected with line segments to form a curve.</span></span> <span data-ttu-id="2f0b0-125">Se a curva for uma aproximação para uma curva real, os pontos deverão ser próximos o suficiente para que o caminho resultante apareça curvo na resolução usada no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2f0b0-125">If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.</span></span>

<span data-ttu-id="2f0b0-126">Se *Type* for Glu \_ MAP1 \_ Trim \_ 2, ele descreve uma curva no espaço de parâmetro bidimensional (*u* e *v*).</span><span class="sxs-lookup"><span data-stu-id="2f0b0-126">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="2f0b0-127">Se for GLU \_ MAP1 \_ Trim \_ 3, ele descreverá uma curva no espaço de parâmetro bidimensional homogêneo (*u*, *v* e *w*).</span><span class="sxs-lookup"><span data-stu-id="2f0b0-127">If it is GLU\_MAP1\_TRIM\_3, then it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="2f0b0-128">Para obter mais informações sobre as curvas de corte, consulte [**gluBeginTrim**](glubegintrim.md).</span><span class="sxs-lookup"><span data-stu-id="2f0b0-128">For more information about trimming curves, see [**gluBeginTrim**](glubegintrim.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f0b0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f0b0-129">Requirements</span></span>



| <span data-ttu-id="2f0b0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f0b0-130">Requirement</span></span> | <span data-ttu-id="2f0b0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2f0b0-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0b0-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f0b0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2f0b0-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f0b0-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2f0b0-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f0b0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2f0b0-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f0b0-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2f0b0-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2f0b0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f0b0-137"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f0b0-137"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="2f0b0-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f0b0-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f0b0-139"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f0b0-139"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f0b0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2f0b0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f0b0-141"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f0b0-141"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f0b0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f0b0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f0b0-143">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="2f0b0-143">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="2f0b0-144">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="2f0b0-144">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="2f0b0-145">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="2f0b0-145">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="2f0b0-146">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="2f0b0-146">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





