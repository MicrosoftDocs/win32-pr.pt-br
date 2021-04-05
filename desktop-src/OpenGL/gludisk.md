---
title: função gluDisk (Glu. h)
description: A função gluDisk desenha um disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- função gluDisk OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009336"
---
# <a name="gludisk-function"></a><span data-ttu-id="4c9a6-104">função gluDisk</span><span class="sxs-lookup"><span data-stu-id="4c9a6-104">gluDisk function</span></span>

<span data-ttu-id="4c9a6-105">A função **gluDisk** desenha um disco.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-105">The **gluDisk** function draws a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9a6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c9a6-106">Syntax</span></span>


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a><span data-ttu-id="4c9a6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c9a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c9a6-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="4c9a6-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="4c9a6-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="4c9a6-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="4c9a6-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="4c9a6-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="4c9a6-111">O raio interno do disco (pode ser zero).</span><span class="sxs-lookup"><span data-stu-id="4c9a6-111">The inner radius of the disk (may be zero).</span></span>

</dd> <dt>

<span data-ttu-id="4c9a6-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="4c9a6-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="4c9a6-113">O raio externo do disco.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-113">The outer radius of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="4c9a6-114">*fatia*</span><span class="sxs-lookup"><span data-stu-id="4c9a6-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="4c9a6-115">O número de subdivisãos em volta do eixo z.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="4c9a6-116">*loops*</span><span class="sxs-lookup"><span data-stu-id="4c9a6-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="4c9a6-117">O número de anéis concêntricos sobre a origem na qual o disco é subdividido.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-117">The number of concentric rings about the origin into which the disk is subdivided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c9a6-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c9a6-118">Return value</span></span>

<span data-ttu-id="4c9a6-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c9a6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c9a6-120">Remarks</span></span>

<span data-ttu-id="4c9a6-121">A função **gluDisk** renderiza um disco no plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-121">The **gluDisk** function renders a disk on the *z* = 0 plane.</span></span> <span data-ttu-id="4c9a6-122">O disco tem um raio de *outerRadius* e contém um buraco circular concêntrico com um raio de *innerRadius*.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-122">The disk has a radius of *outerRadius*, and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="4c9a6-123">Se *innerRadius* for 0, nenhum orifício será gerado.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-123">If *innerRadius* is 0, then no hole is generated.</span></span> <span data-ttu-id="4c9a6-124">O disco é subdividido em torno do eixo z em fatias (como fatias de pizza) e também sobre o eixo z em anéis (conforme especificado por *fatias* e *loops*, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="4c9a6-124">The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="4c9a6-125">Em relação à orientação, o lado *z* positivo do disco é considerado *fora* (consulte [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="4c9a6-125">With respect to orientation, the positive *z*-side of the disk is considered to be *outside* (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="4c9a6-126">Isso significa que, se a orientação for definida como GLU \_ externamente, qualquer normal gerado apontará ao longo do eixo z positivo.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-126">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="4c9a6-127">Se texturing estiver ativado (com [**gluQuadricTexture**](gluquadrictexture.md)), as coordenadas de textura serão geradas linearmente, de onde *r*  =  *outerRadius*, o valor em (*r*, 0, 0) é (1, 0,5); at (0, *r*, 0) é (0,5, 1); at (-*r*, 0, 0) é (0, 0,5); e at (0,-*r*, 0) é (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="4c9a6-127">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)), texture coordinates are generated linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (-*r*, 0, 0) it is (0, 0.5); and at (0, -*r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c9a6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c9a6-128">Requirements</span></span>



| <span data-ttu-id="4c9a6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c9a6-129">Requirement</span></span> | <span data-ttu-id="4c9a6-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4c9a6-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9a6-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c9a6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c9a6-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c9a6-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4c9a6-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c9a6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c9a6-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c9a6-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4c9a6-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4c9a6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c9a6-136"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9a6-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="4c9a6-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c9a6-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c9a6-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c9a6-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4c9a6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4c9a6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c9a6-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c9a6-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9a6-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c9a6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9a6-142">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="4c9a6-142">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="4c9a6-143">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="4c9a6-143">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="4c9a6-144">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="4c9a6-144">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="4c9a6-145">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="4c9a6-145">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="4c9a6-146">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="4c9a6-146">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="4c9a6-147">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="4c9a6-147">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





