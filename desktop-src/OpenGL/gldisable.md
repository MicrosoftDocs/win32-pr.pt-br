---
title: função glDisable (GL. h)
description: As funções glEnable e glDisable habilitam ou desabilitam os recursos do OpenGL. | função glDisable (GL. h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- função glDisable OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105761408"
---
# <a name="gldisable-function"></a><span data-ttu-id="281da-105">função glDisable</span><span class="sxs-lookup"><span data-stu-id="281da-105">glDisable function</span></span>

<span data-ttu-id="281da-106">As funções [**glEnable**](glenable.md) e **glDisable** habilitam ou desabilitam os recursos do OpenGL.</span><span class="sxs-lookup"><span data-stu-id="281da-106">The [**glEnable**](glenable.md) and **glDisable** functions enable or disable OpenGL capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="281da-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="281da-107">Syntax</span></span>


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a><span data-ttu-id="281da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="281da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="281da-109">*extremidade*</span><span class="sxs-lookup"><span data-stu-id="281da-109">*cap*</span></span> 
</dt> <dd>

<span data-ttu-id="281da-110">Uma constante simbólica que indica um recurso OpenGL.</span><span class="sxs-lookup"><span data-stu-id="281da-110">A symbolic constant indicating an OpenGL capability.</span></span>

<span data-ttu-id="281da-111">Para obter uma discussão sobre os valores que o *limite* pode tomar, consulte a seção de comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="281da-111">For discussion of the values *cap* can take, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="281da-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="281da-112">Return value</span></span>

<span data-ttu-id="281da-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="281da-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="281da-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="281da-114">Error codes</span></span>

<span data-ttu-id="281da-115">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="281da-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="281da-116">Name</span><span class="sxs-lookup"><span data-stu-id="281da-116">Name</span></span>                                                                                                  | <span data-ttu-id="281da-117">Significado</span><span class="sxs-lookup"><span data-stu-id="281da-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="281da-118"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="281da-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="281da-119">*Cap* não era um dos valores listados na seção de comentários anterior.</span><span class="sxs-lookup"><span data-stu-id="281da-119">*cap* was not one of the values listed in the preceding Remarks section.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="281da-120"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="281da-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="281da-121">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="281da-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="281da-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="281da-122">Remarks</span></span>

<span data-ttu-id="281da-123">As funções [**glEnable**](glenable.md) e **glDisable** habilitam e desabilitam vários recursos gráficos OpenGL.</span><span class="sxs-lookup"><span data-stu-id="281da-123">The [**glEnable**](glenable.md) and **glDisable** functions enable and disable various OpenGL graphics capabilities.</span></span> <span data-ttu-id="281da-124">Use [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar a configuração atual de qualquer recurso.</span><span class="sxs-lookup"><span data-stu-id="281da-124">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="281da-125">[**GlEnable**](glenable.md) e **glDisable** usam um único argumento, *Cap*, que pode assumir um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="281da-125">Both [**glEnable**](glenable.md) and **glDisable** take a single argument, *cap*, which can assume one of the following values:</span></span>



| <span data-ttu-id="281da-126">Valor</span><span class="sxs-lookup"><span data-stu-id="281da-126">Value</span></span>                       | <span data-ttu-id="281da-127">Significado</span><span class="sxs-lookup"><span data-stu-id="281da-127">Meaning</span></span>                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="281da-128">\_teste de alfa do GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-128">GL\_ALPHA\_TEST</span></span>             | <span data-ttu-id="281da-129">Se habilitada, faça testes alfa.</span><span class="sxs-lookup"><span data-stu-id="281da-129">If enabled, do alpha testing.</span></span> <span data-ttu-id="281da-130">Consulte [**glAlphaFunc**](glalphafunc.md).</span><span class="sxs-lookup"><span data-stu-id="281da-130">See [**glAlphaFunc**](glalphafunc.md).</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="281da-131">GL \_ automático \_ normal</span><span class="sxs-lookup"><span data-stu-id="281da-131">GL\_AUTO\_NORMAL</span></span>            | <span data-ttu-id="281da-132">Se habilitada, os vetores normais da superfície de computação são analíticos de forma analítica quando o GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ Vertex \_ 4 gerou vértices.</span><span class="sxs-lookup"><span data-stu-id="281da-132">If enabled, compute surface normal vectors analytically when either GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4 has generated vertices.</span></span> <span data-ttu-id="281da-133">Consulte [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="281da-133">See [**glMap2**](glmap2.md).</span></span>                                                                                        |
| <span data-ttu-id="281da-134">a \_ combinação GL</span><span class="sxs-lookup"><span data-stu-id="281da-134">GL\_BLEND</span></span>                   | <span data-ttu-id="281da-135">Se habilitado, misture os valores de cor RGBA de entrada com os valores nos buffers de cor.</span><span class="sxs-lookup"><span data-stu-id="281da-135">If enabled, blend the incoming RGBA color values with the values in the color buffers.</span></span> <span data-ttu-id="281da-136">Consulte [**glBlendFunc**](glblendfunc.md).</span><span class="sxs-lookup"><span data-stu-id="281da-136">See [**glBlendFunc**](glblendfunc.md).</span></span>                                                                                                                              |
| <span data-ttu-id="281da-137">Recorte de \_ \_ plano GL *i*</span><span class="sxs-lookup"><span data-stu-id="281da-137">GL\_CLIP\_PLANE *i*</span></span>          | <span data-ttu-id="281da-138">Se habilitada, cortar a geometria em relação ao plano de recorte definido pelo usuário *i*.</span><span class="sxs-lookup"><span data-stu-id="281da-138">If enabled, clip geometry against user-defined clipping plane *i*.</span></span> <span data-ttu-id="281da-139">Consulte [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="281da-139">See [**glClipPlane**](glclipplane.md).</span></span>                                                                                                                                                  |
| <span data-ttu-id="281da-140">\_ \_ operação lógica de cores GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-140">GL\_COLOR\_LOGIC\_OP</span></span>        | <span data-ttu-id="281da-141">Se habilitada, aplique a operação lógica atual aos valores de cor e buffer de cor RGBA de entrada.</span><span class="sxs-lookup"><span data-stu-id="281da-141">If enabled, apply the current logical operation to the incoming RGBA color and color buffer values.</span></span> <span data-ttu-id="281da-142">Consulte [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="281da-142">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                     |
| <span data-ttu-id="281da-143">\_material de cor GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-143">GL\_COLOR\_MATERIAL</span></span>         | <span data-ttu-id="281da-144">Se habilitada, um ou mais parâmetros de material acompanharão a cor atual.</span><span class="sxs-lookup"><span data-stu-id="281da-144">If enabled, have one or more material parameters track the current color.</span></span> <span data-ttu-id="281da-145">Consulte [**glColorMaterial**](glcolormaterial.md).</span><span class="sxs-lookup"><span data-stu-id="281da-145">See [**glColorMaterial**](glcolormaterial.md).</span></span>                                                                                                                                   |
| <span data-ttu-id="281da-146">\_face de seleção GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-146">GL\_CULL\_FACE</span></span>              | <span data-ttu-id="281da-147">Se habilitada, a seleção de polígonos com base em seu enrolamento nas coordenadas da janela.</span><span class="sxs-lookup"><span data-stu-id="281da-147">If enabled, cull polygons based on their winding in window coordinates.</span></span> <span data-ttu-id="281da-148">Consulte [**glCullFace**](glcullface.md).</span><span class="sxs-lookup"><span data-stu-id="281da-148">See [**glCullFace**](glcullface.md).</span></span>                                                                                                                                               |
| <span data-ttu-id="281da-149">\_teste de profundidade GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-149">GL\_DEPTH\_TEST</span></span>             | <span data-ttu-id="281da-150">Se habilitada, faça comparações de profundidade e atualize o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="281da-150">If enabled, do depth comparisons and update the depth buffer.</span></span> <span data-ttu-id="281da-151">Consulte [**glDepthFunc**](gldepthfunc.md) e [**glDepthRange**](gldepthrange.md).</span><span class="sxs-lookup"><span data-stu-id="281da-151">See [**glDepthFunc**](gldepthfunc.md) and [**glDepthRange**](gldepthrange.md).</span></span>                                                                                                              |
| <span data-ttu-id="281da-152">\_pontilhamento GL</span><span class="sxs-lookup"><span data-stu-id="281da-152">GL\_DITHER</span></span>                  | <span data-ttu-id="281da-153">Se habilitado, os componentes ou índices de cores de pontilhamento antes de serem gravados no buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="281da-153">If enabled, dither color components or indexes before they are written to the color buffer.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="281da-154">neblina do GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-154">GL\_FOG</span></span>                     | <span data-ttu-id="281da-155">Se habilitada, misture uma cor de neblina para a cor texturing.</span><span class="sxs-lookup"><span data-stu-id="281da-155">If enabled, blend a fog color into the post-texturing color.</span></span> <span data-ttu-id="281da-156">Consulte [**glFog**](glfog.md).</span><span class="sxs-lookup"><span data-stu-id="281da-156">See [**glFog**](glfog.md).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="281da-157">\_ \_ op lógico de índice GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-157">GL\_INDEX\_LOGIC\_OP</span></span>        | <span data-ttu-id="281da-158">Se habilitada, aplique a operação lógica atual aos índices de entrada de índice e buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="281da-158">If enabled, apply the current logical operation to the incoming index and color buffer indices.</span></span> <span data-ttu-id="281da-159">Consulte [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="281da-159">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                         |
| <span data-ttu-id="281da-160">GL \_ claro *i*</span><span class="sxs-lookup"><span data-stu-id="281da-160">GL\_LIGHT *i*</span></span>                | <span data-ttu-id="281da-161">Se habilitada, inclua a luz *i* na avaliação da equação de iluminação.</span><span class="sxs-lookup"><span data-stu-id="281da-161">If enabled, include light *i* in the evaluation of the lighting equation.</span></span> <span data-ttu-id="281da-162">Consulte [**glLightModel**](gllightmodel-functions.md) e [**glLight**](gllight-functions.md).</span><span class="sxs-lookup"><span data-stu-id="281da-162">See [**glLightModel**](gllightmodel-functions.md) and [**glLight**](gllight-functions.md).</span></span>                                                                                      |
| <span data-ttu-id="281da-163">\_iluminação GL</span><span class="sxs-lookup"><span data-stu-id="281da-163">GL\_LIGHTING</span></span>                | <span data-ttu-id="281da-164">Se habilitada, use os parâmetros de iluminação atuais para computar a cor ou o índice do vértice.</span><span class="sxs-lookup"><span data-stu-id="281da-164">If enabled, use the current lighting parameters to compute the vertex color or index.</span></span> <span data-ttu-id="281da-165">Se desabilitado, associe a cor ou o índice atual a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="281da-165">If disabled, associate the current color or index with each vertex.</span></span> <span data-ttu-id="281da-166">Consulte [**glMaterial**](glmaterial-functions.md), **glLightModel** e **glLight**.</span><span class="sxs-lookup"><span data-stu-id="281da-166">See [**glMaterial**](glmaterial-functions.md), **glLightModel**, and **glLight**.</span></span>                |
| <span data-ttu-id="281da-167">linha do GL \_ \_ Smooth</span><span class="sxs-lookup"><span data-stu-id="281da-167">GL\_LINE\_SMOOTH</span></span>            | <span data-ttu-id="281da-168">Se habilitada, desenhe linhas com a filtragem correta.</span><span class="sxs-lookup"><span data-stu-id="281da-168">If enabled, draw lines with correct filtering.</span></span> <span data-ttu-id="281da-169">Se desabilitado, desenhe linhas com alias.</span><span class="sxs-lookup"><span data-stu-id="281da-169">If disabled, draw aliased lines.</span></span> <span data-ttu-id="281da-170">Consulte [**glLineWidth**](gllinewidth.md).</span><span class="sxs-lookup"><span data-stu-id="281da-170">See [**glLineWidth**](gllinewidth.md).</span></span>                                                                                                                                     |
| <span data-ttu-id="281da-171">\_STIPPLE de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="281da-171">GL\_LINE\_STIPPLE</span></span>           | <span data-ttu-id="281da-172">Se habilitada, use o padrão de Stipple de linha atual ao desenhar linhas.</span><span class="sxs-lookup"><span data-stu-id="281da-172">If enabled, use the current line stipple pattern when drawing lines.</span></span> <span data-ttu-id="281da-173">Consulte [**glLineStipple**](gllinestipple.md).</span><span class="sxs-lookup"><span data-stu-id="281da-173">See [**glLineStipple**](gllinestipple.md).</span></span>                                                                                                                                            |
| <span data-ttu-id="281da-174">\_op lógico \_ GL</span><span class="sxs-lookup"><span data-stu-id="281da-174">GL\_LOGIC\_OP</span></span>               | <span data-ttu-id="281da-175">Se habilitada, aplique a operação lógica selecionada no momento aos índices de entrada e de buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="281da-175">If enabled, apply the currently selected logical operation to the incoming and color-buffer indexes.</span></span> <span data-ttu-id="281da-176">Consulte [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="281da-176">See [**glLogicOp**](gllogicop.md).</span></span>                                                                                                                    |
| <span data-ttu-id="281da-177">GL \_ MAP1 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="281da-177">GL\_MAP1\_COLOR\_4</span></span>          | <span data-ttu-id="281da-178">Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram valores RGBA.</span><span class="sxs-lookup"><span data-stu-id="281da-178">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="281da-179">Consulte também [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="281da-179">See also [**glMap1**](glmap1.md).</span></span>                                           |
| <span data-ttu-id="281da-180">\_Índice MAP1 \_ GL</span><span class="sxs-lookup"><span data-stu-id="281da-180">GL\_MAP1\_INDEX</span></span>             | <span data-ttu-id="281da-181">Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram índices de cores.</span><span class="sxs-lookup"><span data-stu-id="281da-181">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate color indexes.</span></span> <span data-ttu-id="281da-182">Consulte também **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="281da-182">See also **glMap1**.</span></span>                                                                                                                                   |
| <span data-ttu-id="281da-183">GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="281da-183">GL\_MAP1\_NORMAL</span></span>            | <span data-ttu-id="281da-184">Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram Normals.</span><span class="sxs-lookup"><span data-stu-id="281da-184">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="281da-185">Consulte também [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="281da-185">See also [**glMap1**](glmap1.md).</span></span>                                               |
| <span data-ttu-id="281da-186">GL \_ MAP1 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="281da-186">GL\_MAP1\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="281da-187">Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram coordenadas de textura *s* .</span><span class="sxs-lookup"><span data-stu-id="281da-187">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s* texture coordinates.</span></span> <span data-ttu-id="281da-188">Consulte também **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="281da-188">See also **glMap1**.</span></span>                                                                                                                         |
| <span data-ttu-id="281da-189">GL \_ MAP1 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="281da-189">GL\_MAP1\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="281da-190">Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram coordenadas de textura *s* e *t* .</span><span class="sxs-lookup"><span data-stu-id="281da-190">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="281da-191">Consulte também [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="281da-191">See also [**glMap1**](glmap1.md).</span></span>                       |
| <span data-ttu-id="281da-192">GL \_ MAP1 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="281da-192">GL\_MAP1\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="281da-193">Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram coordenadas de textura *s*, *t* e *r* .</span><span class="sxs-lookup"><span data-stu-id="281da-193">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="281da-194">Consulte também **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="281da-194">See also **glMap1**.</span></span>                                                                                                           |
| <span data-ttu-id="281da-195">GL \_ MAP1 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="281da-195">GL\_MAP1\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="281da-196">Se habilitada, as chamadas para [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram coordenadas *s*, *t*, *r* e *q* Texture.</span><span class="sxs-lookup"><span data-stu-id="281da-196">If enabled, calls to [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="281da-197">Consulte também [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="281da-197">See also [**glMap1**](glmap1.md).</span></span>                    |
| <span data-ttu-id="281da-198">GL \_ MAP1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="281da-198">GL\_MAP1\_VERTEX\_3</span></span>         | <span data-ttu-id="281da-199">Se habilitada, as chamadas para **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** geram coordenadas de vértice *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="281da-199">If enabled, calls to **glEvalCoord1**, **glEvalMesh1**, and **glEvalPoint1** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="281da-200">Consulte também **glMap1**.</span><span class="sxs-lookup"><span data-stu-id="281da-200">See also **glMap1**.</span></span>                                                                                                            |
| <span data-ttu-id="281da-201">MAP1 do GL de \_ \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="281da-201">GL\_MAP1\_VERTEX\_4</span></span>         | <span data-ttu-id="281da-202">Se habilitada, as chamadas para [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) geram coordenadas de vértice *x*, *y*, *z* e *w* homogêneos.</span><span class="sxs-lookup"><span data-stu-id="281da-202">If enabled, calls to [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md), and [**glEvalPoint1**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="281da-203">Consulte também [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="281da-203">See also [**glMap1**](glmap1.md).</span></span> |
| <span data-ttu-id="281da-204">GL \_ map2 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="281da-204">GL\_MAP2\_COLOR\_4</span></span>          | <span data-ttu-id="281da-205">Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram valores RGBA.</span><span class="sxs-lookup"><span data-stu-id="281da-205">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate RGBA values.</span></span> <span data-ttu-id="281da-206">Consulte também [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="281da-206">See also [**glMap2**](glmap2.md).</span></span>                                           |
| <span data-ttu-id="281da-207">\_Índice map2 \_ GL</span><span class="sxs-lookup"><span data-stu-id="281da-207">GL\_MAP2\_INDEX</span></span>             | <span data-ttu-id="281da-208">Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram índices de cores.</span><span class="sxs-lookup"><span data-stu-id="281da-208">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate color indexes.</span></span> <span data-ttu-id="281da-209">Consulte também **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="281da-209">See also **glMap2**.</span></span>                                                                                                                                   |
| <span data-ttu-id="281da-210">GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="281da-210">GL\_MAP2\_NORMAL</span></span>            | <span data-ttu-id="281da-211">Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram Normals.</span><span class="sxs-lookup"><span data-stu-id="281da-211">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate normals.</span></span> <span data-ttu-id="281da-212">Consulte também [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="281da-212">See also [**glMap2**](glmap2.md).</span></span>                                               |
| <span data-ttu-id="281da-213">GL \_ map2 \_ Texture \_ coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="281da-213">GL\_MAP2\_TEXTURE\_COORD\_1</span></span> | <span data-ttu-id="281da-214">Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram coordenadas de textura *s* .</span><span class="sxs-lookup"><span data-stu-id="281da-214">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s* texture coordinates.</span></span> <span data-ttu-id="281da-215">Consulte também **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="281da-215">See also **glMap2**.</span></span>                                                                                                                         |
| <span data-ttu-id="281da-216">GL \_ map2 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="281da-216">GL\_MAP2\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="281da-217">Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram coordenadas de textura *s* e *t* .</span><span class="sxs-lookup"><span data-stu-id="281da-217">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s* and *t* texture coordinates.</span></span> <span data-ttu-id="281da-218">Consulte também [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="281da-218">See also [**glMap2**](glmap2.md).</span></span>                       |
| <span data-ttu-id="281da-219">GL \_ map2 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="281da-219">GL\_MAP2\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="281da-220">Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram coordenadas de textura *s*, *t* e *r* .</span><span class="sxs-lookup"><span data-stu-id="281da-220">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *s*, *t*, and *r* texture coordinates.</span></span> <span data-ttu-id="281da-221">Consulte também **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="281da-221">See also **glMap2**.</span></span>                                                                                                           |
| <span data-ttu-id="281da-222">GL \_ map2 \_ Texture \_ coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="281da-222">GL\_MAP2\_TEXTURE\_COORD\_4</span></span> | <span data-ttu-id="281da-223">Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram coordenadas *s*, *t*, *r* e *q* Texture.</span><span class="sxs-lookup"><span data-stu-id="281da-223">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate *s*, *t*, *r*, and *q* texture coordinates.</span></span> <span data-ttu-id="281da-224">Consulte também [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="281da-224">See also [**glMap2**](glmap2.md).</span></span>            |
| <span data-ttu-id="281da-225">GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="281da-225">GL\_MAP2\_VERTEX\_3</span></span>         | <span data-ttu-id="281da-226">Se habilitada, as chamadas para **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** geram coordenadas de vértice *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="281da-226">If enabled, calls to **glEvalCoord2**, **glEvalMesh2**, and **glEvalPoint2** generate *x*, *y*, and *z* vertex coordinates.</span></span> <span data-ttu-id="281da-227">Consulte também **glMap2**.</span><span class="sxs-lookup"><span data-stu-id="281da-227">See also **glMap2**.</span></span>                                                                                                            |
| <span data-ttu-id="281da-228">Map2 do GL de \_ \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="281da-228">GL\_MAP2\_VERTEX\_4</span></span>         | <span data-ttu-id="281da-229">Se habilitada, as chamadas para [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) geram coordenadas de vértice *x*, *y*, *z* e *w* homogêneos.</span><span class="sxs-lookup"><span data-stu-id="281da-229">If enabled, calls to [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md), and [**glEvalPoint2**](glevalpoint.md) generate homogeneous *x*, *y*, *z*, and *w* vertex coordinates.</span></span> <span data-ttu-id="281da-230">Consulte também [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="281da-230">See also [**glMap2**](glmap2.md).</span></span> |
| <span data-ttu-id="281da-231">\_NORMALIZE GL</span><span class="sxs-lookup"><span data-stu-id="281da-231">GL\_NORMALIZE</span></span>               | <span data-ttu-id="281da-232">Se habilitado, os vetores normais especificados com **glNormal** serão dimensionados para o comprimento da unidade após a transformação.</span><span class="sxs-lookup"><span data-stu-id="281da-232">If enabled, normal vectors specified with **glNormal** are scaled to unit length after transformation.</span></span> <span data-ttu-id="281da-233">Consulte [**glNormal**](glnormal-functions.md).</span><span class="sxs-lookup"><span data-stu-id="281da-233">See [**glNormal**](glnormal-functions.md).</span></span>                                                                                                          |
| <span data-ttu-id="281da-234">\_simples ponto \_ GL</span><span class="sxs-lookup"><span data-stu-id="281da-234">GL\_POINT\_SMOOTH</span></span>           | <span data-ttu-id="281da-235">Se habilitado, desenhe pontos com a filtragem correta.</span><span class="sxs-lookup"><span data-stu-id="281da-235">If enabled, draw points with proper filtering.</span></span> <span data-ttu-id="281da-236">Se desabilitado, desenhe pontos com alias.</span><span class="sxs-lookup"><span data-stu-id="281da-236">If disabled, draw aliased points.</span></span> <span data-ttu-id="281da-237">Consulte [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="281da-237">See [**glPointSize**](glpointsize.md).</span></span>                                                                                                                                    |
| <span data-ttu-id="281da-238">\_preenchimento de \_ deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-238">GL\_POLYGON\_OFFSET\_FILL</span></span>   | <span data-ttu-id="281da-239">Se habilitado, e se o polígono for renderizado no \_ modo de preenchimento GL, um deslocamento será adicionado aos valores de profundidade dos fragmentos de um polígono antes da execução da comparação de profundidade.</span><span class="sxs-lookup"><span data-stu-id="281da-239">If enabled, and if the polygon is rendered in GL\_FILL mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="281da-240">Consulte [**glPolygonOffset**](glpolygonoffset.md)**.**</span><span class="sxs-lookup"><span data-stu-id="281da-240">See [**glPolygonOffset**](glpolygonoffset.md)**.**</span></span>                                      |
| <span data-ttu-id="281da-241">\_linha de \_ deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-241">GL\_POLYGON\_OFFSET\_LINE</span></span>   | <span data-ttu-id="281da-242">Se habilitado, e se o polígono for renderizado no \_ modo de linha gl, um deslocamento será adicionado aos valores de profundidade dos fragmentos de um polígono antes da execução da comparação de profundidade.</span><span class="sxs-lookup"><span data-stu-id="281da-242">If enabled, and if the polygon is rendered in GL\_LINE mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed.</span></span> <span data-ttu-id="281da-243">Consulte **glPolygonOffset**.</span><span class="sxs-lookup"><span data-stu-id="281da-243">See **glPolygonOffset**.</span></span>                                                                 |
| <span data-ttu-id="281da-244">\_ponto de \_ deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-244">GL\_POLYGON\_OFFSET\_POINT</span></span>  | <span data-ttu-id="281da-245">Se habilitada, um deslocamento será adicionado aos valores de profundidade dos fragmentos de um polígono antes que a comparação de profundidade seja executada, se o polígono for renderizado no \_ modo de ponto GL.</span><span class="sxs-lookup"><span data-stu-id="281da-245">If enabled, an offset is added to depth values of a polygon's fragments before the depth comparison is performed, if the polygon is rendered in GL\_POINT mode.</span></span> <span data-ttu-id="281da-246">Consulte [**glPolygonOffset**](glpolygonoffset.md).</span><span class="sxs-lookup"><span data-stu-id="281da-246">See [**glPolygonOffset**](glpolygonoffset.md).</span></span>                                             |
| <span data-ttu-id="281da-247">\_suavização do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-247">GL\_POLYGON\_SMOOTH</span></span>         | <span data-ttu-id="281da-248">Se habilitado, desenhe polígonos com a filtragem adequada.</span><span class="sxs-lookup"><span data-stu-id="281da-248">If enabled, draw polygons with proper filtering.</span></span> <span data-ttu-id="281da-249">Se desabilitado, desenhe polígonos com alias.</span><span class="sxs-lookup"><span data-stu-id="281da-249">If disabled, draw aliased polygons.</span></span> <span data-ttu-id="281da-250">Consulte [**glPolygonMode**](glpolygonmode.md).</span><span class="sxs-lookup"><span data-stu-id="281da-250">See [**glPolygonMode**](glpolygonmode.md).</span></span>                                                                                                                            |
| <span data-ttu-id="281da-251">polígono do GL \_ \_ STIPPLE</span><span class="sxs-lookup"><span data-stu-id="281da-251">GL\_POLYGON\_STIPPLE</span></span>        | <span data-ttu-id="281da-252">Se habilitada, use o padrão Stipple Polygon atual ao renderizar polígonos.</span><span class="sxs-lookup"><span data-stu-id="281da-252">If enabled, use the current polygon stipple pattern when rendering polygons.</span></span> <span data-ttu-id="281da-253">Consulte [**glPolygonStipple**](glpolygonstipple.md).</span><span class="sxs-lookup"><span data-stu-id="281da-253">See [**glPolygonStipple**](glpolygonstipple.md).</span></span>                                                                                                                              |
| <span data-ttu-id="281da-254">\_teste de tesoura do GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-254">GL\_SCISSOR\_TEST</span></span>           | <span data-ttu-id="281da-255">Se habilitado, descarte os fragmentos que estão fora do retângulo da mola.</span><span class="sxs-lookup"><span data-stu-id="281da-255">If enabled, discard fragments that are outside the scissor rectangle.</span></span> <span data-ttu-id="281da-256">Consulte [**glScissor**](glscissor.md).</span><span class="sxs-lookup"><span data-stu-id="281da-256">See [**glScissor**](glscissor.md).</span></span>                                                                                                                                                   |
| <span data-ttu-id="281da-257">\_teste de estêncil GL \_</span><span class="sxs-lookup"><span data-stu-id="281da-257">GL\_STENCIL\_TEST</span></span>           | <span data-ttu-id="281da-258">Se habilitada, faça o teste do estêncil e atualize o buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="281da-258">If enabled, do stencil testing and update the stencil buffer.</span></span> <span data-ttu-id="281da-259">Consulte [**glStencilFunc**](glstencilfunc.md) e [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="281da-259">See [**glStencilFunc**](glstencilfunc.md) and [**glStencilOp**](glstencilop.md).</span></span>                                                                                                            |
| <span data-ttu-id="281da-260">Somente \_ textura GL \_ 1D</span><span class="sxs-lookup"><span data-stu-id="281da-260">GL\_TEXTURE\_1D</span></span>             | <span data-ttu-id="281da-261">Se habilitado, o texturing unidimensional será executado (a menos que texturing bidimensional também esteja habilitado).</span><span class="sxs-lookup"><span data-stu-id="281da-261">If enabled, one-dimensional texturing is performed (unless two-dimensional texturing is also enabled).</span></span> <span data-ttu-id="281da-262">Consulte [**glTexImage1D**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="281da-262">See [**glTexImage1D**](glteximage1d.md).</span></span>                                                                                                            |
| <span data-ttu-id="281da-263">A \_ textura GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="281da-263">GL\_TEXTURE\_2D</span></span>             | <span data-ttu-id="281da-264">Se habilitado, o texturing bidimensional será executado.</span><span class="sxs-lookup"><span data-stu-id="281da-264">If enabled, two-dimensional texturing is performed.</span></span> <span data-ttu-id="281da-265">Consulte [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="281da-265">See [**glTexImage2D**](glteximage2d.md).</span></span>                                                                                                                                                               |
| <span data-ttu-id="281da-266">GL \_ Texture \_ Gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="281da-266">GL\_TEXTURE\_GEN\_Q</span></span>         | <span data-ttu-id="281da-267">Se habilitada, a coordenada de textura *q* é computada usando a função de geração de textura definida com [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="281da-267">If enabled, the *q* texture coordinate is computed using the texture-generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="281da-268">Caso contrário, a coordenada de textura *q* atual será usada.</span><span class="sxs-lookup"><span data-stu-id="281da-268">Otherwise, the current *q* texture coordinate is used.</span></span>                                                        |
| <span data-ttu-id="281da-269">o GL de \_ Texture \_ Gen \_ R</span><span class="sxs-lookup"><span data-stu-id="281da-269">GL\_TEXTURE\_GEN\_R</span></span>         | <span data-ttu-id="281da-270">Se habilitada, a coordenada de textura do *r* é computada usando a função de geração de textura definida com [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="281da-270">If enabled, the *r* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="281da-271">Se desabilitado, a coordenada de textura do *r* atual será usada.</span><span class="sxs-lookup"><span data-stu-id="281da-271">If disabled, the current *r* texture coordinate is used.</span></span>                                                      |
| <span data-ttu-id="281da-272">S do GL \_ Texture \_ Gen \_</span><span class="sxs-lookup"><span data-stu-id="281da-272">GL\_TEXTURE\_GEN\_S</span></span>         | <span data-ttu-id="281da-273">Se habilitada, a coordenada de textura *s* é computada usando a função de geração de textura definida com **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="281da-273">If enabled, the *s* texture coordinate is computed using the texture generation function defined with **glTexGen**.</span></span> <span data-ttu-id="281da-274">Se desabilitado, a coordenada de textura *s* atual será usada.</span><span class="sxs-lookup"><span data-stu-id="281da-274">If disabled, the current *s* texture coordinate is used.</span></span>                                                                                |
| <span data-ttu-id="281da-275">\_geração de textura de Texture GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="281da-275">GL\_TEXTURE\_GEN\_T</span></span>         | <span data-ttu-id="281da-276">Se habilitada, a coordenada de textura *t* é computada usando a função de geração de textura definida com [**glTexGen**](gltexgen-functions.md).</span><span class="sxs-lookup"><span data-stu-id="281da-276">If enabled, the *t* texture coordinate is computed using the texture generation function defined with [**glTexGen**](gltexgen-functions.md).</span></span> <span data-ttu-id="281da-277">Se desabilitado, a coordenada de textura *t* atual será usada.</span><span class="sxs-lookup"><span data-stu-id="281da-277">If disabled, the current *t* texture coordinate is used.</span></span>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="281da-278">Requisitos</span><span class="sxs-lookup"><span data-stu-id="281da-278">Requirements</span></span>



| <span data-ttu-id="281da-279">Requisito</span><span class="sxs-lookup"><span data-stu-id="281da-279">Requirement</span></span> | <span data-ttu-id="281da-280">Valor</span><span class="sxs-lookup"><span data-stu-id="281da-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="281da-281">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="281da-281">Minimum supported client</span></span><br/> | <span data-ttu-id="281da-282">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="281da-282">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="281da-283">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="281da-283">Minimum supported server</span></span><br/> | <span data-ttu-id="281da-284">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="281da-284">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="281da-285">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="281da-285">Header</span></span><br/>                   | <dl> <span data-ttu-id="281da-286"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="281da-286"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="281da-287">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="281da-287">Library</span></span><br/>                  | <dl> <span data-ttu-id="281da-288"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="281da-288"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="281da-289">DLL</span><span class="sxs-lookup"><span data-stu-id="281da-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="281da-290"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="281da-290"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="281da-291">Confira também</span><span class="sxs-lookup"><span data-stu-id="281da-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281da-292">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="281da-292">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="281da-293">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="281da-293">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="281da-294">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="281da-294">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="281da-295">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="281da-295">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="281da-296">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="281da-296">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="281da-297">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="281da-297">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="281da-298">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="281da-298">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="281da-299">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="281da-299">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="281da-300">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="281da-300">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="281da-301">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="281da-301">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="281da-302">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="281da-302">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="281da-303">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="281da-303">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="281da-304">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="281da-304">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="281da-305">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="281da-305">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="281da-306">**glEvalCoord1**</span><span class="sxs-lookup"><span data-stu-id="281da-306">**glEvalCoord1**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="281da-307">**glEvalMesh1**</span><span class="sxs-lookup"><span data-stu-id="281da-307">**glEvalMesh1**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="281da-308">**glEvalPoint1**</span><span class="sxs-lookup"><span data-stu-id="281da-308">**glEvalPoint1**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="281da-309">**glFog**</span><span class="sxs-lookup"><span data-stu-id="281da-309">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="281da-310">**glGet**</span><span class="sxs-lookup"><span data-stu-id="281da-310">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="281da-311">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="281da-311">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="281da-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="281da-312">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="281da-313">**glLight**</span><span class="sxs-lookup"><span data-stu-id="281da-313">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="281da-314">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="281da-314">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="281da-315">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="281da-315">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="281da-316">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="281da-316">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="281da-317">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="281da-317">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="281da-318">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="281da-318">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="281da-319">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="281da-319">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="281da-320">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="281da-320">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="281da-321">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="281da-321">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="281da-322">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="281da-322">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="281da-323">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="281da-323">**glPointSize**</span></span>](glpointsize.md)
</dt> <dt>

[<span data-ttu-id="281da-324">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="281da-324">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="281da-325">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="281da-325">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="281da-326">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="281da-326">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="281da-327">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="281da-327">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> <dt>

[<span data-ttu-id="281da-328">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="281da-328">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="281da-329">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="281da-329">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="281da-330">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="281da-330">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="281da-331">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="281da-331">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="281da-332">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="281da-332">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





