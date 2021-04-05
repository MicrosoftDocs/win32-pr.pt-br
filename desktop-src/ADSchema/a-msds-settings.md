---
title: atributo ms-DS-Settings
description: Usado para armazenar as configurações de um objeto. Seu uso é determinado exclusivamente pelo proprietário do objeto. É recomendável usá-lo para armazenar pares de nome/valor. Por exemplo, cor azul.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- ms-DS-Settings atributo AD Schema
- atributo msDS-Settings do esquema do AD
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825182"
---
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="6374d-108">atributo ms-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="6374d-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="6374d-109">Usado para armazenar as configurações de um objeto.</span><span class="sxs-lookup"><span data-stu-id="6374d-109">Used to store settings for an object.</span></span> <span data-ttu-id="6374d-110">Seu uso é determinado exclusivamente pelo proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="6374d-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="6374d-111">É recomendável usá-lo para armazenar pares de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="6374d-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="6374d-112">Por exemplo, Color = Blue.</span><span class="sxs-lookup"><span data-stu-id="6374d-112">For example, color=blue.</span></span>



| <span data-ttu-id="6374d-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="6374d-113">Entry</span></span> | <span data-ttu-id="6374d-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6374d-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6374d-115">CN</span><span class="sxs-lookup"><span data-stu-id="6374d-115">CN</span></span>                | <span data-ttu-id="6374d-116">ms-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="6374d-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="6374d-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6374d-117">Ldap-Display-Name</span></span> | <span data-ttu-id="6374d-118">msDS-configurações</span><span class="sxs-lookup"><span data-stu-id="6374d-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="6374d-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6374d-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="6374d-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6374d-120">Update Privilege</span></span>  | <span data-ttu-id="6374d-121">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="6374d-121">Domain administrator</span></span>                        |
| <span data-ttu-id="6374d-122">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6374d-122">Update Frequency</span></span>  | <span data-ttu-id="6374d-123">Cada vez que os valores das configurações são alterados.</span><span class="sxs-lookup"><span data-stu-id="6374d-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="6374d-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6374d-124">Attribute-Id</span></span>      | <span data-ttu-id="6374d-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="6374d-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="6374d-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6374d-126">System-Id-Guid</span></span>    | <span data-ttu-id="6374d-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="6374d-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="6374d-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="6374d-128">Syntax</span></span>            | [<span data-ttu-id="6374d-129">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="6374d-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6374d-130">Implementações</span><span class="sxs-lookup"><span data-stu-id="6374d-130">Implementations</span></span>

-   [<span data-ttu-id="6374d-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6374d-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6374d-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6374d-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6374d-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6374d-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6374d-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6374d-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6374d-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6374d-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6374d-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6374d-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6374d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6374d-137">Windows Server 2003</span></span>



| <span data-ttu-id="6374d-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="6374d-138">Entry</span></span> | <span data-ttu-id="6374d-139">Valor</span><span class="sxs-lookup"><span data-stu-id="6374d-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6374d-140">ID do link</span><span class="sxs-lookup"><span data-stu-id="6374d-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6374d-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="6374d-142">System-Only</span></span>            | <span data-ttu-id="6374d-143">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-144">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6374d-144">Is-Single-Valued</span></span>       | <span data-ttu-id="6374d-145">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-146">É indexado</span><span class="sxs-lookup"><span data-stu-id="6374d-146">Is Indexed</span></span>             | <span data-ttu-id="6374d-147">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-148">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6374d-148">In Global Catalog</span></span>      | <span data-ttu-id="6374d-149">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6374d-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="6374d-151">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6374d-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="6374d-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6374d-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6374d-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-154">Search-Flags</span></span>           | <span data-ttu-id="6374d-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-156">System-Flags</span></span>           | <span data-ttu-id="6374d-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6374d-158">Classes used in</span></span>        | [<span data-ttu-id="6374d-159">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="6374d-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="6374d-160">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="6374d-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6374d-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="6374d-161">ADAM</span></span>



| <span data-ttu-id="6374d-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="6374d-162">Entry</span></span> | <span data-ttu-id="6374d-163">Valor</span><span class="sxs-lookup"><span data-stu-id="6374d-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="6374d-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="6374d-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6374d-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6374d-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="6374d-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="6374d-166">System-Only</span></span>            | <span data-ttu-id="6374d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-167">False</span></span>                                                            |
| <span data-ttu-id="6374d-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6374d-168">Is-Single-Valued</span></span>       | <span data-ttu-id="6374d-169">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-169">False</span></span>                                                            |
| <span data-ttu-id="6374d-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="6374d-170">Is Indexed</span></span>             | <span data-ttu-id="6374d-171">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-171">False</span></span>                                                            |
| <span data-ttu-id="6374d-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6374d-172">In Global Catalog</span></span>      | <span data-ttu-id="6374d-173">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-173">False</span></span>                                                            |
| <span data-ttu-id="6374d-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6374d-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="6374d-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6374d-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="6374d-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6374d-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="6374d-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6374d-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="6374d-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-178">Search-Flags</span></span>           | <span data-ttu-id="6374d-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="6374d-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-180">System-Flags</span></span>           | <span data-ttu-id="6374d-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="6374d-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6374d-182">Classes used in</span></span>        | [<span data-ttu-id="6374d-183">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="6374d-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6374d-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6374d-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6374d-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="6374d-185">Entry</span></span> | <span data-ttu-id="6374d-186">Valor</span><span class="sxs-lookup"><span data-stu-id="6374d-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6374d-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="6374d-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6374d-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="6374d-189">System-Only</span></span>            | <span data-ttu-id="6374d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6374d-191">Is-Single-Valued</span></span>       | <span data-ttu-id="6374d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="6374d-193">Is Indexed</span></span>             | <span data-ttu-id="6374d-194">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6374d-195">In Global Catalog</span></span>      | <span data-ttu-id="6374d-196">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6374d-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="6374d-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6374d-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="6374d-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6374d-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6374d-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-201">Search-Flags</span></span>           | <span data-ttu-id="6374d-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-203">System-Flags</span></span>           | <span data-ttu-id="6374d-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6374d-205">Classes used in</span></span>        | [<span data-ttu-id="6374d-206">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="6374d-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="6374d-207">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="6374d-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6374d-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6374d-208">Windows Server 2008</span></span>



| <span data-ttu-id="6374d-209">Entrada</span><span class="sxs-lookup"><span data-stu-id="6374d-209">Entry</span></span> | <span data-ttu-id="6374d-210">Valor</span><span class="sxs-lookup"><span data-stu-id="6374d-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6374d-211">ID do link</span><span class="sxs-lookup"><span data-stu-id="6374d-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6374d-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="6374d-213">System-Only</span></span>            | <span data-ttu-id="6374d-214">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6374d-215">Is-Single-Valued</span></span>       | <span data-ttu-id="6374d-216">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="6374d-217">Is Indexed</span></span>             | <span data-ttu-id="6374d-218">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6374d-219">In Global Catalog</span></span>      | <span data-ttu-id="6374d-220">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6374d-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="6374d-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6374d-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="6374d-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6374d-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6374d-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-225">Search-Flags</span></span>           | <span data-ttu-id="6374d-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-227">System-Flags</span></span>           | <span data-ttu-id="6374d-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6374d-229">Classes used in</span></span>        | [<span data-ttu-id="6374d-230">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="6374d-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="6374d-231">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="6374d-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6374d-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6374d-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6374d-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="6374d-233">Entry</span></span> | <span data-ttu-id="6374d-234">Valor</span><span class="sxs-lookup"><span data-stu-id="6374d-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6374d-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="6374d-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6374d-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="6374d-237">System-Only</span></span>            | <span data-ttu-id="6374d-238">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6374d-239">Is-Single-Valued</span></span>       | <span data-ttu-id="6374d-240">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="6374d-241">Is Indexed</span></span>             | <span data-ttu-id="6374d-242">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6374d-243">In Global Catalog</span></span>      | <span data-ttu-id="6374d-244">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6374d-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="6374d-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6374d-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="6374d-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6374d-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6374d-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-249">Search-Flags</span></span>           | <span data-ttu-id="6374d-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-251">System-Flags</span></span>           | <span data-ttu-id="6374d-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6374d-253">Classes used in</span></span>        | [<span data-ttu-id="6374d-254">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="6374d-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="6374d-255">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="6374d-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6374d-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6374d-256">Windows Server 2012</span></span>



| <span data-ttu-id="6374d-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="6374d-257">Entry</span></span> | <span data-ttu-id="6374d-258">Valor</span><span class="sxs-lookup"><span data-stu-id="6374d-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6374d-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="6374d-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6374d-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="6374d-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6374d-261">System-Only</span></span>            | <span data-ttu-id="6374d-262">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6374d-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6374d-264">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="6374d-265">Is Indexed</span></span>             | <span data-ttu-id="6374d-266">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6374d-267">In Global Catalog</span></span>      | <span data-ttu-id="6374d-268">Falso</span><span class="sxs-lookup"><span data-stu-id="6374d-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="6374d-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6374d-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6374d-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6374d-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="6374d-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6374d-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6374d-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="6374d-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-273">Search-Flags</span></span>           | <span data-ttu-id="6374d-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6374d-275">System-Flags</span></span>           | <span data-ttu-id="6374d-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6374d-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="6374d-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6374d-277">Classes used in</span></span>        | [<span data-ttu-id="6374d-278">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="6374d-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="6374d-279">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="6374d-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





