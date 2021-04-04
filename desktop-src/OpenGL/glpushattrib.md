---
title: função glPushAttrib (GL. h)
description: Envia a pilha de atributos por push.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- função glPushAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009051"
---
# <a name="glpushattrib-function"></a><span data-ttu-id="7a4ec-104">função glPushAttrib</span><span class="sxs-lookup"><span data-stu-id="7a4ec-104">glPushAttrib function</span></span>

<span data-ttu-id="7a4ec-105">Envia a pilha de atributos por push.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-105">Pushes the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4ec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a4ec-106">Syntax</span></span>


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="7a4ec-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a4ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a4ec-108">*mascara*</span><span class="sxs-lookup"><span data-stu-id="7a4ec-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="7a4ec-109">Uma máscara que indica quais atributos salvar.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-109">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="7a4ec-110">As constantes de máscara simbólica e seu estado de OpenGL associado são os seguintes (os parágrafos recuados listam os atributos que são salvos):</span><span class="sxs-lookup"><span data-stu-id="7a4ec-110">The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):</span></span>

<dl> <dt>

<span data-ttu-id="7a4ec-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>BIT de buffer do GL \_ Accum \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL\_ACCUM\_BUFFER\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="7a4ec-112">Valor de limpeza do buffer de acumulação</span><span class="sxs-lookup"><span data-stu-id="7a4ec-112">Accumulation buffer clear value</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit do \_ buffer de cores GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL\_COLOR\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-114">\_Bit de \_ habilitação de teste do GL alfa</span><span class="sxs-lookup"><span data-stu-id="7a4ec-114">GL\_ALPHA\_TEST enable bit</span></span>

<span data-ttu-id="7a4ec-115">Função de teste alfa e valor de referência</span><span class="sxs-lookup"><span data-stu-id="7a4ec-115">Alpha test function and reference value</span></span>

<span data-ttu-id="7a4ec-116">\_Bit de habilitação do GL Blend</span><span class="sxs-lookup"><span data-stu-id="7a4ec-116">GL\_BLEND enable bit</span></span>

<span data-ttu-id="7a4ec-117">Combinando funções de origem e de destino</span><span class="sxs-lookup"><span data-stu-id="7a4ec-117">Blending source and destination functions</span></span>

<span data-ttu-id="7a4ec-118">\_Bit de habilitação de pontilhamento GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-118">GL\_DITHER enable bit</span></span>

<span data-ttu-id="7a4ec-119">Configuração do buffer de \_ desenho GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-119">GL\_DRAW\_BUFFER setting</span></span>

<span data-ttu-id="7a4ec-120">\_Bit de \_ habilitação de op lógico GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-120">GL\_LOGIC\_OP enable bit</span></span>

<span data-ttu-id="7a4ec-121">Função op lógica</span><span class="sxs-lookup"><span data-stu-id="7a4ec-121">Logic op function</span></span>

<span data-ttu-id="7a4ec-122">Valores claros de modo de cor e de modo de índice</span><span class="sxs-lookup"><span data-stu-id="7a4ec-122">Color-mode and index-mode clear values</span></span>

<span data-ttu-id="7a4ec-123">Modo de cor e writemasks de modo de índice</span><span class="sxs-lookup"><span data-stu-id="7a4ec-123">Color-mode and index-mode writemasks</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>BIT do GL \_ atual \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL\_CURRENT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-125">Cor RGBA atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-125">Current RGBA color</span></span>

<span data-ttu-id="7a4ec-126">Índice de cores atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-126">Current color index</span></span>

<span data-ttu-id="7a4ec-127">Vetor normal atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-127">Current normal vector</span></span>

<span data-ttu-id="7a4ec-128">Coordenadas de textura atuais</span><span class="sxs-lookup"><span data-stu-id="7a4ec-128">Current texture coordinates</span></span>

<span data-ttu-id="7a4ec-129">\_ \_ \_ Sinalizador válido de posição de \_ rasterização atual de posição de varredura atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-129">Current raster position GL\_CURRENT\_RASTER\_POSITION\_VALID flag</span></span>

<span data-ttu-id="7a4ec-130">Cor RGBA associada à posição de rasterização atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-130">RGBA color associated with current raster position</span></span>

<span data-ttu-id="7a4ec-131">Índice de cores associado à posição de rasterização atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-131">Color index associated with current raster position</span></span>

<span data-ttu-id="7a4ec-132">Coordenadas de textura associadas à posição de rasterização atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-132">Texture coordinates associated with current raster position</span></span>

<span data-ttu-id="7a4ec-133">Sinalizador de sinalizador de \_ borda GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-133">GL\_EDGE\_FLAG flag</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_bit de \_ buffer de profundidade GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL\_DEPTH\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-135">\_Bit de \_ habilitação de teste de profundidade GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-135">GL\_DEPTH\_TEST enable bit</span></span>

<span data-ttu-id="7a4ec-136">Função de teste do buffer de profundidade</span><span class="sxs-lookup"><span data-stu-id="7a4ec-136">Depth buffer test function</span></span>

<span data-ttu-id="7a4ec-137">Valor de limpeza do buffer de profundidade</span><span class="sxs-lookup"><span data-stu-id="7a4ec-137">Depth buffer clear value</span></span>

<span data-ttu-id="7a4ec-138">\_Bit GL \_ WRITEMASK de habilitação de profundidade</span><span class="sxs-lookup"><span data-stu-id="7a4ec-138">GL\_DEPTH\_WRITEMASK enable bit</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit de habilitação GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL\_ENABLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-140">\_Sinalizador de teste alfa do GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-140">GL\_ALPHA\_TEST flag</span></span>

<span data-ttu-id="7a4ec-141">\_Sinalizador normal automático do GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-141">GL\_AUTO\_NORMAL flag</span></span>

<span data-ttu-id="7a4ec-142">\_Sinalizador de combinação GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-142">GL\_BLEND flag</span></span>

<span data-ttu-id="7a4ec-143">Habilitar bits para os planos de recorte definíveis pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7a4ec-143">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="7a4ec-144">\_material de cor GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-144">GL\_COLOR\_MATERIAL</span></span>

<span data-ttu-id="7a4ec-145">Sinalizador de face de \_ seleção GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-145">GL\_CULL\_FACE flag</span></span>

<span data-ttu-id="7a4ec-146">Sinalizador de teste de \_ profundidade GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-146">GL\_DEPTH\_TEST flag</span></span>

<span data-ttu-id="7a4ec-147">\_Sinalizador de pontilhamento GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-147">GL\_DITHER flag</span></span>

<span data-ttu-id="7a4ec-148">\_Sinalizador de neblina GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-148">GL\_FOG flag</span></span>

<span data-ttu-id="7a4ec-149">GL \_ Light *i* em que 0 <= *i* < GL \_ Max \_ luzes</span><span class="sxs-lookup"><span data-stu-id="7a4ec-149">GL\_LIGHT *i* where 0 <= *i* < GL\_MAX\_LIGHTS</span></span>

<span data-ttu-id="7a4ec-150">\_Sinalizador de iluminação GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-150">GL\_LIGHTING flag</span></span>

<span data-ttu-id="7a4ec-151">\_Sinalizador Smooth de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-151">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="7a4ec-152">Sinalizador de STIPPLE de \_ linha gl \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-152">GL\_LINE\_STIPPLE flag</span></span>

<span data-ttu-id="7a4ec-153">\_Sinalizador de \_ op da lógica de cores GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-153">GL\_COLOR\_LOGIC\_OP flag</span></span>

<span data-ttu-id="7a4ec-154">\_Sinalizador de \_ op lógico de índice GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-154">GL\_INDEX\_LOGIC\_OP flag</span></span>

<span data-ttu-id="7a4ec-155">GL \_ MAP1 \_ x, em que x é um tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="7a4ec-155">GL\_MAP1\_x where x is a map type</span></span>

<span data-ttu-id="7a4ec-156">GL \_ map2 \_ x, em que x é um tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="7a4ec-156">GL\_MAP2\_x where x is a map type</span></span>

<span data-ttu-id="7a4ec-157">\_Sinalizador de NORMALIZE GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-157">GL\_NORMALIZE flag</span></span>

<span data-ttu-id="7a4ec-158">\_Sinalizador suave de ponto GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-158">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="7a4ec-159">\_Sinalizador de \_ linha de deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-159">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="7a4ec-160">\_Sinalizador de \_ preenchimento de deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-160">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="7a4ec-161">\_Sinalizador de \_ ponto de deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-161">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="7a4ec-162">\_Sinalizador suave do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-162">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="7a4ec-163">\_Sinalizador STIPPLE de polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-163">GL\_POLYGON\_STIPPLE flag</span></span>

<span data-ttu-id="7a4ec-164">Sinalizador de teste de \_ tesoura GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-164">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="7a4ec-165">Sinalizador de teste do \_ estêncil GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-165">GL\_STENCIL\_TEST flag</span></span>

<span data-ttu-id="7a4ec-166">Sinalizador de 1D de \_ textura GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-166">GL\_TEXTURE\_1D flag</span></span>

<span data-ttu-id="7a4ec-167">\_Sinalizador de textura 2D do GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-167">GL\_TEXTURE\_2D flag</span></span>

<span data-ttu-id="7a4ec-168">Sinalizadores GL \_ Texture \_ Gen \_ x em que x é S, T, R ou Q</span><span class="sxs-lookup"><span data-stu-id="7a4ec-168">Flags GL\_TEXTURE\_GEN\_x where x is S, T, R, or Q</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>\_bit de avaliação GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL\_EVAL\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-170">GL \_ MAP1 \_ x habilitar bits, em que x é um tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="7a4ec-170">GL\_MAP1\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="7a4ec-171">GL \_ map2 \_ x habilitar bits, em que x é um tipo de mapa</span><span class="sxs-lookup"><span data-stu-id="7a4ec-171">GL\_MAP2\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="7a4ec-172">pontos de extremidade de grade 1-D e divisões</span><span class="sxs-lookup"><span data-stu-id="7a4ec-172">1-D grid endpoints and divisions</span></span>

<span data-ttu-id="7a4ec-173">pontos de extremidade de grade 2D e divisões</span><span class="sxs-lookup"><span data-stu-id="7a4ec-173">2-D grid endpoints and divisions</span></span>

<span data-ttu-id="7a4ec-174">\_Bit de \_ habilitação normal automática do GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-174">GL\_AUTO\_NORMAL enable bit</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit de neblina GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL\_FOG\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-176">\_Sinalizador de habilitação de neblina do GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-176">GL\_FOG enable flag</span></span>

<span data-ttu-id="7a4ec-177">Cor da neblina</span><span class="sxs-lookup"><span data-stu-id="7a4ec-177">Fog color</span></span>

<span data-ttu-id="7a4ec-178">Densidade de neblina</span><span class="sxs-lookup"><span data-stu-id="7a4ec-178">Fog density</span></span>

<span data-ttu-id="7a4ec-179">Início da neblina linear</span><span class="sxs-lookup"><span data-stu-id="7a4ec-179">Linear fog start</span></span>

<span data-ttu-id="7a4ec-180">Fim da neblina linear</span><span class="sxs-lookup"><span data-stu-id="7a4ec-180">Linear fog end</span></span>

<span data-ttu-id="7a4ec-181">Índice de neblina</span><span class="sxs-lookup"><span data-stu-id="7a4ec-181">Fog index</span></span>

<span data-ttu-id="7a4ec-182">Valor do modo de \_ neblina do GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-182">GL\_FOG\_MODE value</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit de dica GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL\_HINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-184">\_Configuração da \_ dica de correção de perspectiva GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-184">GL\_PERSPECTIVE\_CORRECTION\_HINT setting</span></span>

<span data-ttu-id="7a4ec-185">\_Configuração de \_ dica simples do ponto GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-185">GL\_POINT\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="7a4ec-186">\_Configuração de \_ dica Smooth de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-186">GL\_LINE\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="7a4ec-187">\_Configuração de \_ \_ dica do Polygon do GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-187">GL\_POLYGON\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="7a4ec-188">Configuração de dica de \_ neblina do GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-188">GL\_FOG\_HINT setting</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit de iluminação GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL\_LIGHTING\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-190">\_Bit de \_ habilitação do material de cor GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-190">GL\_COLOR\_MATERIAL enable bit</span></span>

<span data-ttu-id="7a4ec-191">\_Valor de \_ face do material de cor GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-191">GL\_COLOR\_MATERIAL\_FACE value</span></span>

<span data-ttu-id="7a4ec-192">Parâmetros de material de cor que estão acompanhando a cor atual</span><span class="sxs-lookup"><span data-stu-id="7a4ec-192">Color material parameters that are tracking the current color</span></span>

<span data-ttu-id="7a4ec-193">Cor da cena ambiente</span><span class="sxs-lookup"><span data-stu-id="7a4ec-193">Ambient scene color</span></span>

<span data-ttu-id="7a4ec-194">\_Valor do \_ \_ Visualizador local do modelo Light GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-194">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER value</span></span>

<span data-ttu-id="7a4ec-195">\_ \_ \_ \_ Configuração do lado do modelo Light GL dois lados</span><span class="sxs-lookup"><span data-stu-id="7a4ec-195">GL\_LIGHT\_MODEL\_TWO\_SIDE setting</span></span>

<span data-ttu-id="7a4ec-196">\_Bit de habilitação de iluminação GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-196">GL\_LIGHTING enable bit</span></span>

<span data-ttu-id="7a4ec-197">Habilitar bit para cada luz</span><span class="sxs-lookup"><span data-stu-id="7a4ec-197">Enable bit for each light</span></span>

<span data-ttu-id="7a4ec-198">Intensidade de ambiente, difuso e especular para cada luz</span><span class="sxs-lookup"><span data-stu-id="7a4ec-198">Ambient, diffuse, and specular intensity for each light</span></span>

<span data-ttu-id="7a4ec-199">Direção, posição, expoente e ângulo de corte para cada luz</span><span class="sxs-lookup"><span data-stu-id="7a4ec-199">Direction, position, exponent, and cutoff angle for each light</span></span>

<span data-ttu-id="7a4ec-200">Fatores de atenuação constantes, lineares e quadráticas para cada luz</span><span class="sxs-lookup"><span data-stu-id="7a4ec-200">Constant, linear, and quadratic attenuation factors for each light</span></span>

<span data-ttu-id="7a4ec-201">Cor de ambiente, difuso, especular e emissiva para cada material</span><span class="sxs-lookup"><span data-stu-id="7a4ec-201">Ambient, diffuse, specular, and emissive color for each material</span></span>

<span data-ttu-id="7a4ec-202">Índices de cores de ambiente, difuso e especulares para cada material</span><span class="sxs-lookup"><span data-stu-id="7a4ec-202">Ambient, diffuse, and specular color indexes for each material</span></span>

<span data-ttu-id="7a4ec-203">Expoente especular para cada configuração de modelo de \_ tonalidade de material GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-203">Specular exponent for each material GL\_SHADE\_MODEL setting</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL\_LINE\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="7a4ec-205">\_Sinalizador Smooth de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-205">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="7a4ec-206">\_STIPPLE de linha gl \_ habilitar bit</span><span class="sxs-lookup"><span data-stu-id="7a4ec-206">GL\_LINE\_STIPPLE enable bit</span></span>

<span data-ttu-id="7a4ec-207">Padrão de Stipple de linha e contador de repetição</span><span class="sxs-lookup"><span data-stu-id="7a4ec-207">Line stipple pattern and repeat counter</span></span>

<span data-ttu-id="7a4ec-208">Largura da linha</span><span class="sxs-lookup"><span data-stu-id="7a4ec-208">Line width</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit da lista GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL\_LIST\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-210">Configuração da base da \_ lista GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-210">GL\_LIST\_BASE setting</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit do \_ modo de pixel GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL\_PIXEL\_MODE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-212">\_Configurações de escala do GL vermelho \_ e GL em \_ vermelho \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-212">GL\_RED\_BIAS and GL\_RED\_SCALE settings</span></span>

<span data-ttu-id="7a4ec-213">\_ \_ Valores de escala GL verde e GL \_ verde \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-213">GL\_GREEN\_BIAS and GL\_GREEN\_SCALE values</span></span>

<span data-ttu-id="7a4ec-214">\_Diferença azul do GL \_ e \_ escala azul do GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-214">GL\_BLUE\_BIAS and GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="7a4ec-215">\_ \_ Escala de alfa de polarização alfa e GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-215">GL\_ALPHA\_BIAS and GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="7a4ec-216">\_ \_ Escala de profundidade de nível GL e GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-216">GL\_DEPTH\_BIAS and GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="7a4ec-217">\_ \_ Valores de deslocamento do índice GL e do \_ índice GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-217">GL\_INDEX\_OFFSET and GL\_INDEX\_SHIFT values</span></span>

<span data-ttu-id="7a4ec-218">\_ \_ Sinalizadores de estêncil de mapa de cores e de \_ mapas GL GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-218">GL\_MAP\_COLOR and GL\_MAP\_STENCIL flags</span></span>

<span data-ttu-id="7a4ec-219">GL \_ \_ de zoom X e GL- \_ \_ fatores Y de zoom</span><span class="sxs-lookup"><span data-stu-id="7a4ec-219">GL\_ZOOM\_X and GL\_ZOOM\_Y factors</span></span>

<span data-ttu-id="7a4ec-220">Configuração do buffer de \_ leitura GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-220">GL\_READ\_BUFFER setting</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit de ponto GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL\_POINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-222">\_Sinalizador suave de ponto GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-222">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="7a4ec-223">Tamanho do ponto</span><span class="sxs-lookup"><span data-stu-id="7a4ec-223">Point size</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL\_POLYGON\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-225">\_Bit de \_ habilitação de face de seleção GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-225">GL\_CULL\_FACE enable bit</span></span>

<span data-ttu-id="7a4ec-226">\_Valor do modo de seleção de \_ face GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-226">GL\_CULL\_FACE\_MODE value</span></span>

<span data-ttu-id="7a4ec-227">\_Indicador de front face do GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-227">GL\_FRONT\_FACE indicator</span></span>

<span data-ttu-id="7a4ec-228">Configuração do modo de \_ polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-228">GL\_POLYGON\_MODE setting</span></span>

<span data-ttu-id="7a4ec-229">\_Sinalizador suave do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-229">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="7a4ec-230">\_STIPPLE Polygon GL \_ bit de habilitação</span><span class="sxs-lookup"><span data-stu-id="7a4ec-230">GL\_POLYGON\_STIPPLE enable bit</span></span>

<span data-ttu-id="7a4ec-231">\_Sinalizador de \_ preenchimento de deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-231">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="7a4ec-232">\_Sinalizador de \_ linha de deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-232">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="7a4ec-233">\_Sinalizador de \_ ponto de deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-233">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="7a4ec-234">\_fator de \_ deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-234">GL\_POLYGON\_OFFSET\_FACTOR</span></span>

<span data-ttu-id="7a4ec-235">\_unidades de \_ deslocamento do polígono GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-235">GL\_POLYGON\_OFFSET\_UNITS</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_STIPPLE de polígono do GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL\_POLYGON\_STIPPLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-237">Imagem de Stipple do polígono</span><span class="sxs-lookup"><span data-stu-id="7a4ec-237">Polygon stipple image</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>BIT GL de \_ tesoura \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL\_SCISSOR\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-239">Sinalizador de teste de \_ tesoura GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-239">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="7a4ec-240">Caixa de tesoura</span><span class="sxs-lookup"><span data-stu-id="7a4ec-240">Scissor box</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_bit de \_ buffer do estêncil GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL\_STENCIL\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-242">\_Bit de \_ habilitação de teste do estêncil GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-242">GL\_STENCIL\_TEST enable bit</span></span>

<span data-ttu-id="7a4ec-243">Função de estêncil e valor de referência</span><span class="sxs-lookup"><span data-stu-id="7a4ec-243">Stencil function and reference value</span></span>

<span data-ttu-id="7a4ec-244">Máscara de valor do estêncil</span><span class="sxs-lookup"><span data-stu-id="7a4ec-244">Stencil value mask</span></span>

<span data-ttu-id="7a4ec-245">Ações de passagem de buffer de falha, passagem e profundidade do estêncil</span><span class="sxs-lookup"><span data-stu-id="7a4ec-245">Stencil fail, pass, and depth buffer pass actions</span></span>

<span data-ttu-id="7a4ec-246">Valor de limpeza do buffer do estêncil</span><span class="sxs-lookup"><span data-stu-id="7a4ec-246">Stencil buffer clear value</span></span>

<span data-ttu-id="7a4ec-247">Writemask do buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="7a4ec-247">Stencil buffer writemask</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL\_TEXTURE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-249">Habilitar bits para as quatro coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="7a4ec-249">Enable bits for the four texture coordinates</span></span>

<span data-ttu-id="7a4ec-250">Cor da borda de cada imagem de textura</span><span class="sxs-lookup"><span data-stu-id="7a4ec-250">Border color for each texture image</span></span>

<span data-ttu-id="7a4ec-251">Função minificação para cada imagem de textura</span><span class="sxs-lookup"><span data-stu-id="7a4ec-251">Minification function for each texture image</span></span>

<span data-ttu-id="7a4ec-252">Função de ampliação para cada imagem de textura</span><span class="sxs-lookup"><span data-stu-id="7a4ec-252">Magnification function for each texture image</span></span>

<span data-ttu-id="7a4ec-253">Coordenadas de textura e modo de encapsulamento para cada imagem de textura</span><span class="sxs-lookup"><span data-stu-id="7a4ec-253">Texture coordinates and wrap mode for each texture image</span></span>

<span data-ttu-id="7a4ec-254">Cor e modo para cada ambiente de textura</span><span class="sxs-lookup"><span data-stu-id="7a4ec-254">Color and mode for each texture environment</span></span>

<span data-ttu-id="7a4ec-255">Habilitar o bits GL \_ Texture \_ Gen \_ *x*; *x* é S, T, R e Q</span><span class="sxs-lookup"><span data-stu-id="7a4ec-255">Enable bits GL\_TEXTURE\_GEN\_*x*; *x* is S, T, R, and Q</span></span>

<span data-ttu-id="7a4ec-256">\_ \_ \_ Configuração do modo do GL Texture Gen para S, T, R e Q</span><span class="sxs-lookup"><span data-stu-id="7a4ec-256">GL\_TEXTURE\_GEN\_MODE setting for S, T, R, and Q</span></span>

<span data-ttu-id="7a4ec-257">equações do plano glTexGen para S, T, R e Q</span><span class="sxs-lookup"><span data-stu-id="7a4ec-257">glTexGen plane equations for S, T, R, and Q</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit de transformação GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL\_TRANSFORM\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-259">Coeficientes dos seis planos de recorte</span><span class="sxs-lookup"><span data-stu-id="7a4ec-259">Coefficients of the six clipping planes</span></span>

<span data-ttu-id="7a4ec-260">Habilitar bits para os planos de recorte definíveis pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7a4ec-260">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="7a4ec-261">Valor do modo de \_ matriz GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-261">GL\_MATRIX\_MODE value</span></span>

<span data-ttu-id="7a4ec-262">\_Sinalizador de NORMALIZE GL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-262">GL\_NORMALIZE flag</span></span>

</dd> <dt>

<span data-ttu-id="7a4ec-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit GL viewport \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL\_VIEWPORT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="7a4ec-264">Intervalo de profundidade (próximo e longe)</span><span class="sxs-lookup"><span data-stu-id="7a4ec-264">Depth range (near and far)</span></span>

<span data-ttu-id="7a4ec-265">Origem e extensão do visor</span><span class="sxs-lookup"><span data-stu-id="7a4ec-265">Viewport origin and extent</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a4ec-266">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a4ec-266">Return value</span></span>

<span data-ttu-id="7a4ec-267">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-267">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a4ec-268">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7a4ec-268">Error codes</span></span>

<span data-ttu-id="7a4ec-269">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7a4ec-269">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7a4ec-270">Nome</span><span class="sxs-lookup"><span data-stu-id="7a4ec-270">Name</span></span>                                                                                                  | <span data-ttu-id="7a4ec-271">Significado</span><span class="sxs-lookup"><span data-stu-id="7a4ec-271">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a4ec-272"><dt>**\_estouro de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7a4ec-272"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="7a4ec-273">A função foi chamada enquanto a pilha de atributos estava cheia.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-273">The function was called while the attribute stack was full.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7a4ec-274"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7a4ec-274"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7a4ec-275">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ec-275">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7a4ec-276">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a4ec-276">Remarks</span></span>

<span data-ttu-id="7a4ec-277">A função **glPushAttrib** usa um argumento, uma máscara que indica quais grupos de variáveis de estado salvar na pilha de atributos.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-277">The **glPushAttrib** function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="7a4ec-278">As constantes simbólicas são usadas para definir os bits na máscara.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-278">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="7a4ec-279">O parâmetro Mask normalmente é construído aplicando-se a operação **or** lógica a várias dessas constantes.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-279">The mask parameter is typically constructed by applying the logical **OR** operation to several of these constants.</span></span> <span data-ttu-id="7a4ec-280">Você pode usar a máscara especial GL \_ todos \_ os \_ bits de Atrib para salvar todos os Estados empilháveis.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-280">You can use the special mask GL\_ALL\_ATTRIB\_BITS to save all stackable states.</span></span>

<span data-ttu-id="7a4ec-281">A função [**glPopAttrib**](glpopattrib.md) restaura os valores das variáveis de estado salvas com o último comando **glPushAttrib** .</span><span class="sxs-lookup"><span data-stu-id="7a4ec-281">The [**glPopAttrib**](glpopattrib.md) function restores the values of the state variables saved with the last **glPushAttrib** command.</span></span> <span data-ttu-id="7a4ec-282">Aqueles não salvos são deixados inalterados.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-282">Those not saved are left unchanged.</span></span>

<span data-ttu-id="7a4ec-283">É um erro enviar atributos por push para uma pilha completa ou para os atributos pop de uma pilha vazia.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-283">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="7a4ec-284">Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-284">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="7a4ec-285">Inicialmente, a pilha de atributos está vazia.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-285">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="7a4ec-286">Nem todos os valores para o estado OpenGL podem ser salvos na pilha de atributos.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-286">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="7a4ec-287">Por exemplo, você não pode salvar o pacote de pixel e o estado de desempacotamento, estado do modo de renderização e estado de seleção e comentários.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-287">For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.</span></span>

<span data-ttu-id="7a4ec-288">A profundidade da pilha de atributos depende da implementação, mas deve ser pelo menos 16.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-288">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="7a4ec-289">As funções a seguir recuperam informações relacionadas a **glPushAttrib** e [**glPopAttrib**](glpopattrib.md):</span><span class="sxs-lookup"><span data-stu-id="7a4ec-289">The following functions retrieve information related to **glPushAttrib** and [**glPopAttrib**](glpopattrib.md):</span></span>

<span data-ttu-id="7a4ec-290">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) profundidade de pilha de Atrib glGet com Argument GL \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="7a4ec-291">[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ profundidade máxima de pilha de \_ ATRIB \_ glGet com Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="7a4ec-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="7a4ec-292">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a4ec-292">Requirements</span></span>



| <span data-ttu-id="7a4ec-293">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a4ec-293">Requirement</span></span> | <span data-ttu-id="7a4ec-294">Valor</span><span class="sxs-lookup"><span data-stu-id="7a4ec-294">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4ec-295">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a4ec-295">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4ec-296">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7a4ec-296">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7a4ec-297">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a4ec-297">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4ec-298">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7a4ec-298">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a4ec-299">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7a4ec-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a4ec-300"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a4ec-300"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7a4ec-301">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a4ec-301">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a4ec-302"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a4ec-302"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a4ec-303">DLL</span><span class="sxs-lookup"><span data-stu-id="7a4ec-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a4ec-304"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a4ec-304"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a4ec-305">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a4ec-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a4ec-306">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-306">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-307">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-307">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-308">**glGet**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-308">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-309">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-309">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-310">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-310">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-311">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-311">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-312">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-312">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-313">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-313">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-314">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-314">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-315">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-315">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-316">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-316">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-317">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-317">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-318">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-318">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-319">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-319">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-320">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-320">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-321">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-321">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="7a4ec-322">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-322">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





