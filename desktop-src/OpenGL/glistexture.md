---
title: função glIsTexture (GL. h)
description: A função glIsTexture determina se um nome corresponde a uma textura.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- função glIsTexture OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8897cc0eb004da701f28b410f2ca28b6194c9d26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455811"
---
# <a name="glistexture-function"></a><span data-ttu-id="554de-104">função glIsTexture</span><span class="sxs-lookup"><span data-stu-id="554de-104">glIsTexture function</span></span>

<span data-ttu-id="554de-105">A função **glIsTexture** determina se um nome corresponde a uma textura.</span><span class="sxs-lookup"><span data-stu-id="554de-105">The **glIsTexture** function determines if a name corresponds to a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="554de-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="554de-106">Syntax</span></span>


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a><span data-ttu-id="554de-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="554de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="554de-108">*textura*</span><span class="sxs-lookup"><span data-stu-id="554de-108">*texture*</span></span> 
</dt> <dd>

<span data-ttu-id="554de-109">Um valor que é o nome de uma textura.</span><span class="sxs-lookup"><span data-stu-id="554de-109">A value that is the name of a texture.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="554de-110">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="554de-110">Error codes</span></span>

<span data-ttu-id="554de-111">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="554de-111">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="554de-112">Nome</span><span class="sxs-lookup"><span data-stu-id="554de-112">Name</span></span>                                                                                                  | <span data-ttu-id="554de-113">Significado</span><span class="sxs-lookup"><span data-stu-id="554de-113">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="554de-114"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="554de-114"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="554de-115">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="554de-115">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="554de-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="554de-116">Remarks</span></span>

<span data-ttu-id="554de-117">Se o parâmetro *Texture* for atualmente o nome de uma textura, a função **glIsTexture** retornará GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="554de-117">If the *texture* parameter is currently the name of a texture, the **glIsTexture** function returns GL\_TRUE.</span></span> <span data-ttu-id="554de-118">A função **glIsTexture** retornará GL \_ false se a *textura* for zero.</span><span class="sxs-lookup"><span data-stu-id="554de-118">The **glIsTexture** function returns GL\_FALSE if *texture* is zero.</span></span> <span data-ttu-id="554de-119">Ele também retornará GL \_ false se for um valor diferente de zero que não seja o nome de uma textura no momento ou se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="554de-119">It also returns GL\_FALSE if it is a non-zero value that is not currently the name of a texture, or if an error occurs.</span></span>

<span data-ttu-id="554de-120">Você não pode incluir chamadas para **glIsTexture** em listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="554de-120">You cannot include calls to **glIsTexture** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="554de-121">A função **glIsTexture** só está disponível no OpenGL versão 1,1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="554de-121">The **glIsTexture** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="554de-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="554de-122">Requirements</span></span>



| <span data-ttu-id="554de-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="554de-123">Requirement</span></span> | <span data-ttu-id="554de-124">Valor</span><span class="sxs-lookup"><span data-stu-id="554de-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="554de-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="554de-125">Minimum supported client</span></span><br/> | <span data-ttu-id="554de-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="554de-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="554de-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="554de-127">Minimum supported server</span></span><br/> | <span data-ttu-id="554de-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="554de-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="554de-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="554de-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="554de-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="554de-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="554de-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="554de-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="554de-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="554de-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="554de-133">DLL</span><span class="sxs-lookup"><span data-stu-id="554de-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="554de-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="554de-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="554de-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="554de-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="554de-136">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="554de-136">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="554de-137">**glBindTexture**</span><span class="sxs-lookup"><span data-stu-id="554de-137">**glBindTexture**</span></span>](glbindtexture.md)
</dt> <dt>

[<span data-ttu-id="554de-138">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="554de-138">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="554de-139">**glGenTextures**</span><span class="sxs-lookup"><span data-stu-id="554de-139">**glGenTextures**</span></span>](glgentextures.md)
</dt> <dt>

[<span data-ttu-id="554de-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="554de-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="554de-141">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="554de-141">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="554de-142">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="554de-142">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="554de-143">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="554de-143">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="554de-144">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="554de-144">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





