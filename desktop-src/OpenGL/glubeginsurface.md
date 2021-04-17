---
title: função gluBeginSurface (Glu. h)
description: As funções gluBeginSurface e gluEndSurface delimitam uma definição de superfície de B-spline racional não uniforme (NURBS). | função gluBeginSurface (Glu. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- função gluBeginSurface OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105813124"
---
# <a name="glubeginsurface-function"></a><span data-ttu-id="12e94-105">função gluBeginSurface</span><span class="sxs-lookup"><span data-stu-id="12e94-105">gluBeginSurface function</span></span>

<span data-ttu-id="12e94-106">As funções **gluBeginSurface** e [**gluEndSurface**](gluendsurface.md) delimitam uma definição de superfície de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="12e94-106">The **gluBeginSurface** and [**gluEndSurface**](gluendsurface.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e94-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12e94-107">Syntax</span></span>


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="12e94-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12e94-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e94-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="12e94-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="12e94-110">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="12e94-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12e94-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12e94-111">Return value</span></span>

<span data-ttu-id="12e94-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="12e94-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12e94-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="12e94-113">Remarks</span></span>

<span data-ttu-id="12e94-114">As funções **gluBeginSurface** e **gluEndSurface** marcam o início e o fim das definições de superfície NURBS, que são definidas com chamadas para **gluNurbsSurface**.</span><span class="sxs-lookup"><span data-stu-id="12e94-114">The **gluBeginSurface** and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="12e94-115">Chame **gluBeginSurface** para marcar o início de uma definição de superfície NURBS.</span><span class="sxs-lookup"><span data-stu-id="12e94-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="12e94-116">Faça uma ou mais chamadas para **gluNurbsSurface** para definir os atributos da superfície.</span><span class="sxs-lookup"><span data-stu-id="12e94-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="12e94-117">Exatamente uma dessas chamadas para **gluNurbsSurface** deve ter um tipo de superfície de GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ vértice \_ 4.</span><span class="sxs-lookup"><span data-stu-id="12e94-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="12e94-118">Para marcar o final da definição da superfície NURBS, chame **gluEndSurface**.</span><span class="sxs-lookup"><span data-stu-id="12e94-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="12e94-119">As funções [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)e [**GLUENDTRIM**](gluendtrim.md) dão suporte à remoção de superfícies NURBS.</span><span class="sxs-lookup"><span data-stu-id="12e94-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and [**gluEndTrim**](gluendtrim.md) functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="12e94-120">Use avaliadores OpenGL para renderizar a superfície NURBS como um conjunto de polígonos.</span><span class="sxs-lookup"><span data-stu-id="12e94-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="12e94-121">Preserve o estado do avaliador durante a renderização com [**glPushAttrib**](glpushattrib.md)( \_ bit de avaliação GL \_ ) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="12e94-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md)(GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="12e94-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="12e94-122">Examples</span></span>

<span data-ttu-id="12e94-123">As funções a seguir renderizam uma superfície NURBS texturizada com Normals; as coordenadas de textura e normais também são descritas como superfícies NURBS:</span><span class="sxs-lookup"><span data-stu-id="12e94-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="12e94-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12e94-124">Requirements</span></span>



| <span data-ttu-id="12e94-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e94-125">Requirement</span></span> | <span data-ttu-id="12e94-126">Valor</span><span class="sxs-lookup"><span data-stu-id="12e94-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="12e94-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12e94-127">Minimum supported client</span></span><br/> | <span data-ttu-id="12e94-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12e94-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="12e94-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12e94-129">Minimum supported server</span></span><br/> | <span data-ttu-id="12e94-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12e94-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="12e94-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="12e94-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="12e94-132"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="12e94-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="12e94-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12e94-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="12e94-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12e94-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="12e94-135">DLL</span><span class="sxs-lookup"><span data-stu-id="12e94-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12e94-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12e94-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e94-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="12e94-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e94-138">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="12e94-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="12e94-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="12e94-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="12e94-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="12e94-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="12e94-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="12e94-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="12e94-142">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="12e94-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="12e94-143">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="12e94-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





