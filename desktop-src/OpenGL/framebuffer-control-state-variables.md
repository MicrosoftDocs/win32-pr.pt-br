---
title: Variáveis de estado de controle framebuffer
description: Variáveis de estado de controle framebuffer
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variáveis de estado de controle framebuffer OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998414271956de44710e9ef456722d7499adb862
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910074"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="d4922-104">Variáveis de estado de controle framebuffer</span><span class="sxs-lookup"><span data-stu-id="d4922-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="d4922-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_buffer de desenho GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

| <span data-ttu-id="d4922-106">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-106">Property</span></span> | <span data-ttu-id="d4922-107">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-107">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="d4922-108">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-108">Description:</span></span>     | <span data-ttu-id="d4922-109">Buffers selecionados para desenho</span><span class="sxs-lookup"><span data-stu-id="d4922-109">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="d4922-110">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-110">Attribute group:</span></span> | <span data-ttu-id="d4922-111">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="d4922-111">color-buffer</span></span>                           |
| <span data-ttu-id="d4922-112">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-112">Initial value:</span></span>   |                                        |
| <span data-ttu-id="d4922-113">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-113">Get command:</span></span>     | [<span data-ttu-id="d4922-114">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="d4922-114">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="d4922-115"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK de índice GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-115"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="d4922-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-116">Property</span></span> | <span data-ttu-id="d4922-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-117">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-118">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-118">Description:</span></span>     | <span data-ttu-id="d4922-119">Writemask de índice de cores</span><span class="sxs-lookup"><span data-stu-id="d4922-119">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="d4922-120">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-120">Attribute group:</span></span> | <span data-ttu-id="d4922-121">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="d4922-121">color-buffer</span></span>                                                                     |
| <span data-ttu-id="d4922-122">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-122">Initial value:</span></span>   | <span data-ttu-id="d4922-123">1 ' s</span><span class="sxs-lookup"><span data-stu-id="d4922-123">1's</span></span>                                                                              |
| <span data-ttu-id="d4922-124">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-124">Get command:</span></span>     | [<span data-ttu-id="d4922-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="d4922-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-126"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de cores GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-126"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="d4922-127">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-127">Property</span></span> | <span data-ttu-id="d4922-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-128">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-129">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-129">Description:</span></span>     | <span data-ttu-id="d4922-130">Habilitação de gravação de cores; R, G, B ou A</span><span class="sxs-lookup"><span data-stu-id="d4922-130">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="d4922-131">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-131">Attribute group:</span></span> | <span data-ttu-id="d4922-132">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="d4922-132">color-buffer</span></span>                                                                     |
| <span data-ttu-id="d4922-133">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-133">Initial value:</span></span>   | <span data-ttu-id="d4922-134">GL \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="d4922-134">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="d4922-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-135">Get command:</span></span>     | [<span data-ttu-id="d4922-136">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="d4922-136">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-137"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_WRITEMASK de profundidade GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-137"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="d4922-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-138">Property</span></span> | <span data-ttu-id="d4922-139">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-140">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-140">Description:</span></span>     | <span data-ttu-id="d4922-141">Buffer de profundidade habilitado para gravação</span><span class="sxs-lookup"><span data-stu-id="d4922-141">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="d4922-142">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-142">Attribute group:</span></span> | <span data-ttu-id="d4922-143">profundidade-buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-143">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="d4922-144">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-144">Initial value:</span></span>   | <span data-ttu-id="d4922-145">GL \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="d4922-145">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="d4922-146">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-146">Get command:</span></span>     | [<span data-ttu-id="d4922-147">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="d4922-147">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-148"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-148"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

| <span data-ttu-id="d4922-149">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-149">Property</span></span> | <span data-ttu-id="d4922-150">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-151">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-151">Description:</span></span>     | <span data-ttu-id="d4922-152">Writemask de buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="d4922-152">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="d4922-153">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-153">Attribute group:</span></span> | <span data-ttu-id="d4922-154">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="d4922-155">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-155">Initial value:</span></span>   | <span data-ttu-id="d4922-156">1 ' s</span><span class="sxs-lookup"><span data-stu-id="d4922-156">1's</span></span>                                                                              |
| <span data-ttu-id="d4922-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-157">Get command:</span></span>     | [<span data-ttu-id="d4922-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="d4922-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-159"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_valor de \_ limpeza de cor GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-159"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="d4922-160">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-160">Property</span></span> | <span data-ttu-id="d4922-161">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-161">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-162">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-162">Description:</span></span>     | <span data-ttu-id="d4922-163">Valor de limpeza do buffer de cores (modo RGBA)</span><span class="sxs-lookup"><span data-stu-id="d4922-163">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="d4922-164">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-164">Attribute group:</span></span> | <span data-ttu-id="d4922-165">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="d4922-165">color-buffer</span></span>                                                                   |
| <span data-ttu-id="d4922-166">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-166">Initial value:</span></span>   | <span data-ttu-id="d4922-167">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="d4922-167">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="d4922-168">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-168">Get command:</span></span>     | [<span data-ttu-id="d4922-169">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="d4922-169">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-170"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_valor de \_ limpeza de índice GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-170"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="d4922-171">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-171">Property</span></span> | <span data-ttu-id="d4922-172">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-172">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-173">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-173">Description:</span></span>     | <span data-ttu-id="d4922-174">Valor de limpeza do buffer de cores (modo de índice de cor)</span><span class="sxs-lookup"><span data-stu-id="d4922-174">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="d4922-175">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-175">Attribute group:</span></span> | <span data-ttu-id="d4922-176">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="d4922-176">color-buffer</span></span>                                                                   |
| <span data-ttu-id="d4922-177">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-177">Initial value:</span></span>   | <span data-ttu-id="d4922-178">0</span><span class="sxs-lookup"><span data-stu-id="d4922-178">0</span></span>                                                                              |
| <span data-ttu-id="d4922-179">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-179">Get command:</span></span>     | [<span data-ttu-id="d4922-180">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="d4922-180">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-181"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_valor de \_ limpeza de profundidade GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-181"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="d4922-182">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-182">Property</span></span> | <span data-ttu-id="d4922-183">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-184">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-184">Description:</span></span>     | <span data-ttu-id="d4922-185">Profundidade-valor de limpeza do buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-185">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="d4922-186">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-186">Attribute group:</span></span> | <span data-ttu-id="d4922-187">profundidade-buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-187">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="d4922-188">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-188">Initial value:</span></span>   | <span data-ttu-id="d4922-189">1</span><span class="sxs-lookup"><span data-stu-id="d4922-189">1</span></span>                                                                                |
| <span data-ttu-id="d4922-190">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-190">Get command:</span></span>     | [<span data-ttu-id="d4922-191">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="d4922-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-192"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_valor de \_ limpeza do estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-192"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="d4922-193">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-193">Property</span></span> | <span data-ttu-id="d4922-194">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-195">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-195">Description:</span></span>     | <span data-ttu-id="d4922-196">Estêncil-valor de limpeza do buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-196">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="d4922-197">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-197">Attribute group:</span></span> | <span data-ttu-id="d4922-198">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="d4922-199">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-199">Initial value:</span></span>   | <span data-ttu-id="d4922-200">0</span><span class="sxs-lookup"><span data-stu-id="d4922-200">0</span></span>                                                                                |
| <span data-ttu-id="d4922-201">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-201">Get command:</span></span>     | [<span data-ttu-id="d4922-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="d4922-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="d4922-203"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>valor de limpeza do GL \_ Accum \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="d4922-203"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

| <span data-ttu-id="d4922-204">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4922-204">Property</span></span> | <span data-ttu-id="d4922-205">Valor</span><span class="sxs-lookup"><span data-stu-id="d4922-205">Value</span></span> |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d4922-206">Descrição:</span><span class="sxs-lookup"><span data-stu-id="d4922-206">Description:</span></span>     | <span data-ttu-id="d4922-207">Acumulação-valor de limpeza do buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-207">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="d4922-208">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="d4922-208">Attribute group:</span></span> | <span data-ttu-id="d4922-209">Accum-buffer</span><span class="sxs-lookup"><span data-stu-id="d4922-209">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="d4922-210">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="d4922-210">Initial value:</span></span>   | <span data-ttu-id="d4922-211">0</span><span class="sxs-lookup"><span data-stu-id="d4922-211">0</span></span>                                                                              |
| <span data-ttu-id="d4922-212">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="d4922-212">Get command:</span></span>     | [<span data-ttu-id="d4922-213">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="d4922-213">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




