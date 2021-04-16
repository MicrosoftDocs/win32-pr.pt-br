---
title: função gluSphere (Glu. h)
description: A função gluSphere desenha uma esfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- função gluSphere OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455579"
---
# <a name="glusphere-function"></a><span data-ttu-id="9dd31-104">função gluSphere</span><span class="sxs-lookup"><span data-stu-id="9dd31-104">gluSphere function</span></span>

<span data-ttu-id="9dd31-105">A função **gluSphere** desenha uma esfera.</span><span class="sxs-lookup"><span data-stu-id="9dd31-105">The **gluSphere** function draws a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd31-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9dd31-106">Syntax</span></span>


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="9dd31-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9dd31-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd31-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="9dd31-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="9dd31-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="9dd31-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9dd31-110">*radiano*</span><span class="sxs-lookup"><span data-stu-id="9dd31-110">*radius*</span></span> 
</dt> <dd>

<span data-ttu-id="9dd31-111">O raio da esfera.</span><span class="sxs-lookup"><span data-stu-id="9dd31-111">The radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="9dd31-112">*fatia*</span><span class="sxs-lookup"><span data-stu-id="9dd31-112">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="9dd31-113">O número de subdivisãos em volta do eixo z (semelhante às linhas de longitude).</span><span class="sxs-lookup"><span data-stu-id="9dd31-113">The number of subdivisions around the z-axis (similar to lines of longitude).</span></span>

</dd> <dt>

<span data-ttu-id="9dd31-114">*pilhas*</span><span class="sxs-lookup"><span data-stu-id="9dd31-114">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="9dd31-115">O número de subdivisãos ao longo do eixo z (semelhante às linhas de latitude).</span><span class="sxs-lookup"><span data-stu-id="9dd31-115">The number of subdivisions along the z-axis (similar to lines of latitude).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd31-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9dd31-116">Return value</span></span>

<span data-ttu-id="9dd31-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9dd31-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd31-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dd31-118">Remarks</span></span>

<span data-ttu-id="9dd31-119">A função **gluSphere** desenha uma esfera do raio determinado centralizado em relação à origem.</span><span class="sxs-lookup"><span data-stu-id="9dd31-119">The **gluSphere** function draws a sphere of the given radius centered around the origin.</span></span> <span data-ttu-id="9dd31-120">A esfera é subdividida em torno do eixo z em fatias e ao longo do eixo z em pilhas (semelhante às linhas de longitude e latitude).</span><span class="sxs-lookup"><span data-stu-id="9dd31-120">The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).</span></span>

<span data-ttu-id="9dd31-121">Se a orientação for definida como GLU \_ fora (com **gluQuadricOrientation**), qualquer normal gerado apontará para fora do centro da esfera.</span><span class="sxs-lookup"><span data-stu-id="9dd31-121">If the orientation is set to GLU\_OUTSIDE (with **gluQuadricOrientation**), any normals generated point away from the center of the sphere.</span></span> <span data-ttu-id="9dd31-122">Caso contrário, eles apontam para o centro da esfera.</span><span class="sxs-lookup"><span data-stu-id="9dd31-122">Otherwise, they point toward the center of the sphere.</span></span>

<span data-ttu-id="9dd31-123">Se texturing estiver ativado (com **gluQuadricTexture**): coordenadas de textura são geradas para *que t* varie de 0,0 a *z* =-*RADIUS* para 1,0 a *z*  =  *RADIUS* (*t* aumenta linearmente ao longo das linhas longitudinal); e *s* varia de 0,0 no eixo y positivo, até 0,25, no eixo x positivo, para 0,5 no eixo y negativo, para 0,75 no eixo x negativo, e de volta para 1,0 no eixo y positivo do.</span><span class="sxs-lookup"><span data-stu-id="9dd31-123">If texturing is turned on (with **gluQuadricTexture**): texture coordinates are generated so that *t* ranges from 0.0 at *z* = -*radius* to 1.0 at *z* = *radius* (*t* increases linearly along longitudinal lines); and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd31-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dd31-124">Requirements</span></span>



| <span data-ttu-id="9dd31-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd31-125">Requirement</span></span> | <span data-ttu-id="9dd31-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9dd31-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd31-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dd31-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd31-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9dd31-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9dd31-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9dd31-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd31-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9dd31-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9dd31-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9dd31-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dd31-132"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd31-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9dd31-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9dd31-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9dd31-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dd31-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9dd31-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9dd31-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dd31-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dd31-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dd31-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dd31-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd31-138">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="9dd31-138">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="9dd31-139">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="9dd31-139">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="9dd31-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="9dd31-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="9dd31-141">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="9dd31-141">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="9dd31-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="9dd31-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="9dd31-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="9dd31-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





