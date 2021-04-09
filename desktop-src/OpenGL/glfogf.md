---
title: Função glFogf (Gl.h)
description: O glFogf e a função especificam parâmetros de neblina.
ms.assetid: 69961d8f-385c-4353-aef3-38fb654c44f8
keywords:
- função glFogf OpenGL
topic_type:
- apiref
api_name:
- glFogf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe0509b30e91797752604110068701fcedaa266
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104011887"
---
# <a name="glfogf-function"></a><span data-ttu-id="c03c6-104">função glFogf</span><span class="sxs-lookup"><span data-stu-id="c03c6-104">glFogf function</span></span>

<span data-ttu-id="c03c6-105">O **glFogf** e a função especificam parâmetros de neblina.</span><span class="sxs-lookup"><span data-stu-id="c03c6-105">The **glFogf** and function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c03c6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c03c6-106">Syntax</span></span>


```C++
void WINAPI glFogf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="c03c6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c03c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03c6-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="c03c6-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="c03c6-109">Especifica um parâmetro de neblina de valor único.</span><span class="sxs-lookup"><span data-stu-id="c03c6-109">Specifies a single-valued fog parameter.</span></span>

<span data-ttu-id="c03c6-110">Aceita um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c03c6-110">Accepts one of the following values.</span></span>



| <span data-ttu-id="c03c6-111">Valor</span><span class="sxs-lookup"><span data-stu-id="c03c6-111">Value</span></span>                                                                                                                                                             | <span data-ttu-id="c03c6-112">Significado</span><span class="sxs-lookup"><span data-stu-id="c03c6-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="c03c6-113"><dt>**\_modo de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-113"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="c03c6-114">O parâmetro *params* é um único valor de ponto flutuante que especifica a equação a ser usada para calcular o fator de mistura de neblina, *f*.</span><span class="sxs-lookup"><span data-stu-id="c03c6-114">The *params* parameter is a single floating-point value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="c03c6-115">Três constantes simbólicas são aceitas: GL \_ linear, GL \_ exp e GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="c03c6-115">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="c03c6-116">As equações correspondentes a essas constantes simbólicas são definidas na seção comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="c03c6-116">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="c03c6-117">O modo de neblina padrão é GL \_ exp.</span><span class="sxs-lookup"><span data-stu-id="c03c6-117">The default fog mode is GL\_EXP.</span></span><br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="c03c6-118"><dt>**\_densidade de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-118"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="c03c6-119">O parâmetro *params* é um único valor de ponto flutuante que especifica a *densidade*, a densidade de neblina usada nas equações de neblina exponencial.</span><span class="sxs-lookup"><span data-stu-id="c03c6-119">The *params* parameter is a single floating-point value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="c03c6-120">Somente as densidades não negativas são aceitas.</span><span class="sxs-lookup"><span data-stu-id="c03c6-120">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="c03c6-121">A densidade de neblina padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="c03c6-121">The default fog density is 1.0.</span></span><br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="c03c6-122"><dt>**\_início da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-122"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="c03c6-123">O parâmetro *params* é um único valor de ponto flutuante que especifica *Start*, a distância próxima usada na equação de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="c03c6-123">The *params* parameter is a single floating-point value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="c03c6-124">O padrão próximo à distância é de 0,0.</span><span class="sxs-lookup"><span data-stu-id="c03c6-124">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="c03c6-125"><dt>**\_fim da neblina do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-125"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="c03c6-126">O parâmetro *params* é um único valor de ponto flutuante que especifica *end*, a distância mais usada na equação de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="c03c6-126">The *params* parameter is a single floating-point value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="c03c6-127">A distância padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="c03c6-127">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="c03c6-128"><dt>**\_índice de neblina GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-128"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="c03c6-129">O parâmetro *params* é um único valor de ponto flutuante que especifica *i*<sub>f</sub> , o índice de cores de neblina.</span><span class="sxs-lookup"><span data-stu-id="c03c6-129">The *params* parameter is a single floating-point value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="c03c6-130">O índice de neblina padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="c03c6-130">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="c03c6-131">*param*</span><span class="sxs-lookup"><span data-stu-id="c03c6-131">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="c03c6-132">Especifica o valor para o qual *pname* será definido.</span><span class="sxs-lookup"><span data-stu-id="c03c6-132">Specifies the value that *pname* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03c6-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c03c6-133">Return value</span></span>

<span data-ttu-id="c03c6-134">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c03c6-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c03c6-135">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c03c6-135">Error codes</span></span>

<span data-ttu-id="c03c6-136">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c03c6-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c03c6-137">Nome</span><span class="sxs-lookup"><span data-stu-id="c03c6-137">Name</span></span>                                                                                                  | <span data-ttu-id="c03c6-138">Significado</span><span class="sxs-lookup"><span data-stu-id="c03c6-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c03c6-139"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="c03c6-140">*pname* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="c03c6-140">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="c03c6-141"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c03c6-142">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c03c6-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c03c6-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="c03c6-143">Remarks</span></span>

<span data-ttu-id="c03c6-144">Você habilita e desabilita a neblina com [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), usando o argumento GL \_ neblina.</span><span class="sxs-lookup"><span data-stu-id="c03c6-144">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="c03c6-145">Enquanto habilitado, a neblina afeta a geometria, os bitmaps e os blocos de pixels rasterizados, mas não as operações de limpeza de buffer.</span><span class="sxs-lookup"><span data-stu-id="c03c6-145">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="c03c6-146">A função **glFogf** atribui o valor ou valores em *params* para o parâmetro de neblina especificado por *pname*.</span><span class="sxs-lookup"><span data-stu-id="c03c6-146">The **glFogf** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="c03c6-147">A neblina combina uma cor de neblina com cada cor de posttexturing do fragmento de pixel rasterizado usando um fator de mistura *f*.</span><span class="sxs-lookup"><span data-stu-id="c03c6-147">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="c03c6-148">O fator *f* é calculado de uma das três maneiras, dependendo do modo de neblina.</span><span class="sxs-lookup"><span data-stu-id="c03c6-148">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="c03c6-149">Deixe que *z* seja a distância em coordenadas de olho da origem para o fragmento sendo fogged.</span><span class="sxs-lookup"><span data-stu-id="c03c6-149">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="c03c6-150">A equação para a \_ neblina linear do GL é:</span><span class="sxs-lookup"><span data-stu-id="c03c6-150">The equation for GL\_LINEAR fog is:</span></span>

![Equação mostrando o valor de GL_LINEAR neblina.](images/fog01.png)

<span data-ttu-id="c03c6-152">A equação para o GL \_ exp neblina é:</span><span class="sxs-lookup"><span data-stu-id="c03c6-152">The equation for GL\_EXP fog is:</span></span>

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP neblina.](images/fog02.png)

<span data-ttu-id="c03c6-154">A equação para o GL \_ EXP2 neblina é:</span><span class="sxs-lookup"><span data-stu-id="c03c6-154">The equation for GL\_EXP2 fog is:</span></span>

![Equação mostrando o valor do fator de mesclagem no modo GL_EXP2 neblina.](images/fog03.png)

<span data-ttu-id="c03c6-156">Independentemente do modo de neblina, *f* é clamped para o intervalo de \[ 0, 1 \] após ser computado.</span><span class="sxs-lookup"><span data-stu-id="c03c6-156">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="c03c6-157">Em seguida, se OpenGL estiver no modo de cor RGBA, a cor *C*<sub>r</sub> do fragmento será substituída por</span><span class="sxs-lookup"><span data-stu-id="c03c6-157">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Equação mostrando a cor do fragmento fogged como uma função de fator de mesclagem e cor de neblina.](images/fog04.png)

<span data-ttu-id="c03c6-159">No modo de índice de cor, o índice de cores do fragmento *i*<sub>r</sub> é substituído por</span><span class="sxs-lookup"><span data-stu-id="c03c6-159">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Equação mostrando o índice de cores do fragmento fogged como uma função de fator de mesclagem e cor indexada.](images/fog05.png)

<span data-ttu-id="c03c6-161">As funções a seguir recuperam informações relacionadas às funções **glFog** :</span><span class="sxs-lookup"><span data-stu-id="c03c6-161">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="c03c6-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com a \_ cor de neblina do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="c03c6-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="c03c6-163">**glGet** com índice de neblina do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="c03c6-163">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="c03c6-164">**glGet** com densidade de neblina de Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="c03c6-164">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="c03c6-165">início da sombra do **glGet** com Argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="c03c6-165">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="c03c6-166">**glGet** com término da neblina do argumento GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="c03c6-166">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="c03c6-167">**glGet** com o \_ modo de sombra do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="c03c6-167">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="c03c6-168">[**glIsEnabled**](glisenabled.md) com sombra do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="c03c6-168">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="c03c6-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c03c6-169">Requirements</span></span>



| <span data-ttu-id="c03c6-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="c03c6-170">Requirement</span></span> | <span data-ttu-id="c03c6-171">Valor</span><span class="sxs-lookup"><span data-stu-id="c03c6-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c03c6-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c03c6-172">Minimum supported client</span></span><br/> | <span data-ttu-id="c03c6-173">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c03c6-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c03c6-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c03c6-174">Minimum supported server</span></span><br/> | <span data-ttu-id="c03c6-175">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c03c6-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c03c6-176">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c03c6-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="c03c6-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c03c6-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c03c6-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="c03c6-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c03c6-180">DLL</span><span class="sxs-lookup"><span data-stu-id="c03c6-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c03c6-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c03c6-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c03c6-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="c03c6-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03c6-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c03c6-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c03c6-184">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="c03c6-184">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="c03c6-185">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="c03c6-185">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="c03c6-186">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c03c6-186">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c03c6-187">**glGet**</span><span class="sxs-lookup"><span data-stu-id="c03c6-187">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="c03c6-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="c03c6-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





