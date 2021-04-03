---
title: função glNormal3iv (GL. h)
description: Define o vetor normal atual. | função glNormal3iv (GL. h)
ms.assetid: cf50e801-a34c-43bd-b7eb-facb84a6472d
keywords:
- função glNormal3iv OpenGL
topic_type:
- apiref
api_name:
- glNormal3iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5629a12d6c388da2aa133fbe72177646b4f95d63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930506"
---
# <a name="glnormal3iv-function"></a><span data-ttu-id="fa770-105">função glNormal3iv</span><span class="sxs-lookup"><span data-stu-id="fa770-105">glNormal3iv function</span></span>

<span data-ttu-id="fa770-106">Define o vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="fa770-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa770-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa770-107">Syntax</span></span>


```C++
void WINAPI glNormal3iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="fa770-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa770-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa770-109">*l*</span><span class="sxs-lookup"><span data-stu-id="fa770-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="fa770-110">Um ponteiro para uma matriz de três elementos: as coordenadas x, y e z do novo normal atual.</span><span class="sxs-lookup"><span data-stu-id="fa770-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa770-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa770-111">Return value</span></span>

<span data-ttu-id="fa770-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fa770-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa770-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa770-113">Remarks</span></span>

<span data-ttu-id="fa770-114">O normal atual é definido para as coordenadas fornecidas sempre que você chama a função **glNormal3iv**.</span><span class="sxs-lookup"><span data-stu-id="fa770-114">The current normal is set to the given coordinates whenever you call the **glNormal3iv** function.</span></span>

<span data-ttu-id="fa770-115">Os argumentos byte, Short ou Integer são convertidos em formato de ponto flutuante com um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro reapresentável mais negativo para-1,0.</span><span class="sxs-lookup"><span data-stu-id="fa770-115">Byte, short, or integer arguments are converted to floating-point format with a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="fa770-116">Os normais especificados usando **glNormal3iv** não precisam ter comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="fa770-116">Normals specified by using **glNormal3iv** need not have unit length.</span></span> <span data-ttu-id="fa770-117">Se a normalização estiver habilitada, os normais especificados com **glNormal3iv** serão normalizados após a transformação.</span><span class="sxs-lookup"><span data-stu-id="fa770-117">If normalization is enabled, then normals specified with **glNormal3iv** are normalized after transformation.</span></span> <span data-ttu-id="fa770-118">Você pode controlar a normalização usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE.</span><span class="sxs-lookup"><span data-stu-id="fa770-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="fa770-119">Por padrão, a normalização é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="fa770-119">By default, normalization is disabled.</span></span> <span data-ttu-id="fa770-120">Você pode atualizar o normal atual a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="fa770-120">You can update the current normal at any time.</span></span> <span data-ttu-id="fa770-121">Em particular, você pode chamar **glNormal3iv** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fa770-121">In particular, you can call **glNormal3iv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="fa770-122">As funções a seguir recuperam informações relacionadas ao **glNormal3iv**:</span><span class="sxs-lookup"><span data-stu-id="fa770-122">The following functions retrieve information related to **glNormal3iv**:</span></span>

<span data-ttu-id="fa770-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ atual \_ normal</span><span class="sxs-lookup"><span data-stu-id="fa770-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="fa770-124">[**glIsEnable**](glisenabled.md) com o Argument GL \_ NORMALIZE</span><span class="sxs-lookup"><span data-stu-id="fa770-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="fa770-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa770-125">Requirements</span></span>



| <span data-ttu-id="fa770-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa770-126">Requirement</span></span> | <span data-ttu-id="fa770-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fa770-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa770-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa770-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fa770-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fa770-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa770-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa770-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fa770-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fa770-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa770-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fa770-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa770-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa770-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fa770-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa770-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa770-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa770-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa770-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fa770-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa770-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa770-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa770-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa770-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa770-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fa770-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fa770-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="fa770-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="fa770-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fa770-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fa770-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="fa770-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="fa770-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="fa770-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="fa770-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="fa770-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





