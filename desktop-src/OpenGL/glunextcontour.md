---
title: função gluNextContour (Glu. h)
description: A função gluNextContour marca o início de outra delimitação.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- função gluNextContour OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369412"
---
# <a name="glunextcontour-function"></a><span data-ttu-id="010e6-104">função gluNextContour</span><span class="sxs-lookup"><span data-stu-id="010e6-104">gluNextContour function</span></span>

<span data-ttu-id="010e6-105">\[A função **gluNextContour** é obsoleta e é fornecida somente para fins de compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="010e6-105">\[The **gluNextContour** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="010e6-106">A função **gluNextContour** é mapeada para [**GluTessEndContour**](glutessendcontour.md) seguida por [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="010e6-106">The **gluNextContour** function is mapped to [**gluTessEndContour**](glutessendcontour.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="010e6-107">A função **gluNextContour** marca o início de outra delimitação.</span><span class="sxs-lookup"><span data-stu-id="010e6-107">The **gluNextContour** function marks the beginning of another contour.</span></span>

## <a name="syntax"></a><span data-ttu-id="010e6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="010e6-108">Syntax</span></span>


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a><span data-ttu-id="010e6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="010e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010e6-110">*tess*</span><span class="sxs-lookup"><span data-stu-id="010e6-110">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="010e6-111">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="010e6-111">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="010e6-112">*tipo*</span><span class="sxs-lookup"><span data-stu-id="010e6-112">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="010e6-113">O tipo da delimitação que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="010e6-113">The type of the contour being defined.</span></span> <span data-ttu-id="010e6-114">Os valores a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="010e6-114">The following values are valid.</span></span>



| <span data-ttu-id="010e6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="010e6-115">Value</span></span>                                                                                                                                                                | <span data-ttu-id="010e6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="010e6-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <span data-ttu-id="010e6-117"><dt>**\_exterior Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="010e6-117"><dt>**GLU\_EXTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="010e6-118">Uma delimitação exterior define um limite exterior do polígono.</span><span class="sxs-lookup"><span data-stu-id="010e6-118">An exterior contour defines an exterior boundary of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <span data-ttu-id="010e6-119"><dt>**GLU \_ interior**</dt></span><span class="sxs-lookup"><span data-stu-id="010e6-119"><dt>**GLU\_INTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="010e6-120">Uma delimitação interior define um limite interior do polígono (como uma brecha).</span><span class="sxs-lookup"><span data-stu-id="010e6-120">An interior contour defines an interior boundary of the polygon (such as a hole).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <span data-ttu-id="010e6-121"><dt>**GLU \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="010e6-121"><dt>**GLU\_UNKNOWN**</dt></span></span> </dl>              | <span data-ttu-id="010e6-122">Uma delimitação desconhecida é analisada pela biblioteca para determinar se ela é interior ou exterior.</span><span class="sxs-lookup"><span data-stu-id="010e6-122">An unknown contour is analyzed by the library to determine whether it is interior or exterior.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <span data-ttu-id="010e6-123"><dt>**GLU \_ CCW, glu \_ CW**</dt></span><span class="sxs-lookup"><span data-stu-id="010e6-123"><dt>**GLU\_CCW, GLU\_CW**</dt></span></span> </dl> | <span data-ttu-id="010e6-124">A primeira \_ contorno Glu CCW ou Glu \_ CW definida é considerada exterior.</span><span class="sxs-lookup"><span data-stu-id="010e6-124">The first GLU\_CCW or GLU\_CW contour defined is considered to be exterior.</span></span> <span data-ttu-id="010e6-125">Todas as outras contornos serão consideradas exteriores se forem orientadas na mesma direção (no sentido horário ou anti-horário) como a primeira contorno e interior se não forem.</span><span class="sxs-lookup"><span data-stu-id="010e6-125">All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.</span></span><br/> <span data-ttu-id="010e6-126">Se uma delimitação for do tipo GLU \_ CCW ou Glu \_ CW, todos os contornos deverão ser do mesmo tipo (se não forem, todos os Glu \_ CCW e Glu \_ contornos em PV serão alterados para Glu \_ desconhecido).</span><span class="sxs-lookup"><span data-stu-id="010e6-126">If one contour is of type GLU\_CCW or GLU\_CW, then all contours must be of the same type (if they are not, then all GLU\_CCW and GLU\_CW contours will be changed to GLU\_UNKNOWN).</span></span> <span data-ttu-id="010e6-127">Observe que não há nenhuma diferença real entre os \_ tipos de contorno Glu CCW e Glu \_ CW.</span><span class="sxs-lookup"><span data-stu-id="010e6-127">Note that there is no real difference between the GLU\_CCW and GLU\_CW contour types.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="010e6-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="010e6-128">Return value</span></span>

<span data-ttu-id="010e6-129">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="010e6-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="010e6-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="010e6-130">Remarks</span></span>

<span data-ttu-id="010e6-131">Use a função **gluNextContour** para descrever polígonos com vários contornos.</span><span class="sxs-lookup"><span data-stu-id="010e6-131">Use the **gluNextContour** function to describe polygons with multiple contours.</span></span> <span data-ttu-id="010e6-132">Depois de descrever a primeira delimitação por meio de uma série de chamadas [**gluTessVertex**](glutessvertex.md) , uma chamada **gluNextContour** indica que a delimitação anterior foi concluída e que a próxima delimitação está prestes a começar.</span><span class="sxs-lookup"><span data-stu-id="010e6-132">After you describe the first contour through a series of [**gluTessVertex**](glutessvertex.md) calls, a **gluNextContour** call indicates that the previous contour is complete and that the next contour is about to begin.</span></span> <span data-ttu-id="010e6-133">Execute outra série de chamadas **gluTessVertex** para descrever a nova delimitação.</span><span class="sxs-lookup"><span data-stu-id="010e6-133">Perform another series of **gluTessVertex** calls to describe the new contour.</span></span> <span data-ttu-id="010e6-134">Repita esse processo até que todos os contornos tenham sido descritos.</span><span class="sxs-lookup"><span data-stu-id="010e6-134">Repeat this process until all contours have been described.</span></span>

<span data-ttu-id="010e6-135">O parâmetro de *tipo* define o tipo de delimitação a seguir.</span><span class="sxs-lookup"><span data-stu-id="010e6-135">The *type* parameter defines what type of contour follows.</span></span>

<span data-ttu-id="010e6-136">Para definir o tipo da primeira delimitação, você pode chamar **gluNextContour** antes de descrever a primeira delimitação.</span><span class="sxs-lookup"><span data-stu-id="010e6-136">To define the type of the first contour, you can call **gluNextContour** before describing the first contour.</span></span> <span data-ttu-id="010e6-137">Se você não chamar **gluNextContour** antes da primeira delimitação, a primeira delimitação será marcada como \_ exterior Glu.</span><span class="sxs-lookup"><span data-stu-id="010e6-137">If you do not call **gluNextContour** before the first contour, the first contour is marked GLU\_EXTERIOR.</span></span>

## <a name="examples"></a><span data-ttu-id="010e6-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="010e6-138">Examples</span></span>

<span data-ttu-id="010e6-139">Você pode descrever um diamante com um buraco triangular, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="010e6-139">You can describe a quadrilateral with a triangular hole in it as follows:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="010e6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="010e6-140">Requirements</span></span>



| <span data-ttu-id="010e6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="010e6-141">Requirement</span></span> | <span data-ttu-id="010e6-142">Valor</span><span class="sxs-lookup"><span data-stu-id="010e6-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="010e6-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010e6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="010e6-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="010e6-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="010e6-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="010e6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="010e6-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="010e6-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="010e6-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="010e6-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="010e6-148"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="010e6-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="010e6-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="010e6-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="010e6-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="010e6-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="010e6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="010e6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="010e6-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="010e6-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010e6-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="010e6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010e6-154">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="010e6-154">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="010e6-155">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="010e6-155">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="010e6-156">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="010e6-156">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="010e6-157">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="010e6-157">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="010e6-158">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="010e6-158">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="010e6-159">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="010e6-159">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





