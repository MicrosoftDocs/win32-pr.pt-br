---
title: função glAccum (GL. h)
description: A função glAccum opera no buffer de acumulação.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- função glAccum OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644761"
---
# <a name="glaccum-function"></a><span data-ttu-id="e41a5-104">função glAccum</span><span class="sxs-lookup"><span data-stu-id="e41a5-104">glAccum function</span></span>

<span data-ttu-id="e41a5-105">A função **glAccum** opera no buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-105">The **glAccum** function operates on the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e41a5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e41a5-106">Syntax</span></span>


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a><span data-ttu-id="e41a5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e41a5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41a5-108">*parar*</span><span class="sxs-lookup"><span data-stu-id="e41a5-108">*op*</span></span> 
</dt> <dd>

<span data-ttu-id="e41a5-109">A operação de buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-109">The accumulation buffer operation.</span></span> <span data-ttu-id="e41a5-110">As constantes simbólicas aceitas são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="e41a5-110">The accepted symbolic constants are as follows.</span></span>



| <span data-ttu-id="e41a5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="e41a5-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="e41a5-112">Significado</span><span class="sxs-lookup"><span data-stu-id="e41a5-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <span data-ttu-id="e41a5-113"><dt>**GL \_ Accum**</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-113"><dt>**GL\_ACCUM**</dt></span></span> </dl>    | <span data-ttu-id="e41a5-114">Obtém R, G, B e valores do buffer selecionado no momento para leitura (consulte [**glReadBuffer**](glreadbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="e41a5-114">Obtains R, G, B, and A values from the buffer currently selected for reading (see [**glReadBuffer**](glreadbuffer.md)).</span></span> <span data-ttu-id="e41a5-115">Cada valor de componente é dividido por 2 *n*  1, em que *n* é o número de bits alocados para cada componente de cor no buffer selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e41a5-115">Each component value is divided by 2 *n*  1, where *n* is the number of bits allocated to each color component in the currently selected buffer.</span></span> <span data-ttu-id="e41a5-116">O resultado é um valor de ponto flutuante no intervalo de \[ 0, 1 \] , que é multiplicado pelo *valor* e adicionado ao componente de pixel correspondente no buffer de acumulação, atualizando assim o buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-116">The result is a floating-point value in the range \[0,1\], which is multiplied by *value* and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.</span></span><br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <span data-ttu-id="e41a5-117"><dt>**\_carga GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-117"><dt>**GL\_LOAD**</dt></span></span> </dl>       | <span data-ttu-id="e41a5-118">Semelhante ao GL \_ Accum, exceto pelo fato de que o valor atual no buffer de acumulação não é usado no cálculo do novo valor.</span><span class="sxs-lookup"><span data-stu-id="e41a5-118">Similar to GL\_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value.</span></span> <span data-ttu-id="e41a5-119">Ou seja, os valores R, G, B e a do buffer selecionado atualmente são divididos por 2 *n*  1, multiplicados por *valor* e, em seguida, armazenados na célula de buffer de acumulação correspondente, substituindo o valor atual.</span><span class="sxs-lookup"><span data-stu-id="e41a5-119">That is, the R, G, B, and A values from the currently selected buffer are divided by 2 *n*  1, multiplied by *value*, and then stored in the corresponding accumulation buffer cell, overwriting the current value.</span></span><br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <span data-ttu-id="e41a5-120"><dt>**adição de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-120"><dt>**GL\_ADD**</dt></span></span> </dl>          | <span data-ttu-id="e41a5-121">Adiciona o *valor* a cada R, G, B e a no buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-121">Adds *value* to each R, G, B, and A in the accumulation buffer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <span data-ttu-id="e41a5-122"><dt>**\_mult GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-122"><dt>**GL\_MULT**</dt></span></span> </dl>       | <span data-ttu-id="e41a5-123">Multiplica cada R, G, B e A no buffer de acumulação por *valor* e retorna o componente dimensionado para seu local de buffer de acumulação correspondente.</span><span class="sxs-lookup"><span data-stu-id="e41a5-123">Multiplies each R, G, B, and A in the accumulation buffer by *value* and returns the scaled component to its corresponding accumulation buffer location.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <span data-ttu-id="e41a5-124"><dt>**retorno do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-124"><dt>**GL\_RETURN**</dt></span></span> </dl> | <span data-ttu-id="e41a5-125">Transfere valores de buffer de acumulação para o buffer de cores ou buffers selecionados atualmente para gravação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-125">Transfers accumulation buffer values to the color buffer or buffers currently selected for writing.</span></span> <span data-ttu-id="e41a5-126">Cada R, G, B e um componente é multiplicado por *valor*, então multiplicado por 2 *n*  1, clamped ao intervalo de \[ 0, 2 *n*  1 \] e armazenado na célula de buffer de exibição correspondente.</span><span class="sxs-lookup"><span data-stu-id="e41a5-126">Each R, G, B, and A component is multiplied by *value*, then multiplied by 2 *n*  1, clamped to the range \[0, 2 *n*  1 \], and stored in the corresponding display buffer cell.</span></span> <span data-ttu-id="e41a5-127">As únicas operações de fragmento que são aplicadas a essa transferência são propriedade de pixel, mola, pontilhamento e writemasks de cor.</span><span class="sxs-lookup"><span data-stu-id="e41a5-127">The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.</span></span><br/>                                                                        |



 

</dd> <dt>

<span data-ttu-id="e41a5-128">*value*</span><span class="sxs-lookup"><span data-stu-id="e41a5-128">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="e41a5-129">Um valor de ponto flutuante usado na operação de buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-129">A floating-point value used in the accumulation buffer operation.</span></span> <span data-ttu-id="e41a5-130">O parâmetro *op* determina como o *valor* é usado.</span><span class="sxs-lookup"><span data-stu-id="e41a5-130">The *op* parameter determines how *value* is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41a5-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e41a5-131">Return value</span></span>

<span data-ttu-id="e41a5-132">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e41a5-132">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e41a5-133">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e41a5-133">Error codes</span></span>

<span data-ttu-id="e41a5-134">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e41a5-134">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e41a5-135">Name</span><span class="sxs-lookup"><span data-stu-id="e41a5-135">Name</span></span>                                                                                                  | <span data-ttu-id="e41a5-136">Significado</span><span class="sxs-lookup"><span data-stu-id="e41a5-136">Meaning</span></span>                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e41a5-137"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-137"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e41a5-138">*op* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="e41a5-138">*op* was not an accepted value.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="e41a5-139"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e41a5-140">Não havia um buffer de acumulação ou a função **glAccum** foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e41a5-140">There was no accumulation buffer or the function **glAccum** was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e41a5-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="e41a5-141">Remarks</span></span>

<span data-ttu-id="e41a5-142">O buffer de acumulação é um buffer de cores de intervalo estendido.</span><span class="sxs-lookup"><span data-stu-id="e41a5-142">The accumulation buffer is an extended-range color buffer.</span></span> <span data-ttu-id="e41a5-143">As imagens não são renderizadas nela.</span><span class="sxs-lookup"><span data-stu-id="e41a5-143">Images are not rendered into it.</span></span> <span data-ttu-id="e41a5-144">Em vez disso, as imagens renderizadas em um dos buffers de cor são adicionadas ao conteúdo do buffer de acumulação após a renderização.</span><span class="sxs-lookup"><span data-stu-id="e41a5-144">Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering.</span></span> <span data-ttu-id="e41a5-145">Você pode criar efeitos como anti-aliasing (de pontos, linhas e polígonos), Desfoque de movimento e profundidade de campo acumulando imagens geradas com matrizes de transformação diferentes.</span><span class="sxs-lookup"><span data-stu-id="e41a5-145">You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.</span></span>

<span data-ttu-id="e41a5-146">Cada pixel no buffer de acumulação consiste em valores vermelho, verde, azul e alfa.</span><span class="sxs-lookup"><span data-stu-id="e41a5-146">Each pixel in the accumulation buffer consists of red, green, blue, and alpha values.</span></span> <span data-ttu-id="e41a5-147">O número de bits por componente no buffer de acumulação depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-147">The number of bits per component in the accumulation buffer depends on the implementation.</span></span> <span data-ttu-id="e41a5-148">Você pode examinar esse número chamando [**glGetIntegerv**](glgetintegerv.md) quatro vezes, com os argumentos GL \_ Accum \_ vermelho \_ bits, GL \_ Accum \_ verde \_ bits, GL \_ Accum \_ bits azuis \_ e GL \_ Accum \_ \_ bits alfa, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e41a5-148">You can examine this number by calling [**glGetIntegerv**](glgetintegerv.md) four times, with the arguments GL\_ACCUM\_RED\_BITS, GL\_ACCUM\_GREEN\_BITS, GL\_ACCUM\_BLUE\_BITS, and GL\_ACCUM\_ALPHA\_BITS, respectively.</span></span> <span data-ttu-id="e41a5-149">Independentemente do número de bits por componente, no entanto, o intervalo de valores armazenados por cada componente é \[ 1,? 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e41a5-149">Regardless of the number of bits per component, however, the range of values stored by each component is \[ 1,?1\].</span></span> <span data-ttu-id="e41a5-150">Os pixels do buffer de acumulação são mapeados um para um com framebuffer pixels.</span><span class="sxs-lookup"><span data-stu-id="e41a5-150">The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.</span></span>

<span data-ttu-id="e41a5-151">A função **glAccum** opera no buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-151">The **glAccum** function operates on the accumulation buffer.</span></span> <span data-ttu-id="e41a5-152">O primeiro argumento, *op*, é uma constante simbólica que seleciona uma operação de buffer de acumulação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-152">The first argument, *op*, is a symbolic constant that selects an accumulation buffer operation.</span></span> <span data-ttu-id="e41a5-153">O segundo argumento, *Value*, é um valor de ponto flutuante a ser usado nessa operação.</span><span class="sxs-lookup"><span data-stu-id="e41a5-153">The second argument, *value*, is a floating-point value to be used in that operation.</span></span> <span data-ttu-id="e41a5-154">Cinco operações são especificadas: GL \_ Accum, GL \_ upload, GL \_ Add, GL \_ mult, e GL \_ Return.</span><span class="sxs-lookup"><span data-stu-id="e41a5-154">Five operations are specified: GL\_ACCUM, GL\_LOAD, GL\_ADD, GL\_MULT, and GL\_RETURN.</span></span>

<span data-ttu-id="e41a5-155">Todas as operações de buffer de acumulação são limitadas à área da caixa de tesoura atual e são aplicadas de forma idêntica aos componentes vermelho, verde, azul e alfa de cada pixel.</span><span class="sxs-lookup"><span data-stu-id="e41a5-155">All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel.</span></span> <span data-ttu-id="e41a5-156">O conteúdo de um componente de pixel do buffer de acumulação será indefinido se a operação **glAccum** resultar em um valor fora do intervalo \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e41a5-156">The contents of an accumulation buffer pixel component are undefined if the **glAccum** operation results in a value outside the range \[ 1,1\].</span></span>

<span data-ttu-id="e41a5-157">Para limpar o buffer de acumulação, use a função [**glClearAccum**](glclearaccum.md) para especificar R, G, B e valores para defini-lo e emitir uma função [**glClear**](glclear.md) com o buffer de acumulação habilitado.</span><span class="sxs-lookup"><span data-stu-id="e41a5-157">To clear the accumulation buffer, use the [**glClearAccum**](glclearaccum.md) function to specify R, G, B, and A values to set it to, and issue a [**glClear**](glclear.md) function with the accumulation buffer enabled.</span></span>

<span data-ttu-id="e41a5-158">Somente os pixels dentro da caixa de tesoura atual são atualizados por qualquer operação **glAccum** .</span><span class="sxs-lookup"><span data-stu-id="e41a5-158">Only those pixels within the current scissor box are updated by any **glAccum** operation.</span></span>

<span data-ttu-id="e41a5-159">As funções a seguir recuperam informações relacionadas à função **glAccum** :</span><span class="sxs-lookup"><span data-stu-id="e41a5-159">The following functions retrieve information related to the **glAccum** function:</span></span>

<span data-ttu-id="e41a5-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ accuum \_ \_ bits vermelhos</span><span class="sxs-lookup"><span data-stu-id="e41a5-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_RED\_BITS</span></span>

<span data-ttu-id="e41a5-161">**glGet** com Argument GL \_ accuum \_ \_ bits verdes</span><span class="sxs-lookup"><span data-stu-id="e41a5-161">**glGet** with argument GL\_ACCUM\_GREEN\_BITS</span></span>

<span data-ttu-id="e41a5-162">**glGet** com argumento GL \_ Accum \_ \_ bits azuis</span><span class="sxs-lookup"><span data-stu-id="e41a5-162">**glGet** with argument GL\_ACCUM\_BLUE\_BITS</span></span>

<span data-ttu-id="e41a5-163">**glGet** com Argument GL \_ accuum \_ \_ bits alfa</span><span class="sxs-lookup"><span data-stu-id="e41a5-163">**glGet** with argument GL\_ACCUM\_ALPHA\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="e41a5-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e41a5-164">Requirements</span></span>



| <span data-ttu-id="e41a5-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="e41a5-165">Requirement</span></span> | <span data-ttu-id="e41a5-166">Valor</span><span class="sxs-lookup"><span data-stu-id="e41a5-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e41a5-167">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e41a5-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e41a5-168">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e41a5-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e41a5-169">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e41a5-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e41a5-170">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e41a5-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e41a5-171">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e41a5-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="e41a5-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e41a5-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e41a5-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="e41a5-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e41a5-175">DLL</span><span class="sxs-lookup"><span data-stu-id="e41a5-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e41a5-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e41a5-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e41a5-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="e41a5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41a5-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e41a5-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e41a5-179">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="e41a5-179">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="e41a5-180">**glClear**</span><span class="sxs-lookup"><span data-stu-id="e41a5-180">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="e41a5-181">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="e41a5-181">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="e41a5-182">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="e41a5-182">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="e41a5-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e41a5-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e41a5-184">**glGet**</span><span class="sxs-lookup"><span data-stu-id="e41a5-184">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e41a5-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="e41a5-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="e41a5-186">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="e41a5-186">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="e41a5-187">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="e41a5-187">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="e41a5-188">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="e41a5-188">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="e41a5-189">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="e41a5-189">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="e41a5-190">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="e41a5-190">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="e41a5-191">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="e41a5-191">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





