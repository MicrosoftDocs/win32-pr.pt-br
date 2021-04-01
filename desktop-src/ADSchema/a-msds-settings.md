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
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="8fea9-108">atributo ms-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="8fea9-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="8fea9-109">Usado para armazenar as configurações de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8fea9-109">Used to store settings for an object.</span></span> <span data-ttu-id="8fea9-110">Seu uso é determinado exclusivamente pelo proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="8fea9-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="8fea9-111">É recomendável usá-lo para armazenar pares de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="8fea9-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="8fea9-112">Por exemplo, Color = Blue.</span><span class="sxs-lookup"><span data-stu-id="8fea9-112">For example, color=blue.</span></span>



| <span data-ttu-id="8fea9-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fea9-113">Entry</span></span> | <span data-ttu-id="8fea9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8fea9-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8fea9-115">CN</span><span class="sxs-lookup"><span data-stu-id="8fea9-115">CN</span></span>                | <span data-ttu-id="8fea9-116">ms-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="8fea9-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="8fea9-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8fea9-117">Ldap-Display-Name</span></span> | <span data-ttu-id="8fea9-118">msDS-configurações</span><span class="sxs-lookup"><span data-stu-id="8fea9-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="8fea9-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8fea9-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="8fea9-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8fea9-120">Update Privilege</span></span>  | <span data-ttu-id="8fea9-121">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="8fea9-121">Domain administrator</span></span>                        |
| <span data-ttu-id="8fea9-122">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8fea9-122">Update Frequency</span></span>  | <span data-ttu-id="8fea9-123">Cada vez que os valores das configurações são alterados.</span><span class="sxs-lookup"><span data-stu-id="8fea9-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="8fea9-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8fea9-124">Attribute-Id</span></span>      | <span data-ttu-id="8fea9-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="8fea9-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="8fea9-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8fea9-126">System-Id-Guid</span></span>    | <span data-ttu-id="8fea9-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="8fea9-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="8fea9-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fea9-128">Syntax</span></span>            | [<span data-ttu-id="8fea9-129">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8fea9-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8fea9-130">Implementações</span><span class="sxs-lookup"><span data-stu-id="8fea9-130">Implementations</span></span>

-   [<span data-ttu-id="8fea9-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8fea9-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8fea9-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8fea9-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8fea9-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8fea9-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8fea9-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8fea9-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8fea9-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8fea9-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8fea9-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8fea9-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8fea9-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8fea9-137">Windows Server 2003</span></span>



| <span data-ttu-id="8fea9-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fea9-138">Entry</span></span> | <span data-ttu-id="8fea9-139">Valor</span><span class="sxs-lookup"><span data-stu-id="8fea9-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fea9-140">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fea9-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fea9-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fea9-142">System-Only</span></span>            | <span data-ttu-id="8fea9-143">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-144">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fea9-144">Is-Single-Valued</span></span>       | <span data-ttu-id="8fea9-145">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-146">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fea9-146">Is Indexed</span></span>             | <span data-ttu-id="8fea9-147">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-148">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fea9-148">In Global Catalog</span></span>      | <span data-ttu-id="8fea9-149">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-150">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fea9-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fea9-151">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fea9-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="8fea9-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fea9-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fea9-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-154">Search-Flags</span></span>           | <span data-ttu-id="8fea9-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-156">System-Flags</span></span>           | <span data-ttu-id="8fea9-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fea9-158">Classes used in</span></span>        | [<span data-ttu-id="8fea9-159">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="8fea9-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="8fea9-160">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="8fea9-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8fea9-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="8fea9-161">ADAM</span></span>



| <span data-ttu-id="8fea9-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fea9-162">Entry</span></span> | <span data-ttu-id="8fea9-163">Valor</span><span class="sxs-lookup"><span data-stu-id="8fea9-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="8fea9-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fea9-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="8fea9-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fea9-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="8fea9-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fea9-166">System-Only</span></span>            | <span data-ttu-id="8fea9-167">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-167">False</span></span>                                                            |
| <span data-ttu-id="8fea9-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fea9-168">Is-Single-Valued</span></span>       | <span data-ttu-id="8fea9-169">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-169">False</span></span>                                                            |
| <span data-ttu-id="8fea9-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fea9-170">Is Indexed</span></span>             | <span data-ttu-id="8fea9-171">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-171">False</span></span>                                                            |
| <span data-ttu-id="8fea9-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fea9-172">In Global Catalog</span></span>      | <span data-ttu-id="8fea9-173">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-173">False</span></span>                                                            |
| <span data-ttu-id="8fea9-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fea9-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fea9-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fea9-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="8fea9-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fea9-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="8fea9-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fea9-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="8fea9-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-178">Search-Flags</span></span>           | <span data-ttu-id="8fea9-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="8fea9-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-180">System-Flags</span></span>           | <span data-ttu-id="8fea9-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="8fea9-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fea9-182">Classes used in</span></span>        | [<span data-ttu-id="8fea9-183">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="8fea9-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8fea9-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8fea9-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8fea9-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fea9-185">Entry</span></span> | <span data-ttu-id="8fea9-186">Valor</span><span class="sxs-lookup"><span data-stu-id="8fea9-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fea9-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fea9-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fea9-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fea9-189">System-Only</span></span>            | <span data-ttu-id="8fea9-190">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fea9-191">Is-Single-Valued</span></span>       | <span data-ttu-id="8fea9-192">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fea9-193">Is Indexed</span></span>             | <span data-ttu-id="8fea9-194">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fea9-195">In Global Catalog</span></span>      | <span data-ttu-id="8fea9-196">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fea9-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fea9-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fea9-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="8fea9-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fea9-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fea9-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-201">Search-Flags</span></span>           | <span data-ttu-id="8fea9-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-203">System-Flags</span></span>           | <span data-ttu-id="8fea9-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-205">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fea9-205">Classes used in</span></span>        | [<span data-ttu-id="8fea9-206">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="8fea9-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="8fea9-207">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="8fea9-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8fea9-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fea9-208">Windows Server 2008</span></span>



| <span data-ttu-id="8fea9-209">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fea9-209">Entry</span></span> | <span data-ttu-id="8fea9-210">Valor</span><span class="sxs-lookup"><span data-stu-id="8fea9-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fea9-211">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fea9-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fea9-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fea9-213">System-Only</span></span>            | <span data-ttu-id="8fea9-214">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fea9-215">Is-Single-Valued</span></span>       | <span data-ttu-id="8fea9-216">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fea9-217">Is Indexed</span></span>             | <span data-ttu-id="8fea9-218">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fea9-219">In Global Catalog</span></span>      | <span data-ttu-id="8fea9-220">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fea9-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fea9-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fea9-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="8fea9-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fea9-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fea9-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-225">Search-Flags</span></span>           | <span data-ttu-id="8fea9-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-227">System-Flags</span></span>           | <span data-ttu-id="8fea9-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fea9-229">Classes used in</span></span>        | [<span data-ttu-id="8fea9-230">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="8fea9-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="8fea9-231">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="8fea9-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8fea9-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8fea9-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8fea9-233">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fea9-233">Entry</span></span> | <span data-ttu-id="8fea9-234">Valor</span><span class="sxs-lookup"><span data-stu-id="8fea9-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fea9-235">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fea9-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fea9-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fea9-237">System-Only</span></span>            | <span data-ttu-id="8fea9-238">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-239">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fea9-239">Is-Single-Valued</span></span>       | <span data-ttu-id="8fea9-240">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-241">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fea9-241">Is Indexed</span></span>             | <span data-ttu-id="8fea9-242">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-243">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fea9-243">In Global Catalog</span></span>      | <span data-ttu-id="8fea9-244">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-245">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fea9-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fea9-246">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fea9-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="8fea9-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fea9-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fea9-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-249">Search-Flags</span></span>           | <span data-ttu-id="8fea9-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-251">System-Flags</span></span>           | <span data-ttu-id="8fea9-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-253">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fea9-253">Classes used in</span></span>        | [<span data-ttu-id="8fea9-254">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="8fea9-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="8fea9-255">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="8fea9-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8fea9-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fea9-256">Windows Server 2012</span></span>



| <span data-ttu-id="8fea9-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fea9-257">Entry</span></span> | <span data-ttu-id="8fea9-258">Valor</span><span class="sxs-lookup"><span data-stu-id="8fea9-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fea9-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="8fea9-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8fea9-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="8fea9-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="8fea9-261">System-Only</span></span>            | <span data-ttu-id="8fea9-262">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8fea9-263">Is-Single-Valued</span></span>       | <span data-ttu-id="8fea9-264">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="8fea9-265">Is Indexed</span></span>             | <span data-ttu-id="8fea9-266">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8fea9-267">In Global Catalog</span></span>      | <span data-ttu-id="8fea9-268">Falso</span><span class="sxs-lookup"><span data-stu-id="8fea9-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="8fea9-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8fea9-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="8fea9-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8fea9-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="8fea9-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8fea9-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8fea9-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="8fea9-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-273">Search-Flags</span></span>           | <span data-ttu-id="8fea9-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8fea9-275">System-Flags</span></span>           | <span data-ttu-id="8fea9-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8fea9-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="8fea9-277">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8fea9-277">Classes used in</span></span>        | [<span data-ttu-id="8fea9-278">**Aplicativo-configurações**</span><span class="sxs-lookup"><span data-stu-id="8fea9-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="8fea9-279">**Ponto de conexão**</span><span class="sxs-lookup"><span data-stu-id="8fea9-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





