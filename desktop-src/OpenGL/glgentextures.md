---
title: função glGenTextures (GL. h)
description: A função glGenTextures gera nomes de textura.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- função glGenTextures OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204a5d4fb736a88cf615577f4c740cde15d75829
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919061"
---
# <a name="glgentextures-function"></a><span data-ttu-id="3c1ea-104">função glGenTextures</span><span class="sxs-lookup"><span data-stu-id="3c1ea-104">glGenTextures function</span></span>

<span data-ttu-id="3c1ea-105">A função **glGenTextures** gera nomes de textura.</span><span class="sxs-lookup"><span data-stu-id="3c1ea-105">The **glGenTextures** function generates texture names.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1ea-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c1ea-106">Syntax</span></span>


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="3c1ea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c1ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c1ea-108">*n*</span><span class="sxs-lookup"><span data-stu-id="3c1ea-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="3c1ea-109">O número de nomes de textura a serem gerados.</span><span class="sxs-lookup"><span data-stu-id="3c1ea-109">The number of texture names to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="3c1ea-110">*textura*</span><span class="sxs-lookup"><span data-stu-id="3c1ea-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="3c1ea-111">Um ponteiro para o primeiro elemento de uma matriz na qual os nomes de textura gerados são armazenados.</span><span class="sxs-lookup"><span data-stu-id="3c1ea-111">A pointer to the first element of an array in which the generated texture names are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c1ea-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c1ea-112">Return value</span></span>

<span data-ttu-id="3c1ea-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3c1ea-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c1ea-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3c1ea-114">Error codes</span></span>

<span data-ttu-id="3c1ea-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3c1ea-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3c1ea-116">Nome</span><span class="sxs-lookup"><span data-stu-id="3c1ea-116">Name</span></span>                                                                                                  | <span data-ttu-id="3c1ea-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3c1ea-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c1ea-118"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c1ea-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="3c1ea-119">*n* era um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="3c1ea-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="3c1ea-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c1ea-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3c1ea-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3c1ea-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3c1ea-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c1ea-122">Remarks</span></span>

<span data-ttu-id="3c1ea-123">A função **glGenTextures** retorna *n* nomes de textura no parâmetro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="3c1ea-123">The **glGenTextures** function returns *n* texture names in the *textures* parameter.</span></span> <span data-ttu-id="3c1ea-124">Os nomes de textura não são necessariamente um conjunto contíguo de inteiros, no entanto, nenhum dos nomes retornados pode estar em uso imediatamente antes de chamar a função **glGenTextures** .</span><span class="sxs-lookup"><span data-stu-id="3c1ea-124">The texture names are not necessarily a contiguous set of integers, however, none of the returned names can have been in use immediately prior to calling the **glGenTextures** function.</span></span> <span data-ttu-id="3c1ea-125">As texturas geradas pressupõem a dimensionalidade do destino de textura ao qual elas são vinculadas pela primeira vez com a função [**glBindTexture**](glbindtexture.md) .</span><span class="sxs-lookup"><span data-stu-id="3c1ea-125">The generated textures assume the dimensionality of the texture target to which they are first bound with the [**glBindTexture**](glbindtexture.md) function.</span></span> <span data-ttu-id="3c1ea-126">Os nomes de textura retornados por **glGenTextures** não são retornados por chamadas subsequentes para **glGenTextures** , a menos que sejam excluídos primeiro com a chamada de [**glDeleteTextures**](gldeletetextures.md).</span><span class="sxs-lookup"><span data-stu-id="3c1ea-126">Texture names returned by **glGenTextures** are not returned by subsequent calls to **glGenTextures** unless they are first deleted by calling [**glDeleteTextures**](gldeletetextures.md).</span></span>

<span data-ttu-id="3c1ea-127">Você não pode incluir **glGenTextures** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="3c1ea-127">You cannot include **glGenTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="3c1ea-128">A função **glGenTextures** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3c1ea-128">The **glGenTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="3c1ea-129">A função a seguir recupera informações relacionadas a **glGenTextures**:</span><span class="sxs-lookup"><span data-stu-id="3c1ea-129">The following function retrieves information related to **glGenTextures**:</span></span>

-   [<span data-ttu-id="3c1ea-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="3c1ea-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c1ea-131">Requirements</span></span>



| <span data-ttu-id="3c1ea-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c1ea-132">Requirement</span></span> | <span data-ttu-id="3c1ea-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3c1ea-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c1ea-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c1ea-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3c1ea-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c1ea-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c1ea-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c1ea-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3c1ea-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c1ea-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c1ea-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3c1ea-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c1ea-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c1ea-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3c1ea-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c1ea-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c1ea-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c1ea-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c1ea-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3c1ea-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c1ea-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c1ea-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c1ea-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c1ea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1ea-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-146">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-146">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-147">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-147">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-149">**glGet**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-149">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-150">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-150">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-151">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-151">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-152">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-152">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-153">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-153">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="3c1ea-154">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="3c1ea-154">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





