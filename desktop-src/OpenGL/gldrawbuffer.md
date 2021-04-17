---
title: função glDrawBuffer (GL. h)
description: A função glDrawBuffer especifica em quais buffers de cores devem ser desenhados.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- função glDrawBuffer OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754522"
---
# <a name="gldrawbuffer-function"></a><span data-ttu-id="8492c-104">função glDrawBuffer</span><span class="sxs-lookup"><span data-stu-id="8492c-104">glDrawBuffer function</span></span>

<span data-ttu-id="8492c-105">A função **glDrawBuffer** especifica em quais buffers de cores devem ser desenhados.</span><span class="sxs-lookup"><span data-stu-id="8492c-105">The **glDrawBuffer** function specifies which color buffers are to be drawn into.</span></span>

## <a name="syntax"></a><span data-ttu-id="8492c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8492c-106">Syntax</span></span>


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="8492c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8492c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8492c-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="8492c-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="8492c-109">Especifica até quatro buffers de cores a serem desenhados com as constantes simbólicas aceitáveis a seguir.</span><span class="sxs-lookup"><span data-stu-id="8492c-109">Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.</span></span>



| <span data-ttu-id="8492c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8492c-110">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="8492c-111">Significado</span><span class="sxs-lookup"><span data-stu-id="8492c-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <span data-ttu-id="8492c-112"><dt>**\_nenhum GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-112"><dt>**GL\_NONE**</dt></span></span> </dl>                                 | <span data-ttu-id="8492c-113">Nenhum buffer de cores é gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-113">No color buffers are written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <span data-ttu-id="8492c-114"><dt>**GL \_ frontal \_ esquerdo**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-114"><dt>**GL\_FRONT\_LEFT**</dt></span></span> </dl>              | <span data-ttu-id="8492c-115">Somente o buffer de cores do lado esquerdo é gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-115">Only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <span data-ttu-id="8492c-116"><dt>**\_frontal \_ do GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-116"><dt>**GL\_FRONT\_RIGHT**</dt></span></span> </dl>           | <span data-ttu-id="8492c-117">Somente o buffer de cores do lado direito é gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-117">Only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <span data-ttu-id="8492c-118"><dt>**\_voltar \_ à esquerda do GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-118"><dt>**GL\_BACK\_LEFT**</dt></span></span> </dl>                 | <span data-ttu-id="8492c-119">Somente o buffer de cores de trás para a esquerda é gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-119">Only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <span data-ttu-id="8492c-120"><dt>**\_direito de voltar \_ do GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-120"><dt>**GL\_BACK\_RIGHT**</dt></span></span> </dl>              | <span data-ttu-id="8492c-121">Somente o buffer de cores de fundo à direita é gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-121">Only the back-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <span data-ttu-id="8492c-122"><dt>**frente do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-122"><dt>**GL\_FRONT**</dt></span></span> </dl>                              | <span data-ttu-id="8492c-123">Somente os buffers de cores front-Left e front-Right são gravados.</span><span class="sxs-lookup"><span data-stu-id="8492c-123">Only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="8492c-124">Se não houver buffer de cor de front-Right, somente o buffer de cor frontal à esquerda será gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-124">If there is no front-right color buffer, only the front left-color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <span data-ttu-id="8492c-125"><dt>**GL \_ regressivo**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-125"><dt>**GL\_BACK**</dt></span></span> </dl>                                 | <span data-ttu-id="8492c-126">Somente os buffers de cor back-Left e back-Right são gravados.</span><span class="sxs-lookup"><span data-stu-id="8492c-126">Only the back-left and back-right color buffers are written.</span></span> <span data-ttu-id="8492c-127">Se não houver buffer de cor do lado direito, somente o buffer de cores do lado esquerdo será gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-127">If there is no back-right color buffer, only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <span data-ttu-id="8492c-128"><dt>**GL \_ restante**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-128"><dt>**GL\_LEFT**</dt></span></span> </dl>                                 | <span data-ttu-id="8492c-129">Somente os buffers de cores front-Left e back-Left são gravados.</span><span class="sxs-lookup"><span data-stu-id="8492c-129">Only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="8492c-130">Se não houver nenhum buffer de cor de back-Left, somente o buffer de cores do lado esquerdo será gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-130">If there is no back-left color buffer, only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <span data-ttu-id="8492c-131"><dt>**GL \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-131"><dt>**GL\_RIGHT**</dt></span></span> </dl>                              | <span data-ttu-id="8492c-132">Somente os buffers de cores front-Right e back-Right são gravados.</span><span class="sxs-lookup"><span data-stu-id="8492c-132">Only the front-right and back-right color buffers are written.</span></span> <span data-ttu-id="8492c-133">Se não houver buffer de cor do lado direito, somente o buffer de cores do lado direito será gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-133">If there is no back-right color buffer, only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <span data-ttu-id="8492c-134"><dt>**GL \_ frontal \_ e \_ posterior**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-134"><dt>**GL\_FRONT\_AND\_BACK**</dt></span></span> </dl> | <span data-ttu-id="8492c-135">Todos os buffers de cor frontal e traseira (front-Left, frontal direita, back-Left, back-right) são gravados.</span><span class="sxs-lookup"><span data-stu-id="8492c-135">All the front and back color buffers (front-left, front-right, back-left, back-right) are written.</span></span> <span data-ttu-id="8492c-136">Se não houver buffers de cor de fundo, somente os buffers de cores front-Left e front-Right serão gravados.</span><span class="sxs-lookup"><span data-stu-id="8492c-136">If there are no back color buffers, only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="8492c-137">Se não houver buffers de cor corretos, somente os buffers de cores front-Left e back-Left serão gravados.</span><span class="sxs-lookup"><span data-stu-id="8492c-137">If there are no right color buffers, only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="8492c-138">Se não houver buffers de cor direita ou voltar, somente o buffer de cores do lado esquerdo será gravado.</span><span class="sxs-lookup"><span data-stu-id="8492c-138">If there are no right or back color buffers, only the front-left color buffer is written.</span></span><br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <span data-ttu-id="8492c-139"><dt>**\_AUXI GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-139"><dt>**GL\_AUXi**</dt></span></span> </dl>       | <span data-ttu-id="8492c-140">Somente o buffer de cores auxiliares *i* é gravado; *estou* entre \_ buffers auxiliares 0 e GL \_ -1.</span><span class="sxs-lookup"><span data-stu-id="8492c-140">Only the auxiliary color buffer *i* is written; *i* is between 0 and GL\_AUX\_BUFFERS - 1.</span></span> <span data-ttu-id="8492c-141">(GL \_ \_Os buffers de aux não são o limite superior; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para consultar o número de buffers auxiliares disponíveis.)</span><span class="sxs-lookup"><span data-stu-id="8492c-141">(GL\_AUX\_BUFFERS is not the upper limit; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to query the number of available auxiliary buffers.)</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="8492c-142">O valor padrão é GL \_ frontal para contextos de buffer único e GL \_ volta para contextos de buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="8492c-142">The default value is GL\_FRONT for single-buffered contexts, and GL\_BACK for double-buffered contexts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8492c-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8492c-143">Return value</span></span>

<span data-ttu-id="8492c-144">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8492c-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8492c-145">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8492c-145">Error codes</span></span>

<span data-ttu-id="8492c-146">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8492c-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8492c-147">Nome</span><span class="sxs-lookup"><span data-stu-id="8492c-147">Name</span></span>                                                                                                  | <span data-ttu-id="8492c-148">Significado</span><span class="sxs-lookup"><span data-stu-id="8492c-148">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8492c-149"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-149"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8492c-150">o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="8492c-150">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="8492c-151"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8492c-152">Nenhum dos buffers indicados pelo *modo* existia.</span><span class="sxs-lookup"><span data-stu-id="8492c-152">None of the buffers indicated by *mode* existed.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="8492c-153"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8492c-154">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8492c-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |


## <a name="remarks"></a><span data-ttu-id="8492c-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="8492c-155">Remarks</span></span>

<span data-ttu-id="8492c-156">Quando as cores são gravadas no framebuffer, elas são gravadas nos buffers de cores especificados por **glDrawBuffer**.</span><span class="sxs-lookup"><span data-stu-id="8492c-156">When colors are written to the framebuffer, they are written into the color buffers specified by **glDrawBuffer**.</span></span>

<span data-ttu-id="8492c-157">Se mais de um buffer de cores for selecionado para desenho, as operações de mesclagem ou lógicas serão computadas e aplicadas de forma independente para cada buffer de cor e poderão produzir resultados diferentes em cada buffer.</span><span class="sxs-lookup"><span data-stu-id="8492c-157">If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.</span></span>

<span data-ttu-id="8492c-158">Contextos de Monoscopic incluem somente buffers à esquerda e contextos estereoscópico incluem buffers esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="8492c-158">Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers.</span></span> <span data-ttu-id="8492c-159">Da mesma forma, contextos de buffer único incluem somente buffers frontais e contextos com buffer duplo incluem buffers de frente e de trás.</span><span class="sxs-lookup"><span data-stu-id="8492c-159">Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers.</span></span> <span data-ttu-id="8492c-160">O contexto é selecionado na inicialização do OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8492c-160">The context is selected at OpenGL initialization.</span></span>

<span data-ttu-id="8492c-161">É sempre o caso que GL \_ aux *i* = GL \_ AUX0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="8492c-161">It is always the case that GL\_AUX *i* = GL\_AUX0 + *i*.</span></span>

<span data-ttu-id="8492c-162">As funções a seguir recuperam informações relacionadas à função **glDrawBuffer** :</span><span class="sxs-lookup"><span data-stu-id="8492c-162">The following functions retrieve information related to the **glDrawBuffer** function:</span></span>

<span data-ttu-id="8492c-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento de desenho do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8492c-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DRAW\_BUFFER</span></span>

<span data-ttu-id="8492c-164">**glGet** com \_ buffers auxiliares do Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="8492c-164">**glGet** with argument GL\_AUX\_BUFFERS</span></span>

## <a name="requirements"></a><span data-ttu-id="8492c-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8492c-165">Requirements</span></span>



| <span data-ttu-id="8492c-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="8492c-166">Requirement</span></span> | <span data-ttu-id="8492c-167">Valor</span><span class="sxs-lookup"><span data-stu-id="8492c-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8492c-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8492c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8492c-169">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8492c-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8492c-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8492c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8492c-171">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8492c-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8492c-172">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8492c-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="8492c-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8492c-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8492c-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="8492c-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8492c-176">DLL</span><span class="sxs-lookup"><span data-stu-id="8492c-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8492c-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8492c-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8492c-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="8492c-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8492c-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8492c-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8492c-180">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="8492c-180">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="8492c-181">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="8492c-181">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="8492c-182">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8492c-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8492c-183">**glGet**</span><span class="sxs-lookup"><span data-stu-id="8492c-183">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8492c-184">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="8492c-184">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="8492c-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="8492c-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="8492c-186">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="8492c-186">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





