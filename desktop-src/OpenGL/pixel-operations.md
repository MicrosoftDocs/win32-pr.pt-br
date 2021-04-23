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
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908874"
---
# <a name="pixel-operations"></a><span data-ttu-id="7fbc2-104">Operações de pixel</span><span class="sxs-lookup"><span data-stu-id="7fbc2-104">Pixel Operations</span></span>

<dl> <span data-ttu-id="7fbc2-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_teste de tesoura do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-105"><dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>GL\_SCISSOR\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-106">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-106">Property</span></span> | <span data-ttu-id="7fbc2-107">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-107">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fbc2-108">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-108">Description:</span></span>     | <span data-ttu-id="7fbc2-109">Recorte habilitado</span><span class="sxs-lookup"><span data-stu-id="7fbc2-109">Scissoring enabled</span></span>                 |
| <span data-ttu-id="7fbc2-110">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-110">Attribute group:</span></span> | <span data-ttu-id="7fbc2-111">recorte/habilitação</span><span class="sxs-lookup"><span data-stu-id="7fbc2-111">scissor/enable</span></span>                     |
| <span data-ttu-id="7fbc2-112">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-112">Initial value:</span></span>   | <span data-ttu-id="7fbc2-113">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="7fbc2-113">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fbc2-114">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-114">Get command:</span></span>     | [<span data-ttu-id="7fbc2-115">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-115">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fbc2-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_caixa de tesoura GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-116"></dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>GL\_SCISSOR\_BOX</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-117">Property</span></span> | <span data-ttu-id="7fbc2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-118">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-119">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-119">Description:</span></span>     | <span data-ttu-id="7fbc2-120">Caixa de tesoura</span><span class="sxs-lookup"><span data-stu-id="7fbc2-120">Scissor box</span></span>                                                                      |
| <span data-ttu-id="7fbc2-121">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-121">Attribute group:</span></span> | <span data-ttu-id="7fbc2-122">tesoura</span><span class="sxs-lookup"><span data-stu-id="7fbc2-122">scissor</span></span>                                                                          |
| <span data-ttu-id="7fbc2-123">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-123">Initial value:</span></span>   |                                                                                  |
| <span data-ttu-id="7fbc2-124">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-124">Get command:</span></span>     | [<span data-ttu-id="7fbc2-125">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-125">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_teste de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-126"></dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL\_STENCIL\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-127">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-127">Property</span></span> | <span data-ttu-id="7fbc2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-128">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fbc2-129">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-129">Description:</span></span>     | <span data-ttu-id="7fbc2-130">Estêncil habilitado</span><span class="sxs-lookup"><span data-stu-id="7fbc2-130">Stenciling enabled</span></span>                 |
| <span data-ttu-id="7fbc2-131">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-131">Attribute group:</span></span> | <span data-ttu-id="7fbc2-132">estêncil-buffer/habilitar</span><span class="sxs-lookup"><span data-stu-id="7fbc2-132">stencil-buffer/enable</span></span>              |
| <span data-ttu-id="7fbc2-133">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-133">Initial value:</span></span>   | <span data-ttu-id="7fbc2-134">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="7fbc2-134">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fbc2-135">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-135">Get command:</span></span>     | [<span data-ttu-id="7fbc2-136">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-136">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fbc2-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>o \_ estêncil GL \_ Func</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-137"></dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>GL\_STENCIL\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-138">Property</span></span> | <span data-ttu-id="7fbc2-139">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-139">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-140">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-140">Description:</span></span>     | <span data-ttu-id="7fbc2-141">Função de estêncil</span><span class="sxs-lookup"><span data-stu-id="7fbc2-141">Stencil function</span></span>                                                                 |
| <span data-ttu-id="7fbc2-142">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-142">Attribute group:</span></span> | <span data-ttu-id="7fbc2-143">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="7fbc2-143">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fbc2-144">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-144">Initial value:</span></span>   | <span data-ttu-id="7fbc2-145">GL \_ sempre</span><span class="sxs-lookup"><span data-stu-id="7fbc2-145">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="7fbc2-146">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-146">Get command:</span></span>     | [<span data-ttu-id="7fbc2-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_máscara de \_ valor de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-148"></dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL\_STENCIL\_VALUE\_MASK</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-149">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-149">Property</span></span> | <span data-ttu-id="7fbc2-150">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-150">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-151">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-151">Description:</span></span>     | <span data-ttu-id="7fbc2-152">Máscara de estêncil</span><span class="sxs-lookup"><span data-stu-id="7fbc2-152">Stencil mask</span></span>                                                                     |
| <span data-ttu-id="7fbc2-153">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-153">Attribute group:</span></span> | <span data-ttu-id="7fbc2-154">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="7fbc2-154">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fbc2-155">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-155">Initial value:</span></span>   | <span data-ttu-id="7fbc2-156">1 ' s</span><span class="sxs-lookup"><span data-stu-id="7fbc2-156">1's</span></span>                                                                              |
| <span data-ttu-id="7fbc2-157">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-157">Get command:</span></span>     | [<span data-ttu-id="7fbc2-158">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-158">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_referência de estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-159"></dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL\_STENCIL\_REF</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-160">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-160">Property</span></span> | <span data-ttu-id="7fbc2-161">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-161">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-162">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-162">Description:</span></span>     | <span data-ttu-id="7fbc2-163">Valor de referência do estêncil</span><span class="sxs-lookup"><span data-stu-id="7fbc2-163">Stencil reference value</span></span>                                                          |
| <span data-ttu-id="7fbc2-164">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-164">Attribute group:</span></span> | <span data-ttu-id="7fbc2-165">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="7fbc2-165">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fbc2-166">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-166">Initial value:</span></span>   | <span data-ttu-id="7fbc2-167">0</span><span class="sxs-lookup"><span data-stu-id="7fbc2-167">0</span></span>                                                                                |
| <span data-ttu-id="7fbc2-168">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-168">Get command:</span></span>     | [<span data-ttu-id="7fbc2-169">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-169">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_falha no estêncil GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-170"></dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>GL\_STENCIL\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-171">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-171">Property</span></span> | <span data-ttu-id="7fbc2-172">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-172">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-173">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-173">Description:</span></span>     | <span data-ttu-id="7fbc2-174">Ação de falha de estêncil</span><span class="sxs-lookup"><span data-stu-id="7fbc2-174">Stencil fail action</span></span>                                                              |
| <span data-ttu-id="7fbc2-175">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-175">Attribute group:</span></span> | <span data-ttu-id="7fbc2-176">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="7fbc2-176">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fbc2-177">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-177">Initial value:</span></span>   | <span data-ttu-id="7fbc2-178">\_Keep GL</span><span class="sxs-lookup"><span data-stu-id="7fbc2-178">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="7fbc2-179">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-179">Get command:</span></span>     | [<span data-ttu-id="7fbc2-180">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-180">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>\_falha de \_ profundidade de aprovação do estêncil GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-181"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>GL\_STENCIL\_PASS\_DEPTH\_FAIL</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-182">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-182">Property</span></span> | <span data-ttu-id="7fbc2-183">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-183">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-184">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-184">Description:</span></span>     | <span data-ttu-id="7fbc2-185">Ação falha no buffer de profundidade do estêncil</span><span class="sxs-lookup"><span data-stu-id="7fbc2-185">Stencil depth buffer fail action</span></span>                                                 |
| <span data-ttu-id="7fbc2-186">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-186">Attribute group:</span></span> | <span data-ttu-id="7fbc2-187">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="7fbc2-187">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fbc2-188">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-188">Initial value:</span></span>   | <span data-ttu-id="7fbc2-189">\_Keep GL</span><span class="sxs-lookup"><span data-stu-id="7fbc2-189">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="7fbc2-190">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-190">Get command:</span></span>     | [<span data-ttu-id="7fbc2-191">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-191">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_passo de \_ profundidade de passagem do estêncil GL \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-192"></dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>GL\_STENCIL\_PASS\_DEPTH\_PASS</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-193">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-193">Property</span></span> | <span data-ttu-id="7fbc2-194">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-194">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-195">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-195">Description:</span></span>     | <span data-ttu-id="7fbc2-196">Ação de passagem do buffer de profundidade do estêncil</span><span class="sxs-lookup"><span data-stu-id="7fbc2-196">Stencil depth buffer pass action</span></span>                                                 |
| <span data-ttu-id="7fbc2-197">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-197">Attribute group:</span></span> | <span data-ttu-id="7fbc2-198">estêncil-buffer</span><span class="sxs-lookup"><span data-stu-id="7fbc2-198">stencil-buffer</span></span>                                                                   |
| <span data-ttu-id="7fbc2-199">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-199">Initial value:</span></span>   | <span data-ttu-id="7fbc2-200">\_Keep GL</span><span class="sxs-lookup"><span data-stu-id="7fbc2-200">GL\_KEEP</span></span>                                                                         |
| <span data-ttu-id="7fbc2-201">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-201">Get command:</span></span>     | [<span data-ttu-id="7fbc2-202">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-202">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>\_teste de alfa do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-203"></dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL\_ALPHA\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-204">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-204">Property</span></span> | <span data-ttu-id="7fbc2-205">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-205">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fbc2-206">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-206">Description:</span></span>     | <span data-ttu-id="7fbc2-207">Teste alfa habilitado</span><span class="sxs-lookup"><span data-stu-id="7fbc2-207">Alpha test enabled</span></span>                 |
| <span data-ttu-id="7fbc2-208">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-208">Attribute group:</span></span> | <span data-ttu-id="7fbc2-209">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="7fbc2-209">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fbc2-210">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-210">Initial value:</span></span>   | <span data-ttu-id="7fbc2-211">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="7fbc2-211">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fbc2-212">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-212">Get command:</span></span>     | [<span data-ttu-id="7fbc2-213">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-213">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fbc2-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>razão de teste do GL \_ alfa \_ \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-214"></dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL\_ALPHA\_TEST\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-215">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-215">Property</span></span> | <span data-ttu-id="7fbc2-216">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-216">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-217">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-217">Description:</span></span>     | <span data-ttu-id="7fbc2-218">Função de teste alfa</span><span class="sxs-lookup"><span data-stu-id="7fbc2-218">Alpha test function</span></span>                                                              |
| <span data-ttu-id="7fbc2-219">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-219">Attribute group:</span></span> | <span data-ttu-id="7fbc2-220">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="7fbc2-220">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fbc2-221">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-221">Initial value:</span></span>   | <span data-ttu-id="7fbc2-222">GL \_ sempre</span><span class="sxs-lookup"><span data-stu-id="7fbc2-222">GL\_ALWAYS</span></span>                                                                       |
| <span data-ttu-id="7fbc2-223">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-223">Get command:</span></span>     | [<span data-ttu-id="7fbc2-224">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-224">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>\_referência de \_ teste \_ alfa do GL</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-225"></dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL\_ALPHA\_TEST\_REF</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-226">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-226">Property</span></span> | <span data-ttu-id="7fbc2-227">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-227">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-228">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-228">Description:</span></span>     | <span data-ttu-id="7fbc2-229">Valor de referência de teste alfa</span><span class="sxs-lookup"><span data-stu-id="7fbc2-229">Alpha test reference value</span></span>                                                       |
| <span data-ttu-id="7fbc2-230">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-230">Attribute group:</span></span> | <span data-ttu-id="7fbc2-231">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="7fbc2-231">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fbc2-232">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-232">Initial value:</span></span>   | <span data-ttu-id="7fbc2-233">0</span><span class="sxs-lookup"><span data-stu-id="7fbc2-233">0</span></span>                                                                                |
| <span data-ttu-id="7fbc2-234">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-234">Get command:</span></span>     | [<span data-ttu-id="7fbc2-235">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-235">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_teste de profundidade GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-236"></dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>GL\_DEPTH\_TEST</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-237">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-237">Property</span></span> | <span data-ttu-id="7fbc2-238">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-238">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fbc2-239">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-239">Description:</span></span>     | <span data-ttu-id="7fbc2-240">Buffer de profundidade habilitado</span><span class="sxs-lookup"><span data-stu-id="7fbc2-240">Depth buffer enabled</span></span>               |
| <span data-ttu-id="7fbc2-241">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-241">Attribute group:</span></span> | <span data-ttu-id="7fbc2-242">profundidade/buffer/habilitar</span><span class="sxs-lookup"><span data-stu-id="7fbc2-242">depth-buffer/enable</span></span>                |
| <span data-ttu-id="7fbc2-243">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-243">Initial value:</span></span>   | <span data-ttu-id="7fbc2-244">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="7fbc2-244">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fbc2-245">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-245">Get command:</span></span>     | [<span data-ttu-id="7fbc2-246">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-246">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fbc2-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_funcm de profundidade do GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-247"></dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL\_DEPTH\_FUNC</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-248">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-248">Property</span></span> | <span data-ttu-id="7fbc2-249">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-249">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-250">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-250">Description:</span></span>     | <span data-ttu-id="7fbc2-251">Função de teste do buffer de profundidade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-251">Depth buffer test function</span></span>                                                       |
| <span data-ttu-id="7fbc2-252">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-252">Attribute group:</span></span> | <span data-ttu-id="7fbc2-253">profundidade-buffer</span><span class="sxs-lookup"><span data-stu-id="7fbc2-253">depth-buffer</span></span>                                                                     |
| <span data-ttu-id="7fbc2-254">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-254">Initial value:</span></span>   | <span data-ttu-id="7fbc2-255">GL \_ menos</span><span class="sxs-lookup"><span data-stu-id="7fbc2-255">GL\_LESS</span></span>                                                                         |
| <span data-ttu-id="7fbc2-256">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-256">Get command:</span></span>     | [<span data-ttu-id="7fbc2-257">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-257">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>a \_ combinação GL</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-258"></dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL\_BLEND</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-259">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-259">Property</span></span> | <span data-ttu-id="7fbc2-260">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-260">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fbc2-261">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-261">Description:</span></span>     | <span data-ttu-id="7fbc2-262">Mesclagem habilitada</span><span class="sxs-lookup"><span data-stu-id="7fbc2-262">Blending enabled</span></span>                   |
| <span data-ttu-id="7fbc2-263">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-263">Attribute group:</span></span> | <span data-ttu-id="7fbc2-264">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="7fbc2-264">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fbc2-265">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-265">Initial value:</span></span>   | <span data-ttu-id="7fbc2-266">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="7fbc2-266">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fbc2-267">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-267">Get command:</span></span>     | [<span data-ttu-id="7fbc2-268">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-268">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fbc2-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_origem GL BLENC \_</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-269"></dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL\_BLENC\_SRC</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-270">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-270">Property</span></span> | <span data-ttu-id="7fbc2-271">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-271">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-272">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-272">Description:</span></span>     | <span data-ttu-id="7fbc2-273">Função de origem de mesclagem</span><span class="sxs-lookup"><span data-stu-id="7fbc2-273">Blending source function</span></span>                                                         |
| <span data-ttu-id="7fbc2-274">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-274">Attribute group:</span></span> | <span data-ttu-id="7fbc2-275">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="7fbc2-275">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fbc2-276">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-276">Initial value:</span></span>   | <span data-ttu-id="7fbc2-277">GL \_ um</span><span class="sxs-lookup"><span data-stu-id="7fbc2-277">GL\_ONE</span></span>                                                                          |
| <span data-ttu-id="7fbc2-278">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-278">Get command:</span></span>     | [<span data-ttu-id="7fbc2-279">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-279">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>\_hora de \_ verão do GL</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-280"></dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL\_BLEND\_DST</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-281">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-281">Property</span></span> | <span data-ttu-id="7fbc2-282">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-282">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-283">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-283">Description:</span></span>     | <span data-ttu-id="7fbc2-284">Função de destino de mesclagem</span><span class="sxs-lookup"><span data-stu-id="7fbc2-284">Blending destination function</span></span>                                                    |
| <span data-ttu-id="7fbc2-285">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-285">Attribute group:</span></span> | <span data-ttu-id="7fbc2-286">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="7fbc2-286">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fbc2-287">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-287">Initial value:</span></span>   | <span data-ttu-id="7fbc2-288">GL \_ zero</span><span class="sxs-lookup"><span data-stu-id="7fbc2-288">GL\_ZERO</span></span>                                                                         |
| <span data-ttu-id="7fbc2-289">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-289">Get command:</span></span>     | [<span data-ttu-id="7fbc2-290">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-290">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="7fbc2-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_pontilhamento GL</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-291"></dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL\_DITHER</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-292">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-292">Property</span></span> | <span data-ttu-id="7fbc2-293">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-293">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fbc2-294">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-294">Description:</span></span>     | <span data-ttu-id="7fbc2-295">Pontilhamento habilitado</span><span class="sxs-lookup"><span data-stu-id="7fbc2-295">Dithering enabled</span></span>                  |
| <span data-ttu-id="7fbc2-296">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-296">Attribute group:</span></span> | <span data-ttu-id="7fbc2-297">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="7fbc2-297">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fbc2-298">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-298">Initial value:</span></span>   | <span data-ttu-id="7fbc2-299">GL \_ verdadeiro</span><span class="sxs-lookup"><span data-stu-id="7fbc2-299">GL\_TRUE</span></span>                           |
| <span data-ttu-id="7fbc2-300">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-300">Get command:</span></span>     | [<span data-ttu-id="7fbc2-301">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-301">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fbc2-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_op lógico \_ GL</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-302"></dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL\_LOGIC\_OP</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-303">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-303">Property</span></span> | <span data-ttu-id="7fbc2-304">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-304">Value</span></span> |
|------------------|------------------------------------|
| <span data-ttu-id="7fbc2-305">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-305">Description:</span></span>     | <span data-ttu-id="7fbc2-306">Operação lógica habilitada</span><span class="sxs-lookup"><span data-stu-id="7fbc2-306">Logical operation enabled</span></span>          |
| <span data-ttu-id="7fbc2-307">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-307">Attribute group:</span></span> | <span data-ttu-id="7fbc2-308">buffer de cores/habilitar</span><span class="sxs-lookup"><span data-stu-id="7fbc2-308">color-buffer/enable</span></span>                |
| <span data-ttu-id="7fbc2-309">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-309">Initial value:</span></span>   | <span data-ttu-id="7fbc2-310">GL \_ falso</span><span class="sxs-lookup"><span data-stu-id="7fbc2-310">GL\_FALSE</span></span>                          |
| <span data-ttu-id="7fbc2-311">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-311">Get command:</span></span>     | [<span data-ttu-id="7fbc2-312">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-312">**glIsEnabled**</span></span>](glisenabled.md) |



 

<span data-ttu-id="7fbc2-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_modo de \_ op \_ lógico GL</dt> </span><span class="sxs-lookup"><span data-stu-id="7fbc2-313"></dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL\_LOGIC\_OP\_MODE</dt> </span></span><dd> 

| <span data-ttu-id="7fbc2-314">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7fbc2-314">Property</span></span> | <span data-ttu-id="7fbc2-315">Valor</span><span class="sxs-lookup"><span data-stu-id="7fbc2-315">Value</span></span> |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7fbc2-316">Descrição:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-316">Description:</span></span>     | <span data-ttu-id="7fbc2-317">Função de operação lógica</span><span class="sxs-lookup"><span data-stu-id="7fbc2-317">Logical operation function</span></span>                                                       |
| <span data-ttu-id="7fbc2-318">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-318">Attribute group:</span></span> | <span data-ttu-id="7fbc2-319">buffer de cores</span><span class="sxs-lookup"><span data-stu-id="7fbc2-319">color-buffer</span></span>                                                                     |
| <span data-ttu-id="7fbc2-320">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-320">Initial value:</span></span>   | <span data-ttu-id="7fbc2-321">\_cópia GL</span><span class="sxs-lookup"><span data-stu-id="7fbc2-321">GL\_COPY</span></span>                                                                         |
| <span data-ttu-id="7fbc2-322">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="7fbc2-322">Get command:</span></span>     | [<span data-ttu-id="7fbc2-323">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="7fbc2-323">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




