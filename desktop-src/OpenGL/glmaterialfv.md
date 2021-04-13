---
title: função glMaterialfv (GL. h)
description: A função glMaterialfv especifica os parâmetros materiais para o modelo de iluminação.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- função glMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44b200abe0588a657f770902a9a897329e1942a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369208"
---
# <a name="glmaterialfv-function"></a><span data-ttu-id="485c3-104">função glMaterialfv</span><span class="sxs-lookup"><span data-stu-id="485c3-104">glMaterialfv function</span></span>

<span data-ttu-id="485c3-105">A função **glMaterialfv** especifica os parâmetros materiais para o modelo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="485c3-105">The **glMaterialfv** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="485c3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="485c3-106">Syntax</span></span>


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="485c3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="485c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="485c3-108">*sorridente*</span><span class="sxs-lookup"><span data-stu-id="485c3-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="485c3-109">A face ou faces que estão sendo atualizadas.</span><span class="sxs-lookup"><span data-stu-id="485c3-109">The face or faces that are being updated.</span></span> <span data-ttu-id="485c3-110">Deve ser um dos seguintes: GL \_ frontal, GL \_ voltar ou GL \_ front e GL de \_ volta.</span><span class="sxs-lookup"><span data-stu-id="485c3-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="485c3-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="485c3-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="485c3-112">O parâmetro material da face ou faces sendo atualizadas.</span><span class="sxs-lookup"><span data-stu-id="485c3-112">The material parameter of the face or faces being updated.</span></span> <span data-ttu-id="485c3-113">Os parâmetros que podem ser especificados usando **glMaterialfv** e suas interpretações pela equação de iluminação são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="485c3-113">The parameters that can be specified using **glMaterialfv**, and their interpretations by the lighting equation, are as follows.</span></span>



| <span data-ttu-id="485c3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="485c3-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="485c3-115">Significado</span><span class="sxs-lookup"><span data-stu-id="485c3-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="485c3-116"><dt>**\_ambiente GL**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-116"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                                       | <span data-ttu-id="485c3-117">O parâmetro params contém quatro valores de ponto flutuante que especificam a reflexão de RGBA de ambiente do material.</span><span class="sxs-lookup"><span data-stu-id="485c3-117">The params parameter contains four floating-point values that specify the ambient RGBA reflectance of the material.</span></span> <span data-ttu-id="485c3-118">Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="485c3-118">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="485c3-119">Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="485c3-119">Floating-point values are mapped directly.</span></span> <span data-ttu-id="485c3-120">Nenhum valor inteiro nem de ponto flutuante são clamped.</span><span class="sxs-lookup"><span data-stu-id="485c3-120">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="485c3-121">A reflexão de ambiente padrão para os materiais voltados para frente e para trás é (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="485c3-121">The default ambient reflectance for both front-facing and back-facing materials is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="485c3-122"><dt>**\_difusão GL**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-122"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                                       | <span data-ttu-id="485c3-123">O parâmetro params contém quatro valores de ponto flutuante que especificam a reflexão da difusão de RGBA do material.</span><span class="sxs-lookup"><span data-stu-id="485c3-123">The params parameter contains four floating-point values that specify the diffuse RGBA reflectance of the material.</span></span> <span data-ttu-id="485c3-124">Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="485c3-124">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="485c3-125">Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="485c3-125">Floating-point values are mapped directly.</span></span> <span data-ttu-id="485c3-126">Nenhum valor inteiro nem de ponto flutuante são clamped.</span><span class="sxs-lookup"><span data-stu-id="485c3-126">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="485c3-127">A reflexão difusa padrão para os materiais voltados para frente e para trás é (0,8, 0,8, 0,8, 1,0).</span><span class="sxs-lookup"><span data-stu-id="485c3-127">The default diffuse reflectance for both front-facing and back-facing materials is (0.8, 0.8, 0.8, 1.0).</span></span> <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="485c3-128"><dt>**\_ESPECULA GL**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-128"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                                    | <span data-ttu-id="485c3-129">O parâmetro params contém quatro valores de ponto flutuante que especificam a reflexão de RGBA de especulação do material.</span><span class="sxs-lookup"><span data-stu-id="485c3-129">The params parameter contains four floating-point values that specify the specular RGBA reflectance of the material.</span></span> <span data-ttu-id="485c3-130">Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="485c3-130">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="485c3-131">Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="485c3-131">Floating-point values are mapped directly.</span></span> <span data-ttu-id="485c3-132">Nenhum valor inteiro nem de ponto flutuante são clamped.</span><span class="sxs-lookup"><span data-stu-id="485c3-132">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="485c3-133">A reflexão de especulares padrão para os materiais de frente e para trás é (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="485c3-133">The default specular reflectance for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="485c3-134"><dt>**\_emissão GL**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-134"><dt>**GL\_EMISSION**</dt></span></span> </dl>                                    | <span data-ttu-id="485c3-135">O parâmetro params contém quatro valores de ponto flutuante que especificam a intensidade de luz emitida de RGBA do material.</span><span class="sxs-lookup"><span data-stu-id="485c3-135">The params parameter contains four floating-point values that specify the RGBA emitted light intensity of the material.</span></span> <span data-ttu-id="485c3-136">Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="485c3-136">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="485c3-137">Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="485c3-137">Floating-point values are mapped directly.</span></span> <span data-ttu-id="485c3-138">Nenhum valor inteiro nem de ponto flutuante são clamped.</span><span class="sxs-lookup"><span data-stu-id="485c3-138">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="485c3-139">A intensidade de emissão padrão para os materiais voltados para frente e para trás é (0,0, 0,0, 0,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="485c3-139">The default emission intensity for both front-facing and back-facing materials is (0.0, 0.0, 0.0, 1.0).</span></span> <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="485c3-140"><dt>**claridade do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-140"><dt>**GL\_SHININESS**</dt></span></span> </dl>                                 | <span data-ttu-id="485c3-141">O parâmetro *param* é um único valor inteiro que especifica o expoente de especular RGBA do material.</span><span class="sxs-lookup"><span data-stu-id="485c3-141">The *param* parameter is a single integer value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="485c3-142">Os valores inteiros são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="485c3-142">Integer values are mapped directly.</span></span> <span data-ttu-id="485c3-143">Somente os valores no intervalo de \[ 0, 128 \] são aceitos.</span><span class="sxs-lookup"><span data-stu-id="485c3-143">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="485c3-144">O expoente especular padrão para os materiais front-end e traseiro é 0.</span><span class="sxs-lookup"><span data-stu-id="485c3-144">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <span data-ttu-id="485c3-145"><dt>**\_ambiente GL \_ e \_ difuso**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-145"><dt>**GL\_AMBIENT\_AND\_DIFFUSE**</dt></span></span> </dl> | <span data-ttu-id="485c3-146">Equivalente a chamar [**glMaterial**](glmaterial-functions.md) duas vezes com os mesmos valores de parâmetro, uma vez com o \_ ambiente GL e uma vez com o GL \_ difuso.</span><span class="sxs-lookup"><span data-stu-id="485c3-146">Equivalent to calling [**glMaterial**](glmaterial-functions.md) twice with the same parameter values, once with GL\_AMBIENT and once with GL\_DIFFUSE.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="485c3-147"><dt>**\_índices de cores GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-147"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl>                    | <span data-ttu-id="485c3-148">O parâmetro params contém três valores de ponto flutuante que especificam os índices de cores para a iluminação ambiente, difuso e especulação.</span><span class="sxs-lookup"><span data-stu-id="485c3-148">The params parameter contains three floating-point values specifying the color indexes for ambient, diffuse, and specular lighting.</span></span> <span data-ttu-id="485c3-149">Esses três valores, e GL \_ luminosidade, são os únicos valores materiais usados pela equação de iluminação do modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="485c3-149">These three values, and GL\_SHININESS, are the only material values used by the color-index mode lighting equation.</span></span> <span data-ttu-id="485c3-150">Consulte [**glLightModel**](gllightmodel-functions.md) para uma discussão sobre a iluminação de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="485c3-150">Refer to [**glLightModel**](gllightmodel-functions.md) for a discussion of color-index lighting.</span></span><br/>                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="485c3-151">*params*</span><span class="sxs-lookup"><span data-stu-id="485c3-151">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="485c3-152">O valor para o qual o parâmetro GL \_ luminosidade será definido.</span><span class="sxs-lookup"><span data-stu-id="485c3-152">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="485c3-153">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="485c3-153">Return value</span></span>

<span data-ttu-id="485c3-154">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="485c3-154">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="485c3-155">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="485c3-155">Error codes</span></span>

<span data-ttu-id="485c3-156">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="485c3-156">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="485c3-157">Nome</span><span class="sxs-lookup"><span data-stu-id="485c3-157">Name</span></span>                                                                                              | <span data-ttu-id="485c3-158">Significado</span><span class="sxs-lookup"><span data-stu-id="485c3-158">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="485c3-159"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-159"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="485c3-160">A *face* ou a *pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="485c3-160">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="485c3-161"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-161"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="485c3-162">Um expoente especular fora do intervalo de \[ 0, 128 \] foi especificado.</span><span class="sxs-lookup"><span data-stu-id="485c3-162">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="485c3-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="485c3-163">Remarks</span></span>

<span data-ttu-id="485c3-164">A função [**glMaterialfv**](glmaterialf.md) atribui valores a parâmetros materiais.</span><span class="sxs-lookup"><span data-stu-id="485c3-164">The [**glMaterialfv**](glmaterialf.md) function assigns values to material parameters.</span></span> <span data-ttu-id="485c3-165">Há dois conjuntos correspondentes de parâmetros materiais.</span><span class="sxs-lookup"><span data-stu-id="485c3-165">There are two matched sets of material parameters.</span></span> <span data-ttu-id="485c3-166">Um, o conjunto *front-end* , é usado para sombrear pontos, linhas, bitmaps e todos os polígonos (quando a iluminação de dois lados está desabilitada) ou apenas polígonos frontais (quando a iluminação de dois lados está habilitada).</span><span class="sxs-lookup"><span data-stu-id="485c3-166">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="485c3-167">O outro conjunto, *voltado*, é usado para sombrear polígonos voltados somente quando a iluminação de dois lados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="485c3-167">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="485c3-168">Consulte [**glLightModel**](gllightmodel-functions.md) para obter detalhes sobre cálculos de iluminação de um lado e dois lados.</span><span class="sxs-lookup"><span data-stu-id="485c3-168">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="485c3-169">A função [**glMaterialfv**](glmaterialf.md) usa três argumentos.</span><span class="sxs-lookup"><span data-stu-id="485c3-169">The [**glMaterialfv**](glmaterialf.md) function takes three arguments.</span></span> <span data-ttu-id="485c3-170">A primeira, *face*, especifica se o \_ material frontal do GL, os \_ materiais traseiros do GL ou os \_ materiais de frente \_ e de trás do GL \_ serão modificados.</span><span class="sxs-lookup"><span data-stu-id="485c3-170">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="485c3-171">O segundo, *pname*, especifica qual dos vários parâmetros em um ou ambos os conjuntos serão modificados.</span><span class="sxs-lookup"><span data-stu-id="485c3-171">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="485c3-172">O terceiro, *param*, especifica qual valor será atribuído ao parâmetro especificado.</span><span class="sxs-lookup"><span data-stu-id="485c3-172">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="485c3-173">Os parâmetros materiais são usados na equação de iluminação que é opcionalmente aplicada a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="485c3-173">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="485c3-174">A equação é discutida em [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="485c3-174">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="485c3-175">Os parâmetros de material podem ser atualizados a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="485c3-175">The material parameters can be updated at any time.</span></span> <span data-ttu-id="485c3-176">Em particular, [**glMaterialfv**](glmaterialf.md) pode ser chamado entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="485c3-176">In particular, [**glMaterialfv**](glmaterialf.md) can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="485c3-177">Se apenas um parâmetro de material único for alterado por vértice, no entanto, [**glColorMaterial**](glcolormaterial.md) será preferencial em relação a **glMaterialfv**.</span><span class="sxs-lookup"><span data-stu-id="485c3-177">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialfv**.</span></span>

<span data-ttu-id="485c3-178">A função a seguir recupera informações relacionadas a [**glMaterialfv**](glmaterialf.md):</span><span class="sxs-lookup"><span data-stu-id="485c3-178">The following function retrieves information related to [**glMaterialfv**](glmaterialf.md):</span></span>

[<span data-ttu-id="485c3-179">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="485c3-179">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="485c3-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="485c3-180">Requirements</span></span>



| <span data-ttu-id="485c3-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="485c3-181">Requirement</span></span> | <span data-ttu-id="485c3-182">Valor</span><span class="sxs-lookup"><span data-stu-id="485c3-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="485c3-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="485c3-183">Minimum supported client</span></span><br/> | <span data-ttu-id="485c3-184">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="485c3-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="485c3-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="485c3-185">Minimum supported server</span></span><br/> | <span data-ttu-id="485c3-186">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="485c3-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="485c3-187">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="485c3-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="485c3-188"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-188"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="485c3-189">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="485c3-189">Library</span></span><br/>                  | <dl> <span data-ttu-id="485c3-190"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-190"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="485c3-191">DLL</span><span class="sxs-lookup"><span data-stu-id="485c3-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="485c3-192"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="485c3-192"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="485c3-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="485c3-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485c3-194">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="485c3-194">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="485c3-195">**glLight**</span><span class="sxs-lookup"><span data-stu-id="485c3-195">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="485c3-196">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="485c3-196">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





