---
title: função glClear (GL. h)
description: A função glClear limpa os buffers para valores predefinidos.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- função glClear OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759184"
---
# <a name="glclear-function"></a><span data-ttu-id="df503-104">função glClear</span><span class="sxs-lookup"><span data-stu-id="df503-104">glClear function</span></span>

<span data-ttu-id="df503-105">A função **glClear** limpa os buffers para valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="df503-105">The **glClear** function clears buffers to preset values.</span></span>

## <a name="syntax"></a><span data-ttu-id="df503-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df503-106">Syntax</span></span>


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="df503-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df503-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df503-108">*mascara*</span><span class="sxs-lookup"><span data-stu-id="df503-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="df503-109">Os operadores or de máscaras que indicam os buffers a serem apagados.</span><span class="sxs-lookup"><span data-stu-id="df503-109">Bitwise OR operators of masks that indicate the buffers to be cleared.</span></span> <span data-ttu-id="df503-110">As quatro máscaras são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="df503-110">The four masks are as follows.</span></span>



| <span data-ttu-id="df503-111">Valor</span><span class="sxs-lookup"><span data-stu-id="df503-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="df503-112">Significado</span><span class="sxs-lookup"><span data-stu-id="df503-112">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <span data-ttu-id="df503-113"><dt>**\_bit do \_ buffer de cores GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df503-113"><dt>**GL\_COLOR\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="df503-114">Os buffers atualmente estão habilitados para gravação de cores.</span><span class="sxs-lookup"><span data-stu-id="df503-114">The buffers currently enabled for color writing.</span></span><br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <span data-ttu-id="df503-115"><dt>**\_bit de \_ buffer de profundidade GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df503-115"><dt>**GL\_DEPTH\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="df503-116">O buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="df503-116">The depth buffer.</span></span><br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <span data-ttu-id="df503-117"><dt>**BIT de buffer do GL \_ Accum \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df503-117"><dt>**GL\_ACCUM\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="df503-118">O buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="df503-118">The accumulation buffer.</span></span><br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <span data-ttu-id="df503-119"><dt>**\_bit de \_ buffer do estêncil GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df503-119"><dt>**GL\_STENCIL\_BUFFER\_BIT**</dt></span></span> </dl> | <span data-ttu-id="df503-120">O buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="df503-120">The stencil buffer.</span></span><br/>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df503-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df503-121">Return value</span></span>

<span data-ttu-id="df503-122">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="df503-122">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df503-123">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="df503-123">Error codes</span></span>

<span data-ttu-id="df503-124">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="df503-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="df503-125">Nome</span><span class="sxs-lookup"><span data-stu-id="df503-125">Name</span></span>                                                                                                  | <span data-ttu-id="df503-126">Significado</span><span class="sxs-lookup"><span data-stu-id="df503-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df503-127"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df503-127"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="df503-128">Um pouco além dos quatro bits definidos foi definido em *Mask*.</span><span class="sxs-lookup"><span data-stu-id="df503-128">Any bit other than the four defined bits was set in *mask*.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="df503-129"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df503-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="df503-130">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="df503-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="df503-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="df503-131">Remarks</span></span>

<span data-ttu-id="df503-132">A função **glClear** define a área Bitplane da janela para os valores selecionados anteriormente por [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)e [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="df503-132">The **glClear** function sets the bitplane area of the window to values previously selected by [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), and [**glClearAccum**](glclearaccum.md).</span></span> <span data-ttu-id="df503-133">Você pode limpar vários buffers de cores simultaneamente selecionando mais de um buffer por vez usando [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="df503-133">You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using [**glDrawBuffer**](gldrawbuffer.md).</span></span>

<span data-ttu-id="df503-134">O teste de propriedade de pixel, o teste de tesoura, o pontilhamento e o buffer writemasks afetam a operação de **glClear**.</span><span class="sxs-lookup"><span data-stu-id="df503-134">The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of **glClear**.</span></span> <span data-ttu-id="df503-135">A caixa de tesoura limita a região limpa.</span><span class="sxs-lookup"><span data-stu-id="df503-135">The scissor box bounds the cleared region.</span></span> <span data-ttu-id="df503-136">A função **glClear** ignora a função Alpha, a função Blend, a operação lógica, a estêncil, o mapeamento de textura e o buffer *z*.</span><span class="sxs-lookup"><span data-stu-id="df503-136">The **glClear** function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and *z*-buffering.</span></span>

<span data-ttu-id="df503-137">A função **glClear** usa um único argumento (*Mask*) que é o bit a bit ou vários valores indicando qual buffer deve ser limpo.</span><span class="sxs-lookup"><span data-stu-id="df503-137">The **glClear** function takes a single argument (*mask*) that is the bitwise OR of several values indicating which buffer is to be cleared.</span></span>

<span data-ttu-id="df503-138">O valor para o qual cada buffer é limpo depende da configuração do valor de limpeza para esse buffer.</span><span class="sxs-lookup"><span data-stu-id="df503-138">The value to which each buffer is cleared depends on the setting of the clear value for that buffer.</span></span>

<span data-ttu-id="df503-139">Se um buffer não estiver presente, uma chamada **glClear** direcionada a esse buffer não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="df503-139">If a buffer is not present, a **glClear** call directed at that buffer has no effect.</span></span>

<span data-ttu-id="df503-140">As funções a seguir recuperam informações relacionadas ao **glClear**:</span><span class="sxs-lookup"><span data-stu-id="df503-140">The following functions retrieve information related to **glClear**:</span></span>

<span data-ttu-id="df503-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com argumento GL \_ Accum \_ valor de limpeza \_</span><span class="sxs-lookup"><span data-stu-id="df503-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="df503-142">**glGet** com \_ \_ valor claro de profundidade do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="df503-142">**glGet** with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

<span data-ttu-id="df503-143">**glGet** com o \_ \_ valor Clear do índice do Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="df503-143">**glGet** with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="df503-144">**glGet** com o \_ valor de \_ limpeza de cor do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="df503-144">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

<span data-ttu-id="df503-145">**glGet** com o \_ valor de \_ limpeza do estêncil GL do argumento \_</span><span class="sxs-lookup"><span data-stu-id="df503-145">**glGet** with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="df503-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df503-146">Requirements</span></span>



| <span data-ttu-id="df503-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="df503-147">Requirement</span></span> | <span data-ttu-id="df503-148">Valor</span><span class="sxs-lookup"><span data-stu-id="df503-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df503-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df503-149">Minimum supported client</span></span><br/> | <span data-ttu-id="df503-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df503-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="df503-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df503-151">Minimum supported server</span></span><br/> | <span data-ttu-id="df503-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="df503-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df503-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="df503-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="df503-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="df503-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="df503-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df503-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="df503-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df503-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="df503-157">DLL</span><span class="sxs-lookup"><span data-stu-id="df503-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df503-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df503-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df503-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="df503-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df503-160">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="df503-160">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="df503-161">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="df503-161">**glClearColor**</span></span>](glclearcolor.md)
</dt> <dt>

[<span data-ttu-id="df503-162">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="df503-162">**glClearDepth**</span></span>](glcleardepth.md)
</dt> <dt>

[<span data-ttu-id="df503-163">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="df503-163">**glClearIndex**</span></span>](glclearindex.md)
</dt> <dt>

[<span data-ttu-id="df503-164">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="df503-164">**glClearStencil**</span></span>](glclearstencil.md)
</dt> <dt>

[<span data-ttu-id="df503-165">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="df503-165">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="df503-166">**glGet**</span><span class="sxs-lookup"><span data-stu-id="df503-166">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="df503-167">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="df503-167">**glScissor**</span></span>](glscissor.md)
</dt> </dl>

 

 





