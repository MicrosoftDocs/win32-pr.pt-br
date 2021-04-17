---
title: função gluTessEndPolygon (Glu. h)
description: As funções gluTessBeginPolygon e gluTessEndPolygon delimitam uma descrição de polígono. | função gluTessEndPolygon (Glu. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- função gluTessEndPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780185"
---
# <a name="glutessendpolygon-function"></a><span data-ttu-id="82cb0-105">função gluTessEndPolygon</span><span class="sxs-lookup"><span data-stu-id="82cb0-105">gluTessEndPolygon function</span></span>

<span data-ttu-id="82cb0-106">As funções [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitam uma descrição de polígono.</span><span class="sxs-lookup"><span data-stu-id="82cb0-106">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="82cb0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82cb0-107">Syntax</span></span>


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="82cb0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82cb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82cb0-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="82cb0-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="82cb0-110">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="82cb0-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82cb0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82cb0-111">Return value</span></span>

<span data-ttu-id="82cb0-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="82cb0-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82cb0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="82cb0-113">Remarks</span></span>

<span data-ttu-id="82cb0-114">As funções [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitam a definição de um polígono nonconvex.</span><span class="sxs-lookup"><span data-stu-id="82cb0-114">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="82cb0-115">Em cada par **gluTessBeginPolygon**  /  **gluTessEndPolygon** , inclua uma ou mais chamadas para [**gluTessBeginContour**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="82cb0-115">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="82cb0-116">Dentro de cada contorno, há zero ou mais chamadas para [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="82cb0-116">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="82cb0-117">Os vértices especificam uma delimitação fechada (o último vértice de cada contorno é automaticamente vinculado ao primeiro).</span><span class="sxs-lookup"><span data-stu-id="82cb0-117">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="82cb0-118">O parâmetro de *\_ dados Polygon* é um ponteiro para uma estrutura de dados definida pelo programador.</span><span class="sxs-lookup"><span data-stu-id="82cb0-118">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="82cb0-119">Se os retornos de chamada apropriados forem especificados (consulte [*gluTessCallback*](glutess.md)), esse ponteiro será retornado para a função ou funções de retorno de chamada, tornando-o uma maneira conveniente de armazenar informações por polígono.</span><span class="sxs-lookup"><span data-stu-id="82cb0-119">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="82cb0-120">Quando você chama **gluTessEndPolygon**, o polígono é mosaico e os triângulos resultantes são descritos por meio de retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="82cb0-120">When you call **gluTessEndPolygon**, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="82cb0-121">Para obter descrições das funções de retorno de chamada, consulte [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="82cb0-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="82cb0-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82cb0-122">Examples</span></span>

<span data-ttu-id="82cb0-123">O seguinte descreve um diamante com um buraco triangular:</span><span class="sxs-lookup"><span data-stu-id="82cb0-123">The following describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a><span data-ttu-id="82cb0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82cb0-124">Requirements</span></span>



| <span data-ttu-id="82cb0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="82cb0-125">Requirement</span></span> | <span data-ttu-id="82cb0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="82cb0-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82cb0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82cb0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="82cb0-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82cb0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="82cb0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82cb0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="82cb0-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82cb0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="82cb0-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82cb0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="82cb0-132"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="82cb0-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="82cb0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82cb0-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="82cb0-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82cb0-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="82cb0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="82cb0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82cb0-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82cb0-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82cb0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="82cb0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82cb0-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="82cb0-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="82cb0-139">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="82cb0-139">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="82cb0-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="82cb0-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="82cb0-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="82cb0-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="82cb0-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="82cb0-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="82cb0-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="82cb0-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="82cb0-144">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="82cb0-144">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





