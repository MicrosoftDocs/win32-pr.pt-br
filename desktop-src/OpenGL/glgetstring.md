---
title: função glGetString (GL. h)
description: A função glGetString retorna uma cadeia de caracteres que descreve a conexão OpenGL atual.
ms.assetid: 768e6ec2-3f00-44e6-b3cb-de0f06d6a73d
keywords:
- função glGetString OpenGL
topic_type:
- apiref
api_name:
- glGetString
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e263e35802af752fa262c898d036fccaa37aff87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919060"
---
# <a name="glgetstring-function"></a><span data-ttu-id="39117-104">função glGetString</span><span class="sxs-lookup"><span data-stu-id="39117-104">glGetString function</span></span>

<span data-ttu-id="39117-105">A função **glGetString** retorna uma cadeia de caracteres que descreve a conexão OpenGL atual.</span><span class="sxs-lookup"><span data-stu-id="39117-105">The **glGetString** function returns a string describing the current OpenGL connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="39117-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39117-106">Syntax</span></span>


```C++
const GLubyte* WINAPI glGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="39117-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39117-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39117-108">*name*</span><span class="sxs-lookup"><span data-stu-id="39117-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="39117-109">Uma das constantes simbólicas a seguir.</span><span class="sxs-lookup"><span data-stu-id="39117-109">One of the following symbolic constants.</span></span>



| <span data-ttu-id="39117-110">Valor</span><span class="sxs-lookup"><span data-stu-id="39117-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="39117-111">Significado</span><span class="sxs-lookup"><span data-stu-id="39117-111">Meaning</span></span>                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_VENDOR"></span><span id="gl_vendor"></span><dl> <span data-ttu-id="39117-112"><dt>**\_fornecedor GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39117-112"><dt>**GL\_VENDOR**</dt></span></span> </dl>             | <span data-ttu-id="39117-113">Retorna a empresa responsável por esta implementação OpenGL.</span><span class="sxs-lookup"><span data-stu-id="39117-113">Returns the company responsible for this OpenGL implementation.</span></span> <span data-ttu-id="39117-114">Esse nome não é alterado de Release para Release.</span><span class="sxs-lookup"><span data-stu-id="39117-114">This name does not change from release to release.</span></span><br/>                                                  |
| <span id="GL_RENDERER"></span><span id="gl_renderer"></span><dl> <span data-ttu-id="39117-115"><dt>**\_renderizador GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39117-115"><dt>**GL\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="39117-116">Retorna o nome do renderizador.</span><span class="sxs-lookup"><span data-stu-id="39117-116">Returns the name of the renderer.</span></span> <span data-ttu-id="39117-117">Esse nome é normalmente específico para uma configuração específica de uma plataforma de hardware.</span><span class="sxs-lookup"><span data-stu-id="39117-117">This name is typically specific to a particular configuration of a hardware platform.</span></span> <span data-ttu-id="39117-118">Ele não muda de liberação para liberação.</span><span class="sxs-lookup"><span data-stu-id="39117-118">It does not change from release to release.</span></span><br/> |
| <span id="GL_VERSION"></span><span id="gl_version"></span><dl> <span data-ttu-id="39117-119"><dt>**versão do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39117-119"><dt>**GL\_VERSION**</dt></span></span> </dl>          | <span data-ttu-id="39117-120">Retorna uma versão ou um número de versão.</span><span class="sxs-lookup"><span data-stu-id="39117-120">Returns a version or release number.</span></span><br/>                                                                                                                                |
| <span id="GL_EXTENSIONS"></span><span id="gl_extensions"></span><dl> <span data-ttu-id="39117-121"><dt>**\_extensões GL**</dt></span><span class="sxs-lookup"><span data-stu-id="39117-121"><dt>**GL\_EXTENSIONS**</dt></span></span> </dl> | <span data-ttu-id="39117-122">Retorna uma lista separada por espaços de extensões com suporte para OpenGL.</span><span class="sxs-lookup"><span data-stu-id="39117-122">Returns a space-separated list of supported extensions to OpenGL.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="39117-123">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="39117-123">Error codes</span></span>

<span data-ttu-id="39117-124">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="39117-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="39117-125">Nome</span><span class="sxs-lookup"><span data-stu-id="39117-125">Name</span></span>                                                                                                  | <span data-ttu-id="39117-126">Significado</span><span class="sxs-lookup"><span data-stu-id="39117-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39117-127"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="39117-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="39117-128">o *nome* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="39117-128">*name* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="39117-129"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39117-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="39117-130">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="39117-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="39117-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="39117-131">Remarks</span></span>

<span data-ttu-id="39117-132">A função **glGetString** retorna um ponteiro para uma cadeia de caracteres estática que descreve algum aspecto da conexão OpenGL atual.</span><span class="sxs-lookup"><span data-stu-id="39117-132">The **glGetString** function returns a pointer to a static string describing some aspect of the current OpenGL connection.</span></span>

<span data-ttu-id="39117-133">Como o OpenGL não inclui consultas para as características de desempenho de uma implementação, espera-se que alguns aplicativos sejam gravados para reconhecer plataformas conhecidas e modificarão o uso do OpenGL com base nas características de desempenho conhecidas dessas plataformas.</span><span class="sxs-lookup"><span data-stu-id="39117-133">Because OpenGL does not include queries for the performance characteristics of an implementation, it is expected that some applications will be written to recognize known platforms and will modify their OpenGL usage based on known performance characteristics of these platforms.</span></span> <span data-ttu-id="39117-134">O fornecedor de cadeias de caracteres GL \_ e o \_ renderizador GL juntos especificam exclusivamente uma plataforma e não serão alterados de liberação para liberação.</span><span class="sxs-lookup"><span data-stu-id="39117-134">The strings GL\_VENDOR and GL\_RENDERER together uniquely specify a platform, and will not change from release to release.</span></span> <span data-ttu-id="39117-135">Eles devem ser usados como tais por algoritmos de reconhecimento de plataforma.</span><span class="sxs-lookup"><span data-stu-id="39117-135">They should be used as such by platform recognition algorithms.</span></span>

<span data-ttu-id="39117-136">O formato e o conteúdo da cadeia de caracteres que o **glGetString** retorna dependem da implementação, exceto pelo fato de que:</span><span class="sxs-lookup"><span data-stu-id="39117-136">The format and contents of the string that **glGetString** returns depend on the implementation, except that:</span></span>

-   <span data-ttu-id="39117-137">Os nomes de extensão não incluirão caracteres de espaço e serão separados por caracteres de espaço na cadeia de caracteres de \_ extensões GL.</span><span class="sxs-lookup"><span data-stu-id="39117-137">Extension names will not include space characters and will be separated by space characters in the GL\_EXTENSIONS string.</span></span>
-   <span data-ttu-id="39117-138">A \_ cadeia de caracteres da versão GL começa com um número de versão.</span><span class="sxs-lookup"><span data-stu-id="39117-138">The GL\_VERSION string begins with a version number.</span></span> <span data-ttu-id="39117-139">O número de versão usa um destes formulários:</span><span class="sxs-lookup"><span data-stu-id="39117-139">The version number uses one of these forms:</span></span>

    <span data-ttu-id="39117-140">*\_ número principal*. *\_ número secundário*</span><span class="sxs-lookup"><span data-stu-id="39117-140">*major\_number*.*minor\_number*</span></span>

    <span data-ttu-id="39117-141">*\_ número principal*. *\_ número secundário*. *\_ número de versão*</span><span class="sxs-lookup"><span data-stu-id="39117-141">*major\_number*.*minor\_number*.*release\_number*</span></span>

-   <span data-ttu-id="39117-142">As informações específicas do fornecedor podem seguir o número de versão.</span><span class="sxs-lookup"><span data-stu-id="39117-142">Vendor-specific information may follow the version number.</span></span> <span data-ttu-id="39117-143">Seu formato depende da implementação, mas um espaço sempre separa o número de versão e as informações específicas do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="39117-143">Its format depends on the implementation, but a space always separates the version number and the vendor-specific information.</span></span>
-   <span data-ttu-id="39117-144">Todas as cadeias de caracteres são terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="39117-144">All strings are null-terminated.</span></span>

<span data-ttu-id="39117-145">Se um erro for gerado, **glGetString** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="39117-145">If an error is generated, **glGetString** returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="39117-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39117-146">Requirements</span></span>



| <span data-ttu-id="39117-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="39117-147">Requirement</span></span> | <span data-ttu-id="39117-148">Valor</span><span class="sxs-lookup"><span data-stu-id="39117-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39117-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39117-149">Minimum supported client</span></span><br/> | <span data-ttu-id="39117-150">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39117-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="39117-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39117-151">Minimum supported server</span></span><br/> | <span data-ttu-id="39117-152">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39117-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39117-153">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="39117-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="39117-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39117-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="39117-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39117-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="39117-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39117-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="39117-157">DLL</span><span class="sxs-lookup"><span data-stu-id="39117-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39117-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39117-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39117-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="39117-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39117-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="39117-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="39117-161">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="39117-161">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





