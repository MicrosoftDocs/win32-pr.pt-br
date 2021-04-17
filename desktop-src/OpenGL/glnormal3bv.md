---
title: função glNormal3bv (GL. h)
description: Define o vetor normal atual. | função glNormal3bv (GL. h)
ms.assetid: 1d9be974-93c9-45ac-89f1-92c14ff1c242
keywords:
- função glNormal3bv OpenGL
topic_type:
- apiref
api_name:
- glNormal3bv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d758c1768425ecb736096d59a49133ff4c8918c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105761881"
---
# <a name="glnormal3bv-function"></a><span data-ttu-id="981f8-105">função glNormal3bv</span><span class="sxs-lookup"><span data-stu-id="981f8-105">glNormal3bv function</span></span>

<span data-ttu-id="981f8-106">Define o vetor normal atual.</span><span class="sxs-lookup"><span data-stu-id="981f8-106">Sets the current normal vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="981f8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="981f8-107">Syntax</span></span>


```C++
void WINAPI glNormal3bv(
   const GLbyte *v
);
```



## <a name="parameters"></a><span data-ttu-id="981f8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="981f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="981f8-109">*l*</span><span class="sxs-lookup"><span data-stu-id="981f8-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="981f8-110">Um ponteiro para uma matriz de três elementos: as coordenadas x, y e z do novo normal atual.</span><span class="sxs-lookup"><span data-stu-id="981f8-110">A pointer to an array of three elements: the x, y, and z coordinates of the new current normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="981f8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="981f8-111">Return value</span></span>

<span data-ttu-id="981f8-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="981f8-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="981f8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="981f8-113">Remarks</span></span>

<span data-ttu-id="981f8-114">O normal atual é definido para as coordenadas fornecidas sempre que você chama a função **glNormal3bv**.</span><span class="sxs-lookup"><span data-stu-id="981f8-114">The current normal is set to the given coordinates whenever you call the **glNormal3bv** function.</span></span>

<span data-ttu-id="981f8-115">Os argumentos byte, Short ou Integer são convertidos em formato de ponto flutuante usando um mapeamento linear que mapeia o valor inteiro representável mais positivo para 1,0 e o valor inteiro reapresentável mais negativo para-1,0.</span><span class="sxs-lookup"><span data-stu-id="981f8-115">Byte, short, or integer arguments are converted to floating-point format by using a linear mapping that maps the most positive representable integer value to 1.0, and the most negative representable integer value to -1.0.</span></span>

<span data-ttu-id="981f8-116">Os normais especificados usando **glNormal3bv** não precisam ter comprimento de unidade.</span><span class="sxs-lookup"><span data-stu-id="981f8-116">Normals specified by using **glNormal3bv** need not have unit length.</span></span> <span data-ttu-id="981f8-117">Se a normalização estiver habilitada, os normais especificados usando **glNormal3bv** serão normalizados após a transformação.</span><span class="sxs-lookup"><span data-stu-id="981f8-117">If normalization is enabled, then normals specified by using **glNormal3bv** are normalized after transformation.</span></span> <span data-ttu-id="981f8-118">Você pode controlar a normalização usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com o argumento GL \_ NORMALIZE.</span><span class="sxs-lookup"><span data-stu-id="981f8-118">You can control normalization by using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_NORMALIZE.</span></span> <span data-ttu-id="981f8-119">Por padrão, a normalização é desabilitada.</span><span class="sxs-lookup"><span data-stu-id="981f8-119">By default, normalization is disabled.</span></span> <span data-ttu-id="981f8-120">Você pode atualizar o normal atual a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="981f8-120">You can update the current normal any time.</span></span> <span data-ttu-id="981f8-121">Em particular, você pode chamar **glNormal3bv** entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="981f8-121">In particular, you can call **glNormal3bv** between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="981f8-122">As funções a seguir recuperam informações relacionadas ao **glNormal3bv**:</span><span class="sxs-lookup"><span data-stu-id="981f8-122">The following functions retrieve information related to **glNormal3bv**:</span></span>

<span data-ttu-id="981f8-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ atual \_ normal</span><span class="sxs-lookup"><span data-stu-id="981f8-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_NORMAL</span></span>

<span data-ttu-id="981f8-124">[**glIsEnable**](glisenabled.md) com o Argument GL \_ NORMALIZE</span><span class="sxs-lookup"><span data-stu-id="981f8-124">[**glIsEnable**](glisenabled.md) with argument GL\_NORMALIZE</span></span>

## <a name="requirements"></a><span data-ttu-id="981f8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="981f8-125">Requirements</span></span>



| <span data-ttu-id="981f8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="981f8-126">Requirement</span></span> | <span data-ttu-id="981f8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="981f8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="981f8-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="981f8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="981f8-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="981f8-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="981f8-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="981f8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="981f8-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="981f8-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="981f8-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="981f8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="981f8-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="981f8-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="981f8-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="981f8-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="981f8-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="981f8-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="981f8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="981f8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="981f8-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="981f8-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="981f8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="981f8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="981f8-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="981f8-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="981f8-140">**glColor**</span><span class="sxs-lookup"><span data-stu-id="981f8-140">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="981f8-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="981f8-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="981f8-142">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="981f8-142">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="981f8-143">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="981f8-143">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="981f8-144">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="981f8-144">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





