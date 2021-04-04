---
title: função glCullFace (GL. h)
description: A função glCullFace especifica se as facetas de front-face ou voltagem para frente podem ser refeitas.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- função glCullFace OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918100"
---
# <a name="glcullface-function"></a><span data-ttu-id="b0719-104">função glCullFace</span><span class="sxs-lookup"><span data-stu-id="b0719-104">glCullFace function</span></span>

<span data-ttu-id="b0719-105">A função **glCullFace** especifica se as facetas de front-face ou voltagem para frente podem ser refeitas.</span><span class="sxs-lookup"><span data-stu-id="b0719-105">The **glCullFace** function specifies whether front-facing or back-facing facets can be culled.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0719-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0719-106">Syntax</span></span>


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="b0719-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0719-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0719-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="b0719-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="b0719-109">Especifica se as facetas voltadas para a frente ou para trás são candidatas para a remoção.</span><span class="sxs-lookup"><span data-stu-id="b0719-109">Specifies whether front-facing or back-facing facets are candidates for culling.</span></span> <span data-ttu-id="b0719-110">As constantes simbólicas GL \_ front, GL \_ back e GL \_ front \_ e \_ back são aceitas.</span><span class="sxs-lookup"><span data-stu-id="b0719-110">The symbolic constants GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK are accepted.</span></span> <span data-ttu-id="b0719-111">O valor padrão é GL de \_ volta.</span><span class="sxs-lookup"><span data-stu-id="b0719-111">The default value is GL\_BACK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0719-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0719-112">Return value</span></span>

<span data-ttu-id="b0719-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b0719-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b0719-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b0719-114">Error codes</span></span>

<span data-ttu-id="b0719-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b0719-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b0719-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b0719-116">Name</span></span>                                                                                                  | <span data-ttu-id="b0719-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b0719-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b0719-118"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="b0719-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b0719-119">o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="b0719-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="b0719-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b0719-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b0719-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b0719-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b0719-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0719-122">Remarks</span></span>

<span data-ttu-id="b0719-123">A função **glCullFace** especifica se as facetas de front-face ou voltagem para frente são examinadas (conforme especificado pelo *modo*) quando a remoção da faceta está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b0719-123">The **glCullFace** function specifies whether front-facing or back-facing facets are culled (as specified by *mode*) when facet culling is enabled.</span></span> <span data-ttu-id="b0719-124">Você habilita e desabilita a remoção de faceta usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com a face de seleção do Argument GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b0719-124">You enable and disable facet culling using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_CULL\_FACE.</span></span> <span data-ttu-id="b0719-125">As facetas incluem triângulos, quadrilaterals, polígonos e retângulos.</span><span class="sxs-lookup"><span data-stu-id="b0719-125">Facets include triangles, quadrilaterals, polygons, and rectangles.</span></span>

<span data-ttu-id="b0719-126">A função [**glFrontFace**](glfrontface.md) especifica qual das facetas no sentido horário e anti-horário são voltadas para frente e para trás.</span><span class="sxs-lookup"><span data-stu-id="b0719-126">The [**glFrontFace**](glfrontface.md) function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.</span></span>

<span data-ttu-id="b0719-127">Se o *modo* for GL \_ frontal \_ e \_ posterior, nenhuma faceta será desenhada, mas outros primitivos, como pontos e linhas, serão desenhados.</span><span class="sxs-lookup"><span data-stu-id="b0719-127">If *mode* is GL\_FRONT\_AND\_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.</span></span>

<span data-ttu-id="b0719-128">As funções a seguir recuperam informações relacionadas ao **glCullFace**:</span><span class="sxs-lookup"><span data-stu-id="b0719-128">The following functions retrieve information related to **glCullFace**:</span></span>

<span data-ttu-id="b0719-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o Argument GL selecionar \_ \_ \_ modo facial</span><span class="sxs-lookup"><span data-stu-id="b0719-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CULL\_FACE\_MODE</span></span>

<span data-ttu-id="b0719-130">[**glIsEnabled**](glisenabled.md) com a face do argumento GL de \_ seleção \_</span><span class="sxs-lookup"><span data-stu-id="b0719-130">[**glIsEnabled**](glisenabled.md) with argument GL\_CULL\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="b0719-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0719-131">Requirements</span></span>



| <span data-ttu-id="b0719-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0719-132">Requirement</span></span> | <span data-ttu-id="b0719-133">Valor</span><span class="sxs-lookup"><span data-stu-id="b0719-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0719-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0719-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b0719-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0719-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b0719-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0719-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b0719-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0719-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0719-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b0719-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0719-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0719-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b0719-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0719-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0719-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0719-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0719-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b0719-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0719-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0719-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0719-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0719-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0719-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b0719-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b0719-146">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="b0719-146">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="b0719-147">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="b0719-147">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="b0719-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b0719-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b0719-149">**glFrontFace**</span><span class="sxs-lookup"><span data-stu-id="b0719-149">**glFrontFace**</span></span>](glfrontface.md)
</dt> <dt>

[<span data-ttu-id="b0719-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b0719-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b0719-151">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b0719-151">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





