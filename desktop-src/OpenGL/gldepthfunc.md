---
title: função glDepthFunc (GL. h)
description: A função glDepthFunc especifica o valor usado para comparações de buffer de profundidade.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- função glDepthFunc OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454855"
---
# <a name="gldepthfunc-function"></a><span data-ttu-id="6d656-104">função glDepthFunc</span><span class="sxs-lookup"><span data-stu-id="6d656-104">glDepthFunc function</span></span>

<span data-ttu-id="6d656-105">A função **glDepthFunc** especifica o valor usado para comparações de buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="6d656-105">The **glDepthFunc** function specifies the value used for depth-buffer comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d656-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d656-106">Syntax</span></span>


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a><span data-ttu-id="6d656-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d656-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d656-108">*func*</span><span class="sxs-lookup"><span data-stu-id="6d656-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="6d656-109">Especifica a função de comparação de profundidade.</span><span class="sxs-lookup"><span data-stu-id="6d656-109">Specifies the depth-comparison function.</span></span> <span data-ttu-id="6d656-110">As constantes simbólicas a seguir são aceitas.</span><span class="sxs-lookup"><span data-stu-id="6d656-110">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="6d656-111">Valor</span><span class="sxs-lookup"><span data-stu-id="6d656-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="6d656-112">Significado</span><span class="sxs-lookup"><span data-stu-id="6d656-112">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="6d656-113"><dt>**GL \_ nunca**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="6d656-114">Nunca passa.</span><span class="sxs-lookup"><span data-stu-id="6d656-114">Never passes.</span></span><br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="6d656-115"><dt>**GL \_ menos**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="6d656-116">Passa se o valor *z* de entrada for menor que o valor *z* armazenado.</span><span class="sxs-lookup"><span data-stu-id="6d656-116">Passes if the incoming *z* value is less than the stored *z* value.</span></span> <span data-ttu-id="6d656-117">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="6d656-117">This is the default value.</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="6d656-118"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-118"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="6d656-119">Passa se o valor z de entrada for menor ou igual ao valor z armazenado.</span><span class="sxs-lookup"><span data-stu-id="6d656-119">Passes if the incoming z value is less than or equal to the stored z value.</span></span><br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="6d656-120"><dt>**GL \_ igual a**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-120"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="6d656-121">Passa se o valor z de entrada for igual ao valor z armazenado.</span><span class="sxs-lookup"><span data-stu-id="6d656-121">Passes if the incoming z value is equal to the stored z value.</span></span><br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="6d656-122"><dt>**GL \_ maior**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-122"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="6d656-123">Passa se o valor z de entrada for maior que o valor z armazenado.</span><span class="sxs-lookup"><span data-stu-id="6d656-123">Passes if the incoming z value is greater than the stored z value.</span></span><br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="6d656-124"><dt>**GL não \_ igual**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-124"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="6d656-125">Passa se o valor z de entrada não for igual ao valor z armazenado.</span><span class="sxs-lookup"><span data-stu-id="6d656-125">Passes if the incoming z value is not equal to the stored z value.</span></span><br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="6d656-126"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-126"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="6d656-127">Passa se o valor z de entrada for maior ou igual ao valor z armazenado.</span><span class="sxs-lookup"><span data-stu-id="6d656-127">Passes if the incoming z value is greater than or equal to the stored z value.</span></span><br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="6d656-128"><dt>**GL \_ sempre**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="6d656-129">Sempre passa.</span><span class="sxs-lookup"><span data-stu-id="6d656-129">Always passes.</span></span><br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d656-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d656-130">Return value</span></span>

<span data-ttu-id="6d656-131">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6d656-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d656-132">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6d656-132">Error codes</span></span>

<span data-ttu-id="6d656-133">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6d656-133">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6d656-134">Nome</span><span class="sxs-lookup"><span data-stu-id="6d656-134">Name</span></span>                                                                                                  | <span data-ttu-id="6d656-135">Significado</span><span class="sxs-lookup"><span data-stu-id="6d656-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d656-136"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6d656-137">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6d656-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6d656-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d656-138">Remarks</span></span>

<span data-ttu-id="6d656-139">A função **glDepthFunc** especifica a função usada para comparar cada valor de pixel *z* de entrada com o valor *z* presente no buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="6d656-139">The **glDepthFunc** function specifies the function used to compare each incoming pixel *z* value with the *z* value present in the depth buffer.</span></span> <span data-ttu-id="6d656-140">A comparação será executada somente se o teste de profundidade estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="6d656-140">The comparison is performed only if depth testing is enabled.</span></span> <span data-ttu-id="6d656-141">(Consulte [**glEnable**](glenable.md) com o argumento GL \_ teste de profundidade \_ .)</span><span class="sxs-lookup"><span data-stu-id="6d656-141">(See [**glEnable**](glenable.md) with the argument GL\_DEPTH\_TEST.)</span></span>

<span data-ttu-id="6d656-142">Inicialmente, o teste de profundidade está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6d656-142">Initially, depth testing is disabled.</span></span>

<span data-ttu-id="6d656-143">As funções a seguir recuperam informações relacionadas ao **glDepthFunc**:</span><span class="sxs-lookup"><span data-stu-id="6d656-143">The following functions retrieve information related to **glDepthFunc**:</span></span>

<span data-ttu-id="6d656-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Depth \_ Func</span><span class="sxs-lookup"><span data-stu-id="6d656-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_FUNC</span></span>

<span data-ttu-id="6d656-145">[**glIsEnabled**](glisenabled.md) com teste de profundidade do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="6d656-145">[**glIsEnabled**](glisenabled.md) with argument GL\_DEPTH\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="6d656-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d656-146">Requirements</span></span>



| <span data-ttu-id="6d656-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d656-147">Requirement</span></span> | <span data-ttu-id="6d656-148">Valor</span><span class="sxs-lookup"><span data-stu-id="6d656-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d656-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d656-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6d656-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d656-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d656-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d656-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6d656-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d656-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d656-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6d656-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d656-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6d656-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d656-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d656-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d656-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6d656-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d656-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d656-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d656-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d656-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d656-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6d656-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6d656-161">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="6d656-161">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="6d656-162">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="6d656-162">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="6d656-163">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6d656-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6d656-164">**glGet**</span><span class="sxs-lookup"><span data-stu-id="6d656-164">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6d656-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="6d656-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





