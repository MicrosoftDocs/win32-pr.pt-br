---
title: função gluNurbsSurface (Glu. h)
description: A função gluNurbsSurface define a forma de uma superfície B-spline racional não uniforme (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- função gluNurbsSurface OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917963"
---
# <a name="glunurbssurface-function"></a><span data-ttu-id="52ecf-104">função gluNurbsSurface</span><span class="sxs-lookup"><span data-stu-id="52ecf-104">gluNurbsSurface function</span></span>

<span data-ttu-id="52ecf-105">A função **gluNurbsSurface** define a forma de uma superfície B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="52ecf-105">The **gluNurbsSurface** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ecf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52ecf-106">Syntax</span></span>


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="52ecf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52ecf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ecf-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="52ecf-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-109">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="52ecf-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-110">*contagem de sknot \_*</span><span class="sxs-lookup"><span data-stu-id="52ecf-110">*sknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-111">O número de nós na direção de *u* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="52ecf-111">The number of knots in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-112">*sknot*</span><span class="sxs-lookup"><span data-stu-id="52ecf-112">*sknot*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-113">Uma matriz de *\_ contagem de sknot* nondecreasing valores de nó na direção de *u* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="52ecf-113">An array of *sknot\_count* nondecreasing knot values in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-114">*contagem de tknot \_*</span><span class="sxs-lookup"><span data-stu-id="52ecf-114">*tknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-115">O número de nós na direção de paramétrica *v* .</span><span class="sxs-lookup"><span data-stu-id="52ecf-115">The number of knots in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-116">*tknot*</span><span class="sxs-lookup"><span data-stu-id="52ecf-116">*tknot*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-117">Uma matriz de *\_ contagem de tknot* nondecreasing valores de nó na direção de paramétrica *v* .</span><span class="sxs-lookup"><span data-stu-id="52ecf-117">An array of *tknot\_count* nondecreasing knot values in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-118">*\_distância s*</span><span class="sxs-lookup"><span data-stu-id="52ecf-118">*s\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-119">O deslocamento (como um número de valores de ponto de precisionfloating único) entre pontos de controle sucessivos na direção de paramétrica *u* em *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="52ecf-119">The offset (as a number of single precisionfloating-point values) between successive control points in the parametric *u* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-120">*t \_ Stride*</span><span class="sxs-lookup"><span data-stu-id="52ecf-120">*t\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-121">O deslocamento (em valores de ponto de precisionfloating único) entre pontos de controle sucessivos na direção de paramétrica *v* em *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="52ecf-121">The offset (in single precisionfloating-point values) between successive control points in the parametric *v* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-122">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="52ecf-122">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-123">Uma matriz que contém pontos de controle para a superfície NURBS.</span><span class="sxs-lookup"><span data-stu-id="52ecf-123">An array containing control points for the NURBS surface.</span></span> <span data-ttu-id="52ecf-124">Os deslocamentos entre pontos de controle sucessivos nas direções paramétrica *u* e *v* são fornecidos por *s \_ Stride* e *t \_ Stride*.</span><span class="sxs-lookup"><span data-stu-id="52ecf-124">The offsets between successive control points in the parametric *u* and *v* directions are given by *s\_stride* and *t\_stride*.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-125">*sorder*</span><span class="sxs-lookup"><span data-stu-id="52ecf-125">*sorder*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-126">A ordem da superfície NURBS na direção de *u* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="52ecf-126">The order of the NURBS surface in the parametric *u* direction.</span></span> <span data-ttu-id="52ecf-127">A ordem é mais do que o grau, portanto, uma superfície que é cúbica em *u* tem uma ordem *u* de 4.</span><span class="sxs-lookup"><span data-stu-id="52ecf-127">The order is one more than the degree, hence a surface that is cubic in *u* has a *u* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-128">*torder*</span><span class="sxs-lookup"><span data-stu-id="52ecf-128">*torder*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-129">A ordem da superfície NURBS na direção *v* paramétrica.</span><span class="sxs-lookup"><span data-stu-id="52ecf-129">The order of the NURBS surface in the parametric *v* direction.</span></span> <span data-ttu-id="52ecf-130">A ordem é mais do que o grau, portanto, uma superfície que é cúbica em *v* tem uma ordem *v* de 4.</span><span class="sxs-lookup"><span data-stu-id="52ecf-130">The order is one more than the degree, hence a surface that is cubic in *v* has a *v* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="52ecf-131">*tipo*</span><span class="sxs-lookup"><span data-stu-id="52ecf-131">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="52ecf-132">O tipo da superfície.</span><span class="sxs-lookup"><span data-stu-id="52ecf-132">The type of the surface.</span></span> <span data-ttu-id="52ecf-133">O parâmetro de *tipo* pode ser qualquer um dos tipos de avaliadores bidimensionais válidos (como GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ Color \_ 4).</span><span class="sxs-lookup"><span data-stu-id="52ecf-133">The *type* parameter can be any of the valid two-dimensional evaluator types (such as GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_COLOR\_4).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ecf-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52ecf-134">Return value</span></span>

<span data-ttu-id="52ecf-135">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="52ecf-135">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52ecf-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="52ecf-136">Remarks</span></span>

<span data-ttu-id="52ecf-137">Use **gluNurbsSurface** em uma definição de superfície NURBS para descrever a forma de uma superfície NURBS (antes de qualquer corte).</span><span class="sxs-lookup"><span data-stu-id="52ecf-137">Use **gluNurbsSurface** within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming).</span></span> <span data-ttu-id="52ecf-138">Para marcar o início de uma definição de superfície NURBS, use a função [**gluBeginSurface**](glubeginsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="52ecf-138">To mark the beginning of a NURBS surface definition, use the [**gluBeginSurface**](glubeginsurface.md) function.</span></span> <span data-ttu-id="52ecf-139">Para marcar o final de uma definição de superfície NURBS, use a função [**gluEndSurface**](gluendsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="52ecf-139">To mark the end of a NURBS surface definition, use the [**gluEndSurface**](gluendsurface.md) function.</span></span> <span data-ttu-id="52ecf-140">Chame **gluNurbsSurface** somente dentro de uma definição de superfície NURBS.</span><span class="sxs-lookup"><span data-stu-id="52ecf-140">Call **gluNurbsSurface** within a NURBS surface definition only.</span></span>

<span data-ttu-id="52ecf-141">Você associa as coordenadas posicionais, de textura e de cores a uma superfície, apresentando cada uma como um **gluNurbsSurface** separado entre um par **gluBeginSurface** / **gluEndSurface** .</span><span class="sxs-lookup"><span data-stu-id="52ecf-141">You associate positional, texture, and color coordinates with a surface by presenting each as a separate **gluNurbsSurface** between a **gluBeginSurface**/**gluEndSurface** pair.</span></span> <span data-ttu-id="52ecf-142">Em um único par **gluBeginSurface** / **gluEndSurface** , você pode fazer apenas uma chamada para **gluNurbsSurface** para cor, posição e dados de textura.</span><span class="sxs-lookup"><span data-stu-id="52ecf-142">Within a single **gluBeginSurface**/**gluEndSurface** pair, you can make only one call to **gluNurbsSurface** for color, position, and texture data.</span></span> <span data-ttu-id="52ecf-143">Faça exatamente uma chamada para descrever a posição da superfície (um *tipo* de GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="52ecf-143">Make exactly one call to describe the position of the surface (a *type* of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4).</span></span>

<span data-ttu-id="52ecf-144">Você pode cortar uma superfície NURBS usando as funções [**gluNurbsCurve**](glunurbscurve.md) e [**gluPwlCurve**](glupwlcurve.md) entre chamadas para [**gluBeginTrim**](glubegintrim.md) e [**gluEndTrim**](gluendtrim.md).</span><span class="sxs-lookup"><span data-stu-id="52ecf-144">You can trim a NURBS surface by using the [**gluNurbsCurve**](glunurbscurve.md) and [**gluPwlCurve**](glupwlcurve.md) functions between calls to [**gluBeginTrim**](glubegintrim.md) and [**gluEndTrim**](gluendtrim.md).</span></span>

<span data-ttu-id="52ecf-145">Um **gluNurbsSurface** com os nós de *\_ contagem sknot* nos nós de *\_ contagem* *u* e tknot na direção *v* com Orders *sorder* e *torder* deve ter os pontos de controle (sknot *\_ Count*  - *sorder*) multipied por (tknot *\_ Count*  - *torder*).</span><span class="sxs-lookup"><span data-stu-id="52ecf-145">A **gluNurbsSurface** with *sknot\_count* knots in the *u* direction and *tknot\_count* knots in the *v* direction with orders *sorder* and *torder* must have (*sknot\_count* -*sorder*) multipied by (*tknot\_count* -*torder*) control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="52ecf-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52ecf-146">Requirements</span></span>



| <span data-ttu-id="52ecf-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ecf-147">Requirement</span></span> | <span data-ttu-id="52ecf-148">Valor</span><span class="sxs-lookup"><span data-stu-id="52ecf-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52ecf-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52ecf-149">Minimum supported client</span></span><br/> | <span data-ttu-id="52ecf-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52ecf-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52ecf-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52ecf-151">Minimum supported server</span></span><br/> | <span data-ttu-id="52ecf-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52ecf-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52ecf-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52ecf-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="52ecf-154"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="52ecf-154"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="52ecf-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52ecf-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="52ecf-156"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52ecf-156"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="52ecf-157">DLL</span><span class="sxs-lookup"><span data-stu-id="52ecf-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52ecf-158"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52ecf-158"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ecf-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="52ecf-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ecf-160">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="52ecf-160">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="52ecf-161">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="52ecf-161">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="52ecf-162">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="52ecf-162">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="52ecf-163">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="52ecf-163">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="52ecf-164">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="52ecf-164">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="52ecf-165">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="52ecf-165">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="52ecf-166">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="52ecf-166">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





