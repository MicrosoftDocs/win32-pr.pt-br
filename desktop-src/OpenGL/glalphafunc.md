---
title: função glAlphaFunc (GL. h)
description: A função glAlphaFunc permite que seu aplicativo defina a função de teste alfa.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- função glAlphaFunc OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784169"
---
# <a name="glalphafunc-function"></a><span data-ttu-id="9bafd-104">função glAlphaFunc</span><span class="sxs-lookup"><span data-stu-id="9bafd-104">glAlphaFunc function</span></span>

<span data-ttu-id="9bafd-105">A função **glAlphaFunc** permite que seu aplicativo defina a função de teste alfa.</span><span class="sxs-lookup"><span data-stu-id="9bafd-105">The **glAlphaFunc** function enables your application to set the alpha test function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bafd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bafd-106">Syntax</span></span>


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a><span data-ttu-id="9bafd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bafd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bafd-108">*func*</span><span class="sxs-lookup"><span data-stu-id="9bafd-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="9bafd-109">A função de comparação alfa.</span><span class="sxs-lookup"><span data-stu-id="9bafd-109">The alpha comparison function.</span></span> <span data-ttu-id="9bafd-110">A seguir estão as constantes simbólicas aceitas e seus significados.</span><span class="sxs-lookup"><span data-stu-id="9bafd-110">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="9bafd-111">Valor</span><span class="sxs-lookup"><span data-stu-id="9bafd-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="9bafd-112">Significado</span><span class="sxs-lookup"><span data-stu-id="9bafd-112">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="9bafd-113"><dt>**GL \_ nunca**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="9bafd-114">Nunca passa.</span><span class="sxs-lookup"><span data-stu-id="9bafd-114">Never passes.</span></span><br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="9bafd-115"><dt>**GL \_ menos**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="9bafd-116">Passa se o valor alfa de entrada for menor que o valor de referência.</span><span class="sxs-lookup"><span data-stu-id="9bafd-116">Passes if the incoming alpha value is less than the reference value.</span></span><br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="9bafd-117"><dt>**GL \_ igual a**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-117"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="9bafd-118">Passa se o valor alfa de entrada for igual ao valor de referência.</span><span class="sxs-lookup"><span data-stu-id="9bafd-118">Passes if the incoming alpha value is equal to the reference value.</span></span><br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="9bafd-119"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-119"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="9bafd-120">Passa se o valor alfa de entrada for menor ou igual ao valor de referência.</span><span class="sxs-lookup"><span data-stu-id="9bafd-120">Passes if the incoming alpha value is less than or equal to the reference value.</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="9bafd-121"><dt>**GL \_ maior**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-121"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="9bafd-122">Passa se o valor alfa de entrada for maior que o valor de referência.</span><span class="sxs-lookup"><span data-stu-id="9bafd-122">Passes if the incoming alpha value is greater than the reference value.</span></span><br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="9bafd-123"><dt>**GL não \_ igual**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-123"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="9bafd-124">Passa se o valor alfa de entrada não for igual ao valor de referência.</span><span class="sxs-lookup"><span data-stu-id="9bafd-124">Passes if the incoming alpha value is not equal to the reference value.</span></span><br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="9bafd-125"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-125"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="9bafd-126">Passa se o valor alfa de entrada for maior ou igual ao valor de referência.</span><span class="sxs-lookup"><span data-stu-id="9bafd-126">Passes if the incoming alpha value is greater than or equal to the reference value.</span></span><br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="9bafd-127"><dt>**GL \_ sempre**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-127"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="9bafd-128">Sempre passa.</span><span class="sxs-lookup"><span data-stu-id="9bafd-128">Always passes.</span></span> <span data-ttu-id="9bafd-129">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="9bafd-129">This is the default.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="9bafd-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="9bafd-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="9bafd-131">O valor de referência para o qual os valores Alfa de entrada são comparados.</span><span class="sxs-lookup"><span data-stu-id="9bafd-131">The reference value to which incoming alpha values are compared.</span></span> <span data-ttu-id="9bafd-132">Esse valor é clamped para o intervalo de 0 a 1, em que 0 representa o menor valor alfa possível e 1 o maior valor possível.</span><span class="sxs-lookup"><span data-stu-id="9bafd-132">This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value.</span></span> <span data-ttu-id="9bafd-133">A referência padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="9bafd-133">The default reference is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bafd-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9bafd-134">Return value</span></span>

<span data-ttu-id="9bafd-135">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9bafd-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9bafd-136">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="9bafd-136">Error codes</span></span>

<span data-ttu-id="9bafd-137">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9bafd-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9bafd-138">Nome</span><span class="sxs-lookup"><span data-stu-id="9bafd-138">Name</span></span>                                                                                                  | <span data-ttu-id="9bafd-139">Significado</span><span class="sxs-lookup"><span data-stu-id="9bafd-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9bafd-140"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9bafd-141">*Func* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="9bafd-141">*func* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="9bafd-142"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9bafd-143">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9bafd-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9bafd-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bafd-144">Remarks</span></span>

<span data-ttu-id="9bafd-145">O teste alfa descarta fragmentos dependendo do resultado de uma comparação entre os valores Alfa dos fragmentos de entrada e um valor de referência constante.</span><span class="sxs-lookup"><span data-stu-id="9bafd-145">The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value.</span></span> <span data-ttu-id="9bafd-146">A função **glAlphaFunc** especifica a função de referência e comparação.</span><span class="sxs-lookup"><span data-stu-id="9bafd-146">The **glAlphaFunc** function specifies the reference and comparison function.</span></span> <span data-ttu-id="9bafd-147">A comparação será executada somente se o teste alfa estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="9bafd-147">The comparison is performed only if alpha testing is enabled.</span></span> <span data-ttu-id="9bafd-148">(Para obter mais informações sobre o GL \_ \_Teste alfa, consulte [**glEnable**](glenable.md).)</span><span class="sxs-lookup"><span data-stu-id="9bafd-148">(For more information on GL\_ALPHA\_TEST, see [**glEnable**](glenable.md).)</span></span>

<span data-ttu-id="9bafd-149">Os parâmetros *Func* e *ref* especificam as condições sob as quais o pixel é desenhado.</span><span class="sxs-lookup"><span data-stu-id="9bafd-149">The *func* and *ref* parameters specify the conditions under which the pixel is drawn.</span></span> <span data-ttu-id="9bafd-150">O valor alfa de entrada é comparado com *ref* usando a função especificada por *Func*.</span><span class="sxs-lookup"><span data-stu-id="9bafd-150">The incoming alpha value is compared to *ref* using the function specified by *func*.</span></span> <span data-ttu-id="9bafd-151">Se a comparação passar, o fragmento de entrada será desenhado, condicional nos testes subseqüentes de estêncil e buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="9bafd-151">If the comparison passes, the incoming fragment is drawn, conditional on subsequent stencil and depth-buffer tests.</span></span> <span data-ttu-id="9bafd-152">Se a comparação falhar, nenhuma alteração será feita no framebuffer naquele local de pixel.</span><span class="sxs-lookup"><span data-stu-id="9bafd-152">If the comparison fails, no change is made to the framebuffer at that pixel location.</span></span>

<span data-ttu-id="9bafd-153">A função **glAlphaFunc** opera em todas as gravações de pixel, incluindo aquelas resultantes da conversão de verificação de pontos, linhas, polígonos e bitmaps e de operações de desenho e de cópia de pixel.</span><span class="sxs-lookup"><span data-stu-id="9bafd-153">The **glAlphaFunc** function operates on all pixel writes, including those resulting from the scan conversion of points, lines, polygons, and bitmaps, and from pixel draw and copy operations.</span></span> <span data-ttu-id="9bafd-154">A função **glAlphaFunc** não afeta as operações de limpeza de tela.</span><span class="sxs-lookup"><span data-stu-id="9bafd-154">The **glAlphaFunc** function does not affect screen clear operations.</span></span>

<span data-ttu-id="9bafd-155">O teste alfa é feito somente no modo RGBA.</span><span class="sxs-lookup"><span data-stu-id="9bafd-155">Alpha testing is done only in RGBA mode.</span></span>

<span data-ttu-id="9bafd-156">As funções a seguir recuperam informações relacionadas à função **glAlphaFunc** :</span><span class="sxs-lookup"><span data-stu-id="9bafd-156">The following functions retrieve information related to the **glAlphaFunc** function:</span></span>

<span data-ttu-id="9bafd-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ alfa \_ test \_ Func</span><span class="sxs-lookup"><span data-stu-id="9bafd-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ALPHA\_TEST\_FUNC</span></span>

<span data-ttu-id="9bafd-158">**glGet** com Argument GL \_ Alpha \_ test \_ ref</span><span class="sxs-lookup"><span data-stu-id="9bafd-158">**glGet** with argument GL\_ALPHA\_TEST\_REF</span></span>

<span data-ttu-id="9bafd-159">teste de [**glIsEnabled**](glisenabled.md) com Argument GL \_ Alpha \_</span><span class="sxs-lookup"><span data-stu-id="9bafd-159">[**glIsEnabled**](glisenabled.md) with argument GL\_ALPHA\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="9bafd-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bafd-160">Requirements</span></span>



| <span data-ttu-id="9bafd-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bafd-161">Requirement</span></span> | <span data-ttu-id="9bafd-162">Valor</span><span class="sxs-lookup"><span data-stu-id="9bafd-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bafd-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bafd-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9bafd-164">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9bafd-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9bafd-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bafd-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9bafd-166">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9bafd-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9bafd-167">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9bafd-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bafd-168"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-168"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9bafd-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9bafd-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bafd-170"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-170"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9bafd-171">DLL</span><span class="sxs-lookup"><span data-stu-id="9bafd-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bafd-172"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bafd-172"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bafd-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bafd-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bafd-174">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9bafd-174">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9bafd-175">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="9bafd-175">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="9bafd-176">**glClear**</span><span class="sxs-lookup"><span data-stu-id="9bafd-176">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="9bafd-177">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="9bafd-177">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="9bafd-178">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="9bafd-178">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="9bafd-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9bafd-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9bafd-180">**glGet**</span><span class="sxs-lookup"><span data-stu-id="9bafd-180">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9bafd-181">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="9bafd-181">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="9bafd-182">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="9bafd-182">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





