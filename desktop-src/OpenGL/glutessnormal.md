---
title: função gluTessNormal (Glu. h)
description: A função gluTessNormal especifica um normal para um polígono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- função gluTessNormal OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919056"
---
# <a name="glutessnormal-function"></a><span data-ttu-id="01389-104">função gluTessNormal</span><span class="sxs-lookup"><span data-stu-id="01389-104">gluTessNormal function</span></span>

<span data-ttu-id="01389-105">A função **gluTessNormal** especifica um normal para um polígono.</span><span class="sxs-lookup"><span data-stu-id="01389-105">The **gluTessNormal** function specifies a normal for a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="01389-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01389-106">Syntax</span></span>


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a><span data-ttu-id="01389-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01389-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01389-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="01389-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="01389-109">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="01389-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="01389-110">*x*</span><span class="sxs-lookup"><span data-stu-id="01389-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="01389-111">O componente de coordenada x de um normal.</span><span class="sxs-lookup"><span data-stu-id="01389-111">The x-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="01389-112">*y*</span><span class="sxs-lookup"><span data-stu-id="01389-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="01389-113">O componente de coordenada y de um normal.</span><span class="sxs-lookup"><span data-stu-id="01389-113">The y-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="01389-114">*z*</span><span class="sxs-lookup"><span data-stu-id="01389-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="01389-115">O componente de coordenada z de um normal.</span><span class="sxs-lookup"><span data-stu-id="01389-115">The z-coordinate component of a normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01389-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01389-116">Return value</span></span>

<span data-ttu-id="01389-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="01389-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01389-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="01389-118">Remarks</span></span>

<span data-ttu-id="01389-119">A função **gluTessNormal** descreve um normal para um polígono que você define.</span><span class="sxs-lookup"><span data-stu-id="01389-119">The **gluTessNormal** function describes a normal for a polygon that you define.</span></span> <span data-ttu-id="01389-120">Todos os dados de entrada são projetados em um plano perpendicular a um dos três eixos de coordenadas antes do mosaico, e todos os triângulos de saída são orientados no sentido anti-horário com relação ao normal.</span><span class="sxs-lookup"><span data-stu-id="01389-120">All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal.</span></span> <span data-ttu-id="01389-121">(Para obter a orientação no sentido horário, inverta o sinal do normal fornecido).</span><span class="sxs-lookup"><span data-stu-id="01389-121">(To obtain clockwise orientation, reverse the sign of the supplied normal).</span></span> <span data-ttu-id="01389-122">Por exemplo, se você souber que todos os polígonos estão no plano x-y, chame **gluTessNormal**(tess, 0,0, 0,0, 1,0) antes de renderizar quaisquer polígonos.</span><span class="sxs-lookup"><span data-stu-id="01389-122">For example, if you know that all polygons lie in the x-y plane, call **gluTessNormal**(tess, 0.0, 0.0, 1.0) before rendering any polygons.</span></span>

<span data-ttu-id="01389-123">Se o normal fornecido for (0,0, 0,0, 0,0) (o valor padrão), o normal será determinado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="01389-123">If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:</span></span>

1.  <span data-ttu-id="01389-124">A direção do normal, até o sinal, é encontrada ao ajustar um plano aos vértices, sem considerar como os vértices estão conectados.</span><span class="sxs-lookup"><span data-stu-id="01389-124">The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected.</span></span> <span data-ttu-id="01389-125">Espera-se que os dados de entrada estejam aproximadamente no plano; caso contrário, a projeção perpendicular a um dos três eixos de coordenadas pode alterar a geometria substancialmente.</span><span class="sxs-lookup"><span data-stu-id="01389-125">It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</span></span>
2.  <span data-ttu-id="01389-126">O sinal do normal é escolhido para que a soma das áreas assinadas de todos os contornos de entrada seja não negativa (onde uma delimitação no sentido anti-horário tem uma área positiva).</span><span class="sxs-lookup"><span data-stu-id="01389-126">The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</span></span>

<span data-ttu-id="01389-127">O normal é mantido até que outra chamada para **gluTessNormal** o altere.</span><span class="sxs-lookup"><span data-stu-id="01389-127">The supplied normal persists until another call to **gluTessNormal** changes it.</span></span>

## <a name="requirements"></a><span data-ttu-id="01389-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01389-128">Requirements</span></span>



| <span data-ttu-id="01389-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="01389-129">Requirement</span></span> | <span data-ttu-id="01389-130">Valor</span><span class="sxs-lookup"><span data-stu-id="01389-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="01389-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01389-131">Minimum supported client</span></span><br/> | <span data-ttu-id="01389-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01389-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="01389-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01389-133">Minimum supported server</span></span><br/> | <span data-ttu-id="01389-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="01389-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="01389-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="01389-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="01389-136"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="01389-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="01389-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01389-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="01389-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01389-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="01389-139">DLL</span><span class="sxs-lookup"><span data-stu-id="01389-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01389-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01389-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01389-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="01389-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01389-142">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="01389-142">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="01389-143">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="01389-143">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="01389-144">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="01389-144">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> </dl>

 

 





