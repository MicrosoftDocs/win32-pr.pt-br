---
title: função glPolygonMode (GL. h)
description: A função glPolygonMode seleciona um modo de rasterização de polígono.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- função glPolygonMode OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756394"
---
# <a name="glpolygonmode-function"></a><span data-ttu-id="ab2af-104">função glPolygonMode</span><span class="sxs-lookup"><span data-stu-id="ab2af-104">glPolygonMode function</span></span>

<span data-ttu-id="ab2af-105">A função **glPolygonMode** seleciona um modo de rasterização de polígono.</span><span class="sxs-lookup"><span data-stu-id="ab2af-105">The **glPolygonMode** function selects a polygon rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2af-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab2af-106">Syntax</span></span>


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="ab2af-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab2af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab2af-108">*sorridente*</span><span class="sxs-lookup"><span data-stu-id="ab2af-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="ab2af-109">Os polígonos aos quais o *modo* se aplica.</span><span class="sxs-lookup"><span data-stu-id="ab2af-109">The polygons that *mode* applies to.</span></span> <span data-ttu-id="ab2af-110">Deve ser o GL \_ frontal para polígonos frontais, o GL \_ volta para polígonos traseiros ou o GL \_ frontal \_ e \_ posterior para polígonos frontais e traseiros.</span><span class="sxs-lookup"><span data-stu-id="ab2af-110">Must be GL\_FRONT for front-facing polygons, GL\_BACK for back-facing polygons, or GL\_FRONT\_AND\_BACK for front- and back-facing polygons.</span></span>

</dd> <dt>

<span data-ttu-id="ab2af-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="ab2af-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ab2af-112">A maneira como os polígonos serão rasterizados.</span><span class="sxs-lookup"><span data-stu-id="ab2af-112">The way polygons will be rasterized.</span></span> <span data-ttu-id="ab2af-113">Os modos a seguir são definidos e podem ser especificados no *modo*.</span><span class="sxs-lookup"><span data-stu-id="ab2af-113">The following modes are defined and can be specified in *mode*.</span></span> <span data-ttu-id="ab2af-114">O padrão é que o GL é \_ preenchido para polígonos frente e verso.</span><span class="sxs-lookup"><span data-stu-id="ab2af-114">The default is GL\_FILL for both front- and back-facing polygons.</span></span>



| <span data-ttu-id="ab2af-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ab2af-115">Value</span></span>                                                                                                                                          | <span data-ttu-id="ab2af-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ab2af-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <span data-ttu-id="ab2af-117"><dt>**\_ponto GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-117"><dt>**GL\_POINT**</dt></span></span> </dl> | <span data-ttu-id="ab2af-118">Os vértices do polígono marcados como o início de uma borda de limite são desenhados como pontos.</span><span class="sxs-lookup"><span data-stu-id="ab2af-118">Polygon vertices that are marked as the start of a boundary edge are drawn as points.</span></span> <span data-ttu-id="ab2af-119">Atributos de ponto como \_ \_ o tamanho do ponto GL \_ e \_ o ponto GL insuaves controlam a rasterização dos pontos.</span><span class="sxs-lookup"><span data-stu-id="ab2af-119">Point attributes such as GL\_POINT\_SIZE and GL\_POINT\_SMOOTH control the rasterization of the points.</span></span> <span data-ttu-id="ab2af-120">Os atributos de rasterização de polígono diferentes do \_ modo de polígono GL \_ não têm nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="ab2af-120">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <span data-ttu-id="ab2af-121"><dt>**\_linha GL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-121"><dt>**GL\_LINE**</dt></span></span> </dl>    | <span data-ttu-id="ab2af-122">As bordas de limite do polígono são desenhadas como segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="ab2af-122">Boundary edges of the polygon are drawn as line segments.</span></span> <span data-ttu-id="ab2af-123">Eles são tratados como segmentos de linha conectados para a linha stippling; o contador de Stipple de linha e o padrão não são redefinidos entre os segmentos (consulte [**glLineStipple**](gllinestipple.md)).</span><span class="sxs-lookup"><span data-stu-id="ab2af-123">They are treated as connected line segments for line stippling; the line stipple counter and pattern are not reset between segments (see [**glLineStipple**](gllinestipple.md)).</span></span> <span data-ttu-id="ab2af-124">Atributos de linha como \_ \_ a largura da linha gl \_ e \_ o controle Smooth de linha gl a rasterização das linhas.</span><span class="sxs-lookup"><span data-stu-id="ab2af-124">Line attributes such as GL\_LINE\_WIDTH and GL\_LINE\_SMOOTH control the rasterization of the lines.</span></span> <span data-ttu-id="ab2af-125">Os atributos de rasterização de polígono diferentes do \_ modo de polígono GL \_ não têm nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="ab2af-125">Polygon rasterization attributes other than GL\_POLYGON\_MODE have no effect.</span></span><br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <span data-ttu-id="ab2af-126"><dt>**preenchimento do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-126"><dt>**GL\_FILL**</dt></span></span> </dl>    | <span data-ttu-id="ab2af-127">O interior do polígono é preenchido.</span><span class="sxs-lookup"><span data-stu-id="ab2af-127">The interior of the polygon is filled.</span></span> <span data-ttu-id="ab2af-128">Atributos Polygon, como GL \_ Polygon \_ STIPPLE e GL \_ poligonal \_ controle Smooth a rasterização do polígono.</span><span class="sxs-lookup"><span data-stu-id="ab2af-128">Polygon attributes such as GL\_POLYGON\_STIPPLE and GL\_POLYGON\_SMOOTH control the rasterization of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab2af-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab2af-129">Return value</span></span>

<span data-ttu-id="ab2af-130">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ab2af-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ab2af-131">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ab2af-131">Error codes</span></span>

<span data-ttu-id="ab2af-132">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ab2af-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ab2af-133">Nome</span><span class="sxs-lookup"><span data-stu-id="ab2af-133">Name</span></span>                                                                                                  | <span data-ttu-id="ab2af-134">Significado</span><span class="sxs-lookup"><span data-stu-id="ab2af-134">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab2af-135"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ab2af-136">A *face* ou o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="ab2af-136">Either *face* or *mode* was not an accepted value.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="ab2af-137"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-137"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ab2af-138">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ab2af-138">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ab2af-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab2af-139">Remarks</span></span>

<span data-ttu-id="ab2af-140">A função **glPolygonMode** controla a interpretação de polígonos para rasterização.</span><span class="sxs-lookup"><span data-stu-id="ab2af-140">The **glPolygonMode** function controls the interpretation of polygons for rasterization.</span></span> <span data-ttu-id="ab2af-141">O parâmetro *facial* descreve a qual *modo* polígonos se aplica: polígonos (front-end \_ ), polígonos voltados (GL \_ traseiro) ou ambos (GL \_ frontal \_ e \_ posterior).</span><span class="sxs-lookup"><span data-stu-id="ab2af-141">The *face* parameter describes which polygons *mode* applies to: front-facing polygons (GL\_FRONT), back-facing polygons (GL\_BACK), or both (GL\_FRONT\_AND\_BACK).</span></span> <span data-ttu-id="ab2af-142">O modo Polygon afeta apenas a rasterização final de polígonos.</span><span class="sxs-lookup"><span data-stu-id="ab2af-142">The polygon mode affects only the final rasterization of polygons.</span></span> <span data-ttu-id="ab2af-143">Em particular, os vértices de um polígono estão acesos e o polígono é recortado e possivelmente refigurados antes que esses modos sejam aplicados.</span><span class="sxs-lookup"><span data-stu-id="ab2af-143">In particular, a polygon's vertices are lit and the polygon is clipped and possibly culled before these modes are applied.</span></span>

<span data-ttu-id="ab2af-144">Para desenhar uma superfície com polígonos voltados para trás e com sublinhado polígonos, chame</span><span class="sxs-lookup"><span data-stu-id="ab2af-144">To draw a surface with filled back-facing polygons and outlined front-facing polygons, call</span></span>

<span data-ttu-id="ab2af-145">**glPolygonMode**(GL \_ frontal, \_ linha GL);</span><span class="sxs-lookup"><span data-stu-id="ab2af-145">**glPolygonMode**(GL\_FRONT, GL\_LINE);</span></span>

<span data-ttu-id="ab2af-146">Os vértices são marcados como limite ou não restritos com um sinalizador de borda.</span><span class="sxs-lookup"><span data-stu-id="ab2af-146">Vertices are marked as boundary or nonboundary with an edge flag.</span></span> <span data-ttu-id="ab2af-147">Os sinalizadores de borda são gerados internamente pelo OpenGL quando decompõem polígonos e podem ser definidos explicitamente usando [**glEdgeFlag**](gledgeflag-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ab2af-147">Edge flags are generated internally by OpenGL when it decomposes polygons, and they can be set explicitly using [**glEdgeFlag**](gledgeflag-functions.md).</span></span>

<span data-ttu-id="ab2af-148">A função a seguir recupera informações relacionadas a **glPolygonMode**:</span><span class="sxs-lookup"><span data-stu-id="ab2af-148">The following function retrieves information related to **glPolygonMode**:</span></span>

<span data-ttu-id="ab2af-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com modo de polígono do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="ab2af-149">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2af-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab2af-150">Requirements</span></span>



| <span data-ttu-id="ab2af-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab2af-151">Requirement</span></span> | <span data-ttu-id="ab2af-152">Valor</span><span class="sxs-lookup"><span data-stu-id="ab2af-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2af-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab2af-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ab2af-154">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab2af-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ab2af-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab2af-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ab2af-156">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab2af-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab2af-157">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ab2af-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab2af-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ab2af-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab2af-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab2af-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ab2af-161">DLL</span><span class="sxs-lookup"><span data-stu-id="ab2af-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab2af-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab2af-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab2af-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab2af-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2af-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ab2af-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ab2af-165">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="ab2af-165">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="ab2af-166">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ab2af-166">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ab2af-167">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="ab2af-167">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="ab2af-168">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="ab2af-168">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="ab2af-169">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="ab2af-169">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="ab2af-170">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="ab2af-170">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





