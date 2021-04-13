---
title: função gluTessEndContour (Glu. h)
description: As funções gluTessBeginContour e gluTessEndContour delimitam uma descrição de contorno. | função gluTessEndContour (Glu. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- função gluTessEndContour OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298157"
---
# <a name="glutessendcontour-function"></a><span data-ttu-id="c2f54-105">função gluTessEndContour</span><span class="sxs-lookup"><span data-stu-id="c2f54-105">gluTessEndContour function</span></span>

<span data-ttu-id="c2f54-106">As funções [**gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitam uma descrição de contorno.</span><span class="sxs-lookup"><span data-stu-id="c2f54-106">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f54-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2f54-107">Syntax</span></span>


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="c2f54-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2f54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2f54-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="c2f54-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="c2f54-110">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="c2f54-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2f54-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2f54-111">Return value</span></span>

<span data-ttu-id="c2f54-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c2f54-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f54-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2f54-113">Remarks</span></span>

<span data-ttu-id="c2f54-114">As funções [**gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitam a definição de uma delimitação de polígono.</span><span class="sxs-lookup"><span data-stu-id="c2f54-114">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="c2f54-115">Em cada par **gluTessBeginContour** / **gluTessEndContour** , pode haver zero ou mais chamadas para [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="c2f54-115">Within each **gluTessBeginContour**/**gluTessEndContour** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="c2f54-116">Os vértices especificam uma delimitação fechada (o último vértice de cada contorno é automaticamente vinculado ao primeiro).</span><span class="sxs-lookup"><span data-stu-id="c2f54-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="c2f54-117">Você pode chamar **gluTessBeginContour** somente entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) e [**gluTessEndPolygon**](glutessendpolygon.md).</span><span class="sxs-lookup"><span data-stu-id="c2f54-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and [**gluTessEndPolygon**](glutessendpolygon.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f54-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2f54-118">Requirements</span></span>



| <span data-ttu-id="c2f54-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f54-119">Requirement</span></span> | <span data-ttu-id="c2f54-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c2f54-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f54-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f54-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f54-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2f54-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c2f54-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f54-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f54-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2f54-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c2f54-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2f54-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2f54-126"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2f54-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="c2f54-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2f54-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2f54-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2f54-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2f54-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c2f54-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2f54-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2f54-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2f54-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2f54-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2f54-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="c2f54-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="c2f54-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="c2f54-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="c2f54-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="c2f54-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="c2f54-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="c2f54-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="c2f54-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="c2f54-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="c2f54-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="c2f54-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="c2f54-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="c2f54-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





