---
title: função glDeleteTextures (GL. h)
description: A função glDeleteTextures exclui as texturas nomeadas.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- função glDeleteTextures OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454799"
---
# <a name="gldeletetextures-function"></a><span data-ttu-id="db153-104">função glDeleteTextures</span><span class="sxs-lookup"><span data-stu-id="db153-104">glDeleteTextures function</span></span>

<span data-ttu-id="db153-105">A função **glDeleteTextures** exclui as texturas nomeadas.</span><span class="sxs-lookup"><span data-stu-id="db153-105">The **glDeleteTextures** function deletes named textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="db153-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db153-106">Syntax</span></span>


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a><span data-ttu-id="db153-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db153-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db153-108">*n*</span><span class="sxs-lookup"><span data-stu-id="db153-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="db153-109">O número de texturas a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="db153-109">The number of textures to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="db153-110">*textura*</span><span class="sxs-lookup"><span data-stu-id="db153-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="db153-111">Uma matriz de texturas a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="db153-111">An array of textures to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db153-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db153-112">Return value</span></span>

<span data-ttu-id="db153-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="db153-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="db153-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="db153-114">Error codes</span></span>

<span data-ttu-id="db153-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="db153-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="db153-116">Nome</span><span class="sxs-lookup"><span data-stu-id="db153-116">Name</span></span>                                                                                                  | <span data-ttu-id="db153-117">Significado</span><span class="sxs-lookup"><span data-stu-id="db153-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db153-118"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db153-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="db153-119">*n* era um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="db153-119">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="db153-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="db153-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="db153-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="db153-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="db153-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="db153-122">Remarks</span></span>

<span data-ttu-id="db153-123">A função **glDeleteTextures** exclui *n* texturas nomeadas pelos elementos das *texturas* de matriz.</span><span class="sxs-lookup"><span data-stu-id="db153-123">The **glDeleteTextures** function deletes *n* textures named by the elements of the array *textures*.</span></span> <span data-ttu-id="db153-124">Depois que uma textura é excluída, ela não tem nenhum conteúdo ou dimensionalidade, e seu nome é gratuito para reutilização (por exemplo, por **glGenTextures**).</span><span class="sxs-lookup"><span data-stu-id="db153-124">After a texture is deleted, it has no contents or dimensionality, and its name is free for reuse (for example, by **glGenTextures**).</span></span> <span data-ttu-id="db153-125">A função **glDeleteTextures** ignora zeros e nomes que não correspondem a texturas existentes.</span><span class="sxs-lookup"><span data-stu-id="db153-125">The **glDeleteTextures** function ignores zeros and names that do not correspond to existing textures.</span></span>

<span data-ttu-id="db153-126">Se uma textura atualmente associada for excluída, a associação será revertida para zero (a textura padrão).</span><span class="sxs-lookup"><span data-stu-id="db153-126">If a texture that is currently bound is deleted, the binding reverts to zero (the default texture).</span></span>

<span data-ttu-id="db153-127">Você não pode incluir chamadas para **glDeleteTextures** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="db153-127">You cannot include calls to **glDeleteTextures** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="db153-128">A função **glDeleteTextures** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="db153-128">The **glDeleteTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="db153-129">A função a seguir recupera informações relacionadas a **glDeleteTextures**:</span><span class="sxs-lookup"><span data-stu-id="db153-129">The following function retrieves information related to **glDeleteTextures**:</span></span>

-   [<span data-ttu-id="db153-130">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="db153-130">**glIsTexture**</span></span>](glistexture.md)

## <a name="requirements"></a><span data-ttu-id="db153-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db153-131">Requirements</span></span>



| <span data-ttu-id="db153-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="db153-132">Requirement</span></span> | <span data-ttu-id="db153-133">Valor</span><span class="sxs-lookup"><span data-stu-id="db153-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db153-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db153-134">Minimum supported client</span></span><br/> | <span data-ttu-id="db153-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db153-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="db153-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db153-136">Minimum supported server</span></span><br/> | <span data-ttu-id="db153-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="db153-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db153-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="db153-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="db153-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="db153-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="db153-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="db153-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="db153-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db153-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="db153-142">DLL</span><span class="sxs-lookup"><span data-stu-id="db153-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db153-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db153-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db153-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="db153-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db153-145">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="db153-145">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="db153-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="db153-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="db153-147">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="db153-147">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="db153-148">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="db153-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="db153-149">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="db153-149">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="db153-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="db153-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="db153-151">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="db153-151">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="db153-152">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="db153-152">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="db153-153">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="db153-153">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="db153-154">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="db153-154">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="db153-155">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="db153-155">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="db153-156">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="db153-156">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="db153-157">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="db153-157">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





