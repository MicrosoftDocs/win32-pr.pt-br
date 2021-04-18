---
title: Variáveis de estado texturing
description: Variáveis de estado texturing
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variáveis de estado texturing OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105751088"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="c3148-104">Variáveis de estado texturing</span><span class="sxs-lookup"><span data-stu-id="c3148-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="c3148-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Textura GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="c3148-106">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-106">Description:</span></span>     | <span data-ttu-id="c3148-107">True se *x*   -d texturing habilitado (*x* for 1-d ou 2-d)</span><span class="sxs-lookup"><span data-stu-id="c3148-107">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="c3148-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-108">Attribute group:</span></span> | <span data-ttu-id="c3148-109">textura/Habilitar</span><span class="sxs-lookup"><span data-stu-id="c3148-109">texture/enable</span></span>                                        |
| <span data-ttu-id="c3148-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-110">Initial value:</span></span>   | <span data-ttu-id="c3148-111">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="c3148-111">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="c3148-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-112">Get command:</span></span>     | [<span data-ttu-id="c3148-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="c3148-113">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="c3148-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_textura GL</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-114"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| <span data-ttu-id="c3148-115">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-115">Description:</span></span>     | <span data-ttu-id="c3148-116">*x*   -D imagem de textura no nível de detalhe *i*</span><span class="sxs-lookup"><span data-stu-id="c3148-116">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="c3148-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-117">Attribute group:</span></span> |                                              |
| <span data-ttu-id="c3148-118">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-118">Initial value:</span></span>   |                                              |
| <span data-ttu-id="c3148-119">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-119">Get command:</span></span>     | [<span data-ttu-id="c3148-120">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="c3148-120">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="c3148-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_largura da textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-121"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="c3148-122">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-122">Description:</span></span>     | <span data-ttu-id="c3148-123">*x*   -D largura da imagem de textura *i*  </span><span class="sxs-lookup"><span data-stu-id="c3148-123">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="c3148-124">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-124">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="c3148-125">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-125">Initial value:</span></span>   | <span data-ttu-id="c3148-126">0</span><span class="sxs-lookup"><span data-stu-id="c3148-126">0</span></span>                                                        |
| <span data-ttu-id="c3148-127">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-127">Get command:</span></span>     | [<span data-ttu-id="c3148-128">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-128">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="c3148-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_altura da textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-129"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="c3148-130">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-130">Description:</span></span>     | <span data-ttu-id="c3148-131">*x*   -D altura da imagem de textura *i*  </span><span class="sxs-lookup"><span data-stu-id="c3148-131">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="c3148-132">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-132">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="c3148-133">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-133">Initial value:</span></span>   | <span data-ttu-id="c3148-134">0</span><span class="sxs-lookup"><span data-stu-id="c3148-134">0</span></span>                                                        |
| <span data-ttu-id="c3148-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-135">Get command:</span></span>     | [<span data-ttu-id="c3148-136">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-136">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="c3148-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_borda de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-137"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="c3148-138">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-138">Description:</span></span>     | <span data-ttu-id="c3148-139">*x*   -D borda da imagem de textura *i*  </span><span class="sxs-lookup"><span data-stu-id="c3148-139">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="c3148-140">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="c3148-141">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-141">Initial value:</span></span>   | <span data-ttu-id="c3148-142">0</span><span class="sxs-lookup"><span data-stu-id="c3148-142">0</span></span>                                                        |
| <span data-ttu-id="c3148-143">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-143">Get command:</span></span>     | [<span data-ttu-id="c3148-144">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="c3148-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_componentes de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-145"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="c3148-146">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-146">Description:</span></span>     | <span data-ttu-id="c3148-147">Componentes de imagem de textura</span><span class="sxs-lookup"><span data-stu-id="c3148-147">Texture image components</span></span>                                 |
| <span data-ttu-id="c3148-148">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-148">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="c3148-149">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-149">Initial value:</span></span>   | <span data-ttu-id="c3148-150">1</span><span class="sxs-lookup"><span data-stu-id="c3148-150">1</span></span>                                                        |
| <span data-ttu-id="c3148-151">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-151">Get command:</span></span>     | [<span data-ttu-id="c3148-152">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-152">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="c3148-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_cor da \_ borda da textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-153"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="c3148-154">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-154">Description:</span></span>     | <span data-ttu-id="c3148-155">Cor da borda da textura</span><span class="sxs-lookup"><span data-stu-id="c3148-155">Texture border color</span></span>                           |
| <span data-ttu-id="c3148-156">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-156">Attribute group:</span></span> | <span data-ttu-id="c3148-157">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-157">texture</span></span>                                        |
| <span data-ttu-id="c3148-158">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-158">Initial value:</span></span>   | <span data-ttu-id="c3148-159">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="c3148-159">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="c3148-160">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-160">Get command:</span></span>     | [<span data-ttu-id="c3148-161">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-161">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="c3148-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_filtro de \_ mínimo de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-162"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="c3148-163">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-163">Description:</span></span>     | <span data-ttu-id="c3148-164">Função de minificação de textura</span><span class="sxs-lookup"><span data-stu-id="c3148-164">Texture minification function</span></span>                  |
| <span data-ttu-id="c3148-165">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-165">Attribute group:</span></span> | <span data-ttu-id="c3148-166">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-166">texture</span></span>                                        |
| <span data-ttu-id="c3148-167">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-167">Initial value:</span></span>   | <span data-ttu-id="c3148-168">GL \_ mais próximo \_ MIPMAP \_ linear</span><span class="sxs-lookup"><span data-stu-id="c3148-168">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="c3148-169">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-169">Get command:</span></span>     | [<span data-ttu-id="c3148-170">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-170">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="c3148-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_ \_ filtro mag de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-171"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="c3148-172">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-172">Description:</span></span>     | <span data-ttu-id="c3148-173">Função de ampliação de textura</span><span class="sxs-lookup"><span data-stu-id="c3148-173">Texture magnification function</span></span>                 |
| <span data-ttu-id="c3148-174">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-174">Attribute group:</span></span> | <span data-ttu-id="c3148-175">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-175">texture</span></span>                                        |
| <span data-ttu-id="c3148-176">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-176">Initial value:</span></span>   | <span data-ttu-id="c3148-177">GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="c3148-177">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="c3148-178">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-178">Get command:</span></span>     | [<span data-ttu-id="c3148-179">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-179">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="c3148-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>Encapsule a textura do GL \_ \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-180"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| <span data-ttu-id="c3148-181">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-181">Description:</span></span>     | <span data-ttu-id="c3148-182">Modo de quebra de textura (*x*   é S ou T)</span><span class="sxs-lookup"><span data-stu-id="c3148-182">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="c3148-183">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-183">Attribute group:</span></span> | <span data-ttu-id="c3148-184">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-184">texture</span></span>                                        |
| <span data-ttu-id="c3148-185">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-185">Initial value:</span></span>   | <span data-ttu-id="c3148-186">GL \_ repetir</span><span class="sxs-lookup"><span data-stu-id="c3148-186">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="c3148-187">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-187">Get command:</span></span>     | [<span data-ttu-id="c3148-188">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="c3148-188">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="c3148-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>modo do GL \_ Texture \_ env \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-189"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="c3148-190">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-190">Description:</span></span>     | <span data-ttu-id="c3148-191">Função de aplicativo de textura</span><span class="sxs-lookup"><span data-stu-id="c3148-191">Texture application function</span></span>         |
| <span data-ttu-id="c3148-192">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-192">Attribute group:</span></span> | <span data-ttu-id="c3148-193">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-193">texture</span></span>                              |
| <span data-ttu-id="c3148-194">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-194">Initial value:</span></span>   | <span data-ttu-id="c3148-195">GL \_ modular</span><span class="sxs-lookup"><span data-stu-id="c3148-195">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="c3148-196">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-196">Get command:</span></span>     | [<span data-ttu-id="c3148-197">**glGetTexEnviv**</span><span class="sxs-lookup"><span data-stu-id="c3148-197">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="c3148-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>cor do GL \_ Texture \_ env \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-198"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="c3148-199">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-199">Description:</span></span>     | <span data-ttu-id="c3148-200">Cor do ambiente de textura</span><span class="sxs-lookup"><span data-stu-id="c3148-200">Texture environment color</span></span>            |
| <span data-ttu-id="c3148-201">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-201">Attribute group:</span></span> | <span data-ttu-id="c3148-202">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-202">texture</span></span>                              |
| <span data-ttu-id="c3148-203">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-203">Initial value:</span></span>   | <span data-ttu-id="c3148-204">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="c3148-204">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="c3148-205">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-205">Get command:</span></span>     | [<span data-ttu-id="c3148-206">**glGetTexEnvfv**</span><span class="sxs-lookup"><span data-stu-id="c3148-206">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="c3148-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>A \_ textura GL \_ Gen \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-207"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="c3148-208">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-208">Description:</span></span>     | <span data-ttu-id="c3148-209">Texgen está habilitado (*x*   é S, T, R ou Q)</span><span class="sxs-lookup"><span data-stu-id="c3148-209">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="c3148-210">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-210">Attribute group:</span></span> | <span data-ttu-id="c3148-211">textura/Habilitar</span><span class="sxs-lookup"><span data-stu-id="c3148-211">texture/enable</span></span>                           |
| <span data-ttu-id="c3148-212">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-212">Initial value:</span></span>   | <span data-ttu-id="c3148-213">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="c3148-213">GL\_FALSE</span></span>                                |
| <span data-ttu-id="c3148-214">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-214">Get command:</span></span>     | [<span data-ttu-id="c3148-215">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="c3148-215">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="c3148-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_plano de olho GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-216"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="c3148-217">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-217">Description:</span></span>     | <span data-ttu-id="c3148-218">Coeficientes da equação do plano Texgen</span><span class="sxs-lookup"><span data-stu-id="c3148-218">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="c3148-219">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-219">Attribute group:</span></span> | <span data-ttu-id="c3148-220">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-220">texture</span></span>                              |
| <span data-ttu-id="c3148-221">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-221">Initial value:</span></span>   |                                      |
| <span data-ttu-id="c3148-222">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-222">Get command:</span></span>     | [<span data-ttu-id="c3148-223">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="c3148-223">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="c3148-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_plano de objeto GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-224"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="c3148-225">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-225">Description:</span></span>     | <span data-ttu-id="c3148-226">Coeficientes lineares de objeto Texgen</span><span class="sxs-lookup"><span data-stu-id="c3148-226">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="c3148-227">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-227">Attribute group:</span></span> | <span data-ttu-id="c3148-228">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-228">texture</span></span>                              |
| <span data-ttu-id="c3148-229">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-229">Initial value:</span></span>   |                                      |
| <span data-ttu-id="c3148-230">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-230">Get command:</span></span>     | [<span data-ttu-id="c3148-231">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="c3148-231">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="c3148-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>modo do GL \_ Texture \_ Gen \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c3148-232"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

|                  |                                      |
|------------------|--------------------------------------|
| <span data-ttu-id="c3148-233">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c3148-233">Description:</span></span>     | <span data-ttu-id="c3148-234">Função usada para texgen</span><span class="sxs-lookup"><span data-stu-id="c3148-234">Function used for texgen</span></span>             |
| <span data-ttu-id="c3148-235">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c3148-235">Attribute group:</span></span> | <span data-ttu-id="c3148-236">textura</span><span class="sxs-lookup"><span data-stu-id="c3148-236">texture</span></span>                              |
| <span data-ttu-id="c3148-237">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c3148-237">Initial value:</span></span>   | <span data-ttu-id="c3148-238">olho do GL \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="c3148-238">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="c3148-239">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c3148-239">Get command:</span></span>     | [<span data-ttu-id="c3148-240">**glGetTexGeniv**</span><span class="sxs-lookup"><span data-stu-id="c3148-240">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




