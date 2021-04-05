---
title: função glRenderMode (GL. h)
description: A função glRenderMode define o modo de rasterização.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- função glRenderMode OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086395"
---
# <a name="glrendermode-function"></a><span data-ttu-id="348b8-104">função glRenderMode</span><span class="sxs-lookup"><span data-stu-id="348b8-104">glRenderMode function</span></span>

<span data-ttu-id="348b8-105">A função **glRenderMode** define o modo de rasterização.</span><span class="sxs-lookup"><span data-stu-id="348b8-105">The **glRenderMode** function sets the rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="348b8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="348b8-106">Syntax</span></span>


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="348b8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="348b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="348b8-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="348b8-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="348b8-109">O modo de rasterização.</span><span class="sxs-lookup"><span data-stu-id="348b8-109">The rasterization mode.</span></span> <span data-ttu-id="348b8-110">Os três valores a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="348b8-110">The following three values are accepted.</span></span> <span data-ttu-id="348b8-111">O valor padrão é GL \_ render.</span><span class="sxs-lookup"><span data-stu-id="348b8-111">The default value is GL\_RENDER.</span></span>



| <span data-ttu-id="348b8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="348b8-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="348b8-113">Significado</span><span class="sxs-lookup"><span data-stu-id="348b8-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <span data-ttu-id="348b8-114"><dt>**\_RENDERIZAÇÃO GL**</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-114"><dt>**GL\_RENDER**</dt></span></span> </dl>       | <span data-ttu-id="348b8-115">Modo de renderização.</span><span class="sxs-lookup"><span data-stu-id="348b8-115">Render mode.</span></span> <span data-ttu-id="348b8-116">Os primitivos são rasterizados, produzindo fragmentos de pixel, que são gravados no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="348b8-116">Primitives are rasterized, producing pixel fragments, which are written into the framebuffer.</span></span> <span data-ttu-id="348b8-117">Esse é o modo normal e também o modo padrão.</span><span class="sxs-lookup"><span data-stu-id="348b8-117">This is the normal mode and also the default mode.</span></span><br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <span data-ttu-id="348b8-118"><dt>**\_Select GL**</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-118"><dt>**GL\_SELECT**</dt></span></span> </dl>       | <span data-ttu-id="348b8-119">Modo de seleção.</span><span class="sxs-lookup"><span data-stu-id="348b8-119">Selection mode.</span></span> <span data-ttu-id="348b8-120">Nenhum fragmento de pixel é produzido e nenhuma alteração no conteúdo de framebuffer é feita.</span><span class="sxs-lookup"><span data-stu-id="348b8-120">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="348b8-121">Em vez disso, um registro dos nomes de primitivos que teriam sido desenhados se o modo render era o \_ render GL ser retornado em um buffer Select, que deve ser criado (consulte [**glSelectBuffer**](glselectbuffer.md)) antes de o modo de seleção ser inserido.</span><span class="sxs-lookup"><span data-stu-id="348b8-121">Instead, a record of the names of primitives that would have been drawn if the render mode was GL\_RENDER is returned in a select buffer, which must be created (see [**glSelectBuffer**](glselectbuffer.md)) before selection mode is entered.</span></span><br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <span data-ttu-id="348b8-122"><dt>**Comentários do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-122"><dt>**GL\_FEEDBACK**</dt></span></span> </dl> | <span data-ttu-id="348b8-123">Modo de comentários.</span><span class="sxs-lookup"><span data-stu-id="348b8-123">Feedback mode.</span></span> <span data-ttu-id="348b8-124">Nenhum fragmento de pixel é produzido e nenhuma alteração no conteúdo de framebuffer é feita.</span><span class="sxs-lookup"><span data-stu-id="348b8-124">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="348b8-125">Em vez disso, as coordenadas e os atributos dos vértices que teriam sido desenhados no modo de renderização eram \_ retornados em um buffer de comentários, que deve ser criado (consulte [**glFeedbackBuffer**](glfeedbackbuffer.md)) antes que o modo de comentários seja inserido.</span><span class="sxs-lookup"><span data-stu-id="348b8-125">Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL\_RENDER are returned in a feedback buffer, which must be created (see [**glFeedbackBuffer**](glfeedbackbuffer.md)) before feedback mode is entered.</span></span><br/> |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="348b8-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="348b8-126">Error codes</span></span>

<span data-ttu-id="348b8-127">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="348b8-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="348b8-128">Nome</span><span class="sxs-lookup"><span data-stu-id="348b8-128">Name</span></span>                                                                                                  | <span data-ttu-id="348b8-129">Significado</span><span class="sxs-lookup"><span data-stu-id="348b8-129">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="348b8-130"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="348b8-131">o *modo* não era um dos três valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="348b8-131">*mode* was not one of three accepted values.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="348b8-132"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="348b8-133">A função foi chamada com o argumento GL \_ Select antes de [**glSelectBuffer**](glselectbuffer.md) ser chamado pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="348b8-133">The function was called with argument GL\_SELECT before [**glSelectBuffer**](glselectbuffer.md) was called at least once.</span></span><br/>       |
| <dl> <span data-ttu-id="348b8-134"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="348b8-135">A função foi chamada com comentários do Argument GL \_ antes que [**glBeedbackBuffer**](glfeedbackbuffer.md) fosse chamado pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="348b8-135">The function was called with argument GL\_FEEDBACK before [**glBeedbackBuffer**](glfeedbackbuffer.md) was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="348b8-136"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="348b8-137">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="348b8-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="348b8-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="348b8-138">Remarks</span></span>

<span data-ttu-id="348b8-139">A função **glRenderMode** usa um argumento, *modo*, que pode assumir um dos três valores predefinidos acima.</span><span class="sxs-lookup"><span data-stu-id="348b8-139">The **glRenderMode** function takes one argument, *mode*, which can assume one of three predefined values above.</span></span>

<span data-ttu-id="348b8-140">O valor de retorno da função **glRenderMode** é determinado pelo modo render no momento em que **glRenderMode** é chamado, e não por *modo*.</span><span class="sxs-lookup"><span data-stu-id="348b8-140">The return value of the **glRenderMode** function is determined by the render mode at the time **glRenderMode** is called, rather than by *mode*.</span></span> <span data-ttu-id="348b8-141">Os valores retornados para os três modos de renderização são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="348b8-141">The values returned for the three render modes are as follows.</span></span>



| <span data-ttu-id="348b8-142">Valor</span><span class="sxs-lookup"><span data-stu-id="348b8-142">Value</span></span>        | <span data-ttu-id="348b8-143">Significado</span><span class="sxs-lookup"><span data-stu-id="348b8-143">Meaning</span></span>                                                                 |
|--------------|-------------------------------------------------------------------------|
| <span data-ttu-id="348b8-144">\_RENDERIZAÇÃO GL</span><span class="sxs-lookup"><span data-stu-id="348b8-144">GL\_RENDER</span></span>   | <span data-ttu-id="348b8-145">Zero.</span><span class="sxs-lookup"><span data-stu-id="348b8-145">Zero.</span></span>                                                                   |
| <span data-ttu-id="348b8-146">\_Select GL</span><span class="sxs-lookup"><span data-stu-id="348b8-146">GL\_SELECT</span></span>   | <span data-ttu-id="348b8-147">O número de registros de acesso transferido para o buffer selecionado.</span><span class="sxs-lookup"><span data-stu-id="348b8-147">The number of hit records transferred to the select buffer.</span></span>             |
| <span data-ttu-id="348b8-148">Comentários do GL \_</span><span class="sxs-lookup"><span data-stu-id="348b8-148">GL\_FEEDBACK</span></span> | <span data-ttu-id="348b8-149">O número de valores (não vértices) transferidos para o buffer de comentários.</span><span class="sxs-lookup"><span data-stu-id="348b8-149">The number of values (not vertices) transferred to the feedback buffer.</span></span> |



 

<span data-ttu-id="348b8-150">Consulte [**glSelectBuffer**](glselectbuffer.md) e [**glFeedbackBuffer**](glfeedbackbuffer.md) para obter mais detalhes sobre a operação de seleção e de comentários.</span><span class="sxs-lookup"><span data-stu-id="348b8-150">Refer to [**glSelectBuffer**](glselectbuffer.md) and [**glFeedbackBuffer**](glfeedbackbuffer.md) for more details concerning selection and feedback operation.</span></span>

<span data-ttu-id="348b8-151">Se um erro for gerado, **glRenderMode** retornará zero, independentemente do modo de processamento atual.</span><span class="sxs-lookup"><span data-stu-id="348b8-151">If an error is generated, **glRenderMode** returns zero regardless of the current render mode.</span></span>

<span data-ttu-id="348b8-152">A função a seguir recupera informações relacionadas a **glRenderMode**:</span><span class="sxs-lookup"><span data-stu-id="348b8-152">The following function retrieves information related to **glRenderMode**:</span></span>

<span data-ttu-id="348b8-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="348b8-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="348b8-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="348b8-154">Requirements</span></span>



| <span data-ttu-id="348b8-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="348b8-155">Requirement</span></span> | <span data-ttu-id="348b8-156">Valor</span><span class="sxs-lookup"><span data-stu-id="348b8-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="348b8-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="348b8-157">Minimum supported client</span></span><br/> | <span data-ttu-id="348b8-158">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="348b8-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="348b8-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="348b8-159">Minimum supported server</span></span><br/> | <span data-ttu-id="348b8-160">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="348b8-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="348b8-161">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="348b8-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="348b8-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="348b8-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="348b8-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="348b8-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="348b8-165">DLL</span><span class="sxs-lookup"><span data-stu-id="348b8-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="348b8-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="348b8-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="348b8-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="348b8-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="348b8-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="348b8-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="348b8-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="348b8-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="348b8-170">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="348b8-170">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="348b8-171">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="348b8-171">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="348b8-172">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="348b8-172">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="348b8-173">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="348b8-173">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="348b8-174">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="348b8-174">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="348b8-175">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="348b8-175">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





