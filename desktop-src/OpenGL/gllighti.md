---
title: função glLighti (GL. h)
description: A função glLighti retorna valores de parâmetro de fonte de luz.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- função glLighti OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52225c4db8eaa31c17d12a25590b918cf94b4c3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824492"
---
# <a name="gllighti-function"></a><span data-ttu-id="775fe-104">função glLighti</span><span class="sxs-lookup"><span data-stu-id="775fe-104">glLighti function</span></span>

<span data-ttu-id="775fe-105">A função **glLighti** retorna valores de parâmetro de fonte de luz.</span><span class="sxs-lookup"><span data-stu-id="775fe-105">The **glLighti** function returns light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="775fe-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="775fe-106">Syntax</span></span>


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="775fe-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="775fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="775fe-108">*light*</span><span class="sxs-lookup"><span data-stu-id="775fe-108">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="775fe-109">O identificador de uma luz.</span><span class="sxs-lookup"><span data-stu-id="775fe-109">The identifier of a light.</span></span> <span data-ttu-id="775fe-110">O número de luzes possíveis depende da implementação, mas há suporte para pelo menos oito luzes.</span><span class="sxs-lookup"><span data-stu-id="775fe-110">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="775fe-111">Eles são identificados por nomes simbólicos do formulário GL \_ Light *i,* onde *eu* é um valor: 0 a GL \_ número máximo \_ de luzes-1.</span><span class="sxs-lookup"><span data-stu-id="775fe-111">They are identified by symbolic names of the form GL\_LIGHT *i* where *i* is a value: 0 to GL\_MAX\_LIGHTS - 1.</span></span>

</dd> <dt>

<span data-ttu-id="775fe-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="775fe-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="775fe-113">Um parâmetro de fonte de luz de valor único para *Light*.</span><span class="sxs-lookup"><span data-stu-id="775fe-113">A single-valued light source parameter for *light*.</span></span> <span data-ttu-id="775fe-114">Os nomes simbólicos a seguir são aceitos.</span><span class="sxs-lookup"><span data-stu-id="775fe-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="775fe-115">Valor</span><span class="sxs-lookup"><span data-stu-id="775fe-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="775fe-116">Significado</span><span class="sxs-lookup"><span data-stu-id="775fe-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="775fe-117"><dt>**\_expoente de spot de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-117"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                                                                                                                                                                             | <span data-ttu-id="775fe-118">O parâmetro *param* é um único valor inteiro que especifica a distribuição de intensidade da luz.</span><span class="sxs-lookup"><span data-stu-id="775fe-118">The *param* parameter is a single integer value that specifies the intensity distribution of the light.</span></span> <span data-ttu-id="775fe-119">Valores de ponto flutuante e inteiro são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="775fe-119">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="775fe-120">Somente os valores no intervalo de \[ 0, 128 \] são aceitos.</span><span class="sxs-lookup"><span data-stu-id="775fe-120">Only values in the range \[0, 128\] are accepted.</span></span> <br/> <span data-ttu-id="775fe-121">A intensidade de luz efetiva é atenuada pelo cosseno do ângulo entre a direção da luz e a direção da luz até o vértice ser iluminado, elevado à potência do expoente Spot.</span><span class="sxs-lookup"><span data-stu-id="775fe-121">Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent.</span></span> <span data-ttu-id="775fe-122">Assim, os expoentes de pontos mais altos resultam em uma fonte de luz mais focada, independentemente do ângulo de corte de spot.</span><span class="sxs-lookup"><span data-stu-id="775fe-122">Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle.</span></span> <span data-ttu-id="775fe-123">O expoente de spot padrão é 0, resultando em distribuição de luz uniforme.</span><span class="sxs-lookup"><span data-stu-id="775fe-123">The default spot exponent is 0, resulting in uniform light distribution.</span></span><br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="775fe-124"><dt>**\_corte de spot GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-124"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                                                                                                                                                                                   | <span data-ttu-id="775fe-125">O parâmetro *param* é um único valor inteiro que especifica o ângulo de propagação máximo de uma fonte de luz.</span><span class="sxs-lookup"><span data-stu-id="775fe-125">The *param* parameter is a single integer value that specifies the maximum spread angle of a light source.</span></span> <span data-ttu-id="775fe-126">Valores de ponto flutuante e inteiro são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="775fe-126">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="775fe-127">Somente os valores no intervalo de \[ 0, 90 \] e o valor especial 180 são aceitos.</span><span class="sxs-lookup"><span data-stu-id="775fe-127">Only values in the range \[0, 90\], and the special value 180, are accepted.</span></span> <br/> <span data-ttu-id="775fe-128">Se o ângulo entre a direção da luz e a direção da luz até o vértice que está sendo iluminado for maior que o ângulo de corte de spot, a luz será completamente mascarada.</span><span class="sxs-lookup"><span data-stu-id="775fe-128">If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked.</span></span> <span data-ttu-id="775fe-129">Caso contrário, sua intensidade é controlada pelo expoente de spot e pelos fatores de atenuação.</span><span class="sxs-lookup"><span data-stu-id="775fe-129">Otherwise, its intensity is controlled by the spot exponent and the attenuation factors.</span></span> <span data-ttu-id="775fe-130">O corte de spot padrão é 180, resultando em distribuição de luz uniforme.</span><span class="sxs-lookup"><span data-stu-id="775fe-130">The default spot cutoff is 180, resulting in uniform light distribution.</span></span><br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <span data-ttu-id="775fe-131"><dt>**atenuação constante do GL, atenuação linear do GL \_ \_ \_ \_ , \_ atenuação quadrática do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-131"><dt>**GL\_CONSTANT\_ATTENUATION, GL\_LINEAR\_ATTENUATION, GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="775fe-132">O parâmetro *param* é um valor inteiro único que especifica um dos três fatores de atenuação leves.</span><span class="sxs-lookup"><span data-stu-id="775fe-132">The *param* parameter is a single integer value that specifies one of the three light attenuation factors.</span></span> <span data-ttu-id="775fe-133">Valores de ponto flutuante e inteiro são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="775fe-133">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="775fe-134">Somente valores não negativos são aceitos.</span><span class="sxs-lookup"><span data-stu-id="775fe-134">Only nonnegative values are accepted.</span></span> <br/> <span data-ttu-id="775fe-135">Se a luz for posicional, em vez de direcional, sua intensidade será atenuada pelo recíproco da soma de: o fator de constante, o fator linear multiplicado pela distância entre a luz e o vértice que está sendo iluminado, e o fator quadrática multiplicado pelo quadrado da mesma distância.</span><span class="sxs-lookup"><span data-stu-id="775fe-135">If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance.</span></span> <span data-ttu-id="775fe-136">Os fatores de atenuação padrão são (1, 0, 0), resultando em nenhuma atenuação.</span><span class="sxs-lookup"><span data-stu-id="775fe-136">The default attenuation factors are (1,0,0), resulting in no attenuation.</span></span><br/>                   |



 

</dd> <dt>

<span data-ttu-id="775fe-137">*param*</span><span class="sxs-lookup"><span data-stu-id="775fe-137">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="775fe-138">Especifica o valor para o qual o parâmetro *pname* da *luz* da fonte de luz será definido como.</span><span class="sxs-lookup"><span data-stu-id="775fe-138">Specifies the value that parameter *pname* of light source *light* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="775fe-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="775fe-139">Return value</span></span>

<span data-ttu-id="775fe-140">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="775fe-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="775fe-141">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="775fe-141">Error codes</span></span>

<span data-ttu-id="775fe-142">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="775fe-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="775fe-143">Name</span><span class="sxs-lookup"><span data-stu-id="775fe-143">Name</span></span>                                                                                                  | <span data-ttu-id="775fe-144">Significado</span><span class="sxs-lookup"><span data-stu-id="775fe-144">Meaning</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="775fe-145"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="775fe-146">*Light* ou *pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="775fe-146">*light* or *pname* was not an accepted value.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="775fe-147"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="775fe-148">Um valor de expoente de spot foi especificado fora do intervalo \[ 0, 128 \] ou o corte de spot foi especificado fora do intervalo \[ 0, 90 \] (exceto pelo valor especial 180) ou um fator atenuante negativo foi especificado.</span><span class="sxs-lookup"><span data-stu-id="775fe-148">A spot exponent value was specified outside the range \[0, 128\], or spot cutoff was specified outside the range \[0, 90\] (except for the special value 180), or a negative attenuation factor was specified.</span></span><br/> |
| <dl> <span data-ttu-id="775fe-149"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="775fe-150">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="775fe-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="775fe-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="775fe-151">Remarks</span></span>

<span data-ttu-id="775fe-152">A função **glLighti** define o valor ou os valores de parâmetros de fonte de luz individuais.</span><span class="sxs-lookup"><span data-stu-id="775fe-152">The **glLighti** function sets the value or values of individual light source parameters.</span></span> <span data-ttu-id="775fe-153">O parâmetro *Light* nomeia a luz e é um nome simbólico do formulário GL \_ Light *i*, em que 0 = *i* < GL \_ Max \_ acende.</span><span class="sxs-lookup"><span data-stu-id="775fe-153">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i*, where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

<span data-ttu-id="775fe-154">O parâmetro *pname* especifica um dos parâmetros de origem da luz, novamente pelo nome simbólico.</span><span class="sxs-lookup"><span data-stu-id="775fe-154">The *pname* parameter specifies one of the light source parameters, again by symbolic name.</span></span> <span data-ttu-id="775fe-155">O parâmetro *param* é um único valor ou um ponteiro para uma matriz que contém os novos valores.</span><span class="sxs-lookup"><span data-stu-id="775fe-155">The *param* parameter is either a single value or a pointer to an array that contains the new values.</span></span>

<span data-ttu-id="775fe-156">O cálculo de iluminação é habilitado e desabilitado usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) com a iluminação do Argument GL \_ .</span><span class="sxs-lookup"><span data-stu-id="775fe-156">Lighting calculation is enabled and disabled using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_LIGHTING.</span></span> <span data-ttu-id="775fe-157">Quando a iluminação está habilitada, as fontes de luz habilitadas contribuem para o cálculo de iluminação.</span><span class="sxs-lookup"><span data-stu-id="775fe-157">When lighting is enabled, light sources that are enabled contribute to the lighting calculation.</span></span> <span data-ttu-id="775fe-158">Fonte de luz *eu estou* habilitada e desabilitada usando **glEnable** e **glDisable** com o argumento GL \_ Light *i*.</span><span class="sxs-lookup"><span data-stu-id="775fe-158">Light source *i* is enabled and disabled using **glEnable** and **glDisable** with argument GL\_LIGHT *i*.</span></span>

<span data-ttu-id="775fe-159">É sempre o caso que o GL \_ Light *i* = GL \_ LIGHT0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="775fe-159">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="775fe-160">As funções a seguir recuperam informações relacionadas à função **glLighti** :</span><span class="sxs-lookup"><span data-stu-id="775fe-160">The following functions retrieve information related to the **glLighti** function:</span></span>

[<span data-ttu-id="775fe-161">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="775fe-161">**glGetLight**</span></span>](glgetlight.md)

<span data-ttu-id="775fe-162">[**glIsEnabled**](glisenabled.md) com iluminação do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="775fe-162">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="775fe-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="775fe-163">Requirements</span></span>



| <span data-ttu-id="775fe-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="775fe-164">Requirement</span></span> | <span data-ttu-id="775fe-165">Valor</span><span class="sxs-lookup"><span data-stu-id="775fe-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="775fe-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="775fe-166">Minimum supported client</span></span><br/> | <span data-ttu-id="775fe-167">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="775fe-167">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="775fe-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="775fe-168">Minimum supported server</span></span><br/> | <span data-ttu-id="775fe-169">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="775fe-169">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="775fe-170">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="775fe-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="775fe-171"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-171"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="775fe-172">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="775fe-172">Library</span></span><br/>                  | <dl> <span data-ttu-id="775fe-173"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-173"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="775fe-174">DLL</span><span class="sxs-lookup"><span data-stu-id="775fe-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="775fe-175"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="775fe-175"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="775fe-176">Consulte também</span><span class="sxs-lookup"><span data-stu-id="775fe-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="775fe-177">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="775fe-177">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="775fe-178">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="775fe-178">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="775fe-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="775fe-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="775fe-180">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="775fe-180">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="775fe-181">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="775fe-181">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





