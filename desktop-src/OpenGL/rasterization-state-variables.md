---
title: Variáveis de estado de rasterização
description: Variáveis de estado de rasterização
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Variáveis de estado de rasterização OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1667c530ea1db8c9e463be0edad5de98e8b107
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638568"
---
# <a name="rasterization-state-variables"></a><span data-ttu-id="21862-104">Variáveis de estado de rasterização</span><span class="sxs-lookup"><span data-stu-id="21862-104">Rasterization State Variables</span></span>

<dl> <span data-ttu-id="21862-105"><dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>\_tamanho do ponto GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-105"><dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>GL\_POINT\_SIZE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="21862-106">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-106">Description:</span></span>     | <span data-ttu-id="21862-107">Tamanho do ponto</span><span class="sxs-lookup"><span data-stu-id="21862-107">Point size</span></span>                         |
| <span data-ttu-id="21862-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-108">Attribute group:</span></span> | <span data-ttu-id="21862-109">point</span><span class="sxs-lookup"><span data-stu-id="21862-109">point</span></span>                              |
| <span data-ttu-id="21862-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-110">Initial value:</span></span>   | <span data-ttu-id="21862-111">1.0</span><span class="sxs-lookup"><span data-stu-id="21862-111">1.0</span></span>                                |
| <span data-ttu-id="21862-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-112">Get command:</span></span>     | [<span data-ttu-id="21862-113">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="21862-113">**glGetFloatv**</span></span>](glgetfloatv.md) |



 

<span data-ttu-id="21862-114"></dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>\_simples ponto \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-114"></dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL\_POINT\_SMOOTH</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="21862-115">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-115">Description:</span></span>     | <span data-ttu-id="21862-116">Alias de ponto em</span><span class="sxs-lookup"><span data-stu-id="21862-116">Point aliasing on</span></span>                  |
| <span data-ttu-id="21862-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-117">Attribute group:</span></span> | <span data-ttu-id="21862-118">ponto/ativação</span><span class="sxs-lookup"><span data-stu-id="21862-118">point/enable</span></span>                       |
| <span data-ttu-id="21862-119">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-119">Initial value:</span></span>   | <span data-ttu-id="21862-120">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="21862-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="21862-121">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-121">Get command:</span></span>     | [<span data-ttu-id="21862-122">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="21862-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="21862-123"></dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>\_largura da linha gl \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-123"></dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>GL\_LINE\_WIDTH</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="21862-124">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-124">Description:</span></span>     | <span data-ttu-id="21862-125">Largura da linha</span><span class="sxs-lookup"><span data-stu-id="21862-125">Line width</span></span>                                                                     |
| <span data-ttu-id="21862-126">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-126">Attribute group:</span></span> | <span data-ttu-id="21862-127">line</span><span class="sxs-lookup"><span data-stu-id="21862-127">line</span></span>                                                                           |
| <span data-ttu-id="21862-128">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-128">Initial value:</span></span>   | <span data-ttu-id="21862-129">1.0</span><span class="sxs-lookup"><span data-stu-id="21862-129">1.0</span></span>                                                                            |
| <span data-ttu-id="21862-130">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-130">Get command:</span></span>     | [<span data-ttu-id="21862-131">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="21862-131">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="21862-132"></dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>linha do GL \_ \_ Smooth</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-132"></dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL\_LINE\_SMOOTH</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="21862-133">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-133">Description:</span></span>     | <span data-ttu-id="21862-134">Suavização de linha em</span><span class="sxs-lookup"><span data-stu-id="21862-134">Line antialiasing on</span></span>               |
| <span data-ttu-id="21862-135">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-135">Attribute group:</span></span> | <span data-ttu-id="21862-136">linha/habilitar</span><span class="sxs-lookup"><span data-stu-id="21862-136">line/enable</span></span>                        |
| <span data-ttu-id="21862-137">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-137">Initial value:</span></span>   | <span data-ttu-id="21862-138">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="21862-138">GL\_FALSE</span></span>                          |
| <span data-ttu-id="21862-139">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-139">Get command:</span></span>     | [<span data-ttu-id="21862-140">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="21862-140">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="21862-141"></dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>\_padrão de \_ STIPPLE de linha gl \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-141"></dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>GL\_LINE\_STIPPLE\_PATTERN</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21862-142">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-142">Description:</span></span>     | <span data-ttu-id="21862-143">Stipple de linha</span><span class="sxs-lookup"><span data-stu-id="21862-143">Line stipple</span></span>                                                                     |
| <span data-ttu-id="21862-144">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-144">Attribute group:</span></span> | <span data-ttu-id="21862-145">line</span><span class="sxs-lookup"><span data-stu-id="21862-145">line</span></span>                                                                             |
| <span data-ttu-id="21862-146">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-146">Initial value:</span></span>   | <span data-ttu-id="21862-147">1 ' s</span><span class="sxs-lookup"><span data-stu-id="21862-147">1's</span></span>                                                                              |
| <span data-ttu-id="21862-148">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-148">Get command:</span></span>     | [<span data-ttu-id="21862-149">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="21862-149">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="21862-150"></dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>\_STIPPLE de linha gl \_ \_ repetir</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-150"></dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL\_LINE\_STIPPLE\_REPEAT</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21862-151">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-151">Description:</span></span>     | <span data-ttu-id="21862-152">Repetir Stipple de linha</span><span class="sxs-lookup"><span data-stu-id="21862-152">Line stipple repeat</span></span>                                                              |
| <span data-ttu-id="21862-153">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-153">Attribute group:</span></span> | <span data-ttu-id="21862-154">line</span><span class="sxs-lookup"><span data-stu-id="21862-154">line</span></span>                                                                             |
| <span data-ttu-id="21862-155">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-155">Initial value:</span></span>   | <span data-ttu-id="21862-156">1</span><span class="sxs-lookup"><span data-stu-id="21862-156">1</span></span>                                                                                |
| <span data-ttu-id="21862-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-157">Get command:</span></span>     | [<span data-ttu-id="21862-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="21862-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="21862-159"></dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>\_STIPPLE de linha gl \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-159"></dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL\_LINE\_STIPPLE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="21862-160">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-160">Description:</span></span>     | <span data-ttu-id="21862-161">Habilitar Stipple de linha</span><span class="sxs-lookup"><span data-stu-id="21862-161">Line stipple enable</span></span>                |
| <span data-ttu-id="21862-162">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-162">Attribute group:</span></span> | <span data-ttu-id="21862-163">linha/habilitar</span><span class="sxs-lookup"><span data-stu-id="21862-163">line/enable</span></span>                        |
| <span data-ttu-id="21862-164">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-164">Initial value:</span></span>   | <span data-ttu-id="21862-165">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="21862-165">GL\_FALSE</span></span>                          |
| <span data-ttu-id="21862-166">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-166">Get command:</span></span>     | [<span data-ttu-id="21862-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="21862-167">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="21862-168"></dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>\_face de seleção GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-168"></dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>GL\_CULL\_FACE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="21862-169">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-169">Description:</span></span>     | <span data-ttu-id="21862-170">Remoção de polígono habilitada</span><span class="sxs-lookup"><span data-stu-id="21862-170">Polygon culling enabled</span></span>            |
| <span data-ttu-id="21862-171">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-171">Attribute group:</span></span> | <span data-ttu-id="21862-172">polígono/habilitar</span><span class="sxs-lookup"><span data-stu-id="21862-172">polygon/enable</span></span>                     |
| <span data-ttu-id="21862-173">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-173">Initial value:</span></span>   | <span data-ttu-id="21862-174">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="21862-174">GL\_FALSE</span></span>                          |
| <span data-ttu-id="21862-175">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-175">Get command:</span></span>     | [<span data-ttu-id="21862-176">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="21862-176">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="21862-177"></dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>\_modo de seleção de \_ face GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-177"></dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>GL\_CULL\_FACE\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21862-178">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-178">Description:</span></span>     | <span data-ttu-id="21862-179">Selecionar polígonos front-face/verso</span><span class="sxs-lookup"><span data-stu-id="21862-179">Cull front-facing/back-facing polygons</span></span>                                           |
| <span data-ttu-id="21862-180">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-180">Attribute group:</span></span> | <span data-ttu-id="21862-181">polygon</span><span class="sxs-lookup"><span data-stu-id="21862-181">polygon</span></span>                                                                          |
| <span data-ttu-id="21862-182">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-182">Initial value:</span></span>   | <span data-ttu-id="21862-183">GL \_ regressivo</span><span class="sxs-lookup"><span data-stu-id="21862-183">GL\_BACK</span></span>                                                                         |
| <span data-ttu-id="21862-184">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-184">Get command:</span></span>     | [<span data-ttu-id="21862-185">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="21862-185">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="21862-186"></dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>\_frontal \_ face do GL</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-186"></dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>GL\_FRONT\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21862-187">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-187">Description:</span></span>     | <span data-ttu-id="21862-188">Indicador de PV frontal/CCW do polígono</span><span class="sxs-lookup"><span data-stu-id="21862-188">Polygon front-face CW/CCW indicator</span></span>                                              |
| <span data-ttu-id="21862-189">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-189">Attribute group:</span></span> | <span data-ttu-id="21862-190">polygon</span><span class="sxs-lookup"><span data-stu-id="21862-190">polygon</span></span>                                                                          |
| <span data-ttu-id="21862-191">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-191">Initial value:</span></span>   | <span data-ttu-id="21862-192">\_CCW GL</span><span class="sxs-lookup"><span data-stu-id="21862-192">GL\_CCW</span></span>                                                                          |
| <span data-ttu-id="21862-193">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-193">Get command:</span></span>     | [<span data-ttu-id="21862-194">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="21862-194">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="21862-195"></dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>\_suavização do polígono GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-195"></dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>GL\_POLYGON\_SMOOTH</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="21862-196">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-196">Description:</span></span>     | <span data-ttu-id="21862-197">Anti-aliasing em polígono em</span><span class="sxs-lookup"><span data-stu-id="21862-197">Polygon antialiasing on</span></span>            |
| <span data-ttu-id="21862-198">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-198">Attribute group:</span></span> | <span data-ttu-id="21862-199">polígono/habilitar</span><span class="sxs-lookup"><span data-stu-id="21862-199">polygon/enable</span></span>                     |
| <span data-ttu-id="21862-200">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-200">Initial value:</span></span>   | <span data-ttu-id="21862-201">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="21862-201">GL\_FALSE</span></span>                          |
| <span data-ttu-id="21862-202">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-202">Get command:</span></span>     | [<span data-ttu-id="21862-203">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="21862-203">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="21862-204"></dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_modo de polígono GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-204"></dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>GL\_POLYGON\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="21862-205">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-205">Description:</span></span>     | <span data-ttu-id="21862-206">Modo de rasterização de polígono (frente e verso)</span><span class="sxs-lookup"><span data-stu-id="21862-206">Polygon rasterization mode (front and back)</span></span>                                      |
| <span data-ttu-id="21862-207">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-207">Attribute group:</span></span> | <span data-ttu-id="21862-208">polygon</span><span class="sxs-lookup"><span data-stu-id="21862-208">polygon</span></span>                                                                          |
| <span data-ttu-id="21862-209">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-209">Initial value:</span></span>   | <span data-ttu-id="21862-210">preenchimento do GL \_</span><span class="sxs-lookup"><span data-stu-id="21862-210">GL\_FILL</span></span>                                                                         |
| <span data-ttu-id="21862-211">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-211">Get command:</span></span>     | [<span data-ttu-id="21862-212">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="21862-212">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="21862-213"></dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>polígono do GL \_ \_ STIPPLE</dt> </span><span class="sxs-lookup"><span data-stu-id="21862-213"></dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>GL\_POLYGON\_STIPPLE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="21862-214">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-214">Description:</span></span>     | <span data-ttu-id="21862-215">Habilitar Stipple de polígono</span><span class="sxs-lookup"><span data-stu-id="21862-215">Polygon stipple enable</span></span>             |
| <span data-ttu-id="21862-216">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-216">Attribute group:</span></span> | <span data-ttu-id="21862-217">polígono/habilitar</span><span class="sxs-lookup"><span data-stu-id="21862-217">polygon/enable</span></span>                     |
| <span data-ttu-id="21862-218">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-218">Initial value:</span></span>   | <span data-ttu-id="21862-219">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="21862-219">GL\_FALSE</span></span>                          |
| <span data-ttu-id="21862-220">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-220">Get command:</span></span>     | [<span data-ttu-id="21862-221">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="21862-221">**glIsEnabled**</span></span>](glisenabled.md) |



 



|                  |                                                    |
|------------------|----------------------------------------------------|
| <span data-ttu-id="21862-222">Descrição:</span><span class="sxs-lookup"><span data-stu-id="21862-222">Description:</span></span>     | <span data-ttu-id="21862-223">Padrão Stipple de polígono</span><span class="sxs-lookup"><span data-stu-id="21862-223">Polygon stipple pattern</span></span>                            |
| <span data-ttu-id="21862-224">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="21862-224">Attribute group:</span></span> | <span data-ttu-id="21862-225">polígono-Stipple</span><span class="sxs-lookup"><span data-stu-id="21862-225">polygon-stipple</span></span>                                    |
| <span data-ttu-id="21862-226">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="21862-226">Initial value:</span></span>   | <span data-ttu-id="21862-227">1 ' s</span><span class="sxs-lookup"><span data-stu-id="21862-227">1's</span></span>                                                |
| <span data-ttu-id="21862-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="21862-228">Get command:</span></span>     | [<span data-ttu-id="21862-229">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="21862-229">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




