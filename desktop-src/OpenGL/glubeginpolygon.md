---
title: função gluBeginPolygon (Glu. h)
description: As funções gluBeginPolygon e gluEndPolygon delimitam uma descrição de polígono. | função gluBeginPolygon (Glu. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- função gluBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756179"
---
# <a name="glubeginpolygon-function"></a><span data-ttu-id="e864b-105">função gluBeginPolygon</span><span class="sxs-lookup"><span data-stu-id="e864b-105">gluBeginPolygon function</span></span>

<span data-ttu-id="e864b-106">\[A função **gluBeginPolygon** é obsoleta e é fornecida somente para fins de compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="e864b-106">\[The **gluBeginPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="e864b-107">A função **gluBeginPolygon** é mapeada para [**GluTessBeginPolygon**](glutessbeginpolygon.md) seguida por [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="e864b-107">The **gluBeginPolygon** function is mapped to [**gluTessBeginPolygon**](glutessbeginpolygon.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="e864b-108">As funções **gluBeginPolygon** e [**gluEndPolygon**](gluendpolygon.md) delimitam uma descrição de polígono.</span><span class="sxs-lookup"><span data-stu-id="e864b-108">The **gluBeginPolygon** and [**gluEndPolygon**](gluendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e864b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e864b-109">Syntax</span></span>


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="e864b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e864b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e864b-111">*tess*</span><span class="sxs-lookup"><span data-stu-id="e864b-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="e864b-112">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="e864b-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e864b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e864b-113">Return value</span></span>

<span data-ttu-id="e864b-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e864b-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e864b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e864b-115">Remarks</span></span>

<span data-ttu-id="e864b-116">Use **gluBeginPolygon** e **gluEndPolygon** para delimitar a definição de um polígono nonconvex.</span><span class="sxs-lookup"><span data-stu-id="e864b-116">Use **gluBeginPolygon** and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="e864b-117">Chame **gluBeginPolygon**.</span><span class="sxs-lookup"><span data-stu-id="e864b-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="e864b-118">Defina os contornos do polígono chamando [**gluTessVertex**](glutessvertex.md) para cada vértice e [**gluNextContour**](glunextcontour.md) para iniciar cada delimitação nova.</span><span class="sxs-lookup"><span data-stu-id="e864b-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="e864b-119">Chame **gluEndPolygon** para sinalizar o fim da definição.</span><span class="sxs-lookup"><span data-stu-id="e864b-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="e864b-120">Quando **gluEndPolygon** é chamado, o polígono é mosaico e os triângulos resultantes são descritos por meio de retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="e864b-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="e864b-121">Para obter descrições das funções de retorno de chamada, consulte [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="e864b-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e864b-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e864b-122">Examples</span></span>

<span data-ttu-id="e864b-123">O exemplo a seguir descreve um diamante com um buraco triangular:</span><span class="sxs-lookup"><span data-stu-id="e864b-123">The following example describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="e864b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e864b-124">Requirements</span></span>



| <span data-ttu-id="e864b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e864b-125">Requirement</span></span> | <span data-ttu-id="e864b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e864b-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e864b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e864b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e864b-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e864b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e864b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e864b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e864b-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e864b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e864b-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e864b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e864b-132"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="e864b-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="e864b-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e864b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e864b-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e864b-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e864b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e864b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e864b-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e864b-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e864b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="e864b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e864b-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="e864b-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="e864b-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="e864b-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="e864b-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="e864b-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="e864b-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="e864b-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="e864b-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="e864b-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="e864b-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="e864b-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





