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
ms.openlocfilehash: ff468c701100cc598a519ed3aa290913016a559e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908644"
---
# <a name="texturing-state-variables"></a><span data-ttu-id="4237d-104">Variáveis de estado texturing</span><span class="sxs-lookup"><span data-stu-id="4237d-104">Texturing State Variables</span></span>

<dl> <span data-ttu-id="4237d-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Textura GL \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-105"><dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL\_TEXTURE\_*x*</dt> </span></span><dd> 

| <span data-ttu-id="4237d-106">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-106">Property</span></span> | <span data-ttu-id="4237d-107">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-107">Value</span></span> |
|------------------|-------------------------------------------------------|
| <span data-ttu-id="4237d-108">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-108">Description:</span></span>     | <span data-ttu-id="4237d-109">True se *x* -d texturing habilitado (*x* for 1-D ou 2-d)</span><span class="sxs-lookup"><span data-stu-id="4237d-109">True if *x* - D texturing enabled (*x* is 1-D or 2-D)</span></span> |
| <span data-ttu-id="4237d-110">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-110">Attribute group:</span></span> | <span data-ttu-id="4237d-111">textura/Habilitar</span><span class="sxs-lookup"><span data-stu-id="4237d-111">texture/enable</span></span>                                        |
| <span data-ttu-id="4237d-112">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-112">Initial value:</span></span>   | <span data-ttu-id="4237d-113">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="4237d-113">GL\_FALSE</span></span>                                             |
| <span data-ttu-id="4237d-114">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-114">Get command:</span></span>     | [<span data-ttu-id="4237d-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4237d-115">**glIsEnabled**</span></span>](glisenabled.md)                    |



 

<span data-ttu-id="4237d-116"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_textura GL</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-116"></dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>GL\_TEXTURE</dt> </span></span><dd> 

| <span data-ttu-id="4237d-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-117">Property</span></span> | <span data-ttu-id="4237d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-118">Value</span></span> |
|------------------|----------------------------------------------|
| <span data-ttu-id="4237d-119">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-119">Description:</span></span>     | <span data-ttu-id="4237d-120">imagem de textura *x* -D no nível de detalhe *i*</span><span class="sxs-lookup"><span data-stu-id="4237d-120">*x* - D texture image at level of detail *i*</span></span> |
| <span data-ttu-id="4237d-121">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-121">Attribute group:</span></span> |                                              |
| <span data-ttu-id="4237d-122">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-122">Initial value:</span></span>   |                                              |
| <span data-ttu-id="4237d-123">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-123">Get command:</span></span>     | [<span data-ttu-id="4237d-124">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="4237d-124">**glGetTexImage**</span></span>](glgetteximage.md)       |



 

<span data-ttu-id="4237d-125"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_largura da textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-125"></dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>GL\_TEXTURE\_WIDTH</dt> </span></span><dd> 

| <span data-ttu-id="4237d-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-126">Property</span></span> | <span data-ttu-id="4237d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-127">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="4237d-128">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-128">Description:</span></span>     | <span data-ttu-id="4237d-129">largura *da imagem* de textura *x* -D</span><span class="sxs-lookup"><span data-stu-id="4237d-129">*x* - D texture image *i* 's width</span></span>                       |
| <span data-ttu-id="4237d-130">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-130">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="4237d-131">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-131">Initial value:</span></span>   | <span data-ttu-id="4237d-132">0</span><span class="sxs-lookup"><span data-stu-id="4237d-132">0</span></span>                                                        |
| <span data-ttu-id="4237d-133">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-133">Get command:</span></span>     | [<span data-ttu-id="4237d-134">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-134">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="4237d-135"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_altura da textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-135"></dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>GL\_TEXTURE\_HEIGHT</dt> </span></span><dd> 

| <span data-ttu-id="4237d-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-136">Property</span></span> | <span data-ttu-id="4237d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-137">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="4237d-138">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-138">Description:</span></span>     | <span data-ttu-id="4237d-139">altura *da imagem* de textura *x* -D</span><span class="sxs-lookup"><span data-stu-id="4237d-139">*x* - D texture image *i* 's height</span></span>                      |
| <span data-ttu-id="4237d-140">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-140">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="4237d-141">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-141">Initial value:</span></span>   | <span data-ttu-id="4237d-142">0</span><span class="sxs-lookup"><span data-stu-id="4237d-142">0</span></span>                                                        |
| <span data-ttu-id="4237d-143">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-143">Get command:</span></span>     | [<span data-ttu-id="4237d-144">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-144">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="4237d-145"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_borda de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-145"></dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>GL\_TEXTURE\_BORDER</dt> </span></span><dd> 

| <span data-ttu-id="4237d-146">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-146">Property</span></span> | <span data-ttu-id="4237d-147">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-147">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="4237d-148">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-148">Description:</span></span>     | <span data-ttu-id="4237d-149">borda *da imagem* de textura *x* -D</span><span class="sxs-lookup"><span data-stu-id="4237d-149">*x* - D texture image *i* 's border</span></span>                      |
| <span data-ttu-id="4237d-150">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-150">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="4237d-151">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-151">Initial value:</span></span>   | <span data-ttu-id="4237d-152">0</span><span class="sxs-lookup"><span data-stu-id="4237d-152">0</span></span>                                                        |
| <span data-ttu-id="4237d-153">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-153">Get command:</span></span>     | [<span data-ttu-id="4237d-154">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-154">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="4237d-155"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_componentes de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-155"></dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>GL\_TEXTURE\_COMPONENTS</dt> </span></span><dd> 

| <span data-ttu-id="4237d-156">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-156">Property</span></span> | <span data-ttu-id="4237d-157">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-157">Value</span></span> |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="4237d-158">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-158">Description:</span></span>     | <span data-ttu-id="4237d-159">Componentes de imagem de textura</span><span class="sxs-lookup"><span data-stu-id="4237d-159">Texture image components</span></span>                                 |
| <span data-ttu-id="4237d-160">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-160">Attribute group:</span></span> |                                                          |
| <span data-ttu-id="4237d-161">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-161">Initial value:</span></span>   | <span data-ttu-id="4237d-162">1</span><span class="sxs-lookup"><span data-stu-id="4237d-162">1</span></span>                                                        |
| <span data-ttu-id="4237d-163">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-163">Get command:</span></span>     | [<span data-ttu-id="4237d-164">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-164">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md) |



 

<span data-ttu-id="4237d-165"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_cor da \_ borda da textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-165"></dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>GL\_TEXTURE\_BORDER\_COLOR</dt> </span></span><dd> 

| <span data-ttu-id="4237d-166">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-166">Property</span></span> | <span data-ttu-id="4237d-167">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-167">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="4237d-168">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-168">Description:</span></span>     | <span data-ttu-id="4237d-169">Cor da borda da textura</span><span class="sxs-lookup"><span data-stu-id="4237d-169">Texture border color</span></span>                           |
| <span data-ttu-id="4237d-170">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-170">Attribute group:</span></span> | <span data-ttu-id="4237d-171">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-171">texture</span></span>                                        |
| <span data-ttu-id="4237d-172">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-172">Initial value:</span></span>   | <span data-ttu-id="4237d-173">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="4237d-173">0, 0, 0, 0</span></span>                                     |
| <span data-ttu-id="4237d-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-174">Get command:</span></span>     | [<span data-ttu-id="4237d-175">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-175">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="4237d-176"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_filtro de \_ mínimo de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-176"></dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>GL\_TEXTURE\_MIN\_FILTER</dt> </span></span><dd> 

| <span data-ttu-id="4237d-177">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-177">Property</span></span> | <span data-ttu-id="4237d-178">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-178">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="4237d-179">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-179">Description:</span></span>     | <span data-ttu-id="4237d-180">Função de minificação de textura</span><span class="sxs-lookup"><span data-stu-id="4237d-180">Texture minification function</span></span>                  |
| <span data-ttu-id="4237d-181">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-181">Attribute group:</span></span> | <span data-ttu-id="4237d-182">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-182">texture</span></span>                                        |
| <span data-ttu-id="4237d-183">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-183">Initial value:</span></span>   | <span data-ttu-id="4237d-184">GL \_ mais próximo \_ MIPMAP \_ linear</span><span class="sxs-lookup"><span data-stu-id="4237d-184">GL\_NEAREST\_MIPMAP\_LINEAR</span></span>                    |
| <span data-ttu-id="4237d-185">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-185">Get command:</span></span>     | [<span data-ttu-id="4237d-186">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-186">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="4237d-187"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_ \_ filtro mag de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-187"></dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>GL\_TEXTURE\_MAG\_FILTER</dt> </span></span><dd> 

| <span data-ttu-id="4237d-188">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-188">Property</span></span> | <span data-ttu-id="4237d-189">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-189">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="4237d-190">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-190">Description:</span></span>     | <span data-ttu-id="4237d-191">Função de ampliação de textura</span><span class="sxs-lookup"><span data-stu-id="4237d-191">Texture magnification function</span></span>                 |
| <span data-ttu-id="4237d-192">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-192">Attribute group:</span></span> | <span data-ttu-id="4237d-193">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-193">texture</span></span>                                        |
| <span data-ttu-id="4237d-194">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-194">Initial value:</span></span>   | <span data-ttu-id="4237d-195">GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="4237d-195">GL\_LINEAR</span></span>                                     |
| <span data-ttu-id="4237d-196">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-196">Get command:</span></span>     | [<span data-ttu-id="4237d-197">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-197">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="4237d-198"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>Encapsule a textura do GL \_ \_ \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-198"></dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL\_TEXTURE\_WRAP\_ *x*</dt> </span></span><dd> 

| <span data-ttu-id="4237d-199">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-199">Property</span></span> | <span data-ttu-id="4237d-200">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-200">Value</span></span> |
|------------------|------------------------------------------------|
| <span data-ttu-id="4237d-201">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-201">Description:</span></span>     | <span data-ttu-id="4237d-202">Modo de quebra de textura (*x* é S ou T)</span><span class="sxs-lookup"><span data-stu-id="4237d-202">Texture wrap mode (*x* is S or T)</span></span>              |
| <span data-ttu-id="4237d-203">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-203">Attribute group:</span></span> | <span data-ttu-id="4237d-204">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-204">texture</span></span>                                        |
| <span data-ttu-id="4237d-205">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-205">Initial value:</span></span>   | <span data-ttu-id="4237d-206">GL \_ repetir</span><span class="sxs-lookup"><span data-stu-id="4237d-206">GL\_REPEAT</span></span>                                     |
| <span data-ttu-id="4237d-207">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-207">Get command:</span></span>     | [<span data-ttu-id="4237d-208">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="4237d-208">**glGetTexParameter**</span></span>](glgettexparameter.md) |



 

<span data-ttu-id="4237d-209"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>modo do GL \_ Texture \_ env \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-209"></dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>GL\_TEXTURE\_ENV\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="4237d-210">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-210">Property</span></span> | <span data-ttu-id="4237d-211">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-211">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="4237d-212">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-212">Description:</span></span>     | <span data-ttu-id="4237d-213">Função de aplicativo de textura</span><span class="sxs-lookup"><span data-stu-id="4237d-213">Texture application function</span></span>         |
| <span data-ttu-id="4237d-214">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-214">Attribute group:</span></span> | <span data-ttu-id="4237d-215">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-215">texture</span></span>                              |
| <span data-ttu-id="4237d-216">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-216">Initial value:</span></span>   | <span data-ttu-id="4237d-217">GL \_ modular</span><span class="sxs-lookup"><span data-stu-id="4237d-217">GL\_MODULATE</span></span>                         |
| <span data-ttu-id="4237d-218">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-218">Get command:</span></span>     | [<span data-ttu-id="4237d-219">**glGetTexEnviv**</span><span class="sxs-lookup"><span data-stu-id="4237d-219">**glGetTexEnviv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="4237d-220"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>cor do GL \_ Texture \_ env \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-220"></dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>GL\_TEXTURE\_ENV\_COLOR</dt> </span></span><dd> 

| <span data-ttu-id="4237d-221">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-221">Property</span></span> | <span data-ttu-id="4237d-222">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-222">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="4237d-223">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-223">Description:</span></span>     | <span data-ttu-id="4237d-224">Cor do ambiente de textura</span><span class="sxs-lookup"><span data-stu-id="4237d-224">Texture environment color</span></span>            |
| <span data-ttu-id="4237d-225">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-225">Attribute group:</span></span> | <span data-ttu-id="4237d-226">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-226">texture</span></span>                              |
| <span data-ttu-id="4237d-227">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-227">Initial value:</span></span>   | <span data-ttu-id="4237d-228">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="4237d-228">0, 0, 0, 0</span></span>                           |
| <span data-ttu-id="4237d-229">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-229">Get command:</span></span>     | [<span data-ttu-id="4237d-230">**glGetTexEnvfv**</span><span class="sxs-lookup"><span data-stu-id="4237d-230">**glGetTexEnvfv**</span></span>](glgettexenv.md) |



 

<span data-ttu-id="4237d-231"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>A \_ textura GL \_ Gen \_ *x*</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-231"></dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL\_TEXTURE\_GEN\_ *x*</dt> </span></span><dd> 

| <span data-ttu-id="4237d-232">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-232">Property</span></span> | <span data-ttu-id="4237d-233">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-233">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="4237d-234">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-234">Description:</span></span>     | <span data-ttu-id="4237d-235">Texgen está habilitado (*x* é S, T, R ou Q)</span><span class="sxs-lookup"><span data-stu-id="4237d-235">Texgen is enabled (*x* is S, T, R, or Q)</span></span> |
| <span data-ttu-id="4237d-236">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-236">Attribute group:</span></span> | <span data-ttu-id="4237d-237">textura/Habilitar</span><span class="sxs-lookup"><span data-stu-id="4237d-237">texture/enable</span></span>                           |
| <span data-ttu-id="4237d-238">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-238">Initial value:</span></span>   | <span data-ttu-id="4237d-239">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="4237d-239">GL\_FALSE</span></span>                                |
| <span data-ttu-id="4237d-240">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-240">Get command:</span></span>     | [<span data-ttu-id="4237d-241">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4237d-241">**glIsEnabled**</span></span>](glisenabled.md)       |



 

<span data-ttu-id="4237d-242"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_plano de olho GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-242"></dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL\_EYE\_PLANE</dt> </span></span><dd> 

| <span data-ttu-id="4237d-243">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-243">Property</span></span> | <span data-ttu-id="4237d-244">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-244">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="4237d-245">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-245">Description:</span></span>     | <span data-ttu-id="4237d-246">Coeficientes da equação do plano Texgen</span><span class="sxs-lookup"><span data-stu-id="4237d-246">Texgen plane equation coefficients</span></span>   |
| <span data-ttu-id="4237d-247">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-247">Attribute group:</span></span> | <span data-ttu-id="4237d-248">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-248">texture</span></span>                              |
| <span data-ttu-id="4237d-249">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-249">Initial value:</span></span>   |                                      |
| <span data-ttu-id="4237d-250">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-250">Get command:</span></span>     | [<span data-ttu-id="4237d-251">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="4237d-251">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="4237d-252"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_plano de objeto GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-252"></dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>GL\_OBJECT\_PLANE</dt> </span></span><dd> 

| <span data-ttu-id="4237d-253">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-253">Property</span></span> | <span data-ttu-id="4237d-254">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-254">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="4237d-255">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-255">Description:</span></span>     | <span data-ttu-id="4237d-256">Coeficientes lineares de objeto Texgen</span><span class="sxs-lookup"><span data-stu-id="4237d-256">Texgen object linear coefficients</span></span>    |
| <span data-ttu-id="4237d-257">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-257">Attribute group:</span></span> | <span data-ttu-id="4237d-258">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-258">texture</span></span>                              |
| <span data-ttu-id="4237d-259">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-259">Initial value:</span></span>   |                                      |
| <span data-ttu-id="4237d-260">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-260">Get command:</span></span>     | [<span data-ttu-id="4237d-261">**glGetTexGenfv**</span><span class="sxs-lookup"><span data-stu-id="4237d-261">**glGetTexGenfv**</span></span>](glgettexgen.md) |



 

<span data-ttu-id="4237d-262"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>modo do GL \_ Texture \_ Gen \_</dt> </span><span class="sxs-lookup"><span data-stu-id="4237d-262"></dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>GL\_TEXTURE\_GEN\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="4237d-263">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4237d-263">Property</span></span> | <span data-ttu-id="4237d-264">Valor</span><span class="sxs-lookup"><span data-stu-id="4237d-264">Value</span></span> |
|------------------|--------------------------------------|
| <span data-ttu-id="4237d-265">Descrição:</span><span class="sxs-lookup"><span data-stu-id="4237d-265">Description:</span></span>     | <span data-ttu-id="4237d-266">Função usada para texgen</span><span class="sxs-lookup"><span data-stu-id="4237d-266">Function used for texgen</span></span>             |
| <span data-ttu-id="4237d-267">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="4237d-267">Attribute group:</span></span> | <span data-ttu-id="4237d-268">textura</span><span class="sxs-lookup"><span data-stu-id="4237d-268">texture</span></span>                              |
| <span data-ttu-id="4237d-269">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="4237d-269">Initial value:</span></span>   | <span data-ttu-id="4237d-270">olho do GL \_ \_ linear</span><span class="sxs-lookup"><span data-stu-id="4237d-270">GL\_EYE\_LINEAR</span></span>                      |
| <span data-ttu-id="4237d-271">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="4237d-271">Get command:</span></span>     | [<span data-ttu-id="4237d-272">**glGetTexGeniv**</span><span class="sxs-lookup"><span data-stu-id="4237d-272">**glGetTexGeniv**</span></span>](glgettexgen.md) |



 

</dd> </dl>

 

 




