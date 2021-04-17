---
title: função glNormal3f (GL. h)
description: Define o vetor normal atual. | função glNormal3f (GL. h)
ms.assetid: 8407996e-47fd-4c30-91f6-53d4341a1fca
keywords:
- função glNormal3f OpenGL
topic_type:
- apiref
api_name:
- glNormal3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e83b874b1588ad8bd91da9e5c9f831062de9cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105784165"
---
# <a name="glnormal3f-function"></a><span data-ttu-id="bf17d-105">função glNormal3f</span><span class="sxs-lookup"><span data-stu-id="bf17d-105">glNormal3f function</span></span>

<span data-ttu-id="bf17d-106">Define o vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="bf17d-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf17d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf17d-107">Syntax</span></span>


```C++
void WINAPI glNormal3f(
   GLfloat nx,
   GLfloat ny,
   GLfloat nz
);
```



## <a name="parameters"></a><span data-ttu-id="bf17d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf17d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf17d-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="bf17d-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="bf17d-110">Especifica a coordenada x para o novo vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="bf17d-110">Specifies the x-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="bf17d-111">*York*</span><span class="sxs-lookup"><span data-stu-id="bf17d-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="bf17d-112">Especifica a coordenada y para o novo vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="bf17d-112">Specifies the y-coordinate for the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="bf17d-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="bf17d-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="bf17d-114">Especifica a coordenada z para o novo vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="bf17d-114">Specifies the z-coordinate for the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf17d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf17d-115">Return value</span></span>

<span data-ttu-id="bf17d-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bf17d-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf17d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf17d-117">Remarks</span></span>

<span data-ttu-id="bf17d-118">O normal atual é definido para as coordenadas fornecidas sempre que você chama a função **glNormal3f** .</span><span class="sxs-lookup"><span data-stu-id="bf17d-118">The current normal is set to the given coordinates whenever you call the **glNormal3f** function.</span></span>

<span data-ttu-id="bf17d-119">Os argumentos byte, Short ou Integer são convertidos em formato de ponto flutuante com um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro reapresentável mais negativo para-1,0.</span><span class="sxs-lookup"><span data-stu-id="bf17d-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="bf17d-120">Os normais especificados usando **glNormal3f** não precisam ter comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="bf17d-120">Normals specified by using **glNormal3f** need not have unit length.</span></span> <span data-ttu-id="bf17d-121">Se a normalização estiver habilitada, os normais especificados com **glNormal3f** serão normalizados após a transformação.</span><span class="sxs-lookup"><span data-stu-id="bf17d-121">If normalization is enabled, then normals specified with **glNormal3f** are normalized after transformation.</span></span> <span data-ttu-id="bf17d-122">Você pode controlar a normalização usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE.</span><span class="sxs-lookup"><span data-stu-id="bf17d-122">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="bf17d-123">Por padrão, a normalização é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="bf17d-123">By default, normalization is disabled.</span></span> <span data-ttu-id="bf17d-124">Você pode atualizar o normal atual a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="bf17d-124">You can update the current normal at any time.</span></span> <span data-ttu-id="bf17d-125">Em particular, você pode chamar **glNormal3f** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bf17d-125">In particular, you can call **glNormal3f** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="bf17d-126">As funções a seguir recuperam informações relacionadas ao **glNormal3f**:</span><span class="sxs-lookup"><span data-stu-id="bf17d-126">The following functions retrieve information related to **glNormal3f**:</span></span>

<span data-ttu-id="bf17d-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ atual \_ normal</span><span class="sxs-lookup"><span data-stu-id="bf17d-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="bf17d-128">[**glIsEnable**](glisenabled.md) com o Argument GL \_ NORMALIZE</span><span class="sxs-lookup"><span data-stu-id="bf17d-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="bf17d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf17d-129">Requirements</span></span>



| <span data-ttu-id="bf17d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf17d-130">Requirement</span></span> | <span data-ttu-id="bf17d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="bf17d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf17d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf17d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bf17d-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bf17d-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf17d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf17d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bf17d-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bf17d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf17d-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bf17d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf17d-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf17d-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bf17d-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf17d-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf17d-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf17d-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf17d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bf17d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf17d-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf17d-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf17d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf17d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf17d-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bf17d-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bf17d-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="bf17d-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="bf17d-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bf17d-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bf17d-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="bf17d-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="bf17d-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="bf17d-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="bf17d-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="bf17d-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





