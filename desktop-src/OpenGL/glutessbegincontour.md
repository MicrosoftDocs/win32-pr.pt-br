---
title: função gluTessBeginContour (Glu. h)
description: As funções gluTessBeginContour e gluTessEndContour delimitam uma descrição de contorno. | função gluTessBeginContour (Glu. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- função gluTessBeginContour OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105762037"
---
# <a name="glutessbegincontour-function"></a><span data-ttu-id="dee15-105">função gluTessBeginContour</span><span class="sxs-lookup"><span data-stu-id="dee15-105">gluTessBeginContour function</span></span>

<span data-ttu-id="dee15-106">As funções **gluTessBeginContour** e [**gluTessEndContour**](glutessendcontour.md) delimitam uma descrição de contorno.</span><span class="sxs-lookup"><span data-stu-id="dee15-106">The **gluTessBeginContour** and [**gluTessEndContour**](glutessendcontour.md) functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee15-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dee15-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="dee15-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dee15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dee15-109">*tess*</span><span class="sxs-lookup"><span data-stu-id="dee15-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="dee15-110">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="dee15-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dee15-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dee15-111">Return value</span></span>

<span data-ttu-id="dee15-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dee15-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dee15-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dee15-113">Remarks</span></span>

<span data-ttu-id="dee15-114">As funções **gluTessBeginContour** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitam a definição de uma delimitação de polígono.</span><span class="sxs-lookup"><span data-stu-id="dee15-114">The **gluTessBeginContour** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="dee15-115">Em cada par **gluTessBeginContour** / **gluTessEndPolygon** , pode haver zero ou mais chamadas para [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="dee15-115">Within each **gluTessBeginContour**/**gluTessEndPolygon** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="dee15-116">Os vértices especificam uma delimitação fechada (o último vértice de cada contorno é automaticamente vinculado ao primeiro).</span><span class="sxs-lookup"><span data-stu-id="dee15-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="dee15-117">Você pode chamar **gluTessBeginContour** somente entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon**.</span><span class="sxs-lookup"><span data-stu-id="dee15-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee15-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee15-118">Requirements</span></span>



| <span data-ttu-id="dee15-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee15-119">Requirement</span></span> | <span data-ttu-id="dee15-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dee15-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dee15-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee15-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dee15-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dee15-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dee15-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee15-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dee15-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dee15-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dee15-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dee15-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dee15-126"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="dee15-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="dee15-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dee15-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="dee15-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dee15-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dee15-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dee15-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee15-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee15-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee15-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="dee15-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee15-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="dee15-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="dee15-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="dee15-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="dee15-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="dee15-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="dee15-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="dee15-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="dee15-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="dee15-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="dee15-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="dee15-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="dee15-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="dee15-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





