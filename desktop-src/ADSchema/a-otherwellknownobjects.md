---
title: Outro atributo-well-known-Objects
description: Contém uma lista de contêineres por GUID e nome diferenciado. Isso permite recuperar um objeto depois que ele é movido usando apenas o GUID e o nome de domínio. Sempre que o objeto for movido, o sistema atualizará automaticamente o nome distinto.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Outro esquema do AD do atributo de objeto bem conhecido
- Esquema de AD do atributo otherWellKnownObjects
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d38b4f4b86f90368859f9fb966031f539f0399f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456261"
---
# <a name="other-well-known-objects-attribute"></a><span data-ttu-id="c5936-107">Outro atributo-well-known-Objects</span><span class="sxs-lookup"><span data-stu-id="c5936-107">Other-Well-Known-Objects attribute</span></span>

<span data-ttu-id="c5936-108">Contém uma lista de contêineres por GUID e nome diferenciado.</span><span class="sxs-lookup"><span data-stu-id="c5936-108">Contains a list of containers by GUID and Distinguished Name.</span></span> <span data-ttu-id="c5936-109">Isso permite recuperar um objeto depois que ele é movido usando apenas o GUID e o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="c5936-109">This permits retrieving an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="c5936-110">Sempre que o objeto for movido, o sistema atualizará automaticamente o nome distinto.</span><span class="sxs-lookup"><span data-stu-id="c5936-110">Whenever the object is moved, the system automatically updates the Distinguished Name.</span></span>



| <span data-ttu-id="c5936-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-111">Entry</span></span> | <span data-ttu-id="c5936-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5936-113">CN</span><span class="sxs-lookup"><span data-stu-id="c5936-113">CN</span></span>                | <span data-ttu-id="c5936-114">Outros objetos bem conhecidos</span><span class="sxs-lookup"><span data-stu-id="c5936-114">Other-Well-Known-Objects</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="c5936-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c5936-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c5936-116">otherWellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="c5936-116">otherWellKnownObjects</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="c5936-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c5936-117">Size</span></span>              | <span data-ttu-id="c5936-118">Exemplo para recuperar o contêiner de usuários no domínio da Microsoft: LDAP://(WKGUID = a9d1ca15768811d1aded00c04fd8d5cd, DC = Microsoft, DC = com).</span><span class="sxs-lookup"><span data-stu-id="c5936-118">Sample for retrieving the Users container in the microsoft domain: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com).</span></span> <span data-ttu-id="c5936-119">Observação: colchetes angulares substituídos por parênteses para evitar conflitos XML.</span><span class="sxs-lookup"><span data-stu-id="c5936-119">NOTE: Angle brackets replaced by parentheses to avoid XML conflicts.</span></span> |
| <span data-ttu-id="c5936-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c5936-120">Update Privilege</span></span>  | <span data-ttu-id="c5936-121">Administrador de esquema</span><span class="sxs-lookup"><span data-stu-id="c5936-121">Schema administrator</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c5936-122">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c5936-122">Update Frequency</span></span>  | <span data-ttu-id="c5936-123">Sempre que o objeto for movido.</span><span class="sxs-lookup"><span data-stu-id="c5936-123">Whenever the object is moved.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="c5936-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-124">Attribute-Id</span></span>      | <span data-ttu-id="c5936-125">1.2.840.113556.1.4.1359</span><span class="sxs-lookup"><span data-stu-id="c5936-125">1.2.840.113556.1.4.1359</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="c5936-126">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c5936-126">System-Id-Guid</span></span>    | <span data-ttu-id="c5936-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="c5936-127">1ea64e5d-ac0f-11d2-90df-00c04fd91ab1</span></span>                                                                                                                                                                          |
| <span data-ttu-id="c5936-128">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5936-128">Syntax</span></span>            | [<span data-ttu-id="c5936-129">**Objeto (DN-binário)**</span><span class="sxs-lookup"><span data-stu-id="c5936-129">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a><span data-ttu-id="c5936-130">Implementações</span><span class="sxs-lookup"><span data-stu-id="c5936-130">Implementations</span></span>

-   [<span data-ttu-id="c5936-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c5936-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c5936-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c5936-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c5936-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c5936-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c5936-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c5936-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c5936-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c5936-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c5936-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c5936-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c5936-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c5936-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c5936-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5936-138">Windows 2000 Server</span></span>



| <span data-ttu-id="c5936-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-139">Entry</span></span> | <span data-ttu-id="c5936-140">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-140">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5936-141">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5936-141">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-142">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5936-143">System-Only</span></span>            | <span data-ttu-id="c5936-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-144">False</span></span>                           |
| <span data-ttu-id="c5936-145">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5936-145">Is-Single-Valued</span></span>       | <span data-ttu-id="c5936-146">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-146">False</span></span>                           |
| <span data-ttu-id="c5936-147">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5936-147">Is Indexed</span></span>             | <span data-ttu-id="c5936-148">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-148">False</span></span>                           |
| <span data-ttu-id="c5936-149">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5936-149">In Global Catalog</span></span>      | <span data-ttu-id="c5936-150">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-150">False</span></span>                           |
| <span data-ttu-id="c5936-151">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5936-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5936-152">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5936-152">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5936-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5936-153">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c5936-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5936-154">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c5936-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-155">Search-Flags</span></span>           | <span data-ttu-id="c5936-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5936-156">0x00000000</span></span>                      |
| <span data-ttu-id="c5936-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-157">System-Flags</span></span>           | <span data-ttu-id="c5936-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5936-158">0x00000010</span></span>                      |
| <span data-ttu-id="c5936-159">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5936-159">Classes used in</span></span>        | [<span data-ttu-id="c5936-160">**Início**</span><span class="sxs-lookup"><span data-stu-id="c5936-160">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c5936-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c5936-161">Windows Server 2003</span></span>



| <span data-ttu-id="c5936-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-162">Entry</span></span> | <span data-ttu-id="c5936-163">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-163">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5936-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5936-164">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-165">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5936-166">System-Only</span></span>            | <span data-ttu-id="c5936-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-167">False</span></span>                           |
| <span data-ttu-id="c5936-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5936-168">Is-Single-Valued</span></span>       | <span data-ttu-id="c5936-169">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-169">False</span></span>                           |
| <span data-ttu-id="c5936-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5936-170">Is Indexed</span></span>             | <span data-ttu-id="c5936-171">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-171">False</span></span>                           |
| <span data-ttu-id="c5936-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5936-172">In Global Catalog</span></span>      | <span data-ttu-id="c5936-173">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-173">False</span></span>                           |
| <span data-ttu-id="c5936-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5936-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5936-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5936-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5936-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5936-176">Range-Lower</span></span>            | <span data-ttu-id="c5936-177">16</span><span class="sxs-lookup"><span data-stu-id="c5936-177">16</span></span>                              |
| <span data-ttu-id="c5936-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5936-178">Range-Upper</span></span>            | <span data-ttu-id="c5936-179">16</span><span class="sxs-lookup"><span data-stu-id="c5936-179">16</span></span>                              |
| <span data-ttu-id="c5936-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-180">Search-Flags</span></span>           | <span data-ttu-id="c5936-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5936-181">0x00000000</span></span>                      |
| <span data-ttu-id="c5936-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-182">System-Flags</span></span>           | <span data-ttu-id="c5936-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5936-183">0x00000010</span></span>                      |
| <span data-ttu-id="c5936-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5936-184">Classes used in</span></span>        | [<span data-ttu-id="c5936-185">**Início**</span><span class="sxs-lookup"><span data-stu-id="c5936-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c5936-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="c5936-186">ADAM</span></span>



| <span data-ttu-id="c5936-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-187">Entry</span></span> | <span data-ttu-id="c5936-188">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5936-189">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5936-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-190">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5936-191">System-Only</span></span>            | <span data-ttu-id="c5936-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-192">False</span></span>                           |
| <span data-ttu-id="c5936-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5936-193">Is-Single-Valued</span></span>       | <span data-ttu-id="c5936-194">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-194">False</span></span>                           |
| <span data-ttu-id="c5936-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5936-195">Is Indexed</span></span>             | <span data-ttu-id="c5936-196">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-196">False</span></span>                           |
| <span data-ttu-id="c5936-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5936-197">In Global Catalog</span></span>      | <span data-ttu-id="c5936-198">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-198">False</span></span>                           |
| <span data-ttu-id="c5936-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5936-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5936-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5936-200">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5936-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5936-201">Range-Lower</span></span>            | <span data-ttu-id="c5936-202">16</span><span class="sxs-lookup"><span data-stu-id="c5936-202">16</span></span>                              |
| <span data-ttu-id="c5936-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5936-203">Range-Upper</span></span>            | <span data-ttu-id="c5936-204">16</span><span class="sxs-lookup"><span data-stu-id="c5936-204">16</span></span>                              |
| <span data-ttu-id="c5936-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-205">Search-Flags</span></span>           | <span data-ttu-id="c5936-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5936-206">0x00000000</span></span>                      |
| <span data-ttu-id="c5936-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-207">System-Flags</span></span>           | <span data-ttu-id="c5936-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5936-208">0x00000010</span></span>                      |
| <span data-ttu-id="c5936-209">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5936-209">Classes used in</span></span>        | [<span data-ttu-id="c5936-210">**Início**</span><span class="sxs-lookup"><span data-stu-id="c5936-210">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c5936-211">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c5936-211">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c5936-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-212">Entry</span></span> | <span data-ttu-id="c5936-213">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-213">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5936-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5936-214">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-215">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5936-216">System-Only</span></span>            | <span data-ttu-id="c5936-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-217">False</span></span>                           |
| <span data-ttu-id="c5936-218">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5936-218">Is-Single-Valued</span></span>       | <span data-ttu-id="c5936-219">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-219">False</span></span>                           |
| <span data-ttu-id="c5936-220">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5936-220">Is Indexed</span></span>             | <span data-ttu-id="c5936-221">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-221">False</span></span>                           |
| <span data-ttu-id="c5936-222">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5936-222">In Global Catalog</span></span>      | <span data-ttu-id="c5936-223">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-223">False</span></span>                           |
| <span data-ttu-id="c5936-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5936-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5936-225">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5936-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5936-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5936-226">Range-Lower</span></span>            | <span data-ttu-id="c5936-227">16</span><span class="sxs-lookup"><span data-stu-id="c5936-227">16</span></span>                              |
| <span data-ttu-id="c5936-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5936-228">Range-Upper</span></span>            | <span data-ttu-id="c5936-229">16</span><span class="sxs-lookup"><span data-stu-id="c5936-229">16</span></span>                              |
| <span data-ttu-id="c5936-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-230">Search-Flags</span></span>           | <span data-ttu-id="c5936-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5936-231">0x00000000</span></span>                      |
| <span data-ttu-id="c5936-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-232">System-Flags</span></span>           | <span data-ttu-id="c5936-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5936-233">0x00000010</span></span>                      |
| <span data-ttu-id="c5936-234">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5936-234">Classes used in</span></span>        | [<span data-ttu-id="c5936-235">**Início**</span><span class="sxs-lookup"><span data-stu-id="c5936-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c5936-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5936-236">Windows Server 2008</span></span>



| <span data-ttu-id="c5936-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-237">Entry</span></span> | <span data-ttu-id="c5936-238">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5936-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5936-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-240">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5936-241">System-Only</span></span>            | <span data-ttu-id="c5936-242">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-242">False</span></span>                           |
| <span data-ttu-id="c5936-243">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5936-243">Is-Single-Valued</span></span>       | <span data-ttu-id="c5936-244">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-244">False</span></span>                           |
| <span data-ttu-id="c5936-245">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5936-245">Is Indexed</span></span>             | <span data-ttu-id="c5936-246">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-246">False</span></span>                           |
| <span data-ttu-id="c5936-247">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5936-247">In Global Catalog</span></span>      | <span data-ttu-id="c5936-248">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-248">False</span></span>                           |
| <span data-ttu-id="c5936-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5936-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5936-250">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5936-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5936-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5936-251">Range-Lower</span></span>            | <span data-ttu-id="c5936-252">16</span><span class="sxs-lookup"><span data-stu-id="c5936-252">16</span></span>                              |
| <span data-ttu-id="c5936-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5936-253">Range-Upper</span></span>            | <span data-ttu-id="c5936-254">16</span><span class="sxs-lookup"><span data-stu-id="c5936-254">16</span></span>                              |
| <span data-ttu-id="c5936-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-255">Search-Flags</span></span>           | <span data-ttu-id="c5936-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5936-256">0x00000000</span></span>                      |
| <span data-ttu-id="c5936-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-257">System-Flags</span></span>           | <span data-ttu-id="c5936-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5936-258">0x00000010</span></span>                      |
| <span data-ttu-id="c5936-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5936-259">Classes used in</span></span>        | [<span data-ttu-id="c5936-260">**Início**</span><span class="sxs-lookup"><span data-stu-id="c5936-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c5936-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c5936-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c5936-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-262">Entry</span></span> | <span data-ttu-id="c5936-263">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5936-264">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5936-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-265">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5936-266">System-Only</span></span>            | <span data-ttu-id="c5936-267">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-267">False</span></span>                           |
| <span data-ttu-id="c5936-268">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5936-268">Is-Single-Valued</span></span>       | <span data-ttu-id="c5936-269">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-269">False</span></span>                           |
| <span data-ttu-id="c5936-270">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5936-270">Is Indexed</span></span>             | <span data-ttu-id="c5936-271">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-271">False</span></span>                           |
| <span data-ttu-id="c5936-272">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5936-272">In Global Catalog</span></span>      | <span data-ttu-id="c5936-273">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-273">False</span></span>                           |
| <span data-ttu-id="c5936-274">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5936-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5936-275">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5936-275">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5936-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5936-276">Range-Lower</span></span>            | <span data-ttu-id="c5936-277">16</span><span class="sxs-lookup"><span data-stu-id="c5936-277">16</span></span>                              |
| <span data-ttu-id="c5936-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5936-278">Range-Upper</span></span>            | <span data-ttu-id="c5936-279">16</span><span class="sxs-lookup"><span data-stu-id="c5936-279">16</span></span>                              |
| <span data-ttu-id="c5936-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-280">Search-Flags</span></span>           | <span data-ttu-id="c5936-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5936-281">0x00000000</span></span>                      |
| <span data-ttu-id="c5936-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-282">System-Flags</span></span>           | <span data-ttu-id="c5936-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5936-283">0x00000010</span></span>                      |
| <span data-ttu-id="c5936-284">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5936-284">Classes used in</span></span>        | [<span data-ttu-id="c5936-285">**Início**</span><span class="sxs-lookup"><span data-stu-id="c5936-285">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c5936-286">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5936-286">Windows Server 2012</span></span>



| <span data-ttu-id="c5936-287">Entrada</span><span class="sxs-lookup"><span data-stu-id="c5936-287">Entry</span></span> | <span data-ttu-id="c5936-288">Valor</span><span class="sxs-lookup"><span data-stu-id="c5936-288">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c5936-289">ID do link</span><span class="sxs-lookup"><span data-stu-id="c5936-289">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-290">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c5936-290">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c5936-291">System-Only</span><span class="sxs-lookup"><span data-stu-id="c5936-291">System-Only</span></span>            | <span data-ttu-id="c5936-292">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-292">False</span></span>                           |
| <span data-ttu-id="c5936-293">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c5936-293">Is-Single-Valued</span></span>       | <span data-ttu-id="c5936-294">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-294">False</span></span>                           |
| <span data-ttu-id="c5936-295">É indexado</span><span class="sxs-lookup"><span data-stu-id="c5936-295">Is Indexed</span></span>             | <span data-ttu-id="c5936-296">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-296">False</span></span>                           |
| <span data-ttu-id="c5936-297">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c5936-297">In Global Catalog</span></span>      | <span data-ttu-id="c5936-298">Falso</span><span class="sxs-lookup"><span data-stu-id="c5936-298">False</span></span>                           |
| <span data-ttu-id="c5936-299">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c5936-299">NT-Security-Descriptor</span></span> | <span data-ttu-id="c5936-300">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c5936-300">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c5936-301">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c5936-301">Range-Lower</span></span>            | <span data-ttu-id="c5936-302">16</span><span class="sxs-lookup"><span data-stu-id="c5936-302">16</span></span>                              |
| <span data-ttu-id="c5936-303">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c5936-303">Range-Upper</span></span>            | <span data-ttu-id="c5936-304">16</span><span class="sxs-lookup"><span data-stu-id="c5936-304">16</span></span>                              |
| <span data-ttu-id="c5936-305">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-305">Search-Flags</span></span>           | <span data-ttu-id="c5936-306">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c5936-306">0x00000000</span></span>                      |
| <span data-ttu-id="c5936-307">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c5936-307">System-Flags</span></span>           | <span data-ttu-id="c5936-308">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c5936-308">0x00000010</span></span>                      |
| <span data-ttu-id="c5936-309">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c5936-309">Classes used in</span></span>        | [<span data-ttu-id="c5936-310">**Início**</span><span class="sxs-lookup"><span data-stu-id="c5936-310">**Top**</span></span>](c-top.md)<br/> |



 

 





