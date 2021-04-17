---
title: função gluCylinder (Glu. h)
description: A função gluCylinder desenha um cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- função gluCylinder OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755976"
---
# <a name="glucylinder-function"></a><span data-ttu-id="1e4bd-104">função gluCylinder</span><span class="sxs-lookup"><span data-stu-id="1e4bd-104">gluCylinder function</span></span>

<span data-ttu-id="1e4bd-105">A função **gluCylinder** desenha um cilindro.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-105">The **gluCylinder** function draws a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e4bd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e4bd-106">Syntax</span></span>


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="1e4bd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e4bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e4bd-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="1e4bd-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4bd-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="1e4bd-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1e4bd-110">*baseRadius*</span><span class="sxs-lookup"><span data-stu-id="1e4bd-110">*baseRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4bd-111">O raio do cilindro em *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-111">The radius of the cylinder at *z* = 0.</span></span>

</dd> <dt>

<span data-ttu-id="1e4bd-112">*topRadius*</span><span class="sxs-lookup"><span data-stu-id="1e4bd-112">*topRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4bd-113">O raio do cilindro em altura *z*  =  .</span><span class="sxs-lookup"><span data-stu-id="1e4bd-113">The radius of the cylinder at *z* = *height*.</span></span>

</dd> <dt>

<span data-ttu-id="1e4bd-114">*altura*</span><span class="sxs-lookup"><span data-stu-id="1e4bd-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4bd-115">A altura do cilindro.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-115">The height of the cylinder.</span></span>

</dd> <dt>

<span data-ttu-id="1e4bd-116">*fatia*</span><span class="sxs-lookup"><span data-stu-id="1e4bd-116">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4bd-117">O número de subdivisãos em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-117">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1e4bd-118">*pilhas*</span><span class="sxs-lookup"><span data-stu-id="1e4bd-118">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="1e4bd-119">O número de subdivisãos ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-119">The number of subdivisions along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e4bd-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e4bd-120">Return value</span></span>

<span data-ttu-id="1e4bd-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e4bd-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e4bd-122">Remarks</span></span>

<span data-ttu-id="1e4bd-123">A função **gluCylinder** desenha um cilindro orientado ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-123">The **gluCylinder** function draws a cylinder oriented along the z-axis.</span></span> <span data-ttu-id="1e4bd-124">A base do cilindro é colocada em *z* = 0, e a altura da parte superior em *z*  =  .</span><span class="sxs-lookup"><span data-stu-id="1e4bd-124">The base of the cylinder is placed at *z* = 0, and the top at *z* = *height*.</span></span> <span data-ttu-id="1e4bd-125">Como uma esfera, um cilindro é subdividido em torno do eixo z em fatias e, ao longo do eixo z, em pilhas.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-125">Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.</span></span>

<span data-ttu-id="1e4bd-126">Observe que, se *topRadius* for definido como zero, essa rotina irá gerar um cone.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-126">Note that if *topRadius* is set to zero, then this routine will generate a cone.</span></span>

<span data-ttu-id="1e4bd-127">Se a orientação for definida como GLU \_ externamente (com [**gluQuadricOrientation**](gluquadricorientation.md)), então todos os Normals gerados apontarão do eixo z.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-127">If the orientation is set to GLU\_OUTSIDE (with [**gluQuadricOrientation**](gluquadricorientation.md)), then any generated normals point away from the z-axis.</span></span> <span data-ttu-id="1e4bd-128">Caso contrário, eles apontam para o eixo z.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-128">Otherwise, they point toward the z-axis.</span></span>

<span data-ttu-id="1e4bd-129">Se texturing estiver ativado (com [**gluQuadricTexture**](gluquadrictexture.md)): coordenadas de textura são geradas para que *t* se torne linearmente de 0,0 a *z* = 0 a 1,0 a *z*  =  *Height*; e *s* varia de 0,0 no eixo y positivo, até 0,25 no eixo x positivo, para 0,5 no eixo y negativo, para 0,75 no eixo x negativo e de volta para 1,0 no eixo y positivo.</span><span class="sxs-lookup"><span data-stu-id="1e4bd-129">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)): texture coordinates are generated so that *t* ranges linearly from 0.0 at *z* = 0 to 1.0 at *z* = *height*; and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4bd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e4bd-130">Requirements</span></span>



| <span data-ttu-id="1e4bd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e4bd-131">Requirement</span></span> | <span data-ttu-id="1e4bd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1e4bd-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4bd-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e4bd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1e4bd-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e4bd-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1e4bd-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e4bd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1e4bd-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e4bd-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1e4bd-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1e4bd-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e4bd-138"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4bd-138"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1e4bd-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e4bd-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e4bd-140"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e4bd-140"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e4bd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1e4bd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e4bd-142"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e4bd-142"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e4bd-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e4bd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4bd-144">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="1e4bd-144">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="1e4bd-145">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="1e4bd-145">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="1e4bd-146">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="1e4bd-146">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="1e4bd-147">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="1e4bd-147">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="1e4bd-148">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="1e4bd-148">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="1e4bd-149">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="1e4bd-149">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





