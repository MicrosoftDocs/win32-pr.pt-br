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
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823096"
---
# <a name="framebuffer-control-state-variables"></a><span data-ttu-id="62def-104">Variáveis de estado de controle framebuffer</span><span class="sxs-lookup"><span data-stu-id="62def-104">Framebuffer Control State Variables</span></span>

<dl> <span data-ttu-id="62def-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_buffer de desenho GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-105"><dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>GL\_DRAW\_BUFFER</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="62def-106">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-106">Description:</span></span>     | <span data-ttu-id="62def-107">Buffers selecionados para desenho</span><span class="sxs-lookup"><span data-stu-id="62def-107">Buffers selected for drawing</span></span>           |
| <span data-ttu-id="62def-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-108">Attribute group:</span></span> | <span data-ttu-id="62def-109">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="62def-109">color-buffer</span></span>                           |
| <span data-ttu-id="62def-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-110">Initial value:</span></span>   |                                        |
| <span data-ttu-id="62def-111">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-111">Get command:</span></span>     | [<span data-ttu-id="62def-112">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="62def-112">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="62def-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK de índice GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-113"></dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL\_INDEX\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62def-114">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-114">Description:</span></span>     | <span data-ttu-id="62def-115">Writemask de índice de cores</span><span class="sxs-lookup"><span data-stu-id="62def-115">Color-index writemask</span></span>                                                            |
| <span data-ttu-id="62def-116">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-116">Attribute group:</span></span> | <span data-ttu-id="62def-117">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="62def-117">color-buffer</span></span>                                                                     |
| <span data-ttu-id="62def-118">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-118">Initial value:</span></span>   | <span data-ttu-id="62def-119">1 ' s</span><span class="sxs-lookup"><span data-stu-id="62def-119">1's</span></span>                                                                              |
| <span data-ttu-id="62def-120">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-120">Get command:</span></span>     | [<span data-ttu-id="62def-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="62def-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de cores GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-122"></dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL\_COLOR\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62def-123">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-123">Description:</span></span>     | <span data-ttu-id="62def-124">Habilitação de gravação de cores; R, G, B ou A</span><span class="sxs-lookup"><span data-stu-id="62def-124">Color write enables; R, G, B, or A</span></span>                                               |
| <span data-ttu-id="62def-125">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-125">Attribute group:</span></span> | <span data-ttu-id="62def-126">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="62def-126">color-buffer</span></span>                                                                     |
| <span data-ttu-id="62def-127">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-127">Initial value:</span></span>   | <span data-ttu-id="62def-128">GL \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="62def-128">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="62def-129">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-129">Get command:</span></span>     | [<span data-ttu-id="62def-130">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="62def-130">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_WRITEMASK de profundidade GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-131"></dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL\_DEPTH\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62def-132">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-132">Description:</span></span>     | <span data-ttu-id="62def-133">Buffer de profundidade habilitado para gravação</span><span class="sxs-lookup"><span data-stu-id="62def-133">Depth buffer enabled for writing</span></span>                                                 |
| <span data-ttu-id="62def-134">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-134">Attribute group:</span></span> | <span data-ttu-id="62def-135">profundidade-buffer</span><span class="sxs-lookup"><span data-stu-id="62def-135">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="62def-136">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-136">Initial value:</span></span>   | <span data-ttu-id="62def-137">GL \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="62def-137">GL\_TRUE</span></span>                                                                         |
| <span data-ttu-id="62def-138">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-138">Get command:</span></span>     | [<span data-ttu-id="62def-139">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="62def-139">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-140"></dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL\_STENCIL\_WRITEMASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62def-141">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-141">Description:</span></span>     | <span data-ttu-id="62def-142">Writemask de buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="62def-142">Stencil-buffer writemask</span></span>                                                         |
| <span data-ttu-id="62def-143">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-143">Attribute group:</span></span> | <span data-ttu-id="62def-144">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="62def-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="62def-145">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-145">Initial value:</span></span>   | <span data-ttu-id="62def-146">1 ' s</span><span class="sxs-lookup"><span data-stu-id="62def-146">1's</span></span>                                                                              |
| <span data-ttu-id="62def-147">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-147">Get command:</span></span>     | [<span data-ttu-id="62def-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="62def-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_valor de \_ limpeza de cor GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-149"></dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL\_COLOR\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="62def-150">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-150">Description:</span></span>     | <span data-ttu-id="62def-151">Valor de limpeza do buffer de cores (modo RGBA)</span><span class="sxs-lookup"><span data-stu-id="62def-151">Color-buffer clear value (RGBA mode)</span></span>                                           |
| <span data-ttu-id="62def-152">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-152">Attribute group:</span></span> | <span data-ttu-id="62def-153">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="62def-153">color-buffer</span></span>                                                                   |
| <span data-ttu-id="62def-154">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-154">Initial value:</span></span>   | <span data-ttu-id="62def-155">0, 0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="62def-155">0, 0, 0, 0</span></span>                                                                     |
| <span data-ttu-id="62def-156">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-156">Get command:</span></span>     | [<span data-ttu-id="62def-157">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="62def-157">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_valor de \_ limpeza de índice GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-158"></dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL\_INDEX\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="62def-159">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-159">Description:</span></span>     | <span data-ttu-id="62def-160">Valor de limpeza do buffer de cores (modo de índice de cor)</span><span class="sxs-lookup"><span data-stu-id="62def-160">Color-buffer clear value (color-index mode)</span></span>                                    |
| <span data-ttu-id="62def-161">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-161">Attribute group:</span></span> | <span data-ttu-id="62def-162">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="62def-162">color-buffer</span></span>                                                                   |
| <span data-ttu-id="62def-163">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-163">Initial value:</span></span>   | <span data-ttu-id="62def-164">0</span><span class="sxs-lookup"><span data-stu-id="62def-164">0</span></span>                                                                              |
| <span data-ttu-id="62def-165">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-165">Get command:</span></span>     | [<span data-ttu-id="62def-166">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="62def-166">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_valor de \_ limpeza de profundidade GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-167"></dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL\_DEPTH\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62def-168">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-168">Description:</span></span>     | <span data-ttu-id="62def-169">Profundidade-valor de limpeza do buffer</span><span class="sxs-lookup"><span data-stu-id="62def-169">Depth-buffer clear value</span></span>                                                         |
| <span data-ttu-id="62def-170">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-170">Attribute group:</span></span> | <span data-ttu-id="62def-171">profundidade-buffer</span><span class="sxs-lookup"><span data-stu-id="62def-171">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="62def-172">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-172">Initial value:</span></span>   | <span data-ttu-id="62def-173">1</span><span class="sxs-lookup"><span data-stu-id="62def-173">1</span></span>                                                                                |
| <span data-ttu-id="62def-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-174">Get command:</span></span>     | [<span data-ttu-id="62def-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="62def-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_valor de \_ limpeza do estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-176"></dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL\_STENCIL\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62def-177">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-177">Description:</span></span>     | <span data-ttu-id="62def-178">Estêncil-valor de limpeza do buffer</span><span class="sxs-lookup"><span data-stu-id="62def-178">Stencil-buffer clear value</span></span>                                                       |
| <span data-ttu-id="62def-179">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-179">Attribute group:</span></span> | <span data-ttu-id="62def-180">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="62def-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="62def-181">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-181">Initial value:</span></span>   | <span data-ttu-id="62def-182">0</span><span class="sxs-lookup"><span data-stu-id="62def-182">0</span></span>                                                                                |
| <span data-ttu-id="62def-183">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-183">Get command:</span></span>     | [<span data-ttu-id="62def-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="62def-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="62def-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>valor de limpeza do GL \_ Accum \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="62def-185"></dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL\_ACCUM\_CLEAR\_VALUE</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="62def-186">Descrição:</span><span class="sxs-lookup"><span data-stu-id="62def-186">Description:</span></span>     | <span data-ttu-id="62def-187">Acumulação-valor de limpeza do buffer</span><span class="sxs-lookup"><span data-stu-id="62def-187">Accumulation-buffer clear value</span></span>                                                |
| <span data-ttu-id="62def-188">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="62def-188">Attribute group:</span></span> | <span data-ttu-id="62def-189">Accum-buffer</span><span class="sxs-lookup"><span data-stu-id="62def-189">accum-buffer</span></span>                                                                   |
| <span data-ttu-id="62def-190">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="62def-190">Initial value:</span></span>   | <span data-ttu-id="62def-191">0</span><span class="sxs-lookup"><span data-stu-id="62def-191">0</span></span>                                                                              |
| <span data-ttu-id="62def-192">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="62def-192">Get command:</span></span>     | [<span data-ttu-id="62def-193">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="62def-193">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




