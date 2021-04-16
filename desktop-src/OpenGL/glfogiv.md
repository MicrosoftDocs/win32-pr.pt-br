---
title: Função glFogiv (Gl.h)
description: A função glFogiv especifica parâmetros de neblina. | função glFogiv (GL. h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- função glFogiv OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fa4fefece05529cf5ff3906f19c5ad6e444249
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506407"
---
# <a name="glfogiv-function"></a><span data-ttu-id="1f81d-105">função glFogiv</span><span class="sxs-lookup"><span data-stu-id="1f81d-105">glFogiv function</span></span>

<span data-ttu-id="1f81d-106">A função **glFogfv** especifica parâmetros de neblina.</span><span class="sxs-lookup"><span data-stu-id="1f81d-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f81d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f81d-107">Syntax</span></span>


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="1f81d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f81d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f81d-109">*pname*</span><span class="sxs-lookup"><span data-stu-id="1f81d-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="1f81d-110">Especifica um parâmetro de neblina.</span><span class="sxs-lookup"><span data-stu-id="1f81d-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="1f81d-111">Aceita um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f81d-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="1f81d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="1f81d-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="1f81d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="1f81d-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="1f81d-114"><dt>**\_modo de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="1f81d-115">O parâmetro *params* é um único valor inteiro que especifica a equação a ser usada para calcular o fator de mistura de neblina, *f*.</span><span class="sxs-lookup"><span data-stu-id="1f81d-115">The *params* parameter is a single integer value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="1f81d-116">Três constantes simbólicas são aceitas: GL \_ linear, GL \_ exp e GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="1f81d-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="1f81d-117">As equações correspondentes a essas constantes simbólicas são definidas na seção comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f81d-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="1f81d-118">O modo de neblina padrão é GL \_ exp.</span><span class="sxs-lookup"><span data-stu-id="1f81d-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="1f81d-119"><dt>**\_densidade de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="1f81d-120">O parâmetro *params* é um único valor inteiro que especifica a *densidade*, a densidade de neblina usada em equações de neblina exponencial.</span><span class="sxs-lookup"><span data-stu-id="1f81d-120">The *params* parameter is a single integer value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="1f81d-121">Somente as densidades não negativas são aceitas.</span><span class="sxs-lookup"><span data-stu-id="1f81d-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="1f81d-122">A densidade de neblina padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="1f81d-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="1f81d-123"><dt>**\_início da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="1f81d-124">O parâmetro *params* é um único valor inteiro que especifica *Start*, a distância próxima usada na equação de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="1f81d-124">The *params* parameter is a single integer value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="1f81d-125">O padrão próximo à distância é de 0,0.</span><span class="sxs-lookup"><span data-stu-id="1f81d-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="1f81d-126"><dt>**\_fim da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="1f81d-127">O parâmetro *params* é um único valor inteiro que especifica *end*, a distância mais usada na equação de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="1f81d-127">The *params* parameter is a single integer value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="1f81d-128">A distância padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="1f81d-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="1f81d-129"><dt>**\_índice de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="1f81d-130">O parâmetro *params* é um único valor inteiro que especifica *i*<sub>f</sub> , o índice de cores de neblina.</span><span class="sxs-lookup"><span data-stu-id="1f81d-130">The *params* parameter is a single integer value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="1f81d-131">O índice de neblina padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="1f81d-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="1f81d-132"><dt>**\_cor da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="1f81d-133">O parâmetro *params* contém quatro valores inteiros ou de ponto flutuante que especificam *C*<sub>f</sub> , a cor de neblina.</span><span class="sxs-lookup"><span data-stu-id="1f81d-133">The *params* parameter contains four integer or floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="1f81d-134">Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="1f81d-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="1f81d-135">Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="1f81d-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="1f81d-136">Após a conversão, todos os componentes de cor são clamped para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="1f81d-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="1f81d-137">A cor de neblina padrão é (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="1f81d-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f81d-138">*params*</span><span class="sxs-lookup"><span data-stu-id="1f81d-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="1f81d-139">Especifica o valor ou valores a serem atribuídos a *pname*.</span><span class="sxs-lookup"><span data-stu-id="1f81d-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="1f81d-140">\_ \_ A cor de neblina do GL requer uma matriz de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="1f81d-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="1f81d-141">Todos os outros parâmetros aceitam uma matriz que contém apenas um único valor.</span><span class="sxs-lookup"><span data-stu-id="1f81d-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f81d-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f81d-142">Return value</span></span>

<span data-ttu-id="1f81d-143">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1f81d-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f81d-144">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1f81d-144">Error codes</span></span>

<span data-ttu-id="1f81d-145">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1f81d-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1f81d-146">Nome</span><span class="sxs-lookup"><span data-stu-id="1f81d-146">Name</span></span>                                                                                                  | <span data-ttu-id="1f81d-147">Significado</span><span class="sxs-lookup"><span data-stu-id="1f81d-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f81d-148"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1f81d-149">*pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="1f81d-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="1f81d-150"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1f81d-151">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1f81d-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1f81d-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f81d-152">Remarks</span></span>

<span data-ttu-id="1f81d-153">Você habilita e desabilita a neblina com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), usando o argumento GL \_ neblina.</span><span class="sxs-lookup"><span data-stu-id="1f81d-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="1f81d-154">Enquanto habilitado, a neblina afeta a geometria, os bitmaps e os blocos de pixels rasterizados, mas não as operações de limpeza de buffer.</span><span class="sxs-lookup"><span data-stu-id="1f81d-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="1f81d-155">A função **glFogiv** atribui o valor ou valores em *params* para o parâmetro de neblina especificado por *pname*.</span><span class="sxs-lookup"><span data-stu-id="1f81d-155">The **glFogiv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="1f81d-156">A neblina combina uma cor de neblina com cada cor de posttexturing do fragmento de pixel rasterizado usando um fator de mistura *f*.</span><span class="sxs-lookup"><span data-stu-id="1f81d-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="1f81d-157">O fator *f* é calculado de uma das três maneiras, dependendo do modo de neblina.</span><span class="sxs-lookup"><span data-stu-id="1f81d-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="1f81d-158">Deixe que *z* seja a distância em coordenadas de olho da origem para o fragmento sendo fogged.</span><span class="sxs-lookup"><span data-stu-id="1f81d-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="1f81d-159">A equação para a \_ neblina linear do GL é:</span><span class="sxs-lookup"><span data-stu-id="1f81d-159">The equation for GL\_LINEAR fog is:</span></span>

![Equação mostrando o valor do fator de mesclagem no modo de neblina GL_LINEAR como uma função de distância.](images/fog01.png)

<span data-ttu-id="1f81d-161">A equação para o GL \_ exp neblina é:</span><span class="sxs-lookup"><span data-stu-id="1f81d-161">The equation for GL\_EXP fog is:</span></span>

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP neblina.](images/fog02.png)

<span data-ttu-id="1f81d-163">A equação para o GL \_ EXP2 neblina é:</span><span class="sxs-lookup"><span data-stu-id="1f81d-163">The equation for GL\_EXP2 fog is:</span></span>

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP2 neblina.](images/fog03.png)

<span data-ttu-id="1f81d-165">Independentemente do modo de neblina, *f* é clamped para o intervalo de \[ 0, 1 \] após ser computado.</span><span class="sxs-lookup"><span data-stu-id="1f81d-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="1f81d-166">Em seguida, se OpenGL estiver no modo de cor RGBA, a cor *C*<sub>r</sub> do fragmento será substituída por</span><span class="sxs-lookup"><span data-stu-id="1f81d-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Equação mostrando a cor do fragmento fogged como uma função de fator de mesclagem e cor de neblina.](images/fog04.png)

<span data-ttu-id="1f81d-168">No modo de índice de cor, o índice de cores do fragmento *i*<sub>r</sub> é substituído por</span><span class="sxs-lookup"><span data-stu-id="1f81d-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Equação mostrando o índice de cores do fragmento fogged como uma função de fator de mesclagem e cor indexada.](images/fog05.png)

<span data-ttu-id="1f81d-170">As funções a seguir recuperam informações relacionadas às funções **glFog** :</span><span class="sxs-lookup"><span data-stu-id="1f81d-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="1f81d-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a \_ cor de neblina do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="1f81d-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="1f81d-172">**glGet** com índice de neblina do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1f81d-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="1f81d-173">**glGet** com densidade de neblina de Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1f81d-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="1f81d-174">início da sombra do **glGet** com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1f81d-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="1f81d-175">**glGet** com término da neblina do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1f81d-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="1f81d-176">**glGet** com o \_ modo de sombra do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="1f81d-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="1f81d-177">[**glIsEnabled**](glisenabled.md) com sombra do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="1f81d-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="1f81d-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f81d-178">Requirements</span></span>



| <span data-ttu-id="1f81d-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f81d-179">Requirement</span></span> | <span data-ttu-id="1f81d-180">Valor</span><span class="sxs-lookup"><span data-stu-id="1f81d-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f81d-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f81d-181">Minimum supported client</span></span><br/> | <span data-ttu-id="1f81d-182">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1f81d-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1f81d-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f81d-183">Minimum supported server</span></span><br/> | <span data-ttu-id="1f81d-184">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1f81d-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f81d-185">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1f81d-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f81d-186"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1f81d-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f81d-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f81d-188"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f81d-189">DLL</span><span class="sxs-lookup"><span data-stu-id="1f81d-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f81d-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f81d-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f81d-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f81d-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f81d-192">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1f81d-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1f81d-193">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="1f81d-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="1f81d-194">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="1f81d-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="1f81d-195">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1f81d-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1f81d-196">**glGet**</span><span class="sxs-lookup"><span data-stu-id="1f81d-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="1f81d-197">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1f81d-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





