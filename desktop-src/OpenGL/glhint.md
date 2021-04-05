---
title: função glHint (GL. h)
description: A função glHint especifica dicas específicas de implementação.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- função glHint OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085322"
---
# <a name="glhint-function"></a><span data-ttu-id="81a59-104">função glHint</span><span class="sxs-lookup"><span data-stu-id="81a59-104">glHint function</span></span>

<span data-ttu-id="81a59-105">A função **glHint** especifica dicas específicas de implementação.</span><span class="sxs-lookup"><span data-stu-id="81a59-105">The **glHint** function specifies implementation-specific hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="81a59-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81a59-106">Syntax</span></span>


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="81a59-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81a59-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81a59-108">*destino*</span><span class="sxs-lookup"><span data-stu-id="81a59-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="81a59-109">Uma constante simbólica que indica o comportamento a ser controlado.</span><span class="sxs-lookup"><span data-stu-id="81a59-109">A symbolic constant indicating the behavior to be controlled.</span></span> <span data-ttu-id="81a59-110">As constantes simbólicas a seguir, juntamente com a semântica sugerida, são aceitas.</span><span class="sxs-lookup"><span data-stu-id="81a59-110">The following symbolic constants, along with suggested semantics, are accepted.</span></span>



| <span data-ttu-id="81a59-111">Valor</span><span class="sxs-lookup"><span data-stu-id="81a59-111">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="81a59-112">Significado</span><span class="sxs-lookup"><span data-stu-id="81a59-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <span data-ttu-id="81a59-113"><dt>**\_dica de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-113"><dt>**GL\_FOG\_HINT**</dt></span></span> </dl>                                                           | <span data-ttu-id="81a59-114">Indica a precisão do cálculo de neblina.</span><span class="sxs-lookup"><span data-stu-id="81a59-114">Indicates the accuracy of fog calculation.</span></span> <span data-ttu-id="81a59-115">Se o cálculo de neblina por pixel não for compatível com eficiência pela implementação do OpenGL, a dica GL não se \_ \_ preocupa ou o GL \_ mais rápido pode resultar no cálculo por vértice de efeitos de neblina.</span><span class="sxs-lookup"><span data-stu-id="81a59-115">If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in per-vertex calculation of fog effects.</span></span><br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <span data-ttu-id="81a59-116"><dt>**\_ \_ dica Smooth de linha gl \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-116"><dt>**GL\_LINE\_SMOOTH\_HINT**</dt></span></span> </dl>                                  | <span data-ttu-id="81a59-117">Indica a qualidade de amostragem de linhas AntiAlias.</span><span class="sxs-lookup"><span data-stu-id="81a59-117">Indicates the sampling quality of antialiased lines.</span></span> <span data-ttu-id="81a59-118">O Hint GL \_ mais interessante pode resultar em mais fragmentos de pixel sendo gerados durante a rasterização, se uma função de filtro maior for aplicada.</span><span class="sxs-lookup"><span data-stu-id="81a59-118">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <span data-ttu-id="81a59-119"><dt>**\_dica de \_ correção de perspectiva GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-119"><dt>**GL\_PERSPECTIVE\_CORRECTION\_HINT**</dt></span></span> </dl> | <span data-ttu-id="81a59-120">Indica a qualidade da cor e a interpolação de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="81a59-120">Indicates the quality of color and texture coordinate interpolation.</span></span> <span data-ttu-id="81a59-121">Se a interpolação de parâmetro com correção de perspectiva não tiver suporte eficiente pela implementação do OpenGL, a dica GL não \_ \_ cuidará ou o GL \_ mais rápido poderá resultar em uma interpolação linear simples de cores e/ou coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="81a59-121">If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.</span></span><br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <span data-ttu-id="81a59-122"><dt>**\_ \_ dica Smooth do ponto GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-122"><dt>**GL\_POINT\_SMOOTH\_HINT**</dt></span></span> </dl>                               | <span data-ttu-id="81a59-123">Indica a qualidade de amostragem de pontos AntiAlias.</span><span class="sxs-lookup"><span data-stu-id="81a59-123">Indicates the sampling quality of antialiased points.</span></span> <span data-ttu-id="81a59-124">O Hint GL \_ mais interessante pode resultar em mais fragmentos de pixel sendo gerados durante a rasterização, se uma função de filtro maior for aplicada.</span><span class="sxs-lookup"><span data-stu-id="81a59-124">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <span data-ttu-id="81a59-125"><dt>**\_dica de \_ suavização do polígono GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-125"><dt>**GL\_POLYGON\_SMOOTH\_HINT**</dt></span></span> </dl>                         | <span data-ttu-id="81a59-126">Indica a qualidade de amostragem de polígonos com alias.</span><span class="sxs-lookup"><span data-stu-id="81a59-126">Indicates the sampling quality of antialiased polygons.</span></span> <span data-ttu-id="81a59-127">O Hint GL \_ mais interessante pode resultar em mais fragmentos de pixel sendo gerados durante a rasterização, se uma função de filtro maior for aplicada.</span><span class="sxs-lookup"><span data-stu-id="81a59-127">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="81a59-128">*mode*</span><span class="sxs-lookup"><span data-stu-id="81a59-128">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="81a59-129">Uma constante simbólica que indica o comportamento desejado.</span><span class="sxs-lookup"><span data-stu-id="81a59-129">A symbolic constant indicating the desired behavior.</span></span> <span data-ttu-id="81a59-130">As constantes simbólicas a seguir são aceitas.</span><span class="sxs-lookup"><span data-stu-id="81a59-130">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="81a59-131">Valor</span><span class="sxs-lookup"><span data-stu-id="81a59-131">Value</span></span>                                                                                                                                                       | <span data-ttu-id="81a59-132">Significado</span><span class="sxs-lookup"><span data-stu-id="81a59-132">Meaning</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <span data-ttu-id="81a59-133"><dt>**GL \_ mais rápido**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-133"><dt>**GL\_FASTEST**</dt></span></span> </dl>        | <span data-ttu-id="81a59-134">A opção mais eficiente deve ser escolhida.</span><span class="sxs-lookup"><span data-stu-id="81a59-134">The most efficient option should be chosen.</span></span><br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <span data-ttu-id="81a59-135"><dt>**GL mais \_ interessante**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-135"><dt>**GL\_NICEST**</dt></span></span> </dl>           | <span data-ttu-id="81a59-136">A opção mais correta ou de qualidade mais alta deve ser escolhida.</span><span class="sxs-lookup"><span data-stu-id="81a59-136">The most correct, or highest quality, option should be chosen.</span></span><br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <span data-ttu-id="81a59-137"><dt>**GL não se \_ \_ preocupa**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-137"><dt>**GL\_DONT\_CARE**</dt></span></span> </dl> | <span data-ttu-id="81a59-138">O cliente não tem uma preferência.</span><span class="sxs-lookup"><span data-stu-id="81a59-138">The client doesn't have a preference.</span></span><br/>                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81a59-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81a59-139">Return value</span></span>

<span data-ttu-id="81a59-140">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="81a59-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81a59-141">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="81a59-141">Error codes</span></span>

<span data-ttu-id="81a59-142">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="81a59-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="81a59-143">Nome</span><span class="sxs-lookup"><span data-stu-id="81a59-143">Name</span></span>                                                                                                  | <span data-ttu-id="81a59-144">Significado</span><span class="sxs-lookup"><span data-stu-id="81a59-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81a59-145"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="81a59-146">o *destino* ou o *modo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="81a59-146">*target* or *mode* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="81a59-147"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81a59-148">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="81a59-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="81a59-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="81a59-149">Remarks</span></span>

<span data-ttu-id="81a59-150">Quando há espaço para interpretação, você pode controlar determinados aspectos do comportamento do OpenGL com dicas.</span><span class="sxs-lookup"><span data-stu-id="81a59-150">When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints.</span></span> <span data-ttu-id="81a59-151">Você especifica uma dica com dois argumentos.</span><span class="sxs-lookup"><span data-stu-id="81a59-151">You specify a hint with two arguments.</span></span> <span data-ttu-id="81a59-152">O parâmetro de *destino* é uma constante simbólica que indica o comportamento a ser controlado e o *modo* é outra constante simbólica que indica o comportamento desejado.</span><span class="sxs-lookup"><span data-stu-id="81a59-152">The *target* parameter is a symbolic constant indicating the behavior to be controlled, and *mode* is another symbolic constant indicating the desired behavior.</span></span>

<span data-ttu-id="81a59-153">Embora os aspectos de implementação que podem ser indicados sejam bem definidos, a interpretação das dicas depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="81a59-153">Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.</span></span>

<span data-ttu-id="81a59-154">A função **glHint** pode ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="81a59-154">The **glHint** function can be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="81a59-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81a59-155">Requirements</span></span>



| <span data-ttu-id="81a59-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="81a59-156">Requirement</span></span> | <span data-ttu-id="81a59-157">Valor</span><span class="sxs-lookup"><span data-stu-id="81a59-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81a59-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81a59-158">Minimum supported client</span></span><br/> | <span data-ttu-id="81a59-159">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81a59-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81a59-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81a59-160">Minimum supported server</span></span><br/> | <span data-ttu-id="81a59-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81a59-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81a59-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81a59-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="81a59-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="81a59-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81a59-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="81a59-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="81a59-166">DLL</span><span class="sxs-lookup"><span data-stu-id="81a59-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81a59-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81a59-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81a59-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="81a59-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81a59-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="81a59-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="81a59-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="81a59-170">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





