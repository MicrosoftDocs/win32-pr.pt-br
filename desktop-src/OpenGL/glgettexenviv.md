---
title: função glGetTexEnviv (GL. h)
description: As funções glGetTexEnvfv e glGetTexEnviv retornam parâmetros de ambiente de textura. | função glGetTexEnviv (GL. h)
ms.assetid: c1429cb9-4392-41ef-a978-a51db66445f2
keywords:
- função glGetTexEnviv OpenGL
topic_type:
- apiref
api_name:
- glGetTexEnviv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff222b7de0bfcd5fa50e9fa5f260e329c60c69d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754143"
---
# <a name="glgettexenviv-function"></a><span data-ttu-id="251f5-105">função glGetTexEnviv</span><span class="sxs-lookup"><span data-stu-id="251f5-105">glGetTexEnviv function</span></span>

<span data-ttu-id="251f5-106">As funções [**glGetTexEnvfv**](glgettexenvfv.md) e **glGetTexEnviv** retornam parâmetros de ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="251f5-106">The [**glGetTexEnvfv**](glgettexenvfv.md) and **glGetTexEnviv** functions return texture environment parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="251f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="251f5-107">Syntax</span></span>


```C++
void WINAPI glGetTexEnviv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="251f5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="251f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="251f5-109">*destino*</span><span class="sxs-lookup"><span data-stu-id="251f5-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="251f5-110">Um ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="251f5-110">A texture environment.</span></span> <span data-ttu-id="251f5-111">Deve ser GL \_ Texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="251f5-111">Must be GL\_TEXTURE\_ENV.</span></span>

</dd> <dt>

<span data-ttu-id="251f5-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="251f5-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="251f5-113">O nome simbólico de um parâmetro de ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="251f5-113">The symbolic name of a texture environment parameter.</span></span> <span data-ttu-id="251f5-114">Os valores a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="251f5-114">The following values are accepted.</span></span>



| <span data-ttu-id="251f5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="251f5-115">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="251f5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="251f5-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span><dl> <span data-ttu-id="251f5-117"><dt>**modo do GL \_ Texture \_ env \_**</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-117"><dt>**GL\_TEXTURE\_ENV\_MODE**</dt></span></span> </dl>    | <span data-ttu-id="251f5-118">O parâmetro *params* retorna o modo de ambiente de textura de valor único, uma constante simbólica.</span><span class="sxs-lookup"><span data-stu-id="251f5-118">The *params* parameter returns the single-valued texture environment mode, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span><dl> <span data-ttu-id="251f5-119"><dt>**cor do GL \_ Texture \_ env \_**</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-119"><dt>**GL\_TEXTURE\_ENV\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="251f5-120">O parâmetro *params* retorna quatro valores inteiros ou de ponto flutuante que são a cor do ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="251f5-120">The *params* parameter returns four integer or floating-point values that are the texture environment color.</span></span> <span data-ttu-id="251f5-121">Os valores inteiros, quando solicitados, são mapeados linearmente da representação de ponto flutuante interna, de modo que 1,0 é mapeado para o inteiro representável mais positivo e-1,0 é mapeado para o inteiro representável mais negativo.</span><span class="sxs-lookup"><span data-stu-id="251f5-121">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer, and -1.0 maps to the most negative representable integer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="251f5-122">*params*</span><span class="sxs-lookup"><span data-stu-id="251f5-122">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="251f5-123">Retorna os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="251f5-123">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="251f5-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="251f5-124">Return value</span></span>

<span data-ttu-id="251f5-125">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="251f5-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="251f5-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="251f5-126">Error codes</span></span>

<span data-ttu-id="251f5-127">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="251f5-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="251f5-128">Nome</span><span class="sxs-lookup"><span data-stu-id="251f5-128">Name</span></span>                                                                                                  | <span data-ttu-id="251f5-129">Significado</span><span class="sxs-lookup"><span data-stu-id="251f5-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="251f5-130"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="251f5-131">*target* ou *pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="251f5-131">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="251f5-132"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="251f5-133">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="251f5-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="251f5-134">Remarks</span></span>

<span data-ttu-id="251f5-135">A função **glGetTexEnv** retorna em *params* valores selecionados de um ambiente de textura que foi especificado com [**glTexEnv**](gltexenv-functions.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-135">The **glGetTexEnv** function returns in *params* selected values of a texture environment that was specified with [**glTexEnv**](gltexenv-functions.md).</span></span> <span data-ttu-id="251f5-136">O parâmetro de *destino* especifica um ambiente de textura.</span><span class="sxs-lookup"><span data-stu-id="251f5-136">The *target* parameter specifies a texture environment.</span></span> <span data-ttu-id="251f5-137">Atualmente, apenas um ambiente de textura é definido e tem suporte: GL \_ Texture \_ env.</span><span class="sxs-lookup"><span data-stu-id="251f5-137">Currently, only one texture environment is defined and supported: GL\_TEXTURE\_ENV.</span></span>

<span data-ttu-id="251f5-138">O parâmetro *pname* nomeia um parâmetro de ambiente de textura específico.</span><span class="sxs-lookup"><span data-stu-id="251f5-138">The *pname* parameter names a specific texture environment parameter.</span></span>

<span data-ttu-id="251f5-139">Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.</span><span class="sxs-lookup"><span data-stu-id="251f5-139">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="251f5-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="251f5-140">Requirements</span></span>



| <span data-ttu-id="251f5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="251f5-141">Requirement</span></span> | <span data-ttu-id="251f5-142">Valor</span><span class="sxs-lookup"><span data-stu-id="251f5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="251f5-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="251f5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="251f5-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="251f5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="251f5-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="251f5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="251f5-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="251f5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="251f5-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="251f5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="251f5-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="251f5-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="251f5-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="251f5-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="251f5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="251f5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="251f5-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="251f5-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="251f5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251f5-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="251f5-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="251f5-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="251f5-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="251f5-156">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="251f5-156">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





