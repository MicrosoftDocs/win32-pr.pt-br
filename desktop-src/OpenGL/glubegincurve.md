---
title: função gluBeginCurve (Glu. h)
description: As funções gluBeginCurve e gluEndCurve delimitam uma definição de curva de B-spline racional não uniforme (NURBS). | função gluBeginCurve (Glu. h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- função gluBeginCurve OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e17bd88cfcb49801450ead865c437843d179b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788121"
---
# <a name="glubegincurve-function"></a><span data-ttu-id="23b65-105">função gluBeginCurve</span><span class="sxs-lookup"><span data-stu-id="23b65-105">gluBeginCurve function</span></span>

<span data-ttu-id="23b65-106">As funções **gluBeginCurve** e [**gluEndCurve**](gluendcurve.md) delimitam uma definição de curva de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="23b65-106">The **gluBeginCurve** and [**gluEndCurve**](gluendcurve.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b65-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23b65-107">Syntax</span></span>


```C++
void WINAPI gluBeginCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="23b65-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23b65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b65-109">*nobj*</span><span class="sxs-lookup"><span data-stu-id="23b65-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="23b65-110">O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="23b65-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b65-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23b65-111">Return value</span></span>

<span data-ttu-id="23b65-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="23b65-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23b65-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="23b65-113">Remarks</span></span>

<span data-ttu-id="23b65-114">Use **gluBeginCurve** para marcar o início de uma definição de curva NURBS.</span><span class="sxs-lookup"><span data-stu-id="23b65-114">Use **gluBeginCurve** to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="23b65-115">Depois de chamar **gluBeginCurve**, faça uma ou mais chamadas para [**gluNurbsCurve**](glunurbscurve.md) para definir os atributos da curva.</span><span class="sxs-lookup"><span data-stu-id="23b65-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="23b65-116">Exatamente uma das chamadas para **gluNurbsCurve** deve ter um tipo de curva GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="23b65-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="23b65-117">Para marcar o final da definição de curva NURBS, chame [**gluEndCurve**](gluendcurve.md).</span><span class="sxs-lookup"><span data-stu-id="23b65-117">To mark the end of the NURBS curve definition, call [**gluEndCurve**](gluendcurve.md).</span></span>

<span data-ttu-id="23b65-118">Os avaliadores OpenGL são usados para renderizar a curva NURBS como uma série de segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="23b65-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="23b65-119">O estado do avaliador é preservado durante a renderização com [**glPushAttrib**](glpushattrib.md) ( \_ bit de avaliação GL \_ ) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="23b65-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="23b65-120">Para obter informações sobre exatamente que Estado Essas chamadas preservam, consulte **glPushAttrib**.</span><span class="sxs-lookup"><span data-stu-id="23b65-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="23b65-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23b65-121">Examples</span></span>

<span data-ttu-id="23b65-122">As funções a seguir renderizam uma curva NURBS texturizada com Normals; as coordenadas de textura e normais também são especificadas como curvas NURBS:</span><span class="sxs-lookup"><span data-stu-id="23b65-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="23b65-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23b65-123">Requirements</span></span>



| <span data-ttu-id="23b65-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b65-124">Requirement</span></span> | <span data-ttu-id="23b65-125">Valor</span><span class="sxs-lookup"><span data-stu-id="23b65-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23b65-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b65-126">Minimum supported client</span></span><br/> | <span data-ttu-id="23b65-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="23b65-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="23b65-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b65-128">Minimum supported server</span></span><br/> | <span data-ttu-id="23b65-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="23b65-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23b65-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="23b65-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b65-131"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="23b65-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="23b65-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23b65-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="23b65-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23b65-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="23b65-134">DLL</span><span class="sxs-lookup"><span data-stu-id="23b65-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b65-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b65-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b65-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="23b65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b65-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="23b65-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="23b65-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="23b65-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="23b65-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="23b65-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="23b65-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="23b65-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="23b65-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="23b65-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





