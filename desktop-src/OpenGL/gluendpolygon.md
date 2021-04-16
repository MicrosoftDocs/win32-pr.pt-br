---
title: função gluEndPolygon (Glu. h)
description: As funções gluBeginPolygon e gluEndPolygon delimitam uma descrição de polígono. | função gluEndPolygon (Glu. h)
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- função gluEndPolygon OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754138"
---
# <a name="gluendpolygon-function"></a><span data-ttu-id="7b3f0-105">função gluEndPolygon</span><span class="sxs-lookup"><span data-stu-id="7b3f0-105">gluEndPolygon function</span></span>

<span data-ttu-id="7b3f0-106">\[A função **gluEndPolygon** é obsoleta e é fornecida somente para fins de compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-106">\[The **gluEndPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="7b3f0-107">A função **gluEndPolygon** é mapeada para **GluTessEndPolygon** seguida por **gluTessEndContour**.\]</span><span class="sxs-lookup"><span data-stu-id="7b3f0-107">The **gluEndPolygon** function is mapped to **gluTessEndPolygon** followed by **gluTessEndContour**.\]</span></span>

<span data-ttu-id="7b3f0-108">As funções [**gluBeginPolygon**](glubeginpolygon.md) e **gluEndPolygon** delimitam uma descrição de polígono.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-108">The [**gluBeginPolygon**](glubeginpolygon.md) and **gluEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3f0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b3f0-109">Syntax</span></span>


```C++
void gluEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="7b3f0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b3f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b3f0-111">*tess*</span><span class="sxs-lookup"><span data-stu-id="7b3f0-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3f0-112">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="7b3f0-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b3f0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b3f0-113">Return value</span></span>

<span data-ttu-id="7b3f0-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b3f0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b3f0-115">Remarks</span></span>

<span data-ttu-id="7b3f0-116">Use [**gluBeginPolygon**](glubeginpolygon.md) e **gluEndPolygon** para delimitar a definição de um polígono nonconvex.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-116">Use [**gluBeginPolygon**](glubeginpolygon.md) and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="7b3f0-117">Chame **gluBeginPolygon**.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="7b3f0-118">Defina os contornos do polígono chamando [**gluTessVertex**](glutessvertex.md) para cada vértice e [**gluNextContour**](glunextcontour.md) para iniciar cada delimitação nova.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="7b3f0-119">Chame **gluEndPolygon** para sinalizar o fim da definição.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="7b3f0-120">Quando **gluEndPolygon** é chamado, o polígono é mosaico e os triângulos resultantes são descritos por meio de retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="7b3f0-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="7b3f0-121">Para obter descrições das funções de retorno de chamada, consulte [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="7b3f0-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7b3f0-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b3f0-122">Examples</span></span>

<span data-ttu-id="7b3f0-123">O exemplo a seguir descreve um diamante com um buraco triangular:</span><span class="sxs-lookup"><span data-stu-id="7b3f0-123">The following example describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="7b3f0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b3f0-124">Requirements</span></span>



| <span data-ttu-id="7b3f0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b3f0-125">Requirement</span></span> | <span data-ttu-id="7b3f0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7b3f0-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3f0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b3f0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7b3f0-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b3f0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7b3f0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b3f0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7b3f0-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7b3f0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7b3f0-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7b3f0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b3f0-132"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b3f0-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7b3f0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b3f0-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b3f0-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b3f0-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b3f0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7b3f0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b3f0-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b3f0-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3f0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b3f0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3f0-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="7b3f0-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="7b3f0-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="7b3f0-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="7b3f0-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="7b3f0-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="7b3f0-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="7b3f0-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="7b3f0-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="7b3f0-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="7b3f0-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="7b3f0-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





