---
title: função gluTessBeginPolygon (Glu. h)
description: As funções gluTessBeginPolygon e gluTessEndPolygon delimitam uma descrição de polígono. | função gluTessBeginPolygon (Glu. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- função gluTessBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105755327"
---
# <a name="glutessbeginpolygon-function"></a><span data-ttu-id="fbe4d-105">função gluTessBeginPolygon</span><span class="sxs-lookup"><span data-stu-id="fbe4d-105">gluTessBeginPolygon function</span></span>

<span data-ttu-id="fbe4d-106">As funções **gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitam uma descrição de polígono.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-106">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe4d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fbe4d-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a><span data-ttu-id="fbe4d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fbe4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbe4d-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="fbe4d-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="fbe4d-110">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="fbe4d-111">*dados de polígono \_*</span><span class="sxs-lookup"><span data-stu-id="fbe4d-111">*polygon\_data*</span></span> 
</dt> <dd>

<span data-ttu-id="fbe4d-112">Um ponteiro para uma estrutura de dados Polygon definida pelo programador.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-112">A pointer to a programmer-defined polygon data structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbe4d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fbe4d-113">Return value</span></span>

<span data-ttu-id="fbe4d-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe4d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbe4d-115">Remarks</span></span>

<span data-ttu-id="fbe4d-116">As funções **gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitam a definição de um polígono nonconvex.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-116">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="fbe4d-117">Em cada par **gluTessBeginPolygon**  /  **gluTessEndPolygon** , inclua uma ou mais chamadas para [**gluTessBeginContour**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-117">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="fbe4d-118">Dentro de cada contorno, há zero ou mais chamadas para [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-118">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="fbe4d-119">Os vértices especificam uma delimitação fechada (o último vértice de cada contorno é automaticamente vinculado ao primeiro).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-119">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="fbe4d-120">O parâmetro de *\_ dados Polygon* é um ponteiro para uma estrutura de dados definida pelo programador.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-120">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="fbe4d-121">Se os retornos de chamada apropriados forem especificados (consulte [*gluTessCallback*](glutess.md)), esse ponteiro será retornado para a função ou funções de retorno de chamada, tornando-o uma maneira conveniente de armazenar informações por polígono.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-121">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="fbe4d-122">Quando você chama [**gluTessEndPolygon**](glutessendpolygon.md), o polígono é mosaico e os triângulos resultantes são descritos por meio de retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="fbe4d-122">When you call [**gluTessEndPolygon**](glutessendpolygon.md), the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="fbe4d-123">Para obter descrições das funções de retorno de chamada, consulte [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="fbe4d-123">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fbe4d-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fbe4d-124">Examples</span></span>

<span data-ttu-id="fbe4d-125">O seguinte descreve um diamante com um buraco triangular:</span><span class="sxs-lookup"><span data-stu-id="fbe4d-125">The following describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="fbe4d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbe4d-126">Requirements</span></span>



| <span data-ttu-id="fbe4d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe4d-127">Requirement</span></span> | <span data-ttu-id="fbe4d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fbe4d-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe4d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbe4d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fbe4d-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fbe4d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fbe4d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fbe4d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fbe4d-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fbe4d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fbe4d-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fbe4d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbe4d-134"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbe4d-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="fbe4d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbe4d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbe4d-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbe4d-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fbe4d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fbe4d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbe4d-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbe4d-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe4d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbe4d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe4d-140">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="fbe4d-140">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="fbe4d-141">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="fbe4d-141">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="fbe4d-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="fbe4d-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="fbe4d-143">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="fbe4d-143">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="fbe4d-144">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="fbe4d-144">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="fbe4d-145">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="fbe4d-145">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="fbe4d-146">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="fbe4d-146">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





