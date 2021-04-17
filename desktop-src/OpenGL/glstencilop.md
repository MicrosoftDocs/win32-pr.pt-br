---
title: função glStencilOp (GL. h)
description: A função glStencilOp define as ações de teste de estêncil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- função glStencilOp OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789741"
---
# <a name="glstencilop-function"></a><span data-ttu-id="90cde-104">função glStencilOp</span><span class="sxs-lookup"><span data-stu-id="90cde-104">glStencilOp function</span></span>

<span data-ttu-id="90cde-105">A função **glStencilOp** define as ações de teste de estêncil.</span><span class="sxs-lookup"><span data-stu-id="90cde-105">The **glStencilOp** function sets the stencil test actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="90cde-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90cde-106">Syntax</span></span>


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a><span data-ttu-id="90cde-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90cde-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90cde-108">*recuperação*</span><span class="sxs-lookup"><span data-stu-id="90cde-108">*fail*</span></span> 
</dt> <dd>

<span data-ttu-id="90cde-109">A ação a ser tomada quando o teste de estêncil falhar.</span><span class="sxs-lookup"><span data-stu-id="90cde-109">The action to take when the stencil test fails.</span></span> <span data-ttu-id="90cde-110">As seis constantes simbólicas a seguir são aceitas.</span><span class="sxs-lookup"><span data-stu-id="90cde-110">The following six symbolic constants are accepted.</span></span>



| <span data-ttu-id="90cde-111">Valor</span><span class="sxs-lookup"><span data-stu-id="90cde-111">Value</span></span>                                                                                                                                                | <span data-ttu-id="90cde-112">Significado</span><span class="sxs-lookup"><span data-stu-id="90cde-112">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <span data-ttu-id="90cde-113"><dt>**\_Keep GL**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-113"><dt>**GL\_KEEP**</dt></span></span> </dl>          | <span data-ttu-id="90cde-114">Mantém o valor atual.</span><span class="sxs-lookup"><span data-stu-id="90cde-114">Keeps the current value.</span></span><br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <span data-ttu-id="90cde-115"><dt>**GL \_ zero**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-115"><dt>**GL\_ZERO**</dt></span></span> </dl>          | <span data-ttu-id="90cde-116">Define o valor do buffer de estêncil como zero.</span><span class="sxs-lookup"><span data-stu-id="90cde-116">Sets the stencil buffer value to zero.</span></span><br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <span data-ttu-id="90cde-117"><dt>**\_substituição GL**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-117"><dt>**GL\_REPLACE**</dt></span></span> </dl> | <span data-ttu-id="90cde-118">Define o valor do buffer de estêncil como *ref*, conforme especificado por **glStencilFunc**.</span><span class="sxs-lookup"><span data-stu-id="90cde-118">Sets the stencil buffer value to *ref*, as specified by **glStencilFunc**.</span></span><br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <span data-ttu-id="90cde-119"><dt>**\_incr GL**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-119"><dt>**GL\_INCR**</dt></span></span> </dl>          | <span data-ttu-id="90cde-120">Incrementa o valor do buffer do estêncil atual.</span><span class="sxs-lookup"><span data-stu-id="90cde-120">Increments the current stencil buffer value.</span></span> <span data-ttu-id="90cde-121">Coloca o valor não assinado máximo reapresentável.</span><span class="sxs-lookup"><span data-stu-id="90cde-121">Clamps to the maximum representable unsigned value.</span></span><br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <span data-ttu-id="90cde-122"><dt>**\_DECR GL**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-122"><dt>**GL\_DECR**</dt></span></span> </dl>          | <span data-ttu-id="90cde-123">Decrementa o valor do buffer do estêncil atual.</span><span class="sxs-lookup"><span data-stu-id="90cde-123">Decrements the current stencil buffer value.</span></span> <span data-ttu-id="90cde-124">Coloca para zero.</span><span class="sxs-lookup"><span data-stu-id="90cde-124">Clamps to zero.</span></span><br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="90cde-125"><dt>**\_inverter GL**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-125"><dt>**GL\_INVERT**</dt></span></span> </dl>    | <span data-ttu-id="90cde-126">A bit invertido inverte o valor do buffer do estêncil atual.</span><span class="sxs-lookup"><span data-stu-id="90cde-126">Bitwise inverts the current stencil buffer value.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="90cde-127">*zfail*</span><span class="sxs-lookup"><span data-stu-id="90cde-127">*zfail*</span></span> 
</dt> <dd>

<span data-ttu-id="90cde-128">Ação de estêncil quando o teste de estêncil passa, mas o teste de profundidade falha.</span><span class="sxs-lookup"><span data-stu-id="90cde-128">Stencil action when the stencil test passes, but the depth test fails.</span></span> <span data-ttu-id="90cde-129">Aceita as mesmas constantes simbólicas como *falha.*</span><span class="sxs-lookup"><span data-stu-id="90cde-129">Accepts the same symbolic constants as *fail.*</span></span>

</dd> <dt>

<span data-ttu-id="90cde-130">*zpass*</span><span class="sxs-lookup"><span data-stu-id="90cde-130">*zpass*</span></span> 
</dt> <dd>

<span data-ttu-id="90cde-131">Ação de estêncil quando o teste de estêncil e o teste de profundidade são aprovados, ou quando o teste de estêncil passa e não há um buffer de profundidade ou o teste de profundidade não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="90cde-131">Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled.</span></span> <span data-ttu-id="90cde-132">Aceita as mesmas constantes simbólicas como *falha*.</span><span class="sxs-lookup"><span data-stu-id="90cde-132">Accepts the same symbolic constants as *fail*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90cde-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90cde-133">Return value</span></span>

<span data-ttu-id="90cde-134">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="90cde-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="90cde-135">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="90cde-135">Error codes</span></span>

<span data-ttu-id="90cde-136">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="90cde-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="90cde-137">Nome</span><span class="sxs-lookup"><span data-stu-id="90cde-137">Name</span></span>                                                                                                  | <span data-ttu-id="90cde-138">Significado</span><span class="sxs-lookup"><span data-stu-id="90cde-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90cde-139"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="90cde-140">*Fail*, *zfail* ou *ZPass* era qualquer valor diferente dos seis valores constantes definidos.</span><span class="sxs-lookup"><span data-stu-id="90cde-140">*fail*, *zfail*, or *zpass* was any value other than the six defined constant values.</span></span><br/>                                      |
| <dl> <span data-ttu-id="90cde-141"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="90cde-142">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="90cde-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="90cde-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="90cde-143">Remarks</span></span>

<span data-ttu-id="90cde-144">O estêncil, como o armazenamento em buffer *z*, habilita e desabilita o desenho em uma base por pixel.</span><span class="sxs-lookup"><span data-stu-id="90cde-144">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="90cde-145">Você desenha nos planos de estêncil usando primitivas de desenho OpenGL e, em seguida, renderiza a geometria e as imagens, usando os planos de estêncil para mascarar partes da tela.</span><span class="sxs-lookup"><span data-stu-id="90cde-145">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="90cde-146">A criação de estêncil normalmente é usada em algoritmos de renderização de passagem multipassadas para obter efeitos especiais, como decals, estrutura de tópicos e renderização de geometria sólida construtivas.</span><span class="sxs-lookup"><span data-stu-id="90cde-146">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="90cde-147">O teste de estêncil elimina condicionalmente um pixel com base no resultado de uma comparação entre o valor no buffer do estêncil e um valor de referência.</span><span class="sxs-lookup"><span data-stu-id="90cde-147">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="90cde-148">O teste é habilitado com chamadas [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com teste de estêncil GL do argumento \_ \_ e controlado com [**glStencilFunc**](glstencilfunc.md).</span><span class="sxs-lookup"><span data-stu-id="90cde-148">The test is enabled with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) calls with argument GL\_STENCIL\_TEST, and controlled with [**glStencilFunc**](glstencilfunc.md).</span></span>

<span data-ttu-id="90cde-149">A função **glStencilOp** usa três argumentos que indicam o que acontece com o valor de estêncil armazenado enquanto o estêncil está habilitado.</span><span class="sxs-lookup"><span data-stu-id="90cde-149">The **glStencilOp** function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled.</span></span> <span data-ttu-id="90cde-150">Se o teste de estêncil falhar, nenhuma alteração será feita na cor ou nos buffers de profundidade do pixel e a *falha* especificará o que acontece com o conteúdo do buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="90cde-150">If the stencil test fails, no change is made to the pixel's color or depth buffers, and *fail* specifies what happens to the stencil buffer contents.</span></span>

<span data-ttu-id="90cde-151">Os valores de buffer de estêncil são tratados como inteiros não assinados.</span><span class="sxs-lookup"><span data-stu-id="90cde-151">Stencil buffer values are treated as unsigned integers.</span></span> <span data-ttu-id="90cde-152">Quando incrementado e diminuído, os valores são clamped para 0 e 2 *n* 1, em que *n* é o valor retornado pela consulta de bits de \_ estêncil GL \_ .</span><span class="sxs-lookup"><span data-stu-id="90cde-152">When incremented and decremented, values are clamped to 0 and 2 *n* 1, where *n* is the value returned by querying GL\_STENCIL\_BITS.</span></span>

<span data-ttu-id="90cde-153">Os outros dois argumentos para **glStencilOp** especificar ações de buffer de estêncil devem ter os testes de buffer de profundidade subsequentes com êxito (*ZPass*) ou Fail (*zfail*).</span><span class="sxs-lookup"><span data-stu-id="90cde-153">The other two arguments to **glStencilOp** specify stencil buffer actions should subsequent depth buffer tests succeed (*zpass*) or fail (*zfail*).</span></span> <span data-ttu-id="90cde-154">(Consulte [**glDepthFunc**](gldepthfunc.md).) Eles são especificados usando as mesmas seis constantes simbólicas que *falham*.</span><span class="sxs-lookup"><span data-stu-id="90cde-154">(See [**glDepthFunc**](gldepthfunc.md).) They are specified using the same six symbolic constants as *fail*.</span></span> <span data-ttu-id="90cde-155">Observe que *zfail* é ignorado quando não há um buffer de profundidade ou quando o buffer de profundidade não está habilitado.</span><span class="sxs-lookup"><span data-stu-id="90cde-155">Note that *zfail* is ignored when there is no depth buffer, or when the depth buffer is not enabled.</span></span> <span data-ttu-id="90cde-156">Nesses casos, *falha* e *ZPass* especificam a ação de estêncil quando o teste de estêncil falha e passa, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="90cde-156">In these cases, *fail* and *zpass* specify stencil action when the stencil test fails and passes, respectively.</span></span>

<span data-ttu-id="90cde-157">Inicialmente, o teste de estêncil está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="90cde-157">Initially the stencil test is disabled.</span></span> <span data-ttu-id="90cde-158">Se não houver nenhum buffer de estêncil, nenhuma modificação de estêncil poderá ocorrer e será como se os testes de estêncil sempre passarem, independentemente de qualquer chamada para **glStencilOp**.</span><span class="sxs-lookup"><span data-stu-id="90cde-158">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to **glStencilOp**.</span></span>

<span data-ttu-id="90cde-159">As funções a seguir recuperam informações relacionadas ao **glStencilOp**:</span><span class="sxs-lookup"><span data-stu-id="90cde-159">The following functions retrieve information related to **glStencilOp**:</span></span>

<span data-ttu-id="90cde-160">falha de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o estêncil Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="90cde-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FAIL</span></span>

<span data-ttu-id="90cde-161">**glGet** com a \_ passagem de \_ profundidade de passagem do estêncil GL \_ do argumento \_</span><span class="sxs-lookup"><span data-stu-id="90cde-161">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_PASS</span></span>

<span data-ttu-id="90cde-162">**glGet** com falha de \_ \_ profundidade de aprovação do estêncil do \_ argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="90cde-162">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_FAIL</span></span>

<span data-ttu-id="90cde-163">**glGet** com bits de estêncil do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="90cde-163">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="90cde-164">teste de estêncil [**glIsEnabled**](glisenabled.md) com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="90cde-164">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="90cde-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90cde-165">Requirements</span></span>



| <span data-ttu-id="90cde-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="90cde-166">Requirement</span></span> | <span data-ttu-id="90cde-167">Valor</span><span class="sxs-lookup"><span data-stu-id="90cde-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90cde-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90cde-168">Minimum supported client</span></span><br/> | <span data-ttu-id="90cde-169">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90cde-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="90cde-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90cde-170">Minimum supported server</span></span><br/> | <span data-ttu-id="90cde-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90cde-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90cde-172">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="90cde-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="90cde-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="90cde-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90cde-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="90cde-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="90cde-176">DLL</span><span class="sxs-lookup"><span data-stu-id="90cde-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90cde-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90cde-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90cde-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="90cde-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90cde-179">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="90cde-179">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="90cde-180">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="90cde-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="90cde-181">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="90cde-181">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="90cde-182">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="90cde-182">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="90cde-183">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="90cde-183">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="90cde-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="90cde-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="90cde-185">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="90cde-185">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="90cde-186">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="90cde-186">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="90cde-187">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="90cde-187">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





