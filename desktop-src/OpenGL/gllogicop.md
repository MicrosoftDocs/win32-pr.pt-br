---
title: função glLogicOp (GL. h)
description: A função glLogicOp especifica uma operação de pixel lógica para renderização de índice de cor.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- função glLogicOp OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499824"
---
# <a name="gllogicop-function"></a><span data-ttu-id="26f0e-104">função glLogicOp</span><span class="sxs-lookup"><span data-stu-id="26f0e-104">glLogicOp function</span></span>

<span data-ttu-id="26f0e-105">A função **glLogicOp** especifica uma operação de pixel lógica para renderização de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="26f0e-105">The **glLogicOp** function specifies a logical pixel operation for color index rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f0e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26f0e-106">Syntax</span></span>


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a><span data-ttu-id="26f0e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26f0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f0e-108">*opcode*</span><span class="sxs-lookup"><span data-stu-id="26f0e-108">*opcode*</span></span> 
</dt> <dd>

<span data-ttu-id="26f0e-109">Uma constante simbólica que seleciona uma operação lógica.</span><span class="sxs-lookup"><span data-stu-id="26f0e-109">A symbolic constant that selects a logical operation.</span></span> <span data-ttu-id="26f0e-110">Os símbolos a seguir são aceitos em que s é igual ao valor do bit de origem e d é o valor do bit de destino.</span><span class="sxs-lookup"><span data-stu-id="26f0e-110">The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.</span></span>



| <span data-ttu-id="26f0e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="26f0e-111">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="26f0e-112">Significado</span><span class="sxs-lookup"><span data-stu-id="26f0e-112">Meaning</span></span>              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <span data-ttu-id="26f0e-113"><dt>**GL \_ desmarcado**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-113"><dt>**GL\_CLEAR**</dt></span></span> </dl>                          | <span data-ttu-id="26f0e-114">0</span><span class="sxs-lookup"><span data-stu-id="26f0e-114">0</span></span><br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <span data-ttu-id="26f0e-115"><dt>**\_set GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-115"><dt>**GL\_SET**</dt></span></span> </dl>                                | <span data-ttu-id="26f0e-116">1</span><span class="sxs-lookup"><span data-stu-id="26f0e-116">1</span></span><br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <span data-ttu-id="26f0e-117"><dt>**\_cópia GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-117"><dt>**GL\_COPY**</dt></span></span> </dl>                             | <span data-ttu-id="26f0e-118">s</span><span class="sxs-lookup"><span data-stu-id="26f0e-118">s</span></span><br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <span data-ttu-id="26f0e-119"><dt>**a \_ cópia GL é \_ invertida**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-119"><dt>**GL\_COPY\_INVERTED**</dt></span></span> </dl> | <span data-ttu-id="26f0e-120">! s</span><span class="sxs-lookup"><span data-stu-id="26f0e-120">!s</span></span><br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <span data-ttu-id="26f0e-121"><dt>**o \_ NOOP GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-121"><dt>**GL\_NOOP**</dt></span></span> </dl>                             | <span data-ttu-id="26f0e-122">d</span><span class="sxs-lookup"><span data-stu-id="26f0e-122">d</span></span><br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="26f0e-123"><dt>**\_inverter GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-123"><dt>**GL\_INVERT**</dt></span></span> </dl>                       | <span data-ttu-id="26f0e-124">! d</span><span class="sxs-lookup"><span data-stu-id="26f0e-124">!d</span></span><br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <span data-ttu-id="26f0e-125"><dt>**GL \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-125"><dt>**GL\_AND**</dt></span></span> </dl>                                | <span data-ttu-id="26f0e-126">s & d</span><span class="sxs-lookup"><span data-stu-id="26f0e-126">s & d</span></span><br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <span data-ttu-id="26f0e-127"><dt>**GL \_ NAND**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-127"><dt>**GL\_NAND**</dt></span></span> </dl>                             | <span data-ttu-id="26f0e-128">! (s & d)</span><span class="sxs-lookup"><span data-stu-id="26f0e-128">!(s & d)</span></span><br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <span data-ttu-id="26f0e-129"><dt>**GL \_ ou**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-129"><dt>**GL\_OR**</dt></span></span> </dl>                                   | <span data-ttu-id="26f0e-130">s \| d</span><span class="sxs-lookup"><span data-stu-id="26f0e-130">s \| d</span></span><br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <span data-ttu-id="26f0e-131"><dt>**GL \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-131"><dt>**GL\_NOR**</dt></span></span> </dl>                                | <span data-ttu-id="26f0e-132">! (s \| )</span><span class="sxs-lookup"><span data-stu-id="26f0e-132">!(s \| d)</span></span><br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <span data-ttu-id="26f0e-133"><dt>**\_XOR GL**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-133"><dt>**GL\_XOR**</dt></span></span> </dl>                                | <span data-ttu-id="26f0e-134">s ^ d</span><span class="sxs-lookup"><span data-stu-id="26f0e-134">s ^ d</span></span><br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <span data-ttu-id="26f0e-135"><dt>**GL \_ equiv**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-135"><dt>**GL\_EQUIV**</dt></span></span> </dl>                          | <span data-ttu-id="26f0e-136">! (s ^ d)</span><span class="sxs-lookup"><span data-stu-id="26f0e-136">!(s ^ d)</span></span><br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <span data-ttu-id="26f0e-137"><dt>**GL \_ e \_ reverso**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-137"><dt>**GL\_AND\_REVERSE**</dt></span></span> </dl>       | <span data-ttu-id="26f0e-138">s &! d</span><span class="sxs-lookup"><span data-stu-id="26f0e-138">s & !d</span></span><br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <span data-ttu-id="26f0e-139"><dt>**GL \_ e \_ invertido**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-139"><dt>**GL\_AND\_INVERTED**</dt></span></span> </dl>    | <span data-ttu-id="26f0e-140">! s & d</span><span class="sxs-lookup"><span data-stu-id="26f0e-140">!s & d</span></span><br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <span data-ttu-id="26f0e-141"><dt>**GL \_ ou \_ reverso**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-141"><dt>**GL\_OR\_REVERSE**</dt></span></span> </dl>          | <span data-ttu-id="26f0e-142">s \| ! d</span><span class="sxs-lookup"><span data-stu-id="26f0e-142">s \| !d</span></span><br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <span data-ttu-id="26f0e-143"><dt>**GL \_ ou \_ invertido**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-143"><dt>**GL\_OR\_INVERTED**</dt></span></span> </dl>       | <span data-ttu-id="26f0e-144">! s \| d</span><span class="sxs-lookup"><span data-stu-id="26f0e-144">!s \| d</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f0e-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26f0e-145">Return value</span></span>

<span data-ttu-id="26f0e-146">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="26f0e-146">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="26f0e-147">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="26f0e-147">Error codes</span></span>

<span data-ttu-id="26f0e-148">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="26f0e-148">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="26f0e-149">Nome</span><span class="sxs-lookup"><span data-stu-id="26f0e-149">Name</span></span>                                                                                                  | <span data-ttu-id="26f0e-150">Significado</span><span class="sxs-lookup"><span data-stu-id="26f0e-150">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26f0e-151"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-151"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="26f0e-152">*opcode* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="26f0e-152">*opcode* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="26f0e-153"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="26f0e-154">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="26f0e-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="26f0e-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="26f0e-155">Remarks</span></span>

<span data-ttu-id="26f0e-156">A função **glLogicOp** especifica uma operação lógica que, quando habilitada, é aplicada entre o índice de cores de entrada e o índice de cores no local correspondente no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="26f0e-156">The **glLogicOp** function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer.</span></span> <span data-ttu-id="26f0e-157">A operação lógica está habilitada ou desabilitada com [**glEnable**](glenable.md) e **glDisable** usando a lógica simbólica de Operational do GL de constante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="26f0e-157">The logical operation is enabled or disabled with [**glEnable**](glenable.md) and **glDisable** using the symbolic constant GL\_LOGIC\_OP.</span></span>

<span data-ttu-id="26f0e-158">O parâmetro *opcode* é uma constante simbólica escolhida na lista abaixo.</span><span class="sxs-lookup"><span data-stu-id="26f0e-158">The *opcode* parameter is a symbolic constant chosen from the list below.</span></span> <span data-ttu-id="26f0e-159">Na explicação das operações lógicas, *s* representa o índice de cores de entrada e *d* representa o índice no framebuffer.</span><span class="sxs-lookup"><span data-stu-id="26f0e-159">In the explanation of the logical operations, *s* represents the incoming color index and *d* represents the index in the framebuffer.</span></span> <span data-ttu-id="26f0e-160">Os operadores padrão de linguagem C são usados.</span><span class="sxs-lookup"><span data-stu-id="26f0e-160">Standard C-language operators are used.</span></span> <span data-ttu-id="26f0e-161">À medida que esses operadores bit a pouco sugerem, a operação lógica é aplicada de forma independente a cada par de bits dos índices de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="26f0e-161">As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.</span></span>

<span data-ttu-id="26f0e-162">As operações de pixel lógico não são aplicadas a buffers de cores RGBA.</span><span class="sxs-lookup"><span data-stu-id="26f0e-162">Logical pixel operations are not applied to RGBA color buffers.</span></span>

<span data-ttu-id="26f0e-163">Quando mais de um buffer de índice de cor está habilitado para o desenho, as operações lógicas são feitas separadamente para cada buffer habilitado, usando o conteúdo desse buffer para o índice de destino (consulte [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="26f0e-163">When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span>

<span data-ttu-id="26f0e-164">O parâmetro *opcode* deve ser um dos 16 valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="26f0e-164">The *opcode* parameter must be one of the 16 accepted values.</span></span> <span data-ttu-id="26f0e-165">Outros valores resultam em um erro.</span><span class="sxs-lookup"><span data-stu-id="26f0e-165">Other values result in an error.</span></span>

<span data-ttu-id="26f0e-166">As funções a seguir recuperam informações relacionadas ao **glLogicOp**:</span><span class="sxs-lookup"><span data-stu-id="26f0e-166">The following functions retrieve information related to **glLogicOp**:</span></span>

<span data-ttu-id="26f0e-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com modo de \_ op lógico de Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="26f0e-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LOGIC\_OP\_MODE</span></span>

<span data-ttu-id="26f0e-168">[**glIsEnabled**](glisenabled.md) com o argumento GL \_ lógico \_ op</span><span class="sxs-lookup"><span data-stu-id="26f0e-168">[**glIsEnabled**](glisenabled.md) with argument GL\_LOGIC\_OP</span></span>

## <a name="requirements"></a><span data-ttu-id="26f0e-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f0e-169">Requirements</span></span>



| <span data-ttu-id="26f0e-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f0e-170">Requirement</span></span> | <span data-ttu-id="26f0e-171">Valor</span><span class="sxs-lookup"><span data-stu-id="26f0e-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26f0e-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26f0e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="26f0e-173">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="26f0e-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="26f0e-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26f0e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="26f0e-175">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="26f0e-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26f0e-176">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="26f0e-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f0e-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="26f0e-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26f0e-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="26f0e-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="26f0e-180">DLL</span><span class="sxs-lookup"><span data-stu-id="26f0e-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f0e-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f0e-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f0e-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="26f0e-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f0e-183">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="26f0e-183">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="26f0e-184">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="26f0e-184">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="26f0e-185">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="26f0e-185">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="26f0e-186">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="26f0e-186">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="26f0e-187">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="26f0e-187">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="26f0e-188">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="26f0e-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="26f0e-189">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="26f0e-189">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="26f0e-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="26f0e-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





