---
title: função glGetTexParameterfv (GL. h)
description: As funções glGetTexParameterfv e glGetTexParameteriv retornam valores de parâmetro de textura. | função glGetTexParameterfv (GL. h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- função glGetTexParameterfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0af6e5fd91d38240dd3463b9440333b5da431d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105794437"
---
# <a name="glgettexparameterfv-function"></a><span data-ttu-id="b9f43-105">função glGetTexParameterfv</span><span class="sxs-lookup"><span data-stu-id="b9f43-105">glGetTexParameterfv function</span></span>

<span data-ttu-id="b9f43-106">As funções **glGetTexParameterfv** e [**glGetTexParameteriv**](glgettexparameteriv.md) retornam valores de parâmetro de textura.</span><span class="sxs-lookup"><span data-stu-id="b9f43-106">The **glGetTexParameterfv** and [**glGetTexParameteriv**](glgettexparameteriv.md) functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9f43-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9f43-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="b9f43-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9f43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9f43-109">*destino*</span><span class="sxs-lookup"><span data-stu-id="b9f43-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f43-110">O nome simbólico da textura de destino.</span><span class="sxs-lookup"><span data-stu-id="b9f43-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="b9f43-111">A textura GL \_ \_ 1D e GL de \_ textura \_ 2D são aceitas.</span><span class="sxs-lookup"><span data-stu-id="b9f43-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b9f43-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="b9f43-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f43-113">O nome simbólico de um parâmetro de textura.</span><span class="sxs-lookup"><span data-stu-id="b9f43-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="b9f43-114">Os valores a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="b9f43-114">The following values are accepted.</span></span>



| <span data-ttu-id="b9f43-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b9f43-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="b9f43-116">Significado</span><span class="sxs-lookup"><span data-stu-id="b9f43-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="b9f43-117"><dt>**\_ \_ filtro mag de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="b9f43-118">Retorna o filtro de ampliação de textura de valor único, uma constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="b9f43-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="b9f43-119"><dt>**\_filtro de \_ mínimo de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="b9f43-120">Retorna o filtro de minificação de textura de valor único, uma constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="b9f43-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="b9f43-121"><dt>**\_S de \_ encapsulamento de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="b9f43-122">Retorna a função de disposição de valor único para as coordenadas de textura *s*, uma constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="b9f43-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="b9f43-123"><dt>**\_ \_ & encapsulamento de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="b9f43-124">Retorna a função de disposição de valor único para a coordenada de textura *t*, uma constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="b9f43-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="b9f43-125"><dt>**\_cor da \_ borda da textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="b9f43-126">Retorna quatro números inteiros ou de ponto flutuante que compõem a cor RGBA da borda da textura.</span><span class="sxs-lookup"><span data-stu-id="b9f43-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="b9f43-127">Os valores de ponto flutuante são retornados no intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b9f43-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="b9f43-128">Os valores inteiros são retornados como um mapeamento linear da representação de ponto flutuante interno, de modo que 1,0 é mapeado para o inteiro representável mais positivo e-1,0 é mapeado para o número de inteiro reapresentável mais negativo.</span><span class="sxs-lookup"><span data-stu-id="b9f43-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="b9f43-129"><dt>**\_prioridade de textura GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="b9f43-130">Retorna a prioridade de residência da textura de destino (ou a textura nomeada associada a ela).</span><span class="sxs-lookup"><span data-stu-id="b9f43-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="b9f43-131">O valor inicial é 1.</span><span class="sxs-lookup"><span data-stu-id="b9f43-131">The initial value is 1.</span></span> <span data-ttu-id="b9f43-132">Consulte [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="b9f43-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="b9f43-133"><dt>**de \_ textura GL \_ residente**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="b9f43-134">Retorna o status de residência da textura de destino.</span><span class="sxs-lookup"><span data-stu-id="b9f43-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="b9f43-135">Se o valor retornado em params for GL \_ true, a textura será residente na memória de textura.</span><span class="sxs-lookup"><span data-stu-id="b9f43-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="b9f43-136">Consulte [**glAreTexturesResident**](glaretexturesresident.md).</span><span class="sxs-lookup"><span data-stu-id="b9f43-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="b9f43-137">*params*</span><span class="sxs-lookup"><span data-stu-id="b9f43-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b9f43-138">Retorna os parâmetros de textura.</span><span class="sxs-lookup"><span data-stu-id="b9f43-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9f43-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9f43-139">Return value</span></span>

<span data-ttu-id="b9f43-140">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b9f43-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9f43-141">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b9f43-141">Error codes</span></span>

<span data-ttu-id="b9f43-142">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b9f43-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b9f43-143">Nome</span><span class="sxs-lookup"><span data-stu-id="b9f43-143">Name</span></span>                                                                                                  | <span data-ttu-id="b9f43-144">Significado</span><span class="sxs-lookup"><span data-stu-id="b9f43-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9f43-145"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b9f43-146">o *destino* ou o *nome* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="b9f43-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b9f43-147"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b9f43-148">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b9f43-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b9f43-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9f43-149">Remarks</span></span>

<span data-ttu-id="b9f43-150">A função **glGetTexParameter** retorna em *params* o valor ou os valores do parâmetro de textura especificado como *pname*.</span><span class="sxs-lookup"><span data-stu-id="b9f43-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="b9f43-151">O parâmetro de *destino* define a textura de destino, ou seja, GL \_ textura \_ 1D ou GL \_ \_ de textura 2D, para especificar um texturing unidimensional ou bidimensional.</span><span class="sxs-lookup"><span data-stu-id="b9f43-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="b9f43-152">O parâmetro *pname* aceita os mesmos símbolos que [**glTexParameter**](gltexparameter-functions.md), com as mesmas interpretações.</span><span class="sxs-lookup"><span data-stu-id="b9f43-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="b9f43-153">Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.</span><span class="sxs-lookup"><span data-stu-id="b9f43-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9f43-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9f43-154">Requirements</span></span>



| <span data-ttu-id="b9f43-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9f43-155">Requirement</span></span> | <span data-ttu-id="b9f43-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b9f43-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f43-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9f43-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f43-158">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9f43-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9f43-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9f43-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f43-160">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9f43-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9f43-161">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b9f43-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9f43-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b9f43-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9f43-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9f43-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9f43-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b9f43-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9f43-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9f43-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9f43-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9f43-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f43-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b9f43-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b9f43-169">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b9f43-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b9f43-170">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="b9f43-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





