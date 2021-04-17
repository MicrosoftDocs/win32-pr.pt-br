---
title: função gluEndCurve (Glu. h)
description: As funções gluBeginCurve e gluEndCurve delimitam uma definição de curva de B-spline racional não uniforme (NURBS). | função gluEndCurve (Glu. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- função gluEndCurve OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105775668"
---
# <a name="gluendcurve-function"></a><span data-ttu-id="01e0c-105">função gluEndCurve</span><span class="sxs-lookup"><span data-stu-id="01e0c-105">gluEndCurve function</span></span>

<span data-ttu-id="01e0c-106">As funções [**gluBeginCurve**](glubegincurve.md) e **gluEndCurve** delimitam uma definição de curva de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="01e0c-106">The [**gluBeginCurve**](glubegincurve.md) and **gluEndCurve** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e0c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01e0c-107">Syntax</span></span>


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="01e0c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01e0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01e0c-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="01e0c-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="01e0c-110">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="01e0c-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01e0c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01e0c-111">Return value</span></span>

<span data-ttu-id="01e0c-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="01e0c-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01e0c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="01e0c-113">Remarks</span></span>

<span data-ttu-id="01e0c-114">Use [**gluBeginCurve**](glubegincurve.md) para marcar o início de uma definição de curva NURBS.</span><span class="sxs-lookup"><span data-stu-id="01e0c-114">Use [**gluBeginCurve**](glubegincurve.md) to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="01e0c-115">Depois de chamar **gluBeginCurve**, faça uma ou mais chamadas para [**gluNurbsCurve**](glunurbscurve.md) para definir os atributos da curva.</span><span class="sxs-lookup"><span data-stu-id="01e0c-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="01e0c-116">Exatamente uma das chamadas para **gluNurbsCurve** deve ter um tipo de curva GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="01e0c-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="01e0c-117">Para marcar o final da definição de curva NURBS, chame **gluEndCurve**.</span><span class="sxs-lookup"><span data-stu-id="01e0c-117">To mark the end of the NURBS curve definition, call **gluEndCurve**.</span></span>

<span data-ttu-id="01e0c-118">Os avaliadores OpenGL são usados para renderizar a curva NURBS como uma série de segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="01e0c-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="01e0c-119">O estado do avaliador é preservado durante a renderização com [**glPushAttrib**](glpushattrib.md) ( \_ bit de avaliação GL \_ ) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="01e0c-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT ) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="01e0c-120">Para obter informações sobre exatamente que Estado Essas chamadas preservam, consulte **glPushAttrib**.</span><span class="sxs-lookup"><span data-stu-id="01e0c-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="01e0c-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01e0c-121">Examples</span></span>

<span data-ttu-id="01e0c-122">As funções a seguir renderizam uma curva NURBS texturizada com Normals; as coordenadas de textura e normais também são especificadas como curvas NURBS:</span><span class="sxs-lookup"><span data-stu-id="01e0c-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="01e0c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01e0c-123">Requirements</span></span>



| <span data-ttu-id="01e0c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e0c-124">Requirement</span></span> | <span data-ttu-id="01e0c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="01e0c-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="01e0c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01e0c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="01e0c-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01e0c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="01e0c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01e0c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="01e0c-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01e0c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="01e0c-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="01e0c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="01e0c-131"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="01e0c-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="01e0c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01e0c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="01e0c-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01e0c-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="01e0c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="01e0c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01e0c-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01e0c-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01e0c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="01e0c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e0c-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="01e0c-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="01e0c-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="01e0c-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="01e0c-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="01e0c-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="01e0c-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="01e0c-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="01e0c-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="01e0c-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





