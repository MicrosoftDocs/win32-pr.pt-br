---
title: função glAreTexturesResident (GL. h)
description: A função glAreTexturesResident determina se os objetos de textura especificados são residentes na memória de textura.
ms.assetid: 55d068a8-d366-4fee-85d5-49373b8c5e02
keywords:
- função glAreTexturesResident OpenGL
topic_type:
- apiref
api_name:
- glAreTexturesResident
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e7e5965da9604c690384301de6f1879a98994
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778533"
---
# <a name="glaretexturesresident-function"></a><span data-ttu-id="e82d3-104">função glAreTexturesResident</span><span class="sxs-lookup"><span data-stu-id="e82d3-104">glAreTexturesResident function</span></span>

<span data-ttu-id="e82d3-105">A função **glAreTexturesResident** determina se os objetos de textura especificados são residentes na memória de textura.</span><span class="sxs-lookup"><span data-stu-id="e82d3-105">The **glAreTexturesResident** function determines whether specified texture objects are resident in texture memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e82d3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e82d3-106">Syntax</span></span>


```C++
GLboolean WINAPI glAreTexturesResident(
         GLsizei   n,
   const GLuint    *textures,
         GLboolean *residences
);
```



## <a name="parameters"></a><span data-ttu-id="e82d3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e82d3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e82d3-108">*n*</span><span class="sxs-lookup"><span data-stu-id="e82d3-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="e82d3-109">O número de texturas a serem consultadas.</span><span class="sxs-lookup"><span data-stu-id="e82d3-109">The number of textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="e82d3-110">*textura*</span><span class="sxs-lookup"><span data-stu-id="e82d3-110">*textures*</span></span> 
</dt> <dd>

<span data-ttu-id="e82d3-111">O endereço de uma matriz que contém os nomes das texturas a serem consultadas.</span><span class="sxs-lookup"><span data-stu-id="e82d3-111">The address of an array containing the names of the textures to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="e82d3-112">*residências*</span><span class="sxs-lookup"><span data-stu-id="e82d3-112">*residences*</span></span> 
</dt> <dd>

<span data-ttu-id="e82d3-113">O endereço de uma matriz na qual o status de residência de textura é retornado.</span><span class="sxs-lookup"><span data-stu-id="e82d3-113">The address of an array in which the texture residence status is returned.</span></span> <span data-ttu-id="e82d3-114">O status de residência de uma textura chamada por um elemento de *texturas* é retornado no elemento correspondente de *residências*.</span><span class="sxs-lookup"><span data-stu-id="e82d3-114">The residence status of a texture named by an element of *textures* is returned in the corresponding element of *residences*.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="e82d3-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e82d3-115">Error codes</span></span>

<span data-ttu-id="e82d3-116">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e82d3-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e82d3-117">Nome</span><span class="sxs-lookup"><span data-stu-id="e82d3-117">Name</span></span>                                                                                                  | <span data-ttu-id="e82d3-118">Significado</span><span class="sxs-lookup"><span data-stu-id="e82d3-118">Meaning</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e82d3-119"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e82d3-119"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="e82d3-120">*n* era um valor negativo, um elemento em *texturas* era zero ou um elemento em *texturas* não continha um identificador de textura.</span><span class="sxs-lookup"><span data-stu-id="e82d3-120">*n* was a negative value, an element in *textures* was zero, or an element in *textures* did not contain a texture identifier.</span></span><br/> |
| <dl> <span data-ttu-id="e82d3-121"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e82d3-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e82d3-122">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e82d3-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>     |



## <a name="remarks"></a><span data-ttu-id="e82d3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="e82d3-123">Remarks</span></span>

<span data-ttu-id="e82d3-124">Em computadores com uma quantidade limitada de memória de textura, o OpenGL estabelece um conjunto de trabalho de texturas que são residentes na memória de textura.</span><span class="sxs-lookup"><span data-stu-id="e82d3-124">On machines with a limited amount of texture memory, OpenGL establishes a working set of textures that are resident in texture memory.</span></span> <span data-ttu-id="e82d3-125">Essas texturas podem ser associadas a um destino de textura de forma muito mais eficiente do que as texturas que não são residentes.</span><span class="sxs-lookup"><span data-stu-id="e82d3-125">These textures can be bound to a texture target much more efficiently than textures that are not resident.</span></span>

<span data-ttu-id="e82d3-126">A função **glAreTexturesResident** consulta o status de residência de textura das *n* texturas nomeadas pelos elementos de *texturas*.</span><span class="sxs-lookup"><span data-stu-id="e82d3-126">The **glAreTexturesResident** function queries the texture residence status of the *n* textures named by the elements of *textures*.</span></span> <span data-ttu-id="e82d3-127">Se todas as texturas nomeadas forem residentes, **glAreTexturesResident** retornará GL \_ true e o conteúdo das *residências* não será incomodado.</span><span class="sxs-lookup"><span data-stu-id="e82d3-127">If all the named textures are resident, **glAreTexturesResident** returns GL\_TRUE, and the contents of *residences* are undisturbed.</span></span> <span data-ttu-id="e82d3-128">Se qualquer uma das texturas nomeadas não for residente, **glAreTexturesResident** retornará GL \_ false e o status detalhado será retornado nos elementos *n* de *residências*.</span><span class="sxs-lookup"><span data-stu-id="e82d3-128">If any of the named textures are not resident, **glAreTexturesResident** returns GL\_FALSE, and detailed status is returned in the *n* elements of *residences*.</span></span>

<span data-ttu-id="e82d3-129">Se um elemento de *residências* for GL \_ verdadeiro, a textura nomeada pelo elemento correspondente de *texturas* será residente na memória de textura.</span><span class="sxs-lookup"><span data-stu-id="e82d3-129">If an element of *residences* is GL\_TRUE, then the texture named by the corresponding element of *textures* is resident in texture memory.</span></span>

<span data-ttu-id="e82d3-130">Para consultar o status de residência de uma única textura acoplada, chame [**glGetTexParameter**](glgettexparameter.md) com o parâmetro de *destino* definido como a textura de destino à qual o destino está associado e defina o parâmetro *pname* para a \_ textura GL \_ residente.</span><span class="sxs-lookup"><span data-stu-id="e82d3-130">To query the residence status of a single bound texture, call [**glGetTexParameter**](glgettexparameter.md) with the *target* parameter set to the target texture to which the target is bound and set the *pname* parameter to GL\_TEXTURE\_RESIDENT.</span></span> <span data-ttu-id="e82d3-131">Você deve usar esse método para consultar o status residente de uma textura padrão.</span><span class="sxs-lookup"><span data-stu-id="e82d3-131">You must use this method to query the resident status of a default texture.</span></span>

<span data-ttu-id="e82d3-132">Você não pode incluir **glAreTexturesResident** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="e82d3-132">You cannot include **glAreTexturesResident** in display lists.</span></span>

<span data-ttu-id="e82d3-133">A função **glAreTexturesResident** retorna o status de residência das texturas no momento da invocação.</span><span class="sxs-lookup"><span data-stu-id="e82d3-133">The **glAreTexturesResident** function returns the residency status of the textures at the time of invocation.</span></span> <span data-ttu-id="e82d3-134">Ele não garante que as texturas permanecerão residentes em qualquer outro momento.</span><span class="sxs-lookup"><span data-stu-id="e82d3-134">It does not guarantee that the textures will remain resident at any other time.</span></span>

<span data-ttu-id="e82d3-135">Se as texturas residirem na memória virtual (não há memória de textura), elas serão consideradas sempre residentes.</span><span class="sxs-lookup"><span data-stu-id="e82d3-135">If textures reside in virtual memory (there is no texture memory), they are considered always resident.</span></span>

> [!Note]  
> <span data-ttu-id="e82d3-136">A função **glAreTexturesResident** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e82d3-136">The **glAreTexturesResident** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e82d3-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e82d3-137">Requirements</span></span>



| <span data-ttu-id="e82d3-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e82d3-138">Requirement</span></span> | <span data-ttu-id="e82d3-139">Valor</span><span class="sxs-lookup"><span data-stu-id="e82d3-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e82d3-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e82d3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e82d3-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e82d3-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e82d3-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e82d3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e82d3-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e82d3-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e82d3-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e82d3-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e82d3-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e82d3-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e82d3-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e82d3-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="e82d3-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e82d3-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e82d3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e82d3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e82d3-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e82d3-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e82d3-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="e82d3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e82d3-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e82d3-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e82d3-152">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="e82d3-152">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="e82d3-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e82d3-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e82d3-154">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="e82d3-154">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="e82d3-155">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="e82d3-155">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="e82d3-156">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="e82d3-156">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="e82d3-157">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="e82d3-157">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





