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
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908824"
---
# <a name="transformation-state-variables"></a><span data-ttu-id="cfbb2-104">Variáveis de estado de transformação</span><span class="sxs-lookup"><span data-stu-id="cfbb2-104">Transformation State Variables</span></span>

<dl> <span data-ttu-id="cfbb2-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_MODELVIEW \_ matriz GL</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-105"><dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL\_MODELVIEW\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-106">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-106">Property</span></span> | <span data-ttu-id="cfbb2-107">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="cfbb2-108">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-108">Description:</span></span>     | <span data-ttu-id="cfbb2-109">Pilha de matriz Modelview</span><span class="sxs-lookup"><span data-stu-id="cfbb2-109">Modelview matrix stack</span></span>             |
| <span data-ttu-id="cfbb2-110">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-110">Attribute group:</span></span> |                                    |
| <span data-ttu-id="cfbb2-111">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-111">Initial value:</span></span>   | <span data-ttu-id="cfbb2-112">Identidade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-112">Identity</span></span>                           |
| <span data-ttu-id="cfbb2-113">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-113">Get command:</span></span>     | [<span data-ttu-id="cfbb2-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-114">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="cfbb2-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matriz de projeção GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-115"></dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>GL\_PROJECTION\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-116">Property</span></span> | <span data-ttu-id="cfbb2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-117">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-118">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-118">Description:</span></span>     | <span data-ttu-id="cfbb2-119">Pilha de matriz de projeção</span><span class="sxs-lookup"><span data-stu-id="cfbb2-119">Projection matrix stack</span></span>                                                        |
| <span data-ttu-id="cfbb2-120">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-120">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="cfbb2-121">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-121">Initial value:</span></span>   | <span data-ttu-id="cfbb2-122">Identidade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-122">Identity</span></span>                                                                       |
| <span data-ttu-id="cfbb2-123">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-123">Get command:</span></span>     | [<span data-ttu-id="cfbb2-124">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-124">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matriz de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-125"></dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>GL\_TEXTURE\_MATRIX</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-126">Property</span></span> | <span data-ttu-id="cfbb2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-127">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-128">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-128">Description:</span></span>     | <span data-ttu-id="cfbb2-129">Pilha de matriz de textura</span><span class="sxs-lookup"><span data-stu-id="cfbb2-129">Texture matrix stack</span></span>                                                           |
| <span data-ttu-id="cfbb2-130">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-130">Attribute group:</span></span> |                                                                                |
| <span data-ttu-id="cfbb2-131">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-131">Initial value:</span></span>   | <span data-ttu-id="cfbb2-132">Identidade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-132">Identity</span></span>                                                                       |
| <span data-ttu-id="cfbb2-133">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-133">Get command:</span></span>     | [<span data-ttu-id="cfbb2-134">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-134">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_visor GL</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-135"></dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>GL\_VIEWPORT</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-136">Property</span></span> | <span data-ttu-id="cfbb2-137">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-137">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-138">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-138">Description:</span></span>     | <span data-ttu-id="cfbb2-139">Origem e extensão do visor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-139">Viewport origin and extent</span></span>                                                       |
| <span data-ttu-id="cfbb2-140">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-140">Attribute group:</span></span> | <span data-ttu-id="cfbb2-141">visor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-141">viewport</span></span>                                                                         |
| <span data-ttu-id="cfbb2-142">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-142">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="cfbb2-143">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-143">Get command:</span></span>     | [<span data-ttu-id="cfbb2-144">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-144">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_intervalo de profundidade do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-145"></dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>GL\_DEPTH\_RANGE</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-146">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-146">Property</span></span> | <span data-ttu-id="cfbb2-147">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-147">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-148">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-148">Description:</span></span>     | <span data-ttu-id="cfbb2-149">Intervalo de profundidade próximo e longe</span><span class="sxs-lookup"><span data-stu-id="cfbb2-149">Depth range near and far</span></span>                                                       |
| <span data-ttu-id="cfbb2-150">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-150">Attribute group:</span></span> | <span data-ttu-id="cfbb2-151">visor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-151">viewport</span></span>                                                                       |
| <span data-ttu-id="cfbb2-152">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-152">Initial value:</span></span>   | <span data-ttu-id="cfbb2-153">0, 1</span><span class="sxs-lookup"><span data-stu-id="cfbb2-153">0, 1</span></span>                                                                           |
| <span data-ttu-id="cfbb2-154">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-154">Get command:</span></span>     | [<span data-ttu-id="cfbb2-155">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-155">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_profundidade de \_ pilha \_ MODELVIEW GL</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-156"></dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>GL\_MODELVIEW\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-157">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-157">Property</span></span> | <span data-ttu-id="cfbb2-158">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-158">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-159">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-159">Description:</span></span>     | <span data-ttu-id="cfbb2-160">Ponteiro de pilha de matriz Modelview</span><span class="sxs-lookup"><span data-stu-id="cfbb2-160">Modelview matrix stack pointer</span></span>                                                   |
| <span data-ttu-id="cfbb2-161">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-161">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="cfbb2-162">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-162">Initial value:</span></span>   | <span data-ttu-id="cfbb2-163">1</span><span class="sxs-lookup"><span data-stu-id="cfbb2-163">1</span></span>                                                                                |
| <span data-ttu-id="cfbb2-164">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-164">Get command:</span></span>     | [<span data-ttu-id="cfbb2-165">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-165">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_profundidade da pilha de projeção GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-166"></dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>GL\_PROJECTION\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-167">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-167">Property</span></span> | <span data-ttu-id="cfbb2-168">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-168">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-169">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-169">Description:</span></span>     | <span data-ttu-id="cfbb2-170">Ponteiro da pilha da matriz de projeção</span><span class="sxs-lookup"><span data-stu-id="cfbb2-170">Projection matrix stack pointer</span></span>                                                  |
| <span data-ttu-id="cfbb2-171">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-171">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="cfbb2-172">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-172">Initial value:</span></span>   | <span data-ttu-id="cfbb2-173">1</span><span class="sxs-lookup"><span data-stu-id="cfbb2-173">1</span></span>                                                                                |
| <span data-ttu-id="cfbb2-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-174">Get command:</span></span>     | [<span data-ttu-id="cfbb2-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>\_profundidade da \_ pilha de textura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-176"></dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>GL\_TEXTURE\_STACK\_DEPTH</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-177">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-177">Property</span></span> | <span data-ttu-id="cfbb2-178">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-178">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-179">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-179">Description:</span></span>     | <span data-ttu-id="cfbb2-180">Ponteiro de pilha da matriz de textura</span><span class="sxs-lookup"><span data-stu-id="cfbb2-180">Texture matrix stack pointer</span></span>                                                     |
| <span data-ttu-id="cfbb2-181">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-181">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="cfbb2-182">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-182">Initial value:</span></span>   | <span data-ttu-id="cfbb2-183">1</span><span class="sxs-lookup"><span data-stu-id="cfbb2-183">1</span></span>                                                                                |
| <span data-ttu-id="cfbb2-184">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-184">Get command:</span></span>     | [<span data-ttu-id="cfbb2-185">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_modo de matriz GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-186"></dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>GL\_MATRIX\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-187">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-187">Property</span></span> | <span data-ttu-id="cfbb2-188">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-188">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cfbb2-189">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-189">Description:</span></span>     | <span data-ttu-id="cfbb2-190">Modo de matriz atual</span><span class="sxs-lookup"><span data-stu-id="cfbb2-190">Current matrix mode</span></span>                                                              |
| <span data-ttu-id="cfbb2-191">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-191">Attribute group:</span></span> | <span data-ttu-id="cfbb2-192">transformação</span><span class="sxs-lookup"><span data-stu-id="cfbb2-192">transform</span></span>                                                                        |
| <span data-ttu-id="cfbb2-193">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-193">Initial value:</span></span>   | <span data-ttu-id="cfbb2-194">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="cfbb2-194">GL\_MODELVIEW</span></span>                                                                    |
| <span data-ttu-id="cfbb2-195">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-195">Get command:</span></span>     | [<span data-ttu-id="cfbb2-196">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-196">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="cfbb2-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>\_NORMALIZE GL</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-197"></dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL\_NORMALIZE</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-198">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-198">Property</span></span> | <span data-ttu-id="cfbb2-199">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-199">Value</span></span> |
|------------------|-------------------------------------|
| <span data-ttu-id="cfbb2-200">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-200">Description:</span></span>     | <span data-ttu-id="cfbb2-201">Ativar/desativar normalização normal atual</span><span class="sxs-lookup"><span data-stu-id="cfbb2-201">Current normal normalization on/off</span></span> |
| <span data-ttu-id="cfbb2-202">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-202">Attribute group:</span></span> | <span data-ttu-id="cfbb2-203">transformar/habilitar</span><span class="sxs-lookup"><span data-stu-id="cfbb2-203">transform/enable</span></span>                    |
| <span data-ttu-id="cfbb2-204">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-204">Initial value:</span></span>   | <span data-ttu-id="cfbb2-205">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="cfbb2-205">GL\_FALSE</span></span>                           |
| <span data-ttu-id="cfbb2-206">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-206">Get command:</span></span>     | [<span data-ttu-id="cfbb2-207">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-207">**glIsEnabled**</span></span>](glisenabled.md)  |



 

<span data-ttu-id="cfbb2-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>Recorte de \_ \_ plano GL *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-208"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-209">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-209">Property</span></span> | <span data-ttu-id="cfbb2-210">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-210">Value</span></span> |
|------------------|------------------------------------------|
| <span data-ttu-id="cfbb2-211">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-211">Description:</span></span>     | <span data-ttu-id="cfbb2-212">Coeficientes de plano de recorte do usuário</span><span class="sxs-lookup"><span data-stu-id="cfbb2-212">User clipping plane coefficients</span></span>         |
| <span data-ttu-id="cfbb2-213">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-213">Attribute group:</span></span> | <span data-ttu-id="cfbb2-214">transformação</span><span class="sxs-lookup"><span data-stu-id="cfbb2-214">transform</span></span>                                |
| <span data-ttu-id="cfbb2-215">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-215">Initial value:</span></span>   | <span data-ttu-id="cfbb2-216">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="cfbb2-216">0, 0, 0, 0</span></span>                               |
| <span data-ttu-id="cfbb2-217">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-217">Get command:</span></span>     | [<span data-ttu-id="cfbb2-218">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-218">**glGetClipPlane**</span></span>](glgetclipplane.md) |



 

<span data-ttu-id="cfbb2-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>Recorte de \_ \_ plano GL *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbb2-219"></dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL\_CLIP\_PLANE *i*</dt> </span></span><dd> 

| <span data-ttu-id="cfbb2-220">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cfbb2-220">Property</span></span> | <span data-ttu-id="cfbb2-221">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbb2-221">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="cfbb2-222">Descrição:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-222">Description:</span></span>     | <span data-ttu-id="cfbb2-223"> plano de recorte de usuário habilitado</span><span class="sxs-lookup"><span data-stu-id="cfbb2-223">*i* th user clipping plane enabled</span></span> |
| <span data-ttu-id="cfbb2-224">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-224">Attribute group:</span></span> | <span data-ttu-id="cfbb2-225">transformar/habilitar</span><span class="sxs-lookup"><span data-stu-id="cfbb2-225">transform/enable</span></span>                   |
| <span data-ttu-id="cfbb2-226">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-226">Initial value:</span></span>   | <span data-ttu-id="cfbb2-227">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="cfbb2-227">GL\_FALSE</span></span>                          |
| <span data-ttu-id="cfbb2-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="cfbb2-228">Get command:</span></span>     | [<span data-ttu-id="cfbb2-229">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="cfbb2-229">**glIsEnabled**</span></span>](glisenabled.md) |



 

</dd> </dl>

 

 




