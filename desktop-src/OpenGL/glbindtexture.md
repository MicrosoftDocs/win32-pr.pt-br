---
title: função glBindTexture (GL. h)
description: A função glBindTexture permite a criação de uma textura nomeada associada a um destino de textura.
ms.assetid: 800f2360-b40e-4911-9a45-6f310aeeefeb
keywords:
- função glBindTexture OpenGL
topic_type:
- apiref
api_name:
- glBindTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76009a486e3903ad8230891af8b7593ab8aaa47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369701"
---
# <a name="glbindtexture-function"></a><span data-ttu-id="8398f-104">função glBindTexture</span><span class="sxs-lookup"><span data-stu-id="8398f-104">glBindTexture function</span></span>

<span data-ttu-id="8398f-105">A função **glBindTexture** permite a criação de uma textura nomeada associada a um destino de textura.</span><span class="sxs-lookup"><span data-stu-id="8398f-105">The **glBindTexture** function enables the creation of a named texture that is bound to a texture target.</span></span>

## <a name="syntax"></a><span data-ttu-id="8398f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8398f-106">Syntax</span></span>


```C++
void WINAPI glBindTexture(
   GLenum target,
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="8398f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8398f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8398f-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="8398f-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8398f-109">O destino ao qual a textura está associada.</span><span class="sxs-lookup"><span data-stu-id="8398f-109">The target to which the texture is bound.</span></span> <span data-ttu-id="8398f-110">Deve ter o valor GL \_ Texture \_ 1D ou GL \_ Texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="8398f-110">Must have the value GL\_TEXTURE\_1D or GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="8398f-111">*textura*</span><span class="sxs-lookup"><span data-stu-id="8398f-111">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="8398f-112">O nome de uma textura; o nome da textura não pode estar em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="8398f-112">The name of a texture; the texture name cannot currently be in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8398f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8398f-113">Return value</span></span>

<span data-ttu-id="8398f-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8398f-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8398f-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8398f-115">Error codes</span></span>

<span data-ttu-id="8398f-116">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8398f-116">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8398f-117">Nome</span><span class="sxs-lookup"><span data-stu-id="8398f-117">Name</span></span>                                                                                                  | <span data-ttu-id="8398f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="8398f-118">Meaning</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8398f-119"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="8398f-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8398f-120">O parâmetro de *destino* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="8398f-120">The parameter *target* was not an accepted value.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="8398f-121"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8398f-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8398f-122">A *textura* do parâmetro não tinha a mesma dimensionalidade que o *destino* ou a função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8398f-122">The parameter *texture* did not have the same dimensionality as *target*, or the function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8398f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8398f-123">Remarks</span></span>

<span data-ttu-id="8398f-124">A função **glBindTexture** permite que você crie uma textura nomeada.</span><span class="sxs-lookup"><span data-stu-id="8398f-124">The **glBindTexture** function enables you to create a named texture.</span></span> <span data-ttu-id="8398f-125">Chamar **glBindTexture** com *target* definido como GL \_ Texture \_ 1D ou GL \_ Texture \_ 2D e *Texture* definido como o nome da nova textura que você criou associa o nome da textura ao destino de textura apropriado.</span><span class="sxs-lookup"><span data-stu-id="8398f-125">Calling **glBindTexture** with *target* set to GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, and *texture* set to the name of the new texture you have created binds the texture name to the appropriate texture target.</span></span> <span data-ttu-id="8398f-126">Quando uma textura é associada a um destino, a ligação anterior para esse destino não está mais em vigor.</span><span class="sxs-lookup"><span data-stu-id="8398f-126">When a texture is bound to a target, the previous binding for that target is no longer in effect.</span></span>

<span data-ttu-id="8398f-127">Os nomes de textura são inteiros sem sinal com o valor zero reservado para representar a textura padrão para cada destino de textura.</span><span class="sxs-lookup"><span data-stu-id="8398f-127">Texture names are unsigned integers with the value zero reserved to represent the default texture for each texture target.</span></span> <span data-ttu-id="8398f-128">Os nomes de textura e o conteúdo de textura correspondente são locais para o espaço de lista de exibição compartilhado do contexto de renderização OpenGL atual; dois contextos de renderização compartilham nomes de textura somente se eles também compartilham listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="8398f-128">Texture names and the corresponding texture contents are local to the shared display-list space of the current OpenGL rendering context; two rendering contexts share texture names only if they also share display lists.</span></span> <span data-ttu-id="8398f-129">Você pode gerar um conjunto de novos nomes de textura usando [**glGenTextures**](glgentextures.md).</span><span class="sxs-lookup"><span data-stu-id="8398f-129">You can generate a set of new texture names using [**glGenTextures**](glgentextures.md).</span></span>

<span data-ttu-id="8398f-130">Quando uma textura é vinculada pela primeira vez, ela assume a dimensionalidade de seu destino de textura; uma textura vinculada à \_ textura GL \_ 1D torna-se unidimensional e uma textura associada à \_ textura GL \_ 2D se torna bidimensional.</span><span class="sxs-lookup"><span data-stu-id="8398f-130">When a texture is first bound, it assumes the dimensionality of its texture target; a texture bound to GL\_TEXTURE\_1D becomes one-dimensional and a texture bound to GL\_TEXTURE\_2D becomes two-dimensional.</span></span> <span data-ttu-id="8398f-131">As operações que você executa em um destino de textura também afetam uma textura associada ao destino.</span><span class="sxs-lookup"><span data-stu-id="8398f-131">Operations you perform on a texture target also affect a texture bound to the target.</span></span> <span data-ttu-id="8398f-132">Quando você consulta um destino de textura, o valor de retorno é o estado da textura associada a ele.</span><span class="sxs-lookup"><span data-stu-id="8398f-132">When you query a texture target, the return value is the state of the texture bound to it.</span></span> <span data-ttu-id="8398f-133">Os destinos de textura se tornam aliases para texturas atualmente associadas a eles.</span><span class="sxs-lookup"><span data-stu-id="8398f-133">Texture targets become aliases for textures currently bound to them.</span></span>

<span data-ttu-id="8398f-134">Quando você associa uma textura a **glBindTexture**, a associação permanece ativa até que uma textura diferente seja associada ao mesmo destino ou você exclua a textura associada com a função [**glDeleteTextures**](gldeletetextures.md) .</span><span class="sxs-lookup"><span data-stu-id="8398f-134">When you bind a texture with **glBindTexture**, the binding remains active until a different texture is bound to the same target or you delete the bound texture with the [**glDeleteTextures**](gldeletetextures.md) function.</span></span> <span data-ttu-id="8398f-135">Depois de criar uma textura nomeada, você pode associá-la a um destino de textura que tenha a mesma dimensionalidade sempre que necessário.</span><span class="sxs-lookup"><span data-stu-id="8398f-135">Once you create a named texture you can bind it to a texture target that has the same dimensionality as often as needed.</span></span>

<span data-ttu-id="8398f-136">Geralmente, é muito mais rápido usar **glBindTexture** para associar uma textura nomeada existente a um dos destinos de textura do que recarregar a imagem de textura usando [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8398f-136">It is usually much faster to use **glBindTexture** to bind an existing named texture to one of the texture targets than it is to reload the texture image using [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span> <span data-ttu-id="8398f-137">Para obter mais controle sobre o desempenho do texturing, use [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="8398f-137">For additional control of texturing performance, use [**glPrioritizeTextures**](glprioritizetextures.md).</span></span>

<span data-ttu-id="8398f-138">Você pode incluir chamadas para **glBindTexture** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="8398f-138">You can include calls to **glBindTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="8398f-139">A função **glBindTexture** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8398f-139">The **glBindTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="8398f-140">As funções a seguir recuperam informações relacionadas ao **glBindTexture**:</span><span class="sxs-lookup"><span data-stu-id="8398f-140">The following functions retrieve information related to **glBindTexture**:</span></span>

-   <span data-ttu-id="8398f-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com associação do Argument GL de \_ textura \_ 1D \_</span><span class="sxs-lookup"><span data-stu-id="8398f-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_1D\_BINDING</span></span>

<span data-ttu-id="8398f-142">**glGet** com \_ \_ Associação 2D de textura de Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="8398f-142">**glGet** with argument GL\_TEXTURE\_2D\_BINDING</span></span>

## <a name="requirements"></a><span data-ttu-id="8398f-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8398f-143">Requirements</span></span>



| <span data-ttu-id="8398f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="8398f-144">Requirement</span></span> | <span data-ttu-id="8398f-145">Valor</span><span class="sxs-lookup"><span data-stu-id="8398f-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8398f-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8398f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8398f-147">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8398f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8398f-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8398f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8398f-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8398f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8398f-150">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8398f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="8398f-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8398f-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8398f-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8398f-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="8398f-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8398f-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8398f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8398f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8398f-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8398f-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8398f-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="8398f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8398f-157">**glAreTexturesResident**</span><span class="sxs-lookup"><span data-stu-id="8398f-157">**glAreTexturesResident**</span></span>](glaretexturesresident.md)
</dt> <dt>

[<span data-ttu-id="8398f-158">**glDeleteTextures**</span><span class="sxs-lookup"><span data-stu-id="8398f-158">**glDeleteTextures**</span></span>](gldeletetextures.md)
</dt> <dt>

[<span data-ttu-id="8398f-159">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="8398f-159">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="8398f-160">**glGet**</span><span class="sxs-lookup"><span data-stu-id="8398f-160">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8398f-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8398f-161">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="8398f-162">**glIsTexture**</span><span class="sxs-lookup"><span data-stu-id="8398f-162">**glIsTexture**</span></span>](glistexture.md)
</dt> <dt>

[<span data-ttu-id="8398f-163">**glPrioritizeTextures**</span><span class="sxs-lookup"><span data-stu-id="8398f-163">**glPrioritizeTextures**</span></span>](glprioritizetextures.md)
</dt> <dt>

[<span data-ttu-id="8398f-164">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8398f-164">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8398f-165">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8398f-165">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8398f-166">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8398f-166">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





