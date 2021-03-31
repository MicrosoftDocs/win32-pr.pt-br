---
title: Variáveis de estado de transformação
description: Variáveis de estado de transformação
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variáveis de estado de transformação OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293258"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="5fb8a-104">Variáveis de estado de transformação</span><span class="sxs-lookup"><span data-stu-id="5fb8a-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="5fb8a-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_MODELVIEW \_ matriz GL</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5fb8a-106">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-106">Description:</span></span>     | <span data-ttu-id="5fb8a-107">Pilha de matriz Modelview</span><span class="sxs-lookup"><span data-stu-id="5fb8a-107">Modelview matrix stack</span></span>             |
| <span data-ttu-id="5fb8a-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-108">Attribute group:</span></span> |                                    |
| <span data-ttu-id="5fb8a-109">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-109">Initial value:</span></span>   | <span data-ttu-id="5fb8a-110">Identidade</span><span class="sxs-lookup"><span data-stu-id="5fb8a-110">Identity</span></span>                           |
| <span data-ttu-id="5fb8a-111">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-111">Get command:</span></span>     | [<span data-ttu-id="5fb8a-112">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-112">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="5fb8a-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matriz de projeção GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-113"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-114">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-114">Description:</span></span>     | <span data-ttu-id="5fb8a-115">Pilha de matriz de projeção</span><span class="sxs-lookup"><span data-stu-id="5fb8a-115">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="5fb8a-116">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-116">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="5fb8a-117">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-117">Initial value:</span></span>   | <span data-ttu-id="5fb8a-118">Identidade</span><span class="sxs-lookup"><span data-stu-id="5fb8a-118">Identity</span></span>                                                                       |
| <span data-ttu-id="5fb8a-119">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-119">Get command:</span></span>     | [<span data-ttu-id="5fb8a-120">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-120">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matriz de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-121"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-122">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-122">Description:</span></span>     | <span data-ttu-id="5fb8a-123">Pilha de matriz de textura</span><span class="sxs-lookup"><span data-stu-id="5fb8a-123">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="5fb8a-124">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-124">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="5fb8a-125">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-125">Initial value:</span></span>   | <span data-ttu-id="5fb8a-126">Identidade</span><span class="sxs-lookup"><span data-stu-id="5fb8a-126">Identity</span></span>                                                                       |
| <span data-ttu-id="5fb8a-127">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-127">Get command:</span></span>     | [<span data-ttu-id="5fb8a-128">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-128">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_visor GL</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-129"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-130">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-130">Description:</span></span>     | <span data-ttu-id="5fb8a-131">Origem e extensão do visor</span><span class="sxs-lookup"><span data-stu-id="5fb8a-131">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="5fb8a-132">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-132">Attribute group:</span></span> | <span data-ttu-id="5fb8a-133">visor</span><span class="sxs-lookup"><span data-stu-id="5fb8a-133">viewport</span></span>                                                                         |
| <span data-ttu-id="5fb8a-134">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-134">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="5fb8a-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-135">Get command:</span></span>     | [<span data-ttu-id="5fb8a-136">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-136">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_intervalo de profundidade do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-137"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-138">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-138">Description:</span></span>     | <span data-ttu-id="5fb8a-139">Intervalo de profundidade próximo e longe</span><span class="sxs-lookup"><span data-stu-id="5fb8a-139">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="5fb8a-140">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-140">Attribute group:</span></span> | <span data-ttu-id="5fb8a-141">visor</span><span class="sxs-lookup"><span data-stu-id="5fb8a-141">viewport</span></span>                                                                       |
| <span data-ttu-id="5fb8a-142">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-142">Initial value:</span></span>   | <span data-ttu-id="5fb8a-143">0, 1</span><span class="sxs-lookup"><span data-stu-id="5fb8a-143">0, 1</span></span>                                                                           |
| <span data-ttu-id="5fb8a-144">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-144">Get command:</span></span>     | [<span data-ttu-id="5fb8a-145">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-145">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_profundidade de \_ pilha \_ MODELVIEW GL</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-146"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-147">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-147">Description:</span></span>     | <span data-ttu-id="5fb8a-148">Ponteiro de pilha de matriz Modelview</span><span class="sxs-lookup"><span data-stu-id="5fb8a-148">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="5fb8a-149">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-149">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5fb8a-150">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-150">Initial value:</span></span>   | <span data-ttu-id="5fb8a-151">1</span><span class="sxs-lookup"><span data-stu-id="5fb8a-151">1</span></span>                                                                                |
| <span data-ttu-id="5fb8a-152">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-152">Get command:</span></span>     | [<span data-ttu-id="5fb8a-153">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-153">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_profundidade da pilha de projeção GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-154"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-155">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-155">Description:</span></span>     | <span data-ttu-id="5fb8a-156">Ponteiro da pilha da matriz de projeção</span><span class="sxs-lookup"><span data-stu-id="5fb8a-156">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="5fb8a-157">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-157">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5fb8a-158">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-158">Initial value:</span></span>   | <span data-ttu-id="5fb8a-159">1</span><span class="sxs-lookup"><span data-stu-id="5fb8a-159">1</span></span>                                                                                |
| <span data-ttu-id="5fb8a-160">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-160">Get command:</span></span>     | [<span data-ttu-id="5fb8a-161">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-161">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>\_profundidade da \_ pilha de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-162"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-163">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-163">Description:</span></span>     | <span data-ttu-id="5fb8a-164">Ponteiro de pilha da matriz de textura</span><span class="sxs-lookup"><span data-stu-id="5fb8a-164">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="5fb8a-165">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-165">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="5fb8a-166">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-166">Initial value:</span></span>   | <span data-ttu-id="5fb8a-167">1</span><span class="sxs-lookup"><span data-stu-id="5fb8a-167">1</span></span>                                                                                |
| <span data-ttu-id="5fb8a-168">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-168">Get command:</span></span>     | [<span data-ttu-id="5fb8a-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_modo de matriz GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-170"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5fb8a-171">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-171">Description:</span></span>     | <span data-ttu-id="5fb8a-172">Modo de matriz atual</span><span class="sxs-lookup"><span data-stu-id="5fb8a-172">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="5fb8a-173">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-173">Attribute group:</span></span> | <span data-ttu-id="5fb8a-174">transformação</span><span class="sxs-lookup"><span data-stu-id="5fb8a-174">transform</span></span>                                                                        |
| <span data-ttu-id="5fb8a-175">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-175">Initial value:</span></span>   | <span data-ttu-id="5fb8a-176">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="5fb8a-176">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="5fb8a-177">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-177">Get command:</span></span>     | [<span data-ttu-id="5fb8a-178">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-178">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="5fb8a-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>\_NORMALIZE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-179"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

|                  |                                     |
|------------------|-------------------------------------|
| <span data-ttu-id="5fb8a-180">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-180">Description:</span></span>     | <span data-ttu-id="5fb8a-181">Ativar/desativar normalização normal atual</span><span class="sxs-lookup"><span data-stu-id="5fb8a-181">Current normal normalization on/off</span></span> |
| <span data-ttu-id="5fb8a-182">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-182">Attribute group:</span></span> | <span data-ttu-id="5fb8a-183">transformar/habilitar</span><span class="sxs-lookup"><span data-stu-id="5fb8a-183">transform/enable</span></span>                    |
| <span data-ttu-id="5fb8a-184">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-184">Initial value:</span></span>   | <span data-ttu-id="5fb8a-185">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="5fb8a-185">GL\_FALSE</span></span>                           |
| <span data-ttu-id="5fb8a-186">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-186">Get command:</span></span>     | [<span data-ttu-id="5fb8a-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-187">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="5fb8a-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>Recorte de \_ \_ plano GL *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-188"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="5fb8a-189">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-189">Description:</span></span>     | <span data-ttu-id="5fb8a-190">Coeficientes de plano de recorte do usuário</span><span class="sxs-lookup"><span data-stu-id="5fb8a-190">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="5fb8a-191">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-191">Attribute group:</span></span> | <span data-ttu-id="5fb8a-192">transformação</span><span class="sxs-lookup"><span data-stu-id="5fb8a-192">transform</span></span>                                |
| <span data-ttu-id="5fb8a-193">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-193">Initial value:</span></span>   | <span data-ttu-id="5fb8a-194">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="5fb8a-194">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="5fb8a-195">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-195">Get command:</span></span>     | [<span data-ttu-id="5fb8a-196">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-196">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="5fb8a-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>Recorte de \_ \_ plano GL *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="5fb8a-197"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="5fb8a-198">Descrição:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-198">Description:</span></span>     | <span data-ttu-id="5fb8a-199"> plano de recorte de usuário habilitado</span><span class="sxs-lookup"><span data-stu-id="5fb8a-199">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="5fb8a-200">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-200">Attribute group:</span></span> | <span data-ttu-id="5fb8a-201">transformar/habilitar</span><span class="sxs-lookup"><span data-stu-id="5fb8a-201">transform/enable</span></span>                   |
| <span data-ttu-id="5fb8a-202">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-202">Initial value:</span></span>   | <span data-ttu-id="5fb8a-203">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="5fb8a-203">GL\_FALSE</span></span>                          |
| <span data-ttu-id="5fb8a-204">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="5fb8a-204">Get command:</span></span>     | [<span data-ttu-id="5fb8a-205">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5fb8a-205">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




