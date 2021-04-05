---
title: função glFrontFace (GL. h)
description: A função glFrontFace define polígonos de front-face e voltados para o verso.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- função glFrontFace OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919140"
---
# <a name="glfrontface-function"></a><span data-ttu-id="b1beb-104">função glFrontFace</span><span class="sxs-lookup"><span data-stu-id="b1beb-104">glFrontFace function</span></span>

<span data-ttu-id="b1beb-105">A função **glFrontFace** define polígonos de front-face e voltados para o verso.</span><span class="sxs-lookup"><span data-stu-id="b1beb-105">The **glFrontFace** function defines front-facing and back-facing polygons.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1beb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1beb-106">Syntax</span></span>


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="b1beb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1beb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1beb-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="b1beb-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="b1beb-109">A orientação dos polígonos front-face.</span><span class="sxs-lookup"><span data-stu-id="b1beb-109">The orientation of front-facing polygons.</span></span> <span data-ttu-id="b1beb-110">O GL \_ CW e o GL \_ CCW são aceitos.</span><span class="sxs-lookup"><span data-stu-id="b1beb-110">GL\_CW and GL\_CCW are accepted.</span></span> <span data-ttu-id="b1beb-111">O valor padrão é GL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="b1beb-111">The default value is GL\_CCW.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1beb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1beb-112">Return value</span></span>

<span data-ttu-id="b1beb-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b1beb-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b1beb-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b1beb-114">Error codes</span></span>

<span data-ttu-id="b1beb-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b1beb-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b1beb-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b1beb-116">Name</span></span>                                                                                                  | <span data-ttu-id="b1beb-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b1beb-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1beb-118"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="b1beb-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b1beb-119">o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="b1beb-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b1beb-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b1beb-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b1beb-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b1beb-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b1beb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1beb-122">Remarks</span></span>

<span data-ttu-id="b1beb-123">Em uma cena composta inteiramente de superfícies fechadas opacas, polígonos voltados nunca são visíveis.</span><span class="sxs-lookup"><span data-stu-id="b1beb-123">In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible.</span></span> <span data-ttu-id="b1beb-124">A eliminação desses polígonos invisíveis tem o benefício óbvio de acelerar a renderização da imagem.</span><span class="sxs-lookup"><span data-stu-id="b1beb-124">Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image.</span></span> <span data-ttu-id="b1beb-125">Você habilita e desabilita a eliminação de polígonos voltados com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) usando o tipo de seleção Argument GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b1beb-125">You enable and disable elimination of back-facing polygons with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) using argument GL\_CULL\_FACE.</span></span>

<span data-ttu-id="b1beb-126">A projeção de um polígono para as coordenadas da janela é indicada para ter o enrolamento no sentido horário se um objeto imaginário após o caminho de seu primeiro vértice, seu segundo vértice e assim por diante, para seu último vértice e, finalmente, voltar ao seu primeiro vértice, se mover em uma direção no sentido horário sobre o interior do polígono.</span><span class="sxs-lookup"><span data-stu-id="b1beb-126">The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="b1beb-127">O enrolamento do polígono é considerado no sentido anti-horário se o objeto imaginário após o mesmo caminho se mover em uma direção no sentido anti-horário sobre o interior do polígono.</span><span class="sxs-lookup"><span data-stu-id="b1beb-127">The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="b1beb-128">A função **glFrontFace** especifica se polígonos com o enrolamento no sentido horário nas coordenadas da janela ou o retrocesso anti-horário nas coordenadas da janela são levados para ser front-face.</span><span class="sxs-lookup"><span data-stu-id="b1beb-128">The **glFrontFace** function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing.</span></span> <span data-ttu-id="b1beb-129">Passar \_ o GL CCW para o *modo* seleciona polígonos no sentido anti-horário como front-face; O GL em \_ PV seleciona polígonos no sentido horário como front-face.</span><span class="sxs-lookup"><span data-stu-id="b1beb-129">Passing GL\_CCW to *mode* selects counterclockwise polygons as front-facing; GL\_CW selects clockwise polygons as front-facing.</span></span> <span data-ttu-id="b1beb-130">Por padrão, polígonos no sentido anti-horário são levados a voltar para a frente.</span><span class="sxs-lookup"><span data-stu-id="b1beb-130">By default, counterclockwise polygons are taken to be front-facing.</span></span>

<span data-ttu-id="b1beb-131">A função a seguir recupera informações sobre **glFrontface**:</span><span class="sxs-lookup"><span data-stu-id="b1beb-131">The following function retrieves information about **glFrontface**:</span></span>

<span data-ttu-id="b1beb-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a \_ face frontal do Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="b1beb-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FRONT\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="b1beb-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1beb-133">Requirements</span></span>



| <span data-ttu-id="b1beb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1beb-134">Requirement</span></span> | <span data-ttu-id="b1beb-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b1beb-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1beb-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1beb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b1beb-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1beb-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b1beb-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1beb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b1beb-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b1beb-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1beb-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b1beb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1beb-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1beb-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b1beb-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1beb-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1beb-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1beb-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1beb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b1beb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1beb-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1beb-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1beb-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1beb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1beb-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b1beb-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b1beb-148">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="b1beb-148">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="b1beb-149">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="b1beb-149">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="b1beb-150">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="b1beb-150">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b1beb-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b1beb-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b1beb-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b1beb-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b1beb-153">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="b1beb-153">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





