---
title: Variáveis de estado de iluminação
description: Variáveis de estado de iluminação
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variáveis de estado de iluminação OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823259"
---
# <a name="lighting-state-variables"></a><span data-ttu-id="01091-104">Variáveis de estado de iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-104">Lighting State Variables</span></span>

<dl> <span data-ttu-id="01091-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_iluminação GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-105"><dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL\_LIGHTING</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-106">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-106">Description:</span></span>     | <span data-ttu-id="01091-107">True se a iluminação estiver habilitada</span><span class="sxs-lookup"><span data-stu-id="01091-107">True if lighting is enabled</span></span>        |
| <span data-ttu-id="01091-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-108">Attribute group:</span></span> | <span data-ttu-id="01091-109">iluminação/habilitação</span><span class="sxs-lookup"><span data-stu-id="01091-109">lighting/enable</span></span>                    |
| <span data-ttu-id="01091-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-110">Initial value:</span></span>   | <span data-ttu-id="01091-111">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="01091-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="01091-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-112">Get command:</span></span>     | [<span data-ttu-id="01091-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="01091-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="01091-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_material de cor GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-114"></dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>GL\_COLOR\_MATERIAL</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-115">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-115">Description:</span></span>     | <span data-ttu-id="01091-116">True se o controle de cores estiver habilitado</span><span class="sxs-lookup"><span data-stu-id="01091-116">True if color tracking is enabled</span></span>  |
| <span data-ttu-id="01091-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-117">Attribute group:</span></span> | <span data-ttu-id="01091-118">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-118">lighting</span></span>                           |
| <span data-ttu-id="01091-119">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-119">Initial value:</span></span>   | <span data-ttu-id="01091-120">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="01091-120">GL\_FALSE</span></span>                          |
| <span data-ttu-id="01091-121">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-121">Get command:</span></span>     | [<span data-ttu-id="01091-122">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="01091-122">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="01091-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_parâmetro de \_ material de cor GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-123"></dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>GL\_COLOR\_MATERIAL\_PARAMETER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01091-124">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-124">Description:</span></span>     | <span data-ttu-id="01091-125">Propriedades do material rastreando a cor atual</span><span class="sxs-lookup"><span data-stu-id="01091-125">Material properties tracking current color</span></span>                                       |
| <span data-ttu-id="01091-126">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-126">Attribute group:</span></span> | <span data-ttu-id="01091-127">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-127">lighting</span></span>                                                                         |
| <span data-ttu-id="01091-128">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-128">Initial value:</span></span>   | <span data-ttu-id="01091-129">\_ambiente GL \_ e \_ difuso</span><span class="sxs-lookup"><span data-stu-id="01091-129">GL\_AMBIENT\_AND\_DIFFUSE</span></span>                                                        |
| <span data-ttu-id="01091-130">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-130">Get command:</span></span>     | [<span data-ttu-id="01091-131">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="01091-131">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="01091-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_material de cor GL \_ \_ face</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-132"></dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL\_COLOR\_MATERIAL\_FACE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01091-133">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-133">Description:</span></span>     | <span data-ttu-id="01091-134">Rostos afetadas pelo controle de cores</span><span class="sxs-lookup"><span data-stu-id="01091-134">Faces affected by color tracking</span></span>                                                 |
| <span data-ttu-id="01091-135">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-135">Attribute group:</span></span> | <span data-ttu-id="01091-136">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-136">lighting</span></span>                                                                         |
| <span data-ttu-id="01091-137">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-137">Initial value:</span></span>   | <span data-ttu-id="01091-138">GL \_ frontal \_ e \_ posterior</span><span class="sxs-lookup"><span data-stu-id="01091-138">GL\_FRONT\_AND\_BACK</span></span>                                                             |
| <span data-ttu-id="01091-139">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-139">Get command:</span></span>     | [<span data-ttu-id="01091-140">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="01091-140">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="01091-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-141"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="01091-142">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-142">Description:</span></span>     | <span data-ttu-id="01091-143">Cor do material de ambiente</span><span class="sxs-lookup"><span data-stu-id="01091-143">Ambient material color</span></span>                   |
| <span data-ttu-id="01091-144">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-144">Attribute group:</span></span> | <span data-ttu-id="01091-145">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-145">lighting</span></span>                                 |
| <span data-ttu-id="01091-146">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-146">Initial value:</span></span>   | <span data-ttu-id="01091-147">(0.2, 0.2, 0.2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="01091-147">(0.2,0.2,0.2,1.0)</span></span>                        |
| <span data-ttu-id="01091-148">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-148">Get command:</span></span>     | [<span data-ttu-id="01091-149">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="01091-149">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="01091-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_difusão GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-150"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="01091-151">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-151">Description:</span></span>     | <span data-ttu-id="01091-152">Cor do material difuso</span><span class="sxs-lookup"><span data-stu-id="01091-152">Diffuse material color</span></span>                   |
| <span data-ttu-id="01091-153">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-153">Attribute group:</span></span> | <span data-ttu-id="01091-154">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-154">lighting</span></span>                                 |
| <span data-ttu-id="01091-155">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-155">Initial value:</span></span>   | <span data-ttu-id="01091-156">(0,8, 0,8, 0,8, 1,0)</span><span class="sxs-lookup"><span data-stu-id="01091-156">(0.8,0.8,0.8,1.0)</span></span>                        |
| <span data-ttu-id="01091-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-157">Get command:</span></span>     | [<span data-ttu-id="01091-158">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="01091-158">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="01091-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_ESPECULA GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-159"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="01091-160">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-160">Description:</span></span>     | <span data-ttu-id="01091-161">Cor do material especular</span><span class="sxs-lookup"><span data-stu-id="01091-161">Specular material color</span></span>                  |
| <span data-ttu-id="01091-162">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-162">Attribute group:</span></span> | <span data-ttu-id="01091-163">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-163">lighting</span></span>                                 |
| <span data-ttu-id="01091-164">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-164">Initial value:</span></span>   | <span data-ttu-id="01091-165">(0,0, 0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="01091-165">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="01091-166">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-166">Get command:</span></span>     | [<span data-ttu-id="01091-167">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="01091-167">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="01091-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_emissão GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-168"></dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL\_EMISSION</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="01091-169">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-169">Description:</span></span>     | <span data-ttu-id="01091-170">Cor do material de emissiva</span><span class="sxs-lookup"><span data-stu-id="01091-170">Emissive material color</span></span>                  |
| <span data-ttu-id="01091-171">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-171">Attribute group:</span></span> | <span data-ttu-id="01091-172">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-172">lighting</span></span>                                 |
| <span data-ttu-id="01091-173">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-173">Initial value:</span></span>   | <span data-ttu-id="01091-174">(0,0, 0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="01091-174">(0.0,0.0,0.0,1.0)</span></span>                        |
| <span data-ttu-id="01091-175">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-175">Get command:</span></span>     | [<span data-ttu-id="01091-176">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="01091-176">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="01091-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>claridade do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-177"></dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL\_SHININESS</dt> </span></span><dd> 

|                  |                                          |
|------------------|------------------------------------------|
| <span data-ttu-id="01091-178">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-178">Description:</span></span>     | <span data-ttu-id="01091-179">Expoente de material especular</span><span class="sxs-lookup"><span data-stu-id="01091-179">Specular exponent of material</span></span>            |
| <span data-ttu-id="01091-180">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-180">Attribute group:</span></span> | <span data-ttu-id="01091-181">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-181">lighting</span></span>                                 |
| <span data-ttu-id="01091-182">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-182">Initial value:</span></span>   | <span data-ttu-id="01091-183">0.0</span><span class="sxs-lookup"><span data-stu-id="01091-183">0.0</span></span>                                      |
| <span data-ttu-id="01091-184">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-184">Get command:</span></span>     | [<span data-ttu-id="01091-185">**glGetMaterialfv**</span><span class="sxs-lookup"><span data-stu-id="01091-185">**glGetMaterialfv**</span></span>](glgetmaterial.md) |



 

<span data-ttu-id="01091-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>\_ambiente de \_ modelo \_ Light GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-186"></dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL\_LIGHT\_MODEL\_AMBIENT</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="01091-187">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-187">Description:</span></span>     | <span data-ttu-id="01091-188">Cor da cena ambiente</span><span class="sxs-lookup"><span data-stu-id="01091-188">Ambient scene color</span></span>                                                            |
| <span data-ttu-id="01091-189">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-189">Attribute group:</span></span> | <span data-ttu-id="01091-190">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-190">lighting</span></span>                                                                       |
| <span data-ttu-id="01091-191">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-191">Initial value:</span></span>   | <span data-ttu-id="01091-192">(0.2, 0.2, 0.2, 1,0)</span><span class="sxs-lookup"><span data-stu-id="01091-192">(0.2,0.2,0.2,1.0)</span></span>                                                              |
| <span data-ttu-id="01091-193">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-193">Get command:</span></span>     | [<span data-ttu-id="01091-194">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="01091-194">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="01091-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ Visualizador local de modelo Light \_ GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-195"></dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01091-196">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-196">Description:</span></span>     | <span data-ttu-id="01091-197">O visualizador é local</span><span class="sxs-lookup"><span data-stu-id="01091-197">Viewer is local</span></span>                                                                  |
| <span data-ttu-id="01091-198">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-198">Attribute group:</span></span> | <span data-ttu-id="01091-199">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-199">lighting</span></span>                                                                         |
| <span data-ttu-id="01091-200">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-200">Initial value:</span></span>   | <span data-ttu-id="01091-201">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="01091-201">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="01091-202">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-202">Get command:</span></span>     | [<span data-ttu-id="01091-203">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="01091-203">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="01091-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_Método Light \_ GL \_ dois \_ lados</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-204"></dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL\_LIGHT\_MODEL\_TWO\_SIDE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="01091-205">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-205">Description:</span></span>     | <span data-ttu-id="01091-206">Usar iluminação de dois lados</span><span class="sxs-lookup"><span data-stu-id="01091-206">Use two-sided lighting</span></span>                                                           |
| <span data-ttu-id="01091-207">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-207">Attribute group:</span></span> | <span data-ttu-id="01091-208">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-208">lighting</span></span>                                                                         |
| <span data-ttu-id="01091-209">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-209">Initial value:</span></span>   | <span data-ttu-id="01091-210">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="01091-210">GL\_FALSE</span></span>                                                                        |
| <span data-ttu-id="01091-211">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-211">Get command:</span></span>     | [<span data-ttu-id="01091-212">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="01091-212">**glGetBooleanv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="01091-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>\_ambiente GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-213"></dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL\_AMBIENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-214">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-214">Description:</span></span>     | <span data-ttu-id="01091-215">Intensidade de ambiente da *leve*</span><span class="sxs-lookup"><span data-stu-id="01091-215">Ambient intensity of light *i*</span></span>     |
| <span data-ttu-id="01091-216">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-216">Attribute group:</span></span> | <span data-ttu-id="01091-217">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-217">lighting</span></span>                           |
| <span data-ttu-id="01091-218">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-218">Initial value:</span></span>   | <span data-ttu-id="01091-219">(0,0, 0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="01091-219">(0.0,0.0,0.0,1.0)</span></span>                  |
| <span data-ttu-id="01091-220">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-220">Get command:</span></span>     | [<span data-ttu-id="01091-221">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-221">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_difusão GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-222"></dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL\_DIFFUSE</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-223">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-223">Description:</span></span>     | <span data-ttu-id="01091-224">Intensidade difusa da luz *i*</span><span class="sxs-lookup"><span data-stu-id="01091-224">Diffuse intensity of light *i*</span></span>     |
| <span data-ttu-id="01091-225">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-225">Attribute group:</span></span> | <span data-ttu-id="01091-226">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-226">lighting</span></span>                           |
| <span data-ttu-id="01091-227">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-227">Initial value:</span></span>   |                                    |
| <span data-ttu-id="01091-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-228">Get command:</span></span>     | [<span data-ttu-id="01091-229">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-229">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_ESPECULA GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-230"></dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL\_SPECULAR</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-231">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-231">Description:</span></span>     | <span data-ttu-id="01091-232">Intensidade especular da luz *i*</span><span class="sxs-lookup"><span data-stu-id="01091-232">Specular intensity of light *i*</span></span>    |
| <span data-ttu-id="01091-233">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-233">Attribute group:</span></span> | <span data-ttu-id="01091-234">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-234">lighting</span></span>                           |
| <span data-ttu-id="01091-235">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-235">Initial value:</span></span>   |                                    |
| <span data-ttu-id="01091-236">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-236">Get command:</span></span>     | [<span data-ttu-id="01091-237">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-237">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_posição GL</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-238"></dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>GL\_POSITION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-239">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-239">Description:</span></span>     | <span data-ttu-id="01091-240">Posição da luz *i*</span><span class="sxs-lookup"><span data-stu-id="01091-240">Position of light *i*</span></span>              |
| <span data-ttu-id="01091-241">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-241">Attribute group:</span></span> | <span data-ttu-id="01091-242">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-242">lighting</span></span>                           |
| <span data-ttu-id="01091-243">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-243">Initial value:</span></span>   | <span data-ttu-id="01091-244">(0,0, 0,0, 1,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="01091-244">(0.0,0.0,1.0,0.0)</span></span>                  |
| <span data-ttu-id="01091-245">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-245">Get command:</span></span>     | [<span data-ttu-id="01091-246">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-246">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_atenuação de constante GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-247"></dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>GL\_CONSTANT\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-248">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-248">Description:</span></span>     | <span data-ttu-id="01091-249">Fator de atenuação constante</span><span class="sxs-lookup"><span data-stu-id="01091-249">Constant attenuation factor</span></span>        |
| <span data-ttu-id="01091-250">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-250">Attribute group:</span></span> | <span data-ttu-id="01091-251">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-251">lighting</span></span>                           |
| <span data-ttu-id="01091-252">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-252">Initial value:</span></span>   | <span data-ttu-id="01091-253">1.0</span><span class="sxs-lookup"><span data-stu-id="01091-253">1.0</span></span>                                |
| <span data-ttu-id="01091-254">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-254">Get command:</span></span>     | [<span data-ttu-id="01091-255">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-255">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_atenuação linear do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-256"></dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>GL\_LINEAR\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-257">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-257">Description:</span></span>     | <span data-ttu-id="01091-258">Fator de atenuação linear</span><span class="sxs-lookup"><span data-stu-id="01091-258">Linear attenuation factor</span></span>          |
| <span data-ttu-id="01091-259">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-259">Attribute group:</span></span> | <span data-ttu-id="01091-260">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-260">lighting</span></span>                           |
| <span data-ttu-id="01091-261">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-261">Initial value:</span></span>   | <span data-ttu-id="01091-262">0.0</span><span class="sxs-lookup"><span data-stu-id="01091-262">0.0</span></span>                                |
| <span data-ttu-id="01091-263">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-263">Get command:</span></span>     | [<span data-ttu-id="01091-264">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-264">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_atenuação quadrática do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-265"></dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>GL\_QUADRATIC\_ATTENUATION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-266">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-266">Description:</span></span>     | <span data-ttu-id="01091-267">Fator de atenuação quadrática</span><span class="sxs-lookup"><span data-stu-id="01091-267">Quadratic attenuation factor</span></span>       |
| <span data-ttu-id="01091-268">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-268">Attribute group:</span></span> | <span data-ttu-id="01091-269">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-269">lighting</span></span>                           |
| <span data-ttu-id="01091-270">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-270">Initial value:</span></span>   | <span data-ttu-id="01091-271">0.0</span><span class="sxs-lookup"><span data-stu-id="01091-271">0.0</span></span>                                |
| <span data-ttu-id="01091-272">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-272">Get command:</span></span>     | [<span data-ttu-id="01091-273">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-273">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_direção de spot GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-274"></dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>GL\_SPOT\_DIRECTION</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-275">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-275">Description:</span></span>     | <span data-ttu-id="01091-276">Direção do destaque da luz *i*</span><span class="sxs-lookup"><span data-stu-id="01091-276">Spotlight direction of light *i*</span></span>   |
| <span data-ttu-id="01091-277">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-277">Attribute group:</span></span> | <span data-ttu-id="01091-278">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-278">lighting</span></span>                           |
| <span data-ttu-id="01091-279">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-279">Initial value:</span></span>   | <span data-ttu-id="01091-280">(0,0, 0,0,-1,0)</span><span class="sxs-lookup"><span data-stu-id="01091-280">(0.0,0.0,-1.0)</span></span>                     |
| <span data-ttu-id="01091-281">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-281">Get command:</span></span>     | [<span data-ttu-id="01091-282">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-282">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>\_expoente de spot de GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-283"></dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>GL\_SPOT\_EXPONENT</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-284">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-284">Description:</span></span>     | <span data-ttu-id="01091-285">Expoente de destaque da luz *i*</span><span class="sxs-lookup"><span data-stu-id="01091-285">Spotlight exponent of light *i*</span></span>    |
| <span data-ttu-id="01091-286">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-286">Attribute group:</span></span> | <span data-ttu-id="01091-287">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-287">lighting</span></span>                           |
| <span data-ttu-id="01091-288">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-288">Initial value:</span></span>   | <span data-ttu-id="01091-289">0.0</span><span class="sxs-lookup"><span data-stu-id="01091-289">0.0</span></span>                                |
| <span data-ttu-id="01091-290">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-290">Get command:</span></span>     | [<span data-ttu-id="01091-291">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-291">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>\_corte de spot GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-292"></dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL\_SPOT\_CUTOFF</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-293">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-293">Description:</span></span>     | <span data-ttu-id="01091-294">Ângulo de destaque da leve *i*</span><span class="sxs-lookup"><span data-stu-id="01091-294">Spotlight angle of light *i*</span></span>       |
| <span data-ttu-id="01091-295">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-295">Attribute group:</span></span> | <span data-ttu-id="01091-296">iluminação</span><span class="sxs-lookup"><span data-stu-id="01091-296">lighting</span></span>                           |
| <span data-ttu-id="01091-297">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-297">Initial value:</span></span>   | <span data-ttu-id="01091-298">180,0</span><span class="sxs-lookup"><span data-stu-id="01091-298">180.0</span></span>                              |
| <span data-ttu-id="01091-299">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-299">Get command:</span></span>     | [<span data-ttu-id="01091-300">**glGetLightfv**</span><span class="sxs-lookup"><span data-stu-id="01091-300">**glGetLightfv**</span></span>](glgetlight.md) |



 

<span data-ttu-id="01091-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ claro *i*</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-301"></dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL\_LIGHT *i*</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="01091-302">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-302">Description:</span></span>     | <span data-ttu-id="01091-303">True se o Light *i* estiver habilitado</span><span class="sxs-lookup"><span data-stu-id="01091-303">True if light *i* enabled</span></span>          |
| <span data-ttu-id="01091-304">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-304">Attribute group:</span></span> | <span data-ttu-id="01091-305">iluminação/habilitação</span><span class="sxs-lookup"><span data-stu-id="01091-305">lighting/enable</span></span>                    |
| <span data-ttu-id="01091-306">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-306">Initial value:</span></span>   | <span data-ttu-id="01091-307">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="01091-307">GL\_FALSE</span></span>                          |
| <span data-ttu-id="01091-308">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-308">Get command:</span></span>     | [<span data-ttu-id="01091-309">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="01091-309">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="01091-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_índices de cores GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="01091-310"></dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>GL\_COLOR\_INDEXES</dt> </span></span><dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="01091-311">Descrição:</span><span class="sxs-lookup"><span data-stu-id="01091-311">Description:</span></span>     | <span data-ttu-id="01091-312">*C (a)*, *c (d)* e *c (s)* para a iluminação de índice de cor</span><span class="sxs-lookup"><span data-stu-id="01091-312">*C (a)*, *C (d)*, and *C (s)* for color-index lighting</span></span>                         |
| <span data-ttu-id="01091-313">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="01091-313">Attribute group:</span></span> | <span data-ttu-id="01091-314">iluminação/habilitação</span><span class="sxs-lookup"><span data-stu-id="01091-314">lighting/enable</span></span>                                                                |
| <span data-ttu-id="01091-315">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="01091-315">Initial value:</span></span>   | <span data-ttu-id="01091-316">0, 1, 1</span><span class="sxs-lookup"><span data-stu-id="01091-316">0,1,1</span></span>                                                                          |
| <span data-ttu-id="01091-317">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="01091-317">Get command:</span></span>     | [<span data-ttu-id="01091-318">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="01091-318">**glGetFloatv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




