---
title: função glPrioritizeTextures (GL. h)
description: A função glPrioritizeTextures define a prioridade de residência de texturas.
ms.assetid: 09018c86-c667-4e43-a95a-51a8077aed33
keywords:
- função glPrioritizeTextures OpenGL
topic_type:
- apiref
api_name:
- glPrioritizeTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38ab4b1bd6b5f9682b4d8753e7e84f1f2b58a09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644436"
---
# <a name="glprioritizetextures-function"></a><span data-ttu-id="436d6-104">função glPrioritizeTextures</span><span class="sxs-lookup"><span data-stu-id="436d6-104">glPrioritizeTextures function</span></span>

<span data-ttu-id="436d6-105">A função **glPrioritizeTextures** define a prioridade de residência de texturas.</span><span class="sxs-lookup"><span data-stu-id="436d6-105">The **glPrioritizeTextures** function sets the residence priority of textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="436d6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="436d6-106">Syntax</span></span>


```C++
void WINAPI glPrioritizeTextures(
         GLsizei  n,
   const GLuint   *textures,
   const GLclampf *priorities
);
```



## <a name="parameters"></a><span data-ttu-id="436d6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="436d6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="436d6-108">*n*</span><span class="sxs-lookup"><span data-stu-id="436d6-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="436d6-109">O número de texturas a serem priorizadas.</span><span class="sxs-lookup"><span data-stu-id="436d6-109">The number of textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="436d6-110">*textura*</span><span class="sxs-lookup"><span data-stu-id="436d6-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="436d6-111">Um ponteiro para o primeiro elemento de uma matriz que contém os nomes das texturas a serem priorizadas.</span><span class="sxs-lookup"><span data-stu-id="436d6-111">A pointer to the first element of an array containing the names of the textures to be prioritized.</span></span>

</dd> <dt>

<span data-ttu-id="436d6-112">*suas*</span><span class="sxs-lookup"><span data-stu-id="436d6-112">*priorities*</span></span> 
</dt> <dd>

<span data-ttu-id="436d6-113">Um ponteiro para o primeiro elemento de uma matriz que contém as prioridades de textura.</span><span class="sxs-lookup"><span data-stu-id="436d6-113">A pointer to the first element of an array containing the texture priorities.</span></span> <span data-ttu-id="436d6-114">Uma prioridade fornecida em um elemento do parâmetro de *prioridades* se aplica à textura nomeada pelo elemento correspondente do parâmetro *Textures* .</span><span class="sxs-lookup"><span data-stu-id="436d6-114">A priority given in an element of the *priorities* parameter applies to the texture named by the corresponding element of the *textures* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="436d6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="436d6-115">Return value</span></span>

<span data-ttu-id="436d6-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="436d6-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="436d6-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="436d6-117">Error codes</span></span>

<span data-ttu-id="436d6-118">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="436d6-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="436d6-119">Name</span><span class="sxs-lookup"><span data-stu-id="436d6-119">Name</span></span>                                                                                                  | <span data-ttu-id="436d6-120">Significado</span><span class="sxs-lookup"><span data-stu-id="436d6-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="436d6-121"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="436d6-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="436d6-122">*n* era um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="436d6-122">*n* was a negative value.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="436d6-123"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="436d6-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="436d6-124">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="436d6-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="436d6-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="436d6-125">Remarks</span></span>

<span data-ttu-id="436d6-126">A função **glPrioritizeTextures** atribui as *n* prioridades de textura especificadas no parâmetro *prioridades* para as texturas *n* chamadas no parâmetro *texturas* .</span><span class="sxs-lookup"><span data-stu-id="436d6-126">The **glPrioritizeTextures** function assigns the *n* texture priorities specified in the *priorities* parameter to the *n* textures named in the *textures* parameter.</span></span> <span data-ttu-id="436d6-127">Em computadores com uma quantidade limitada de memória de textura, o OpenGL estabelece um "conjunto de trabalho" de texturas que são residentes na memória de textura.</span><span class="sxs-lookup"><span data-stu-id="436d6-127">On computers with a limited amount of texture memory, OpenGL establishes a "working set" of textures that are resident in texture memory.</span></span> <span data-ttu-id="436d6-128">Essas texturas podem ser associadas a um destino de textura de forma muito mais eficiente do que as texturas que não são residentes.</span><span class="sxs-lookup"><span data-stu-id="436d6-128">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="436d6-129">Ao especificar uma prioridade para cada textura, a função **glPrioritizeTextures** permite que você determine quais texturas devem ser residentes.</span><span class="sxs-lookup"><span data-stu-id="436d6-129">By specifying a priority for each texture, the **glPrioritizeTextures** function enables you to determine which textures should be resident.</span></span>

<span data-ttu-id="436d6-130">Os elementos de prioridades de textura em *prioridades* são clamped ao intervalo de \[ 0,0, 1,0 \] antes de serem atribuídos.</span><span class="sxs-lookup"><span data-stu-id="436d6-130">The texture priorities elements in *priorities* are clamped to the range \[0.0, 1.0\] before being assigned.</span></span> <span data-ttu-id="436d6-131">Zero indica a prioridade mais baixa; Portanto, as texturas com prioridade zero são menos prováveis de serem residentes.</span><span class="sxs-lookup"><span data-stu-id="436d6-131">Zero indicates the lowest priority; thus textures with priority zero are least likely to be resident.</span></span> <span data-ttu-id="436d6-132">O valor 1,0 indica a prioridade mais alta; Portanto, as texturas com prioridade 1,0 têm maior probabilidade de serem residentes.</span><span class="sxs-lookup"><span data-stu-id="436d6-132">The value 1.0 indicates the highest priority; thus textures with priority 1.0 are most likely to be resident.</span></span> <span data-ttu-id="436d6-133">No entanto, não há garantia de que as texturas sejam residentes até que sejam associadas.</span><span class="sxs-lookup"><span data-stu-id="436d6-133">However, textures are not guaranteed to be resident until they are bound.</span></span>

<span data-ttu-id="436d6-134">A função **glPrioritizeTextures** ignora as tentativas de priorizar a textura 0 ou qualquer nome de textura que não corresponda a uma textura existente.</span><span class="sxs-lookup"><span data-stu-id="436d6-134">The **glPrioritizeTextures** function ignores attempts to prioritize texture 0, or any texture name that does not correspond to an existing texture.</span></span> <span data-ttu-id="436d6-135">Nenhuma das funções nomeadas pelo parâmetro de *texturas* precisa estar associada a um destino de textura.</span><span class="sxs-lookup"><span data-stu-id="436d6-135">None of the functions named by the *textures* parameter need to be bound to a texture target.</span></span>

<span data-ttu-id="436d6-136">Se uma textura estiver associada no momento, você também poderá usar a função [**glTexParameter**](gltexparameter-functions.md) para definir sua prioridade.</span><span class="sxs-lookup"><span data-stu-id="436d6-136">If a texture is currently bound, you can also use the [**glTexParameter**](gltexparameter-functions.md) function to set its priority.</span></span> <span data-ttu-id="436d6-137">Essa é a única maneira de definir a prioridade de uma textura padrão.</span><span class="sxs-lookup"><span data-stu-id="436d6-137">This is the only way to set the priority of a default texture.</span></span>

<span data-ttu-id="436d6-138">Você pode incluir **glPrioritizeTextures** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="436d6-138">You can include **glPrioritizeTextures** in display lists.</span></span>

<span data-ttu-id="436d6-139">A função a seguir recupera a prioridade de uma textura atualmente associada relacionada a **glPrioritizeTextures**:</span><span class="sxs-lookup"><span data-stu-id="436d6-139">The following function retrieves the priority of a currently-bound texture related to **glPrioritizeTextures**:</span></span>

-   <span data-ttu-id="436d6-140">[**glGetTexParameter**](glgettexparameter.md) com prioridade de textura de nome de parâmetro GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="436d6-140">[**glGetTexParameter**](glgettexparameter.md) with parameter name GL\_TEXTURE\_PRIORITY</span></span>

> [!Note]  
> <span data-ttu-id="436d6-141">A função **glPrioritizeTextures** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="436d6-141">The **glPrioritizeTextures** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="436d6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="436d6-142">Requirements</span></span>



| <span data-ttu-id="436d6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="436d6-143">Requirement</span></span> | <span data-ttu-id="436d6-144">Valor</span><span class="sxs-lookup"><span data-stu-id="436d6-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="436d6-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="436d6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="436d6-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="436d6-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="436d6-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="436d6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="436d6-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="436d6-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="436d6-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="436d6-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="436d6-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="436d6-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="436d6-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="436d6-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="436d6-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="436d6-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="436d6-153">DLL</span><span class="sxs-lookup"><span data-stu-id="436d6-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="436d6-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="436d6-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="436d6-155">Consulte também</span><span class="sxs-lookup"><span data-stu-id="436d6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="436d6-156">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="436d6-156">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="436d6-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="436d6-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="436d6-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="436d6-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="436d6-159">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="436d6-159">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="436d6-160">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="436d6-160">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="436d6-161">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="436d6-161">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="436d6-162">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="436d6-162">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





