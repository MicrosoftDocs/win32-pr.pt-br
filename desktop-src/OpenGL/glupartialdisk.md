---
title: função gluPartialDisk (Glu. h)
description: A função gluPartialDisk desenha um arco de um disco.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- função gluPartialDisk OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754137"
---
# <a name="glupartialdisk-function"></a><span data-ttu-id="743f5-104">função gluPartialDisk</span><span class="sxs-lookup"><span data-stu-id="743f5-104">gluPartialDisk function</span></span>

<span data-ttu-id="743f5-105">A função **gluPartialDisk** desenha um arco de um disco.</span><span class="sxs-lookup"><span data-stu-id="743f5-105">The **gluPartialDisk** function draws an arc of a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="743f5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="743f5-106">Syntax</span></span>


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a><span data-ttu-id="743f5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="743f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="743f5-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="743f5-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="743f5-109">Um objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="743f5-109">A quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="743f5-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="743f5-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="743f5-111">O raio interno do disco parcial (pode ser zero).</span><span class="sxs-lookup"><span data-stu-id="743f5-111">The inner radius of the partial disk (can be zero).</span></span>

</dd> <dt>

<span data-ttu-id="743f5-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="743f5-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="743f5-113">O raio externo do disco parcial.</span><span class="sxs-lookup"><span data-stu-id="743f5-113">The outer radius of the partial disk.</span></span>

</dd> <dt>

<span data-ttu-id="743f5-114">*fatia*</span><span class="sxs-lookup"><span data-stu-id="743f5-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="743f5-115">O número de subdivisãos em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="743f5-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="743f5-116">*loops*</span><span class="sxs-lookup"><span data-stu-id="743f5-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="743f5-117">O número de anéis concêntricos sobre a origem na qual o disco parcial é subdividido.</span><span class="sxs-lookup"><span data-stu-id="743f5-117">The number of concentric rings about the origin into which the partial disk is subdivided.</span></span>

</dd> <dt>

<span data-ttu-id="743f5-118">*startAngle*</span><span class="sxs-lookup"><span data-stu-id="743f5-118">*startAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="743f5-119">O ângulo inicial, em graus, da parte do disco.</span><span class="sxs-lookup"><span data-stu-id="743f5-119">The starting angle, in degrees, of the disk portion.</span></span>

</dd> <dt>

<span data-ttu-id="743f5-120">*sweepAngle*</span><span class="sxs-lookup"><span data-stu-id="743f5-120">*sweepAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="743f5-121">O ângulo de flecha, em graus, da parte do disco.</span><span class="sxs-lookup"><span data-stu-id="743f5-121">The sweep angle, in degrees, of the disk portion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="743f5-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="743f5-122">Return value</span></span>

<span data-ttu-id="743f5-123">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="743f5-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="743f5-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="743f5-124">Remarks</span></span>

<span data-ttu-id="743f5-125">A função **gluPartialDisk** renderiza um disco parcial no plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="743f5-125">The **gluPartialDisk** function renders a partial disk on the *z* = 0 plane.</span></span> <span data-ttu-id="743f5-126">Um disco parcial é semelhante a um disco cheio, exceto pelo fato de que apenas o subconjunto do disco de *StartAngle* até *StartAngle*  +  *SweepAngle* está incluído (onde 0 graus está ao longo do eixo y positivo, 90 graus é ao longo do eixo x positivo, 180 graus é ao longo do eixo y negativo e 270 graus está ao longo do eixo x negativo).</span><span class="sxs-lookup"><span data-stu-id="743f5-126">A partial disk is similar to a full disk, except that only the subset of the disk from *startAngle* through *startAngle* + *sweepAngle* is included (where 0 degrees is along the positive y-axis, 90 degrees is along the positive x-axis, 180 degrees is along the negative y-axis, and 270 degrees is along the negative x-axis).</span></span>

<span data-ttu-id="743f5-127">O disco parcial tem um raio de *outerRadius* e contém um buraco circular concêntrico com um raio de *innerRadius*.</span><span class="sxs-lookup"><span data-stu-id="743f5-127">The partial disk has a radius of *outerRadius* and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="743f5-128">Se *innerRadius* for zero, nenhum buraco será gerado.</span><span class="sxs-lookup"><span data-stu-id="743f5-128">If *innerRadius* is zero, then no hole is generated.</span></span> <span data-ttu-id="743f5-129">O disco parcial é subdividido em torno do eixo z em fatias (como fatias de pizza) e também sobre o eixo z em anéis (conforme especificado por *fatias* e *loops*, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="743f5-129">The partial disk is subdivided around the z-axis into slices (like pizza slices), and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="743f5-130">Em relação à orientação, o lado z positivo do disco parcial é considerado fora (consulte [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="743f5-130">With respect to orientation, the positive z-side of the partial disk is considered to be outside (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="743f5-131">Isso significa que, se a orientação for definida como GLU \_ externamente, qualquer normal gerado apontará ao longo do eixo z positivo.</span><span class="sxs-lookup"><span data-stu-id="743f5-131">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="743f5-132">Se você tiver ativado texturing (com [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** gerará coordenadas de textura linearmente, de modo que, em que em *r*  =  *outerRadius*, o valor em (*r*, 0, 0) é (1, 0,5); at (0, *r*, 0) é (0,5, 1); at (*r*, 0, 0) é (0, 0,5); e at (0, *r*, 0) é (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="743f5-132">If you have turned on texturing (with [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** generates texture coordinates linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="743f5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="743f5-133">Requirements</span></span>



| <span data-ttu-id="743f5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="743f5-134">Requirement</span></span> | <span data-ttu-id="743f5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="743f5-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="743f5-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="743f5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="743f5-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="743f5-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="743f5-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="743f5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="743f5-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="743f5-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="743f5-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="743f5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="743f5-141"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="743f5-141"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="743f5-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="743f5-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="743f5-143"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="743f5-143"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="743f5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="743f5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="743f5-145"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="743f5-145"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="743f5-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="743f5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743f5-147">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="743f5-147">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="743f5-148">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="743f5-148">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="743f5-149">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="743f5-149">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="743f5-150">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="743f5-150">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="743f5-151">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="743f5-151">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="743f5-152">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="743f5-152">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





