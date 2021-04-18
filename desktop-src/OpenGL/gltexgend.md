---
title: função glTexGend (GL. h)
description: Controla a geração de coordenadas de textura. | função glTexGend (GL. h)
ms.assetid: 75ab3468-281d-4c8d-95cc-138d75646cdf
keywords:
- função glTexGend OpenGL
topic_type:
- apiref
api_name:
- glTexGend
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45854eb1e2070f334bfc906c249fbb4341ab74d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104571547"
---
# <a name="gltexgend-function"></a><span data-ttu-id="6e71a-105">função glTexGend</span><span class="sxs-lookup"><span data-stu-id="6e71a-105">glTexGend function</span></span>

<span data-ttu-id="6e71a-106">Controla a geração de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="6e71a-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e71a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e71a-107">Syntax</span></span>


```C++
void WINAPI glTexGend(
   GLenum   coord,
   GLenum   pname,
   GLdouble param
);
```



## <a name="parameters"></a><span data-ttu-id="6e71a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e71a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e71a-109">*coord*</span><span class="sxs-lookup"><span data-stu-id="6e71a-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="6e71a-110">Uma coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="6e71a-110">A texture coordinate.</span></span> <span data-ttu-id="6e71a-111">Deve ser um dos seguintes: GL \_ S, GL \_ T, GL \_ R ou GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="6e71a-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="6e71a-112">**pname**</span><span class="sxs-lookup"><span data-stu-id="6e71a-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="6e71a-113">O nome simbólico da função de geração de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="6e71a-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="6e71a-114">*param*</span><span class="sxs-lookup"><span data-stu-id="6e71a-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="6e71a-115">Um parâmetro de geração de textura de valor único, um dos \_ objetos GL \_ linear, de \_ olho \_ linear ou GL de \_ esfera \_ .</span><span class="sxs-lookup"><span data-stu-id="6e71a-115">A single valued texture generation parameter, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e71a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e71a-116">Return value</span></span>

<span data-ttu-id="6e71a-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6e71a-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e71a-118">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6e71a-118">Error codes</span></span>

<span data-ttu-id="6e71a-119">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6e71a-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6e71a-120">Nome</span><span class="sxs-lookup"><span data-stu-id="6e71a-120">Name</span></span>                                                                                                  | <span data-ttu-id="6e71a-121">Significado</span><span class="sxs-lookup"><span data-stu-id="6e71a-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e71a-122"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="6e71a-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="6e71a-123">*coord* ou *pname* não era um valor definido aceito ou *pname* o \_ \_ modo de geração de textura do GL \_ e *params* não era um valor definido aceito.</span><span class="sxs-lookup"><span data-stu-id="6e71a-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="6e71a-124"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="6e71a-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="6e71a-125">*pname* foi \_ \_ o modo de radiogeração do GL \_ , *params* foi \_ \_ o mapa de Sphere GL e *coord* era GL \_ R ou GL \_ Q</span><span class="sxs-lookup"><span data-stu-id="6e71a-125">*pname* was GL\_TEXTURE\_GEN\_MODE, *params* was GL\_SPHERE\_MAP, and *coord* was either GL\_R or GL\_Q</span></span><br/>                                     |
| <dl> <span data-ttu-id="6e71a-126"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e71a-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6e71a-127">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6e71a-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="6e71a-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e71a-128">Remarks</span></span>

<span data-ttu-id="6e71a-129">A função **glTexGen** seleciona uma função de geração de coordenadas de textura ou fornece coeficientes para uma das funções.</span><span class="sxs-lookup"><span data-stu-id="6e71a-129">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="6e71a-130">O parâmetro *coord* nomeia uma das coordenadas de textura (s, t, r, q) e deve ser um destes símbolos: GL \_ s, GL \_ t, GL \_ r ou GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="6e71a-130">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="6e71a-131">O parâmetro *pname* deve ser uma das três constantes simbólicas: \_ \_ modo de geração de textura GL \_ , plano de \_ objeto GL \_ ou plano de \_ olho GL \_ .</span><span class="sxs-lookup"><span data-stu-id="6e71a-131">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="6e71a-132">Se *pname* for o \_ modo do GL Texture \_ Gen \_ , o *param* especificará um modo, um dos objetos GL linear, informativo \_ \_ \_ \_ ou \_ mapa de esfera GL \_ .</span><span class="sxs-lookup"><span data-stu-id="6e71a-132">If *pname* is GL\_TEXTURE\_GEN\_MODE, then *param* specifies a mode, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span> <span data-ttu-id="6e71a-133">Se *pname* for plano de \_ objeto GL \_ ou \_ \_ plano de olho GL, *param* conterá coeficientes para a função de geração de textura correspondente.</span><span class="sxs-lookup"><span data-stu-id="6e71a-133">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="6e71a-134">Se a função de geração de textura for \_ Object GL \_ linear, a função</span><span class="sxs-lookup"><span data-stu-id="6e71a-134">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

![Equação mostrando a função glTexGen quando a função de geração de textura é GL_OBJECT_LINEAR.](images/tex02.png)

<span data-ttu-id="6e71a-136">é usado, em que g é o valor calculado para a coordenada chamada em coord; P1, P2, P3 e P4 são os quatro valores fornecidos em params; e x?, y?, z? e w? são as coordenadas de objeto do vértice.</span><span class="sxs-lookup"><span data-stu-id="6e71a-136">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="6e71a-137">Você pode usar essa função para o terreno do mapa de textura usando o nível do mar como um plano de referência (definido por P1, P2, P3 e P4).</span><span class="sxs-lookup"><span data-stu-id="6e71a-137">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="6e71a-138">A \_ função de \_ geração de coordenada linear do objeto GL computa a altitude de um vértice do terreno como sua distância do nível do mar; essa altitude é usada para indexar a imagem de textura para o mapa de Neves brancas em picos e na grama verde em Foothills, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="6e71a-138">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="6e71a-139">Se a função de geração de textura for a \_ atenção \_ linear, a função</span><span class="sxs-lookup"><span data-stu-id="6e71a-139">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

![Equação mostrando a função glTexGen quando a função de geração de textura é GL_EYE_LINEAR.](images/tex02.png)

<span data-ttu-id="6e71a-141">é usado, em que</span><span class="sxs-lookup"><span data-stu-id="6e71a-141">is used, where</span></span>

![Equação mostrando as coordenadas de olho do vértice.](images/tex03.png)

<span data-ttu-id="6e71a-143">e x?, y?, z? e w? são as coordenadas de olho do vértice, P1, P2, P3 e P4, os valores fornecidos no *param* e M é a matriz modelview quando você chama **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="6e71a-143">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="6e71a-144">Se M for insatisfatório ou o singular, as coordenadas de textura geradas pela função resultante poderão ser imprecisas ou indefinidas.</span><span class="sxs-lookup"><span data-stu-id="6e71a-144">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="6e71a-145">Os valores no *param* definem um plano de referência em coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="6e71a-145">The values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="6e71a-146">A matriz modelview que é aplicada a elas não pode ser a mesma em vigor quando os vértices do polígono são transformados.</span><span class="sxs-lookup"><span data-stu-id="6e71a-146">The modelview matrix that is applied to them cannot be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="6e71a-147">Essa função estabelece um campo de coordenadas de textura que pode produzir linhas de delimitação dinâmicas sobre a movimentação de objetos.</span><span class="sxs-lookup"><span data-stu-id="6e71a-147">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="6e71a-148">Se *pname* é \_ \_ o mapa de Sphere GL e *coord* é GL \_ s ou GL \_ t, as coordenadas de textura s e t são geradas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6e71a-148">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="6e71a-149">Deixe u o vetor de unidade apontando da origem para o vértice do polígono (em coordenadas de olho).</span><span class="sxs-lookup"><span data-stu-id="6e71a-149">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="6e71a-150">Deixe que n seja o normal atual, depois da transformação para as coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="6e71a-150">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="6e71a-151">Let f = (FX () AF () FZ) T ser o vetor de reflexão de forma que</span><span class="sxs-lookup"><span data-stu-id="6e71a-151">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Equação mostrando o vetor de reflexo como uma função de vetor de unidade e normal atual.](images/tex05.png)

<span data-ttu-id="6e71a-153">Por fim, deixe</span><span class="sxs-lookup"><span data-stu-id="6e71a-153">Finally, let</span></span>

![Equação mostrando m como uma função de vetor de reflexo.](images/tex07.png)

<span data-ttu-id="6e71a-155">Em seguida, os valores atribuídos às coordenadas de textura i e t são</span><span class="sxs-lookup"><span data-stu-id="6e71a-155">Then the values assigned to the i and t texture coordinates are</span></span>

![Equação mostrando valores atribuídos às coordenadas de textura i e t.](images/tex06.png)

<span data-ttu-id="6e71a-157">Você pode habilitar ou desabilitar uma função de geração de coordenada de textura usando [**glEnable**](glenable.md) ou [**glDisable**](gldisable.md) com um dos nomes de coordenadas de textura simbólicas (GL de textura de recriação de, GL, Reportador de textura do GL \_ \_ \_ \_ \_ \_ T \_ ou GL Texture Gen \_ \_ \_ \_ \_ p) como o argumento.</span><span class="sxs-lookup"><span data-stu-id="6e71a-157">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="6e71a-158">Quando essa função é habilitada, a coordenada de textura especificada é computada de acordo com a função de geração associada a essa coordenada.</span><span class="sxs-lookup"><span data-stu-id="6e71a-158">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="6e71a-159">Quando a função é desabilitada, os vértices subsequentes usam a coordenada de textura especificada do conjunto atual de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="6e71a-159">When the function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="6e71a-160">Inicialmente, todas as funções de geração de textura são definidas como o olho de GL \_ \_ linear e estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="6e71a-160">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="6e71a-161">As equações do plano s são (1, 0, 0, 0); ambas as equações do plano t são (0, 1, 0, 0); e todas as equações do plano r e q são (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6e71a-161">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="6e71a-162">As funções a seguir recuperam informações relacionadas ao glTexGen:</span><span class="sxs-lookup"><span data-stu-id="6e71a-162">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="6e71a-163">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="6e71a-163">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="6e71a-164">[**glIsEnabled**](glisenabled.md) com Argument GL \_ Texture \_ Gen \_ S</span><span class="sxs-lookup"><span data-stu-id="6e71a-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="6e71a-165">[**glIsEnabled**](glisenabled.md) com Argument GL \_ Texture \_ Gen \_ T</span><span class="sxs-lookup"><span data-stu-id="6e71a-165">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="6e71a-166">[**glIsEnabled**](glisenabled.md) com o argumento GL \_ Texture \_ Gen \_ R</span><span class="sxs-lookup"><span data-stu-id="6e71a-166">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="6e71a-167">[**glIsEnabled**](glisenabled.md) com Argument GL \_ Texture \_ Gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="6e71a-167">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="6e71a-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e71a-168">Requirements</span></span>



| <span data-ttu-id="6e71a-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e71a-169">Requirement</span></span> | <span data-ttu-id="6e71a-170">Valor</span><span class="sxs-lookup"><span data-stu-id="6e71a-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e71a-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e71a-171">Minimum supported client</span></span><br/> | <span data-ttu-id="6e71a-172">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e71a-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6e71a-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e71a-173">Minimum supported server</span></span><br/> | <span data-ttu-id="6e71a-174">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e71a-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e71a-175">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e71a-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e71a-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e71a-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6e71a-177">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e71a-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e71a-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e71a-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e71a-179">DLL</span><span class="sxs-lookup"><span data-stu-id="6e71a-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e71a-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e71a-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e71a-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e71a-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e71a-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6e71a-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6e71a-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6e71a-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6e71a-184">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="6e71a-184">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="6e71a-185">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="6e71a-185">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="6e71a-186">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="6e71a-186">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="6e71a-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="6e71a-187">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="6e71a-188">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="6e71a-188">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="6e71a-189">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="6e71a-189">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="6e71a-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="6e71a-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="6e71a-191">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="6e71a-191">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="6e71a-192">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="6e71a-192">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





