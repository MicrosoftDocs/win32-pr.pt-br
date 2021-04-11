---
title: Função glFogfv (Gl.h)
description: A função glFogfv especifica parâmetros de neblina. | função glFogfv (GL. h)
ms.assetid: a2243ff4-4f3a-4b8c-b4fb-ce2cd74815e4
keywords:
- função glFogfv OpenGL
topic_type:
- apiref
api_name:
- glFogfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407dd9b9c984a744e903a2c269d21028d32977a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172880"
---
# <a name="glfogfv-function"></a><span data-ttu-id="8b136-105">função glFogfv</span><span class="sxs-lookup"><span data-stu-id="8b136-105">glFogfv function</span></span>

<span data-ttu-id="8b136-106">A função **glFogfv** especifica parâmetros de neblina.</span><span class="sxs-lookup"><span data-stu-id="8b136-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b136-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b136-107">Syntax</span></span>


```C++
void WINAPI glFogfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="8b136-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b136-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b136-109">*pname*</span><span class="sxs-lookup"><span data-stu-id="8b136-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="8b136-110">Especifica um parâmetro de neblina.</span><span class="sxs-lookup"><span data-stu-id="8b136-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="8b136-111">Aceita um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b136-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="8b136-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8b136-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="8b136-113">Significado</span><span class="sxs-lookup"><span data-stu-id="8b136-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="8b136-114"><dt>**\_modo de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="8b136-115">O parâmetro *params* é um valor de ponto flutuante que especifica a equação a ser usada para calcular o fator de mistura de neblina, *f*.</span><span class="sxs-lookup"><span data-stu-id="8b136-115">The *params* parameter is a floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="8b136-116">Três constantes simbólicas são aceitas: GL \_ linear, GL \_ exp e GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="8b136-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="8b136-117">As equações correspondentes a essas constantes simbólicas são definidas na seção comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b136-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="8b136-118">O modo de neblina padrão é GL \_ exp.</span><span class="sxs-lookup"><span data-stu-id="8b136-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                           |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="8b136-119"><dt>**\_densidade de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="8b136-120">O parâmetro *params* é um valor de ponto flutuante que especifica *densidade*, a densidade de neblina usada em equações de neblina exponencial.</span><span class="sxs-lookup"><span data-stu-id="8b136-120">The *params* parameter is a floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="8b136-121">Somente as densidades não negativas são aceitas.</span><span class="sxs-lookup"><span data-stu-id="8b136-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="8b136-122">A densidade de neblina padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="8b136-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                              |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="8b136-123"><dt>**\_início da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="8b136-124">O parâmetro *params* é um valor de ponto flutuante que especifica *Start*, a distância próxima usada na equação de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="8b136-124">The *params* parameter is a floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="8b136-125">O padrão próximo à distância é de 0,0.</span><span class="sxs-lookup"><span data-stu-id="8b136-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="8b136-126"><dt>**\_fim da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="8b136-127">O parâmetro *params* é um valor de ponto flutuante que especifica *end*, a distância distante usada na equação de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="8b136-127">The *params* parameter is a floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="8b136-128">A distância padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="8b136-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="8b136-129"><dt>**\_índice de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="8b136-130">O parâmetro *params* é um valor de ponto flutuante que especifica *i*<sub>f</sub> , o índice de cores de neblina.</span><span class="sxs-lookup"><span data-stu-id="8b136-130">The *params* parameter is a floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="8b136-131">O índice de neblina padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="8b136-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="8b136-132"><dt>**\_cor da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="8b136-133">O parâmetro *params* contém quatro valores de ponto flutuante que especificam *C*<sub>f</sub> , a cor de neblina.</span><span class="sxs-lookup"><span data-stu-id="8b136-133">The *params* parameter contains four floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="8b136-134">Os valores inteiros são mapeados linearmente, de modo que o valor representável mais positivo é mapeado para 1,0 e o valor reapresentável mais negativo é mapeado para-1,0.</span><span class="sxs-lookup"><span data-stu-id="8b136-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="8b136-135">Os valores de ponto flutuante são mapeados diretamente.</span><span class="sxs-lookup"><span data-stu-id="8b136-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="8b136-136">Após a conversão, todos os componentes de cor são clamped para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="8b136-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="8b136-137">A cor de neblina padrão é (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="8b136-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8b136-138">*params*</span><span class="sxs-lookup"><span data-stu-id="8b136-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="8b136-139">Especifica o valor ou valores a serem atribuídos a *pname*.</span><span class="sxs-lookup"><span data-stu-id="8b136-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="8b136-140">\_ \_ A cor de neblina do GL requer uma matriz de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="8b136-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="8b136-141">Todos os outros parâmetros aceitam uma matriz que contém apenas um único valor.</span><span class="sxs-lookup"><span data-stu-id="8b136-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b136-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b136-142">Return value</span></span>

<span data-ttu-id="8b136-143">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8b136-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b136-144">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8b136-144">Error codes</span></span>

<span data-ttu-id="8b136-145">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8b136-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8b136-146">Nome</span><span class="sxs-lookup"><span data-stu-id="8b136-146">Name</span></span>                                                                                                  | <span data-ttu-id="8b136-147">Significado</span><span class="sxs-lookup"><span data-stu-id="8b136-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b136-148"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8b136-149">*pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="8b136-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="8b136-150"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8b136-151">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8b136-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8b136-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b136-152">Remarks</span></span>

<span data-ttu-id="8b136-153">Você habilita e desabilita a neblina com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), usando o argumento GL \_ neblina.</span><span class="sxs-lookup"><span data-stu-id="8b136-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="8b136-154">Enquanto habilitado, a neblina afeta a geometria, os bitmaps e os blocos de pixels rasterizados, mas não as operações de limpeza de buffer.</span><span class="sxs-lookup"><span data-stu-id="8b136-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="8b136-155">A função **glFogfv** atribui o valor ou valores em *params* para o parâmetro de neblina especificado por *pname*.</span><span class="sxs-lookup"><span data-stu-id="8b136-155">The **glFogfv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="8b136-156">A neblina combina uma cor de neblina com cada cor de posttexturing do fragmento de pixel rasterizado usando um fator de mistura *f*.</span><span class="sxs-lookup"><span data-stu-id="8b136-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="8b136-157">O fator *f* é calculado de uma das três maneiras, dependendo do modo de neblina.</span><span class="sxs-lookup"><span data-stu-id="8b136-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="8b136-158">Deixe que *z* seja a distância em coordenadas de olho da origem para o fragmento sendo fogged.</span><span class="sxs-lookup"><span data-stu-id="8b136-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="8b136-159">A equação para a \_ neblina linear do GL é:</span><span class="sxs-lookup"><span data-stu-id="8b136-159">The equation for GL\_LINEAR fog is:</span></span>

![Equação mostrando o valor de GL_LINEAR neblina.](images/fog01.png)

<span data-ttu-id="8b136-161">A equação para o GL \_ exp neblina é:</span><span class="sxs-lookup"><span data-stu-id="8b136-161">The equation for GL\_EXP fog is:</span></span>

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP neblina.](images/fog02.png)

<span data-ttu-id="8b136-163">A equação para o GL \_ EXP2 neblina é:</span><span class="sxs-lookup"><span data-stu-id="8b136-163">The equation for GL\_EXP2 fog is:</span></span>

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP2 neblina.](images/fog03.png)

<span data-ttu-id="8b136-165">Independentemente do modo de neblina, *f* é clamped para o intervalo de \[ 0, 1 \] após ser computado.</span><span class="sxs-lookup"><span data-stu-id="8b136-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="8b136-166">Em seguida, se OpenGL estiver no modo de cor RGBA, a cor *C*<sub>r</sub> do fragmento será substituída por</span><span class="sxs-lookup"><span data-stu-id="8b136-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Equação mostrando a cor do fragmento fogged como uma função de fator de mesclagem e cor de neblina.](images/fog04.png)

<span data-ttu-id="8b136-168">No modo de índice de cor, o índice de cores do fragmento *i*<sub>r</sub> é substituído por</span><span class="sxs-lookup"><span data-stu-id="8b136-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Equação mostrando o índice de cores do fragmento fogged como uma função de fator de mesclagem e cor indexada.](images/fog05.png)

<span data-ttu-id="8b136-170">As funções a seguir recuperam informações relacionadas às funções **glFog** :</span><span class="sxs-lookup"><span data-stu-id="8b136-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="8b136-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a \_ cor de neblina do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="8b136-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="8b136-172">**glGet** com índice de neblina do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8b136-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="8b136-173">**glGet** com densidade de neblina de Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8b136-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="8b136-174">início da sombra do **glGet** com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8b136-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="8b136-175">**glGet** com término da neblina do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8b136-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="8b136-176">**glGet** com o \_ modo de sombra do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="8b136-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="8b136-177">[**glIsEnabled**](glisenabled.md) com sombra do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="8b136-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="8b136-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b136-178">Requirements</span></span>



| <span data-ttu-id="8b136-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b136-179">Requirement</span></span> | <span data-ttu-id="8b136-180">Valor</span><span class="sxs-lookup"><span data-stu-id="8b136-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b136-181">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b136-181">Minimum supported client</span></span><br/> | <span data-ttu-id="8b136-182">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8b136-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8b136-183">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b136-183">Minimum supported server</span></span><br/> | <span data-ttu-id="8b136-184">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8b136-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b136-185">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8b136-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b136-186"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8b136-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b136-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b136-188"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8b136-189">DLL</span><span class="sxs-lookup"><span data-stu-id="8b136-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b136-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b136-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b136-191">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b136-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b136-192">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8b136-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8b136-193">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="8b136-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="8b136-194">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="8b136-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="8b136-195">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8b136-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8b136-196">**glGet**</span><span class="sxs-lookup"><span data-stu-id="8b136-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8b136-197">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="8b136-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





