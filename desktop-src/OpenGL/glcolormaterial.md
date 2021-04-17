---
title: função glColorMaterial (GL. h)
description: A função glColorMaterial faz com que uma cor de material acompanhe a cor atual.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- função glColorMaterial OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369698"
---
# <a name="glcolormaterial-function"></a><span data-ttu-id="8604e-104">função glColorMaterial</span><span class="sxs-lookup"><span data-stu-id="8604e-104">glColorMaterial function</span></span>

<span data-ttu-id="8604e-105">A função **glColorMaterial** faz com que uma cor de material acompanhe a cor atual.</span><span class="sxs-lookup"><span data-stu-id="8604e-105">The **glColorMaterial** function causes a material color to track the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="8604e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8604e-106">Syntax</span></span>


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="8604e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8604e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8604e-108">*sorridente*</span><span class="sxs-lookup"><span data-stu-id="8604e-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="8604e-109">Especifica se os parâmetros de material frontal, posterior ou dianteiro devem controlar a cor atual.</span><span class="sxs-lookup"><span data-stu-id="8604e-109">Specifies whether front, back, or both front and back material parameters should track the current color.</span></span> <span data-ttu-id="8604e-110">Os valores aceitos são GL \_ front, GL \_ back e GL \_ front \_ e \_ back.</span><span class="sxs-lookup"><span data-stu-id="8604e-110">Accepted values are GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK.</span></span> <span data-ttu-id="8604e-111">O valor padrão é GL \_ front \_ e \_ back.</span><span class="sxs-lookup"><span data-stu-id="8604e-111">The default value is GL\_FRONT\_AND\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="8604e-112">*mode*</span><span class="sxs-lookup"><span data-stu-id="8604e-112">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="8604e-113">Especifica qual dos vários parâmetros de material acompanham a cor atual.</span><span class="sxs-lookup"><span data-stu-id="8604e-113">Specifies which of several material parameters track the current color.</span></span> <span data-ttu-id="8604e-114">Os valores aceitos são \_ emissão GL, ambiente GL, GL difuso, GL \_ \_ \_ especular e \_ ambiente GL \_ e \_ difuso.</span><span class="sxs-lookup"><span data-stu-id="8604e-114">Accepted values are GL\_EMISSION, GL\_AMBIENT, GL\_DIFFUSE, GL\_SPECULAR, and GL\_AMBIENT\_AND\_DIFFUSE.</span></span> <span data-ttu-id="8604e-115">O valor padrão é GL \_ ambiente \_ e \_ difuso.</span><span class="sxs-lookup"><span data-stu-id="8604e-115">The default value is GL\_AMBIENT\_AND\_DIFFUSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8604e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8604e-116">Return value</span></span>

<span data-ttu-id="8604e-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8604e-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8604e-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8604e-118">Error codes</span></span>

<span data-ttu-id="8604e-119">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8604e-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8604e-120">Nome</span><span class="sxs-lookup"><span data-stu-id="8604e-120">Name</span></span>                                                                                                  | <span data-ttu-id="8604e-121">Significado</span><span class="sxs-lookup"><span data-stu-id="8604e-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8604e-122"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="8604e-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8604e-123">a *face* ou o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="8604e-123">*face* or *mode* was not an accepted value.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="8604e-124"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8604e-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8604e-125">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8604e-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8604e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8604e-126">Remarks</span></span>

<span data-ttu-id="8604e-127">A função **glColorMaterial** especifica quais parâmetros materiais acompanham a cor atual.</span><span class="sxs-lookup"><span data-stu-id="8604e-127">The **glColorMaterial** function specifies which material parameters track the current color.</span></span> <span data-ttu-id="8604e-128">Quando você habilita o \_ material de cor GL \_ , para cada material ou material especificado por *face*, o parâmetro de material ou os parâmetros especificados pelo *modo* controlam a cor atual em todos os momentos.</span><span class="sxs-lookup"><span data-stu-id="8604e-128">When you enable GL\_COLOR\_MATERIAL, for each of the material or materials specified by *face*, the material parameter or parameters specified by *mode* track the current color at all times.</span></span> <span data-ttu-id="8604e-129">Habilite e desabilite o \_ \_ material de cor GL com as funções [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), que você chama com material de \_ cores GL \_ como argumento.</span><span class="sxs-lookup"><span data-stu-id="8604e-129">Enable and disable GL\_COLOR\_MATERIAL with the functions [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), which you call with GL\_COLOR\_MATERIAL as their argument.</span></span> <span data-ttu-id="8604e-130">Por padrão, o \_ material de cor GL \_ está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="8604e-130">By default, GL\_COLOR\_MATERIAL is disabled.</span></span>

<span data-ttu-id="8604e-131">Com o **glColorMaterial**, você pode alterar um subconjunto de parâmetros de material para cada vértice usando apenas a função [**glColor**](glcolor-functions.md) , sem chamar [**glMaterial**](glmaterial-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8604e-131">With **glColorMaterial**, you can change a subset of material parameters for each vertex using only the [**glColor**](glcolor-functions.md) function, without calling [**glMaterial**](glmaterial-functions.md).</span></span> <span data-ttu-id="8604e-132">Se você pretende especificar apenas um subconjunto de parâmetros para cada vértice, é melhor fazê-lo com **glColorMaterial** do que com **glMaterial**.</span><span class="sxs-lookup"><span data-stu-id="8604e-132">If you are going to specify only such a subset of parameters for each vertex, it is better to do so with **glColorMaterial** than with **glMaterial**.</span></span>

<span data-ttu-id="8604e-133">As funções a seguir recuperam informações relacionadas ao **glColorMaterial**:</span><span class="sxs-lookup"><span data-stu-id="8604e-133">The following functions retrieve information related to **glColorMaterial**:</span></span>

<span data-ttu-id="8604e-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com parâmetro de \_ material de cor do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8604e-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_MATERIAL\_PARAMETER</span></span>

<span data-ttu-id="8604e-135">**glGet** com material de cor de argumento GL \_ \_ \_ face</span><span class="sxs-lookup"><span data-stu-id="8604e-135">**glGet** with argument GL\_COLOR\_MATERIAL\_FACE</span></span>

<span data-ttu-id="8604e-136">[**glIsEnabled**](glisenabled.md) com material de cor do Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8604e-136">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_MATERIAL</span></span>

## <a name="requirements"></a><span data-ttu-id="8604e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8604e-137">Requirements</span></span>



| <span data-ttu-id="8604e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8604e-138">Requirement</span></span> | <span data-ttu-id="8604e-139">Valor</span><span class="sxs-lookup"><span data-stu-id="8604e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8604e-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8604e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8604e-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8604e-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8604e-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8604e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8604e-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8604e-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8604e-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8604e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8604e-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8604e-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8604e-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8604e-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="8604e-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8604e-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8604e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8604e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8604e-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8604e-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8604e-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="8604e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8604e-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8604e-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8604e-152">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8604e-152">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8604e-153">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="8604e-153">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="8604e-154">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="8604e-154">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="8604e-155">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8604e-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8604e-156">**glGet**</span><span class="sxs-lookup"><span data-stu-id="8604e-156">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8604e-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8604e-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="8604e-158">**glLight**</span><span class="sxs-lookup"><span data-stu-id="8604e-158">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="8604e-159">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="8604e-159">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="8604e-160">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="8604e-160">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





