---
title: função gluQuadricDrawStyle (Glu. h)
description: A função gluQuadricDrawStyle especifica o estilo de desenho desejado para quadrics.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- função gluQuadricDrawStyle OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918830"
---
# <a name="gluquadricdrawstyle-function"></a><span data-ttu-id="9c983-104">função gluQuadricDrawStyle</span><span class="sxs-lookup"><span data-stu-id="9c983-104">gluQuadricDrawStyle function</span></span>

<span data-ttu-id="9c983-105">A função **gluQuadricDrawStyle** especifica o estilo de desenho desejado para quadrics.</span><span class="sxs-lookup"><span data-stu-id="9c983-105">The **gluQuadricDrawStyle** function specifies the draw style desired for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c983-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c983-106">Syntax</span></span>


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a><span data-ttu-id="9c983-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c983-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c983-108">*quádruplo*</span><span class="sxs-lookup"><span data-stu-id="9c983-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="9c983-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="9c983-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9c983-110">*desenharstyle*</span><span class="sxs-lookup"><span data-stu-id="9c983-110">*drawStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="9c983-111">O estilo de desenho desejado.</span><span class="sxs-lookup"><span data-stu-id="9c983-111">The desired draw style.</span></span> <span data-ttu-id="9c983-112">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="9c983-112">The following values are valid.</span></span>



| <span data-ttu-id="9c983-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9c983-113">Value</span></span>                                                                                                                                                            | <span data-ttu-id="9c983-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9c983-114">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <span data-ttu-id="9c983-115"><dt>**preenchimento de GLU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c983-115"><dt>**GLU\_FILL**</dt></span></span> </dl>                   | <span data-ttu-id="9c983-116">Quadrics são renderizados com primitivas de polígono.</span><span class="sxs-lookup"><span data-stu-id="9c983-116">Quadrics are rendered with polygon primitives.</span></span> <span data-ttu-id="9c983-117">Os polígonos são desenhados em um sentido anti-horário com relação aos seus normais (conforme definido com [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="9c983-117">The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span><br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <span data-ttu-id="9c983-118"><dt>**GLU \_ linha**</dt></span><span class="sxs-lookup"><span data-stu-id="9c983-118"><dt>**GLU\_LINE**</dt></span></span> </dl>                   | <span data-ttu-id="9c983-119">Quadrics são renderizados como um conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="9c983-119">Quadrics are rendered as a set of lines.</span></span><br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <span data-ttu-id="9c983-120"><dt>**silhueta de GLU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c983-120"><dt>**GLU\_SILHOUETTE**</dt></span></span> </dl> | <span data-ttu-id="9c983-121">Quadrics são renderizados como um conjunto de linhas, exceto que as bordas que separam rostos de coplanar não serão desenhadas.</span><span class="sxs-lookup"><span data-stu-id="9c983-121">Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.</span></span><br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <span data-ttu-id="9c983-122"><dt>**ponto de GLU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9c983-122"><dt>**GLU\_POINT**</dt></span></span> </dl>                | <span data-ttu-id="9c983-123">Quadrics são renderizados como um conjunto de pontos.</span><span class="sxs-lookup"><span data-stu-id="9c983-123">Quadrics are rendered as a set of points.</span></span><br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c983-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c983-124">Return value</span></span>

<span data-ttu-id="9c983-125">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9c983-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c983-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c983-126">Remarks</span></span>

<span data-ttu-id="9c983-127">A função **gluQuadricDrawStyle** especifica o estilo de desenho para quadrics renderizado com o **quadobject**.</span><span class="sxs-lookup"><span data-stu-id="9c983-127">The **gluQuadricDrawStyle** function specifies the draw style for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c983-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c983-128">Requirements</span></span>



| <span data-ttu-id="9c983-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c983-129">Requirement</span></span> | <span data-ttu-id="9c983-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9c983-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c983-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c983-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9c983-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c983-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9c983-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c983-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9c983-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c983-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9c983-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9c983-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c983-136"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c983-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9c983-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c983-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="9c983-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c983-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9c983-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9c983-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c983-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c983-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c983-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c983-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c983-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="9c983-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="9c983-143">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="9c983-143">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="9c983-144">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="9c983-144">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="9c983-145">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="9c983-145">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





