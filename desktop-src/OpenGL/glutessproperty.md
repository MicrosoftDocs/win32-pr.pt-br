---
title: função gluTessProperty (Glu. h)
description: A função gluTessProperty define a propriedade de um objeto de mosaico.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- função gluTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086295"
---
# <a name="glutessproperty-function"></a><span data-ttu-id="9485b-104">função gluTessProperty</span><span class="sxs-lookup"><span data-stu-id="9485b-104">gluTessProperty function</span></span>

<span data-ttu-id="9485b-105">A função **gluTessProperty** define a propriedade de um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="9485b-105">The **gluTessProperty** function sets the property of a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9485b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9485b-106">Syntax</span></span>


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a><span data-ttu-id="9485b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9485b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9485b-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="9485b-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="9485b-109">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="9485b-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9485b-110">*Onde*</span><span class="sxs-lookup"><span data-stu-id="9485b-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="9485b-111">O valor da propriedade a ser definido.</span><span class="sxs-lookup"><span data-stu-id="9485b-111">The property value to set.</span></span> <span data-ttu-id="9485b-112">Os seguintes valores são válidos: GLU \_ Tess \_ rebobination \_ Rule, glu \_ Tess \_ limite e a \_ \_ tolerância Glu Tess \_ .</span><span class="sxs-lookup"><span data-stu-id="9485b-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>



| <span data-ttu-id="9485b-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9485b-113">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="9485b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9485b-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <span data-ttu-id="9485b-115"><dt>**\_regra de \_ contorno de Tess Glu \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9485b-115"><dt>**GLU\_TESS\_WINDING\_RULE**</dt></span></span> </dl>    | <span data-ttu-id="9485b-116">Determina quais partes do polígono estão no interior.</span><span class="sxs-lookup"><span data-stu-id="9485b-116">Determines which parts of the polygon are on the interior.</span></span> <span data-ttu-id="9485b-117">O parâmetro de valor pode ser definido como um dos seguintes: GLU \_ Tess \_ enventor \_ Odd, glu \_ Tess \_ enrolamento \_ diferente de zero, glu \_ Tess de \_ entorno \_ positivo, glu \_ Tess de \_ enrolamento \_ negativo ou Glu \_ Tess de \_ enventor \_ ABS \_ GEQ \_ dois.</span><span class="sxs-lookup"><span data-stu-id="9485b-117">The value parameter may be set to one of the following: GLU\_TESS\_WINDING\_ODD, GLU\_TESS\_WINDING\_NONZERO, GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, or GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO.</span></span> <br/> <span data-ttu-id="9485b-118">Para entender como a regra de enrolamento funciona, primeiro considere que os contornos de entrada particionam o plano em regiões.</span><span class="sxs-lookup"><span data-stu-id="9485b-118">To understand how the winding rule works, first consider that the input contours partition the plane into regions.</span></span> <span data-ttu-id="9485b-119">A regra de enrolamento determina quais dessas regiões estão dentro do polígono.</span><span class="sxs-lookup"><span data-stu-id="9485b-119">The winding rule determines which of these regions are inside the polygon.</span></span><br/> <span data-ttu-id="9485b-120">Para um C de contorno único, o número de enrolamento de um ponto x é simplesmente o número assinado de rotações que fazemos em torno de x enquanto viajamos uma vez em torno de C (onde o anti-horário é positivo).</span><span class="sxs-lookup"><span data-stu-id="9485b-120">For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive).</span></span> <span data-ttu-id="9485b-121">Quando há várias contornos, os números de enrolamento individuais são somados.</span><span class="sxs-lookup"><span data-stu-id="9485b-121">When there are several contours, the individual winding numbers are summed.</span></span> <span data-ttu-id="9485b-122">Este procedimento associa um valor inteiro assinado a cada ponto x no plano.</span><span class="sxs-lookup"><span data-stu-id="9485b-122">This procedure associates a signed integer value with each point x in the plane.</span></span> <span data-ttu-id="9485b-123">Observe que o número do enrolamento é o mesmo para todos os pontos em uma única região.</span><span class="sxs-lookup"><span data-stu-id="9485b-123">Note that the winding number is the same for all points in a single region.</span></span><br/> <span data-ttu-id="9485b-124">A regra de enrolamento classifica uma região como "interna" se o número do enrolamento pertencer à categoria escolhida (ímpar, diferente de zero, positivo, negativo ou valor absoluto de pelo menos dois).</span><span class="sxs-lookup"><span data-stu-id="9485b-124">The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two).</span></span> <span data-ttu-id="9485b-125">O Tessellator GLU anterior (anterior ao GLU 1,2) usava a regra "Odd".</span><span class="sxs-lookup"><span data-stu-id="9485b-125">The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule.</span></span> <span data-ttu-id="9485b-126">A regra "de zero" (GLU \_ Tess \_ windos de \_ zero) é outra maneira comum de definir o interior.</span><span class="sxs-lookup"><span data-stu-id="9485b-126">The "nonzero" rule (GLU\_TESS\_WINDING\_NONZERO) is another common way to define the interior.</span></span> <span data-ttu-id="9485b-127">As outras três regras (GLU \_ Tess \_ enventor \_ positivos, glu \_ Tess \_ enrolamento \_ negativo, glu \_ Tess de \_ enrolamento \_ do ABS GEQ \_ \_ dois) são úteis para as operações do polígono CSG.</span><span class="sxs-lookup"><span data-stu-id="9485b-127">The other three rules (GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO) are useful for polygon CSG operations.</span></span><br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <span data-ttu-id="9485b-128"><dt>**\_ \_ somente limite de Tess Glu \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9485b-128"><dt>**GLU\_TESS\_BOUNDARY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="9485b-129">Especifica um valor booliano (defina Value como GL \_ true ou GL \_ false).</span><span class="sxs-lookup"><span data-stu-id="9485b-129">Specifies a Boolean value (set value to GL\_TRUE or GL\_FALSE).</span></span> <span data-ttu-id="9485b-130">Quando você define Value como GL \_ true, um conjunto de contornos fechados separando o interior do polígono e o exterior é retornado em vez de um mosaico.</span><span class="sxs-lookup"><span data-stu-id="9485b-130">When you set value to GL\_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation.</span></span> <span data-ttu-id="9485b-131">Os contornos exteriores são orientados no sentido anti-horário em relação ao normal; os contornos interiores são orientados no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="9485b-131">Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise.</span></span> <span data-ttu-id="9485b-132">Os \_ \_ retornos de chamada Glu Tess Begin e Glu \_ Tess \_ begin \_ Data usam o \_ loop de linha do tipo GL \_ para cada contorno.</span><span class="sxs-lookup"><span data-stu-id="9485b-132">The GLU\_TESS\_BEGIN and GLU\_TESS\_BEGIN\_DATA callbacks use the type GL\_LINE\_LOOP for each contour.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <span data-ttu-id="9485b-133"><dt>**GLU \_ Tess \_ tolerância**</dt></span><span class="sxs-lookup"><span data-stu-id="9485b-133"><dt>**GLU\_TESS\_TOLERANCE**</dt></span></span> </dl>              | <span data-ttu-id="9485b-134">Especifica uma tolerância para mesclar recursos para reduzir o tamanho da saída.</span><span class="sxs-lookup"><span data-stu-id="9485b-134">Specifies a tolerance for merging features to reduce the size of the output.</span></span> <span data-ttu-id="9485b-135">Por exemplo, dois vértices muito próximos uns dos outros podem ser substituídos por um único vértice.</span><span class="sxs-lookup"><span data-stu-id="9485b-135">For example, two vertexes that are very close to each other might be replaced by a single vertex.</span></span> <span data-ttu-id="9485b-136">A tolerância é multiplicada pela maior magnitude de coordenadas de qualquer vértice de entrada; Isso especifica a distância máxima que qualquer recurso pode mover como resultado de uma única operação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="9485b-136">The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation.</span></span> <span data-ttu-id="9485b-137">Se um único recurso faz parte de várias operações de mesclagem, a distância total movida pode ser maior.</span><span class="sxs-lookup"><span data-stu-id="9485b-137">If a single feature takes part in several merge operations, the total distance moved can be larger.</span></span> <br/> <span data-ttu-id="9485b-138">A mesclagem de recursos é completamente opcional; a tolerância é apenas uma dica.</span><span class="sxs-lookup"><span data-stu-id="9485b-138">Feature merging is completely optional; the tolerance is only a hint.</span></span> <span data-ttu-id="9485b-139">A implementação é gratuita para mesclar em alguns casos e não em outros, ou para nunca mesclar recursos.</span><span class="sxs-lookup"><span data-stu-id="9485b-139">The implementation is free to merge in some cases and not in others, or to never merge features at all.</span></span> <span data-ttu-id="9485b-140">A tolerância padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="9485b-140">The default tolerance is zero.</span></span><br/> <span data-ttu-id="9485b-141">A implementação atual mesclará vértices somente se eles forem exatamente coincidentes, independentemente da tolerância atual.</span><span class="sxs-lookup"><span data-stu-id="9485b-141">The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance.</span></span> <span data-ttu-id="9485b-142">Um vértice se unirá a uma borda somente se a implementação não puder distinguir em qual lado da borda o vértice está.</span><span class="sxs-lookup"><span data-stu-id="9485b-142">A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on.</span></span> <span data-ttu-id="9485b-143">Duas bordas são mescladas somente quando os dois pontos de extremidade são idênticos.</span><span class="sxs-lookup"><span data-stu-id="9485b-143">Two edges are merged only when both endpoints are identical.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="9485b-144">*value*</span><span class="sxs-lookup"><span data-stu-id="9485b-144">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="9485b-145">O valor da propriedade indicada.</span><span class="sxs-lookup"><span data-stu-id="9485b-145">The value of the indicated property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9485b-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9485b-146">Return value</span></span>

<span data-ttu-id="9485b-147">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9485b-147">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9485b-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="9485b-148">Remarks</span></span>

<span data-ttu-id="9485b-149">A função **gluTessProperty** controla as propriedades armazenadas em um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="9485b-149">The **gluTessProperty** function controls properties stored in a tessellation object.</span></span> <span data-ttu-id="9485b-150">Essas propriedades afetam a maneira como os polígonos são interpretados e renderizados.</span><span class="sxs-lookup"><span data-stu-id="9485b-150">These properties affect the way the polygons are interpreted and rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="9485b-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9485b-151">Requirements</span></span>



| <span data-ttu-id="9485b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="9485b-152">Requirement</span></span> | <span data-ttu-id="9485b-153">Valor</span><span class="sxs-lookup"><span data-stu-id="9485b-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9485b-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9485b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="9485b-155">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9485b-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9485b-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9485b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="9485b-157">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9485b-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9485b-158">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9485b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="9485b-159"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="9485b-159"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9485b-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9485b-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="9485b-161"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9485b-161"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9485b-162">DLL</span><span class="sxs-lookup"><span data-stu-id="9485b-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9485b-163"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9485b-163"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9485b-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="9485b-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9485b-165">**gluGetTessProperty**</span><span class="sxs-lookup"><span data-stu-id="9485b-165">**gluGetTessProperty**</span></span>](glugettessproperty.md)
</dt> <dt>

[<span data-ttu-id="9485b-166">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="9485b-166">**gluNewTess**</span></span>](glunewtess.md)
</dt> </dl>

 

 





