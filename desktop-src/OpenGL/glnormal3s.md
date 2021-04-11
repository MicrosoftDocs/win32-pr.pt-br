---
title: função glNormal3s (GL. h)
description: Define o vetor normal atual. | função glNormal3s (GL. h)
ms.assetid: 4fd98ad5-266d-4ef1-9c1f-2b5166ee65d7
keywords:
- função glNormal3s OpenGL
topic_type:
- apiref
api_name:
- glNormal3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7941fa4e2c4e5ef00a5a14ce1eb913fb22a1f58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172740"
---
# <a name="glnormal3s-function"></a><span data-ttu-id="e89ba-105">função glNormal3s</span><span class="sxs-lookup"><span data-stu-id="e89ba-105">glNormal3s function</span></span>

<span data-ttu-id="e89ba-106">Define o vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="e89ba-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="e89ba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e89ba-107">Syntax</span></span>


```C++
void WINAPI glNormal3s(
   GLshort nx,
   GLshort ny,
   GLshort nz
);
```



## <a name="parameters"></a><span data-ttu-id="e89ba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e89ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e89ba-109">*NX*</span><span class="sxs-lookup"><span data-stu-id="e89ba-109">*nx*</span></span> 
</dt> <dd>

<span data-ttu-id="e89ba-110">Especifica a coordenada x do novo vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="e89ba-110">Specifies the x-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="e89ba-111">*York*</span><span class="sxs-lookup"><span data-stu-id="e89ba-111">*ny*</span></span> 
</dt> <dd>

<span data-ttu-id="e89ba-112">Especifica a coordenada y do novo vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="e89ba-112">Specifies the y-coordinate of the new current normal vector.</span></span>

</dd> <dt>

<span data-ttu-id="e89ba-113">*NZ*</span><span class="sxs-lookup"><span data-stu-id="e89ba-113">*nz*</span></span> 
</dt> <dd>

<span data-ttu-id="e89ba-114">Especifica a coordenada z do novo vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="e89ba-114">Specifies the z-coordinate of the new current normal vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e89ba-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e89ba-115">Return value</span></span>

<span data-ttu-id="e89ba-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e89ba-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e89ba-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e89ba-117">Remarks</span></span>

<span data-ttu-id="e89ba-118">O normal atual é definido para as coordenadas fornecidas sempre que você chama a função **glNormal3s**.</span><span class="sxs-lookup"><span data-stu-id="e89ba-118">The current normal is set to the given coordinates whenever you call the **glNormal3s** function.</span></span>

<span data-ttu-id="e89ba-119">Os argumentos byte, Short ou Integer são convertidos em formato de ponto flutuante com um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro reapresentável mais negativo para-1,0.</span><span class="sxs-lookup"><span data-stu-id="e89ba-119">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="e89ba-120">Os normais especificados usando **glNormal3s** não precisam ter comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="e89ba-120">Normals specified by using **glNormal3s** need not have unit length.</span></span> <span data-ttu-id="e89ba-121">Se a normalização estiver habilitada, os normais especificados com **glNormal3s** serão normalizados após a transformação.</span><span class="sxs-lookup"><span data-stu-id="e89ba-121">If normalization is enabled, then normals specified with **glNormal3s** are normalized after transformation.</span></span> <span data-ttu-id="e89ba-122">Você pode controlar normalizationby usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE.</span><span class="sxs-lookup"><span data-stu-id="e89ba-122">You can control normalizationby using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="e89ba-123">Por padrão, a normalização é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="e89ba-123">By default, normalization is disabled.</span></span> <span data-ttu-id="e89ba-124">Você pode atualizar o normal atual a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="e89ba-124">You can update the current normal at any time.</span></span> <span data-ttu-id="e89ba-125">Em particular, você pode chamar **glNormal3s** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e89ba-125">In particular, you can call **glNormal3s** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="e89ba-126">As funções a seguir recuperam informações relacionadas ao **glNormal3s**:</span><span class="sxs-lookup"><span data-stu-id="e89ba-126">The following functions retrieve information related to **glNormal3s**:</span></span>

<span data-ttu-id="e89ba-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ atual \_ normal</span><span class="sxs-lookup"><span data-stu-id="e89ba-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="e89ba-128">[**glIsEnable**](glisenabled.md) com o Argument GL \_ NORMALIZE</span><span class="sxs-lookup"><span data-stu-id="e89ba-128">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="e89ba-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e89ba-129">Requirements</span></span>



| <span data-ttu-id="e89ba-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e89ba-130">Requirement</span></span> | <span data-ttu-id="e89ba-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e89ba-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e89ba-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e89ba-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e89ba-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e89ba-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e89ba-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e89ba-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e89ba-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e89ba-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e89ba-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e89ba-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e89ba-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e89ba-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e89ba-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e89ba-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="e89ba-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e89ba-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e89ba-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e89ba-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e89ba-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e89ba-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e89ba-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="e89ba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e89ba-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e89ba-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e89ba-144">**glColor**</span><span class="sxs-lookup"><span data-stu-id="e89ba-144">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e89ba-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e89ba-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e89ba-146">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="e89ba-146">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e89ba-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="e89ba-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="e89ba-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="e89ba-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





