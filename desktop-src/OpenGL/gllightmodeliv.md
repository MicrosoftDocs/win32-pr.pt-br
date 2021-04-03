---
title: função glLightModeliv (GL. h)
description: A função glLightModeliv define os parâmetros do modelo de iluminação.
ms.assetid: 5998bb7e-d97a-47a0-b612-e6b0046aa5d2
keywords:
- função glLightModeliv OpenGL
topic_type:
- apiref
api_name:
- glLightModeliv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de61d53d3f4ceb9805ca5560c864379b18c65b3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645053"
---
# <a name="gllightmodeliv-function"></a><span data-ttu-id="5a1b0-104">função glLightModeliv</span><span class="sxs-lookup"><span data-stu-id="5a1b0-104">glLightModeliv function</span></span>

<span data-ttu-id="5a1b0-105">A função [**glLightModeliv**](gllightiv.md) define os parâmetros do modelo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-105">The [**glLightModeliv**](gllightiv.md) function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1b0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a1b0-106">Syntax</span></span>


```C++
void WINAPI glLightModeliv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="5a1b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a1b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a1b0-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="5a1b0-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="5a1b0-109">Um parâmetro de modelo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-109">A lighting model parameter.</span></span> <span data-ttu-id="5a1b0-110">Os valores a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-110">The following values are accepted.</span></span>



| <span data-ttu-id="5a1b0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5a1b0-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="5a1b0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="5a1b0-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <span data-ttu-id="5a1b0-113"><dt>**\_ambiente de \_ modelo \_ Light GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-113"><dt>**GL\_LIGHT\_MODEL\_AMBIENT**</dt></span></span> </dl>                 | <span data-ttu-id="5a1b0-114">O parâmetro *params* contém quatro valores inteiros que especificam a intensidade de RGBA de ambiente de toda a cena.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-114">The *params* parameter contains four integer values that specify the ambient RGBA intensity of the entire scene.</span></span> <span data-ttu-id="5a1b0-115">Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-115">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="5a1b0-116">Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-116">Floating-point values are mapped directly.</span></span> <span data-ttu-id="5a1b0-117">Nenhum valor inteiro nem de ponto flutuante são clamped.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-117">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="5a1b0-118">A intensidade de cena de ambiente padrão é (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="5a1b0-118">The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="5a1b0-119"><dt>**\_ \_ Visualizador local de modelo Light \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-119"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="5a1b0-120">O parâmetro *params* é um único valor inteiro que especifica como os ângulos de reflexão especular são computados.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-120">The *params* parameter is a single integer value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="5a1b0-121">Se *param* for 0 (ou 0,0), os ângulos de reflexo especular usam a direção de exibição para serem paralelos e na direção do eixo-*z* , independentemente do local do vértice em coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-121">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="5a1b0-122">Caso contrário, os reflexos especulares são computados a partir da origem do sistema de coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-122">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="5a1b0-123">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-123">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="5a1b0-124"><dt>**\_Método Light \_ GL \_ dois \_ lados**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-124"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="5a1b0-125">O parâmetro *params* é um único valor inteiro que especifica se os cálculos de iluminação de lado único ou dois lados são feitos para polígonos.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-125">The *params* parameter is a single integer value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="5a1b0-126">Ele não tem nenhum efeito sobre os cálculos de iluminação para pontos, linhas ou bitmaps.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-126">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="5a1b0-127">Se *param* for 0 (ou 0,0), a iluminação unidirecional será especificada e somente os parâmetros de material frontal serão usados na equação de iluminação.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-127">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="5a1b0-128">Caso contrário, a iluminação em dois lados será especificada.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-128">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="5a1b0-129">Nesse caso, os vértices de polígonos voltados são iluminados usando os parâmetros de material de apoio e têm seus normais invertidos antes que a equação de iluminação seja avaliada.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-129">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="5a1b0-130">Os vértices de polígonos front-end sempre são iluminados usando os parâmetros de material frontal, sem nenhuma alteração em seus normais.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-130">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="5a1b0-131">O padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-131">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a1b0-132">*params*</span><span class="sxs-lookup"><span data-stu-id="5a1b0-132">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="5a1b0-133">Um ponteiro para o valor ou valores aos quais *params* serão definidos.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-133">A pointer to the value or values to which *params* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a1b0-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a1b0-134">Return value</span></span>

<span data-ttu-id="5a1b0-135">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a1b0-136">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5a1b0-136">Error codes</span></span>

<span data-ttu-id="5a1b0-137">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5a1b0-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5a1b0-138">Nome</span><span class="sxs-lookup"><span data-stu-id="5a1b0-138">Name</span></span>                                                                                                  | <span data-ttu-id="5a1b0-139">Significado</span><span class="sxs-lookup"><span data-stu-id="5a1b0-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a1b0-140"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5a1b0-141">*pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-141">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="5a1b0-142"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5a1b0-143">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5a1b0-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5a1b0-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a1b0-144">Remarks</span></span>

<span data-ttu-id="5a1b0-145">A função **glLightModeliv** define o parâmetro do modelo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-145">The **glLightModeliv** function sets lighting model parameter.</span></span> <span data-ttu-id="5a1b0-146">O parâmetro *pname* nomeia um parâmetro e *param* fornece o novo valor. o valor ou os valores de parâmetros de fonte de luz individuais.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-146">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="5a1b0-147">No modo RGBA, a cor clara de um vértice é a soma da intensidade de emissão de material, do produto do material de reflexão de ambiente e da intensidade de ambiente de cena completa e a contribuição de cada fonte de luz habilitada.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-147">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="5a1b0-148">Cada fonte de luz contribui com a soma de três termos: ambiente, difuso e especular.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-148">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="5a1b0-149">A contribuição de fonte de luz ambiente é o produto da reflexão de ambiente material e a intensidade de ambiente da luz.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-149">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="5a1b0-150">A contribuição de origem da luz difusa é o produto da reflexão difusa do material, a intensidade difusa da luz e o produto do ponto do vértice normal com o vetor normalizado do vértice para a fonte de luz.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-150">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="5a1b0-151">A contribuição de fonte de luz especular é o produto da reflexão de especulação de material, a intensidade especular da luz e o produto de ponto dos vetores de vértice-to-light e de vértice para claro, aumentados para o poder da luminosidade do material.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-151">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="5a1b0-152">Todas as três contribuições de fonte de luz são atenuadas igualmente com base na distância do vértice até a fonte de luz e na direção da fonte de luz, no expoente de espalhamento e no ângulo de corte de espalhamento.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-152">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="5a1b0-153">Todos os produtos de ponto serão substituídos por zero se forem avaliados como um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-153">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="5a1b0-154">O componente alfa da cor declarada resultante é definido como o valor alfa da reflexão difusa do material.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-154">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="5a1b0-155">No modo de índice de cor, o valor do índice claro de um vértice varia do ambiente para os valores especulares passados para [**glMaterial**](glmaterial-functions.md) usando índices de \_ cores GL \_ .</span><span class="sxs-lookup"><span data-stu-id="5a1b0-155">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="5a1b0-156">Coeficientes difusas e especulares, computados com um peso (. 30,. 59, .11) das cores da luz, da luminosidade do material e das mesmas equações de reflexão e atenuação que no caso de RGBA, determinam o quanto acima do ambiente o índice resultante é.</span><span class="sxs-lookup"><span data-stu-id="5a1b0-156">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="5a1b0-157">As funções a seguir recuperam informações relacionadas à função **glLightModeliv** :</span><span class="sxs-lookup"><span data-stu-id="5a1b0-157">The following functions retrieve information related to the **glLightModeliv** function:</span></span>

<span data-ttu-id="5a1b0-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Light \_ modelo \_ local \_ Viewer</span><span class="sxs-lookup"><span data-stu-id="5a1b0-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="5a1b0-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ Light de \_ \_ dois \_ lados</span><span class="sxs-lookup"><span data-stu-id="5a1b0-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="5a1b0-160">[**glIsEnabled**](glisenabled.md) com iluminação do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="5a1b0-160">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1b0-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a1b0-161">Requirements</span></span>



| <span data-ttu-id="5a1b0-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a1b0-162">Requirement</span></span> | <span data-ttu-id="5a1b0-163">Valor</span><span class="sxs-lookup"><span data-stu-id="5a1b0-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1b0-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a1b0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1b0-165">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a1b0-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5a1b0-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a1b0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1b0-167">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a1b0-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5a1b0-168">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5a1b0-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a1b0-169"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-169"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5a1b0-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a1b0-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a1b0-171"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-171"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5a1b0-172">DLL</span><span class="sxs-lookup"><span data-stu-id="5a1b0-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a1b0-173"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a1b0-173"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a1b0-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a1b0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1b0-175">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5a1b0-175">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5a1b0-176">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5a1b0-176">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5a1b0-177">**glLight**</span><span class="sxs-lookup"><span data-stu-id="5a1b0-177">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="5a1b0-178">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="5a1b0-178">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





