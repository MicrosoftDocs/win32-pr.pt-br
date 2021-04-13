---
title: função gluTessVertex (Glu. h)
description: A função gluTessVertex especifica um vértice em um polígono.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- função gluTessVertex OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499734"
---
# <a name="glutessvertex-function"></a><span data-ttu-id="4eb90-104">função gluTessVertex</span><span class="sxs-lookup"><span data-stu-id="4eb90-104">gluTessVertex function</span></span>

<span data-ttu-id="4eb90-105">A função **gluTessVertex** especifica um vértice em um polígono.</span><span class="sxs-lookup"><span data-stu-id="4eb90-105">The **gluTessVertex** function specifies a vertex on a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb90-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4eb90-106">Syntax</span></span>


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a><span data-ttu-id="4eb90-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4eb90-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb90-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="4eb90-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb90-109">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="4eb90-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4eb90-110">*coords*</span><span class="sxs-lookup"><span data-stu-id="4eb90-110">*coords*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb90-111">O local do vértice.</span><span class="sxs-lookup"><span data-stu-id="4eb90-111">The location of the vertex.</span></span>

</dd> <dt>

<span data-ttu-id="4eb90-112">*data*</span><span class="sxs-lookup"><span data-stu-id="4eb90-112">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb90-113">Um ponteiro passado de volta para o programa com o retorno de chamada de vértice (conforme especificado por [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="4eb90-113">An pointer passed back to the program with the vertex callback (as specified by [*gluTessCallback*](glutess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb90-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4eb90-114">Return value</span></span>

<span data-ttu-id="4eb90-115">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4eb90-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb90-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4eb90-116">Remarks</span></span>

<span data-ttu-id="4eb90-117">A função **gluTessVertex** descreve um vértice em um polígono que o usuário está definindo.</span><span class="sxs-lookup"><span data-stu-id="4eb90-117">The **gluTessVertex** function describes a vertex on a polygon that the user is defining.</span></span> <span data-ttu-id="4eb90-118">As chamadas de **gluTessVertex** sucessivas descrevem uma delimitação de fechamento.</span><span class="sxs-lookup"><span data-stu-id="4eb90-118">Successive **gluTessVertex** calls describe a closed contour.</span></span> <span data-ttu-id="4eb90-119">Por exemplo, para descrever um diamante, chame **gluTessVertex** quatro vezes.</span><span class="sxs-lookup"><span data-stu-id="4eb90-119">For example, to describe a quadrilateral, call **gluTessVertex** four times.</span></span> <span data-ttu-id="4eb90-120">Você só pode chamar **gluTessVertex** entre [**gluTessBeginContour**](glutessbegincontour.md) e [**gluTessEndContour**](glutessendcontour.md).</span><span class="sxs-lookup"><span data-stu-id="4eb90-120">You can only call **gluTessVertex** between [**gluTessBeginContour**](glutessbegincontour.md) and [**gluTessEndContour**](glutessendcontour.md).</span></span>

<span data-ttu-id="4eb90-121">O parâmetro de *dados* normalmente aponta para uma estrutura que contém o local do vértice, bem como outros atributos por vértice, como Color e normal.</span><span class="sxs-lookup"><span data-stu-id="4eb90-121">The *data* parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal.</span></span> <span data-ttu-id="4eb90-122">Esse ponteiro é passado de volta para o programa por meio do \_ retorno de chamada de vértice Glu após o mosaico (consulte [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="4eb90-122">This pointer is passed back to the program through the GLU\_VERTEX callback after tessellation (see [*gluTessCallback*](glutess.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb90-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eb90-123">Requirements</span></span>



| <span data-ttu-id="4eb90-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb90-124">Requirement</span></span> | <span data-ttu-id="4eb90-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4eb90-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb90-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4eb90-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb90-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4eb90-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4eb90-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4eb90-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb90-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4eb90-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4eb90-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4eb90-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb90-131"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb90-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4eb90-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4eb90-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="4eb90-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4eb90-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4eb90-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4eb90-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4eb90-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4eb90-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb90-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4eb90-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb90-137">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="4eb90-137">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="4eb90-138">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="4eb90-138">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="4eb90-139">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="4eb90-139">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="4eb90-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="4eb90-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="4eb90-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="4eb90-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="4eb90-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="4eb90-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="4eb90-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="4eb90-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





