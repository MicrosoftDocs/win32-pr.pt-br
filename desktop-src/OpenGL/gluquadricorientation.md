---
title: função gluQuadricOrientation (Glu. h)
description: A função gluQuadricOrientation especifica a orientação interna ou externa para quadrics.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- função gluQuadricOrientation OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644222"
---
# <a name="gluquadricorientation-function"></a><span data-ttu-id="1bc39-104">função gluQuadricOrientation</span><span class="sxs-lookup"><span data-stu-id="1bc39-104">gluQuadricOrientation function</span></span>

<span data-ttu-id="1bc39-105">A função **gluQuadricOrientation** especifica a orientação interna ou externa para quadrics.</span><span class="sxs-lookup"><span data-stu-id="1bc39-105">The **gluQuadricOrientation** function specifies inside or outside orientation for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc39-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1bc39-106">Syntax</span></span>


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a><span data-ttu-id="1bc39-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bc39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc39-108">*quádruplo*</span><span class="sxs-lookup"><span data-stu-id="1bc39-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc39-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="1bc39-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1bc39-110">*orientation*</span><span class="sxs-lookup"><span data-stu-id="1bc39-110">*orientation*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc39-111">A orientação desejada.</span><span class="sxs-lookup"><span data-stu-id="1bc39-111">The desired orientation.</span></span> <span data-ttu-id="1bc39-112">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="1bc39-112">The following values are valid.</span></span>



| <span data-ttu-id="1bc39-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1bc39-113">Value</span></span>                                                                                                                                                   | <span data-ttu-id="1bc39-114">Significado</span><span class="sxs-lookup"><span data-stu-id="1bc39-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <span data-ttu-id="1bc39-115"><dt>**GLU \_ fora de lugar**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc39-115"><dt>**GLU\_OUTSIDE**</dt></span></span> </dl> | <span data-ttu-id="1bc39-116">Desenhe quadrics com normais apontando para fora.</span><span class="sxs-lookup"><span data-stu-id="1bc39-116">Draw quadrics with normals pointing outward.</span></span> <span data-ttu-id="1bc39-117">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1bc39-117">This is the default value.</span></span><br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <span data-ttu-id="1bc39-118"><dt>**GLU \_ dentro**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc39-118"><dt>**GLU\_INSIDE**</dt></span></span> </dl>    | <span data-ttu-id="1bc39-119">Desenhe quadrics com normais apontando para dentro.</span><span class="sxs-lookup"><span data-stu-id="1bc39-119">Draw quadrics with normals pointing inward.</span></span><br/>                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc39-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1bc39-120">Return value</span></span>

<span data-ttu-id="1bc39-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1bc39-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bc39-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bc39-122">Remarks</span></span>

<span data-ttu-id="1bc39-123">A função **gluQuadricOrientation** especifica que tipo de orientação é desejado para quadrics renderizado com o **quádruploobject**.</span><span class="sxs-lookup"><span data-stu-id="1bc39-123">The **gluQuadricOrientation** function specifies what kind of orientation is desired for quadrics rendered with **quadObject**.</span></span> <span data-ttu-id="1bc39-124">A interpretação de fora e para dentro depende do Quadric que está sendo desenhado.</span><span class="sxs-lookup"><span data-stu-id="1bc39-124">The interpretation of outward and inward depends on the quadric being drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc39-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bc39-125">Requirements</span></span>



| <span data-ttu-id="1bc39-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bc39-126">Requirement</span></span> | <span data-ttu-id="1bc39-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1bc39-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc39-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc39-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc39-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1bc39-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1bc39-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bc39-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc39-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1bc39-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1bc39-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1bc39-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bc39-133"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bc39-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1bc39-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1bc39-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="1bc39-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bc39-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1bc39-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1bc39-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bc39-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bc39-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bc39-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bc39-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc39-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="1bc39-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="1bc39-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="1bc39-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="1bc39-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="1bc39-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="1bc39-142">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="1bc39-142">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





