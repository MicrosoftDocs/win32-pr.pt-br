---
title: função glStencilFunc (GL. h)
description: A função glStencilFunc define a função e o valor de referência para teste de estêncil.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- função glStencilFunc OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759355"
---
# <a name="glstencilfunc-function"></a><span data-ttu-id="278d0-104">função glStencilFunc</span><span class="sxs-lookup"><span data-stu-id="278d0-104">glStencilFunc function</span></span>

<span data-ttu-id="278d0-105">A função **glStencilFunc** define a função e o valor de referência para teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-105">The **glStencilFunc** function sets the function and reference value for stencil testing.</span></span>

## <a name="syntax"></a><span data-ttu-id="278d0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="278d0-106">Syntax</span></span>


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="278d0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="278d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="278d0-108">*func*</span><span class="sxs-lookup"><span data-stu-id="278d0-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="278d0-109">A função de teste.</span><span class="sxs-lookup"><span data-stu-id="278d0-109">The test function.</span></span> <span data-ttu-id="278d0-110">Os oito tokens a seguir são válidos.</span><span class="sxs-lookup"><span data-stu-id="278d0-110">The following eight tokens are valid.</span></span>



| <span data-ttu-id="278d0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="278d0-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="278d0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="278d0-112">Meaning</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="278d0-113"><dt>**GL \_ nunca**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="278d0-114">Sempre falha.</span><span class="sxs-lookup"><span data-stu-id="278d0-114">Always fails.</span></span><br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="278d0-115"><dt>**GL \_ menos**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="278d0-116">Passa se (  &  *máscara* de referência) < (máscara de *estêncil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="278d0-116">Passes if (*ref* & *mask*) < (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="278d0-117"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-117"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="278d0-118">Passa se (  &  *máscara* de referência) = (máscara de *estêncil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="278d0-118">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="278d0-119"><dt>**GL \_ maior**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-119"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="278d0-120">Passa se (  &  *máscara* de referência) > (máscara de *estêncil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="278d0-120">Passes if (*ref* & *mask*) > (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="278d0-121"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-121"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="278d0-122">Passa se (  &  *máscara* de referência) = (máscara de *estêncil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="278d0-122">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="278d0-123"><dt>**GL \_ igual a**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-123"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="278d0-124">Passa se (  &  *máscara* de referência) = (máscara de *estêncil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="278d0-124">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="278d0-125"><dt>**GL não \_ igual**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-125"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="278d0-126">Passa se (  &  *máscara* de referência)?</span><span class="sxs-lookup"><span data-stu-id="278d0-126">Passes if (*ref* & *mask*) ?</span></span> <span data-ttu-id="278d0-127">(*estêncil*  &  *Mask*).</span><span class="sxs-lookup"><span data-stu-id="278d0-127">(*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="278d0-128"><dt>**GL \_ sempre**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="278d0-129">Sempre passa.</span><span class="sxs-lookup"><span data-stu-id="278d0-129">Always passes.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="278d0-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="278d0-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="278d0-131">O valor de referência para o teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-131">The reference value for the stencil test.</span></span> <span data-ttu-id="278d0-132">O parâmetro *ref* é clamped para o intervalo de \[ 0, 2 *n* 1 \] , em que *n* é o número de bitplanes no buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-132">The *ref* parameter is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

</dd> <dt>

<span data-ttu-id="278d0-133">*mascara*</span><span class="sxs-lookup"><span data-stu-id="278d0-133">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="278d0-134">Uma máscara que é **e** Ed com o valor de referência e o valor de estêncil armazenado quando o teste é concluído.</span><span class="sxs-lookup"><span data-stu-id="278d0-134">A mask that is **AND** ed with both the reference value and the stored stencil value when the test is done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="278d0-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="278d0-135">Return value</span></span>

<span data-ttu-id="278d0-136">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="278d0-136">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="278d0-137">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="278d0-137">Error codes</span></span>

<span data-ttu-id="278d0-138">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="278d0-138">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="278d0-139">Nome</span><span class="sxs-lookup"><span data-stu-id="278d0-139">Name</span></span>                                                                                                  | <span data-ttu-id="278d0-140">Significado</span><span class="sxs-lookup"><span data-stu-id="278d0-140">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="278d0-141"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-141"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="278d0-142">*Func* não era um dos oito valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="278d0-142">*func* was not one of the eight accepted values.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="278d0-143"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-143"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="278d0-144">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="278d0-144">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="278d0-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="278d0-145">Remarks</span></span>

<span data-ttu-id="278d0-146">O estêncil, como o armazenamento em buffer *z*, habilita e desabilita o desenho em uma base por pixel.</span><span class="sxs-lookup"><span data-stu-id="278d0-146">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="278d0-147">Você desenha nos planos de estêncil usando primitivas de desenho OpenGL e, em seguida, renderiza a geometria e as imagens, usando os planos de estêncil para mascarar partes da tela.</span><span class="sxs-lookup"><span data-stu-id="278d0-147">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="278d0-148">A criação de estêncil normalmente é usada em algoritmos de renderização de passagem multipassadas para obter efeitos especiais, como decals, estrutura de tópicos e renderização de geometria sólida construtivas.</span><span class="sxs-lookup"><span data-stu-id="278d0-148">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="278d0-149">O teste de estêncil elimina condicionalmente um pixel com base no resultado de uma comparação entre o valor de referência e o valor no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-149">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer.</span></span> <span data-ttu-id="278d0-150">O teste é habilitado por [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o teste de estêncil do Argument GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="278d0-150">The test is enabled by [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_STENCIL\_TEST.</span></span> <span data-ttu-id="278d0-151">Ações executadas com base no resultado do teste de estêncil são especificadas com [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="278d0-151">Actions taken based on the outcome of the stencil test are specified with [**glStencilOp**](glstencilop.md).</span></span>

<span data-ttu-id="278d0-152">O parâmetro *Func* é uma constante simbólica que determina a função de comparação de estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-152">The *func* parameter is a symbolic constant that determines the stencil comparison function.</span></span> <span data-ttu-id="278d0-153">Ele aceita um dos oito valores mostrados acima.</span><span class="sxs-lookup"><span data-stu-id="278d0-153">It accepts one of the eight values shown above.</span></span> <span data-ttu-id="278d0-154">O parâmetro *ref* é um valor de referência de inteiro que é usado na comparação de estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-154">The *ref* parameter is an integer reference value that is used in the stencil comparison.</span></span> <span data-ttu-id="278d0-155">É clamped para o intervalo de \[ 0, 2 *n* 1 \] , em que *n* é o número de bitplanes no buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-155">It is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span> <span data-ttu-id="278d0-156">O parâmetro *Mask* é bit-a **and** Ed com o valor de referência e o valor de estêncil armazenado, com os valores **e** Ed que participam da comparação.</span><span class="sxs-lookup"><span data-stu-id="278d0-156">The *mask* parameter is bitwise **AND** ed with both the reference value and the stored stencil value, with the **AND** ed values participating in the comparison.</span></span>

<span data-ttu-id="278d0-157">Se *stencil* representa o valor armazenado no local do buffer de estêncil correspondente, a lista anterior mostra o efeito de cada função de comparação que pode ser especificada por *Func*.</span><span class="sxs-lookup"><span data-stu-id="278d0-157">If *stencil* represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by *func*.</span></span> <span data-ttu-id="278d0-158">Somente se a comparação for realizada com êxito, o pixel passado para o próximo estágio no processo de rasterização (consulte [**glStencilOp**](glstencilop.md)).</span><span class="sxs-lookup"><span data-stu-id="278d0-158">Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see [**glStencilOp**](glstencilop.md)).</span></span> <span data-ttu-id="278d0-159">Todos os testes tratam valores de *estêncil* como inteiros não assinados no intervalo de \[ 0, 2 *n* 1 \] , em que *n* é o número de bitplanes no buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="278d0-159">All tests treat *stencil* values as unsigned integers in the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

<span data-ttu-id="278d0-160">Inicialmente, o teste de estêncil está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="278d0-160">Initially, the stencil test is disabled.</span></span> <span data-ttu-id="278d0-161">Se não houver nenhum buffer de estêncil, nenhuma modificação de estêncil poderá ocorrer e será como se o teste de estêncil sempre passar.</span><span class="sxs-lookup"><span data-stu-id="278d0-161">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.</span></span>

<span data-ttu-id="278d0-162">As funções a seguir recuperam informações relacionadas ao **glStencilFunc**:</span><span class="sxs-lookup"><span data-stu-id="278d0-162">The following functions retrieve information related to **glStencilFunc**:</span></span>

<span data-ttu-id="278d0-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with o estêncil GL do argumento \_ \_ Func</span><span class="sxs-lookup"><span data-stu-id="278d0-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FUNC</span></span>

<span data-ttu-id="278d0-164"> máscara de valor de estêncil glGet com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="278d0-164">**glGet** with argument GL\_STENCIL\_VALUE\_MASK</span></span>

<span data-ttu-id="278d0-165">**glGet** com ref de estêncil do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="278d0-165">**glGet** with argument GL\_STENCIL\_REF</span></span>

<span data-ttu-id="278d0-166">**glGet** com bits de estêncil do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="278d0-166">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="278d0-167">teste de estêncil [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="278d0-167">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="278d0-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="278d0-168">Requirements</span></span>



| <span data-ttu-id="278d0-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="278d0-169">Requirement</span></span> | <span data-ttu-id="278d0-170">Valor</span><span class="sxs-lookup"><span data-stu-id="278d0-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="278d0-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="278d0-171">Minimum supported client</span></span><br/> | <span data-ttu-id="278d0-172">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="278d0-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="278d0-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="278d0-173">Minimum supported server</span></span><br/> | <span data-ttu-id="278d0-174">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="278d0-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="278d0-175">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="278d0-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="278d0-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="278d0-177">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="278d0-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="278d0-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="278d0-179">DLL</span><span class="sxs-lookup"><span data-stu-id="278d0-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="278d0-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="278d0-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="278d0-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="278d0-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="278d0-182">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="278d0-182">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="278d0-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="278d0-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="278d0-184">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="278d0-184">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="278d0-185">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="278d0-185">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="278d0-186">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="278d0-186">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="278d0-187">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="278d0-187">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="278d0-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="278d0-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="278d0-189">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="278d0-189">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="278d0-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="278d0-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





