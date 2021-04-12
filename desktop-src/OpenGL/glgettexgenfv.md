---
title: função glGetTexGenfv (GL. h)
description: As funções glGetTexGendv, glGetTexGenfv e glGetTexGeniv retornam parâmetros de geração de coordenadas de textura. | função glGetTexGenfv (GL. h)
ms.assetid: 3b5b78a2-6db6-4931-aabb-25624c5af2f6
keywords:
- função glGetTexGenfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexGenfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e527d0388b8aca7239ba1c51dccdce15de3cd8ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298219"
---
# <a name="glgettexgenfv-function"></a><span data-ttu-id="b069b-105">função glGetTexGenfv</span><span class="sxs-lookup"><span data-stu-id="b069b-105">glGetTexGenfv function</span></span>

<span data-ttu-id="b069b-106">As funções [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv** e [**glGetTexGeniv**](glgettexgeniv.md) retornam parâmetros de geração de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b069b-106">The [**glGetTexGendv**](glgettexgendv.md), **glGetTexGenfv**, and [**glGetTexGeniv**](glgettexgeniv.md) functions return texture coordinate generation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b069b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b069b-107">Syntax</span></span>


```C++
void WINAPI glGetTexGenfv(
   GLenum  coord,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="b069b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b069b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b069b-109">*coord*</span><span class="sxs-lookup"><span data-stu-id="b069b-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="b069b-110">Uma coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="b069b-110">A texture coordinate.</span></span> <span data-ttu-id="b069b-111">Deve ser GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="b069b-111">Must be GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="b069b-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="b069b-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="b069b-113">O nome simbólico do (s) valor (es) a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="b069b-113">The symbolic name of the value(s) to be returned.</span></span> <span data-ttu-id="b069b-114">Deve ser o \_ \_ modo do GL Texture Gen \_ ou o nome de uma das equações do plano de geração de textura: plano de \_ objeto GL \_ ou plano de \_ olho GL \_ .</span><span class="sxs-lookup"><span data-stu-id="b069b-114">Must be either GL\_TEXTURE\_GEN\_MODE or the name of one of the texture generation plane equations: GL\_OBJECT\_PLANE or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="b069b-115">Esses valores são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="b069b-115">These values are as follows.</span></span>



| <span data-ttu-id="b069b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b069b-116">Value</span></span>                                                                                                                                                                             | <span data-ttu-id="b069b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="b069b-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <span data-ttu-id="b069b-118"><dt>**modo do GL \_ Texture \_ Gen \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-118"><dt>**GL\_TEXTURE\_GEN\_MODE**</dt></span></span> </dl> | <span data-ttu-id="b069b-119">O parâmetro *params* retorna a função de geração de textura de valor único, uma constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="b069b-119">The *params* parameter returns the single-valued texture generation function, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <span data-ttu-id="b069b-120"><dt>**\_plano de objeto GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-120"><dt>**GL\_OBJECT\_PLANE**</dt></span></span> </dl>              | <span data-ttu-id="b069b-121">O parâmetro *params* retorna os quatro coeficientes da equação do plano que especificam a geração da coordenada linear do objeto.</span><span class="sxs-lookup"><span data-stu-id="b069b-121">The *params* parameter returns the four plane equation coefficients that specify object linear-coordinate generation.</span></span> <span data-ttu-id="b069b-122">Os valores inteiros, quando solicitado, são mapeados diretamente da representação de ponto flutuante interna.</span><span class="sxs-lookup"><span data-stu-id="b069b-122">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <span data-ttu-id="b069b-123"><dt>**\_plano de olho GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-123"><dt>**GL\_EYE\_PLANE**</dt></span></span> </dl>                       | <span data-ttu-id="b069b-124">O parâmetro *params* retorna os quatro coeficientes da equação do plano que especificam a geração de coordenadas lineares.</span><span class="sxs-lookup"><span data-stu-id="b069b-124">The *params* parameter returns the four plane equation coefficients that specify eye linear-coordinate generation.</span></span> <span data-ttu-id="b069b-125">Os valores inteiros, quando solicitado, são mapeados diretamente da representação de ponto flutuante interna.</span><span class="sxs-lookup"><span data-stu-id="b069b-125">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span> <span data-ttu-id="b069b-126">Os valores retornados são aqueles mantidos em coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="b069b-126">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="b069b-127">Eles não são iguais aos valores especificados usando [**glTexGen**](gltexgen-functions.md), a menos que a matriz modelview tenha sido identificada no momento em que **glTexGen** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="b069b-127">They are not equal to the values specified using [**glTexGen**](gltexgen-functions.md), unless the modelview matrix was identified at the time **glTexGen** was called.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b069b-128">*params*</span><span class="sxs-lookup"><span data-stu-id="b069b-128">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="b069b-129">Retorna os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="b069b-129">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b069b-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b069b-130">Return value</span></span>

<span data-ttu-id="b069b-131">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b069b-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b069b-132">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b069b-132">Error codes</span></span>

<span data-ttu-id="b069b-133">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b069b-133">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b069b-134">Nome</span><span class="sxs-lookup"><span data-stu-id="b069b-134">Name</span></span>                                                                                                  | <span data-ttu-id="b069b-135">Significado</span><span class="sxs-lookup"><span data-stu-id="b069b-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b069b-136"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-136"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b069b-137">*coord* ou *pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="b069b-137">*coord* or *pname* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b069b-138"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-138"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b069b-139">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b069b-139">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b069b-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="b069b-140">Remarks</span></span>

<span data-ttu-id="b069b-141">A função **glGetTexGen** retorna em *params* parâmetros selecionados de uma função de geração de coordenada de textura que você especificou com **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="b069b-141">The **glGetTexGen** function returns in *params* selected parameters of a texture-coordinate generation function that you specified with **glTexGen**.</span></span> <span data-ttu-id="b069b-142">O parâmetro *coord* nomeia uma das coordenadas de textura (*s*, *t*, *r*, *q*), usando a constante simbólica GL \_ s, GL \_ t, GL \_ r ou GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="b069b-142">The *coord* parameter names one of the (*s*, *t*, *r*, *q*) texture coordinates, using the symbolic constant GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

<span data-ttu-id="b069b-143">Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.</span><span class="sxs-lookup"><span data-stu-id="b069b-143">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b069b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b069b-144">Requirements</span></span>



| <span data-ttu-id="b069b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="b069b-145">Requirement</span></span> | <span data-ttu-id="b069b-146">Valor</span><span class="sxs-lookup"><span data-stu-id="b069b-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b069b-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b069b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b069b-148">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b069b-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b069b-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b069b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b069b-150">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b069b-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b069b-151">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b069b-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="b069b-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b069b-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b069b-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="b069b-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b069b-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b069b-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b069b-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b069b-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b069b-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="b069b-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b069b-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b069b-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b069b-159">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b069b-159">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b069b-160">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="b069b-160">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> </dl>

 

 





