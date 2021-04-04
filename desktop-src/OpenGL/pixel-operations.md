---
title: Operações de pixel
description: Operações de pixel
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Operações de pixel OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823197"
---
# <a name="pixel-operations"></a><span data-ttu-id="15df3-104">Operações de pixel</span><span class="sxs-lookup"><span data-stu-id="15df3-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="15df3-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_teste de tesoura do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="15df3-106">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-106">Description:</span></span>     | <span data-ttu-id="15df3-107">Recorte habilitado</span><span class="sxs-lookup"><span data-stu-id="15df3-107">Scissoring enabled</span></span>                 |
| <span data-ttu-id="15df3-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-108">Attribute group:</span></span> | <span data-ttu-id="15df3-109">recorte/habilitação</span><span class="sxs-lookup"><span data-stu-id="15df3-109">scissor/enable</span></span>                     |
| <span data-ttu-id="15df3-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-110">Initial value:</span></span>   | <span data-ttu-id="15df3-111">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="15df3-111">GL\_FALSE</span></span>                          |
| <span data-ttu-id="15df3-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-112">Get command:</span></span>     | [<span data-ttu-id="15df3-113">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="15df3-113">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="15df3-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_caixa de tesoura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-114"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-115">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-115">Description:</span></span>     | <span data-ttu-id="15df3-116">Caixa de tesoura</span><span class="sxs-lookup"><span data-stu-id="15df3-116">Scissor box</span></span>                                                                      |
| <span data-ttu-id="15df3-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-117">Attribute group:</span></span> | <span data-ttu-id="15df3-118">tesoura</span><span class="sxs-lookup"><span data-stu-id="15df3-118">scissor</span></span>                                                                          |
| <span data-ttu-id="15df3-119">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-119">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="15df3-120">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-120">Get command:</span></span>     | [<span data-ttu-id="15df3-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_teste de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-122"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="15df3-123">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-123">Description:</span></span>     | <span data-ttu-id="15df3-124">Estêncil habilitado</span><span class="sxs-lookup"><span data-stu-id="15df3-124">Stenciling enabled</span></span>                 |
| <span data-ttu-id="15df3-125">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-125">Attribute group:</span></span> | <span data-ttu-id="15df3-126">estêncil-buffer/habilitar</span><span class="sxs-lookup"><span data-stu-id="15df3-126">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="15df3-127">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-127">Initial value:</span></span>   | <span data-ttu-id="15df3-128">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="15df3-128">GL\_FALSE</span></span>                          |
| <span data-ttu-id="15df3-129">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-129">Get command:</span></span>     | [<span data-ttu-id="15df3-130">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="15df3-130">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="15df3-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>o \_ estêncil GL \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-131"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-132">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-132">Description:</span></span>     | <span data-ttu-id="15df3-133">Função de estêncil</span><span class="sxs-lookup"><span data-stu-id="15df3-133">Stencil function</span></span>                                                                 |
| <span data-ttu-id="15df3-134">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-134">Attribute group:</span></span> | <span data-ttu-id="15df3-135">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="15df3-135">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="15df3-136">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-136">Initial value:</span></span>   | <span data-ttu-id="15df3-137">GL \_ sempre</span><span class="sxs-lookup"><span data-stu-id="15df3-137">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="15df3-138">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-138">Get command:</span></span>     | [<span data-ttu-id="15df3-139">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-139">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_máscara de \_ valor de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-140"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-141">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-141">Description:</span></span>     | <span data-ttu-id="15df3-142">Máscara de estêncil</span><span class="sxs-lookup"><span data-stu-id="15df3-142">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="15df3-143">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-143">Attribute group:</span></span> | <span data-ttu-id="15df3-144">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="15df3-144">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="15df3-145">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-145">Initial value:</span></span>   | <span data-ttu-id="15df3-146">1 ' s</span><span class="sxs-lookup"><span data-stu-id="15df3-146">1's</span></span>                                                                              |
| <span data-ttu-id="15df3-147">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-147">Get command:</span></span>     | [<span data-ttu-id="15df3-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_referência de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-149"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-150">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-150">Description:</span></span>     | <span data-ttu-id="15df3-151">Valor de referência do estêncil</span><span class="sxs-lookup"><span data-stu-id="15df3-151">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="15df3-152">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-152">Attribute group:</span></span> | <span data-ttu-id="15df3-153">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="15df3-153">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="15df3-154">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-154">Initial value:</span></span>   | <span data-ttu-id="15df3-155">0</span><span class="sxs-lookup"><span data-stu-id="15df3-155">0</span></span>                                                                                |
| <span data-ttu-id="15df3-156">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-156">Get command:</span></span>     | [<span data-ttu-id="15df3-157">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-157">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_falha no estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-158"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-159">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-159">Description:</span></span>     | <span data-ttu-id="15df3-160">Ação de falha de estêncil</span><span class="sxs-lookup"><span data-stu-id="15df3-160">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="15df3-161">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-161">Attribute group:</span></span> | <span data-ttu-id="15df3-162">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="15df3-162">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="15df3-163">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-163">Initial value:</span></span>   | <span data-ttu-id="15df3-164">\_Keep GL</span><span class="sxs-lookup"><span data-stu-id="15df3-164">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="15df3-165">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-165">Get command:</span></span>     | [<span data-ttu-id="15df3-166">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-166">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>\_falha de \_ profundidade de aprovação do estêncil GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-167"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-168">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-168">Description:</span></span>     | <span data-ttu-id="15df3-169">Ação falha no buffer de profundidade do estêncil</span><span class="sxs-lookup"><span data-stu-id="15df3-169">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="15df3-170">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-170">Attribute group:</span></span> | <span data-ttu-id="15df3-171">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="15df3-171">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="15df3-172">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-172">Initial value:</span></span>   | <span data-ttu-id="15df3-173">\_Keep GL</span><span class="sxs-lookup"><span data-stu-id="15df3-173">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="15df3-174">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-174">Get command:</span></span>     | [<span data-ttu-id="15df3-175">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-175">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_passo de \_ profundidade de passagem do estêncil GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-176"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-177">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-177">Description:</span></span>     | <span data-ttu-id="15df3-178">Ação de passagem do buffer de profundidade do estêncil</span><span class="sxs-lookup"><span data-stu-id="15df3-178">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="15df3-179">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-179">Attribute group:</span></span> | <span data-ttu-id="15df3-180">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="15df3-180">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="15df3-181">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-181">Initial value:</span></span>   | <span data-ttu-id="15df3-182">\_Keep GL</span><span class="sxs-lookup"><span data-stu-id="15df3-182">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="15df3-183">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-183">Get command:</span></span>     | [<span data-ttu-id="15df3-184">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-184">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>\_teste de alfa do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-185"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="15df3-186">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-186">Description:</span></span>     | <span data-ttu-id="15df3-187">Teste alfa habilitado</span><span class="sxs-lookup"><span data-stu-id="15df3-187">Alpha test enabled</span></span>                 |
| <span data-ttu-id="15df3-188">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-188">Attribute group:</span></span> | <span data-ttu-id="15df3-189">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="15df3-189">color-buffer/enable</span></span>                |
| <span data-ttu-id="15df3-190">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-190">Initial value:</span></span>   | <span data-ttu-id="15df3-191">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="15df3-191">GL\_FALSE</span></span>                          |
| <span data-ttu-id="15df3-192">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-192">Get command:</span></span>     | [<span data-ttu-id="15df3-193">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="15df3-193">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="15df3-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>razão de teste do GL \_ alfa \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-194"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-195">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-195">Description:</span></span>     | <span data-ttu-id="15df3-196">Função de teste alfa</span><span class="sxs-lookup"><span data-stu-id="15df3-196">Alpha test function</span></span>                                                              |
| <span data-ttu-id="15df3-197">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-197">Attribute group:</span></span> | <span data-ttu-id="15df3-198">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="15df3-198">color-buffer</span></span>                                                                     |
| <span data-ttu-id="15df3-199">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-199">Initial value:</span></span>   | <span data-ttu-id="15df3-200">GL \_ sempre</span><span class="sxs-lookup"><span data-stu-id="15df3-200">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="15df3-201">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-201">Get command:</span></span>     | [<span data-ttu-id="15df3-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>\_referência de \_ teste \_ alfa do GL</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-203"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-204">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-204">Description:</span></span>     | <span data-ttu-id="15df3-205">Valor de referência de teste alfa</span><span class="sxs-lookup"><span data-stu-id="15df3-205">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="15df3-206">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-206">Attribute group:</span></span> | <span data-ttu-id="15df3-207">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="15df3-207">color-buffer</span></span>                                                                     |
| <span data-ttu-id="15df3-208">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-208">Initial value:</span></span>   | <span data-ttu-id="15df3-209">0</span><span class="sxs-lookup"><span data-stu-id="15df3-209">0</span></span>                                                                                |
| <span data-ttu-id="15df3-210">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-210">Get command:</span></span>     | [<span data-ttu-id="15df3-211">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-211">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_teste de profundidade GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-212"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="15df3-213">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-213">Description:</span></span>     | <span data-ttu-id="15df3-214">Buffer de profundidade habilitado</span><span class="sxs-lookup"><span data-stu-id="15df3-214">Depth buffer enabled</span></span>               |
| <span data-ttu-id="15df3-215">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-215">Attribute group:</span></span> | <span data-ttu-id="15df3-216">profundidade/buffer/habilitar</span><span class="sxs-lookup"><span data-stu-id="15df3-216">depth-buffer/enable</span></span>                |
| <span data-ttu-id="15df3-217">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-217">Initial value:</span></span>   | <span data-ttu-id="15df3-218">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="15df3-218">GL\_FALSE</span></span>                          |
| <span data-ttu-id="15df3-219">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-219">Get command:</span></span>     | [<span data-ttu-id="15df3-220">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="15df3-220">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="15df3-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_funcm de profundidade do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-221"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-222">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-222">Description:</span></span>     | <span data-ttu-id="15df3-223">Função de teste do buffer de profundidade</span><span class="sxs-lookup"><span data-stu-id="15df3-223">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="15df3-224">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-224">Attribute group:</span></span> | <span data-ttu-id="15df3-225">profundidade-buffer</span><span class="sxs-lookup"><span data-stu-id="15df3-225">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="15df3-226">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-226">Initial value:</span></span>   | <span data-ttu-id="15df3-227">GL \_ menos</span><span class="sxs-lookup"><span data-stu-id="15df3-227">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="15df3-228">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-228">Get command:</span></span>     | [<span data-ttu-id="15df3-229">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-229">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>a \_ combinação GL</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-230"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="15df3-231">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-231">Description:</span></span>     | <span data-ttu-id="15df3-232">Mesclagem habilitada</span><span class="sxs-lookup"><span data-stu-id="15df3-232">Blending enabled</span></span>                   |
| <span data-ttu-id="15df3-233">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-233">Attribute group:</span></span> | <span data-ttu-id="15df3-234">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="15df3-234">color-buffer/enable</span></span>                |
| <span data-ttu-id="15df3-235">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-235">Initial value:</span></span>   | <span data-ttu-id="15df3-236">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="15df3-236">GL\_FALSE</span></span>                          |
| <span data-ttu-id="15df3-237">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-237">Get command:</span></span>     | [<span data-ttu-id="15df3-238">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="15df3-238">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="15df3-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_origem GL BLENC \_</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-239"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-240">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-240">Description:</span></span>     | <span data-ttu-id="15df3-241">Função de origem de mesclagem</span><span class="sxs-lookup"><span data-stu-id="15df3-241">Blending source function</span></span>                                                         |
| <span data-ttu-id="15df3-242">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-242">Attribute group:</span></span> | <span data-ttu-id="15df3-243">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="15df3-243">color-buffer</span></span>                                                                     |
| <span data-ttu-id="15df3-244">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-244">Initial value:</span></span>   | <span data-ttu-id="15df3-245">GL \_ um</span><span class="sxs-lookup"><span data-stu-id="15df3-245">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="15df3-246">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-246">Get command:</span></span>     | [<span data-ttu-id="15df3-247">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-247">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>\_hora de \_ verão do GL</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-248"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-249">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-249">Description:</span></span>     | <span data-ttu-id="15df3-250">Função de destino de mesclagem</span><span class="sxs-lookup"><span data-stu-id="15df3-250">Blending destination function</span></span>                                                    |
| <span data-ttu-id="15df3-251">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-251">Attribute group:</span></span> | <span data-ttu-id="15df3-252">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="15df3-252">color-buffer</span></span>                                                                     |
| <span data-ttu-id="15df3-253">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-253">Initial value:</span></span>   | <span data-ttu-id="15df3-254">GL \_ zero</span><span class="sxs-lookup"><span data-stu-id="15df3-254">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="15df3-255">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-255">Get command:</span></span>     | [<span data-ttu-id="15df3-256">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-256">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="15df3-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_pontilhamento GL</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-257"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="15df3-258">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-258">Description:</span></span>     | <span data-ttu-id="15df3-259">Pontilhamento habilitado</span><span class="sxs-lookup"><span data-stu-id="15df3-259">Dithering enabled</span></span>                  |
| <span data-ttu-id="15df3-260">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-260">Attribute group:</span></span> | <span data-ttu-id="15df3-261">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="15df3-261">color-buffer/enable</span></span>                |
| <span data-ttu-id="15df3-262">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-262">Initial value:</span></span>   | <span data-ttu-id="15df3-263">GL \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="15df3-263">GL\_TRUE</span></span>                           |
| <span data-ttu-id="15df3-264">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-264">Get command:</span></span>     | [<span data-ttu-id="15df3-265">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="15df3-265">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="15df3-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_op lógico \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-266"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

|                  |                                    |
|------------------|------------------------------------|
| <span data-ttu-id="15df3-267">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-267">Description:</span></span>     | <span data-ttu-id="15df3-268">Operação lógica habilitada</span><span class="sxs-lookup"><span data-stu-id="15df3-268">Logical operation enabled</span></span>          |
| <span data-ttu-id="15df3-269">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-269">Attribute group:</span></span> | <span data-ttu-id="15df3-270">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="15df3-270">color-buffer/enable</span></span>                |
| <span data-ttu-id="15df3-271">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-271">Initial value:</span></span>   | <span data-ttu-id="15df3-272">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="15df3-272">GL\_FALSE</span></span>                          |
| <span data-ttu-id="15df3-273">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-273">Get command:</span></span>     | [<span data-ttu-id="15df3-274">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="15df3-274">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="15df3-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_modo de \_ op \_ lógico GL</dt> </span><span class="sxs-lookup"><span data-stu-id="15df3-275"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="15df3-276">Descrição:</span><span class="sxs-lookup"><span data-stu-id="15df3-276">Description:</span></span>     | <span data-ttu-id="15df3-277">Função de operação lógica</span><span class="sxs-lookup"><span data-stu-id="15df3-277">Logical operation function</span></span>                                                       |
| <span data-ttu-id="15df3-278">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="15df3-278">Attribute group:</span></span> | <span data-ttu-id="15df3-279">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="15df3-279">color-buffer</span></span>                                                                     |
| <span data-ttu-id="15df3-280">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="15df3-280">Initial value:</span></span>   | <span data-ttu-id="15df3-281">\_cópia GL</span><span class="sxs-lookup"><span data-stu-id="15df3-281">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="15df3-282">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="15df3-282">Get command:</span></span>     | [<span data-ttu-id="15df3-283">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="15df3-283">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




