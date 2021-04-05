---
title: MS-DS-Machine-Account-atributo quota
description: O número de contas de computador que um usuário tem permissão para criar em um domínio.
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- MS-DS-Machine-Account-quota atributo AD Schema
- Esquema de AD do atributo ms-DS-MachineAccountQuota
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86de012aa876e5a0d52ac866048801872a365f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086953"
---
# <a name="ms-ds-machine-account-quota-attribute"></a><span data-ttu-id="691cf-105">MS-DS-Machine-Account-atributo quota</span><span class="sxs-lookup"><span data-stu-id="691cf-105">MS-DS-Machine-Account-Quota attribute</span></span>

<span data-ttu-id="691cf-106">O número de contas de computador que um usuário tem permissão para criar em um domínio.</span><span class="sxs-lookup"><span data-stu-id="691cf-106">The number of computer accounts that a user is allowed to create in a domain.</span></span>



| <span data-ttu-id="691cf-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="691cf-107">Entry</span></span> | <span data-ttu-id="691cf-108">Valor</span><span class="sxs-lookup"><span data-stu-id="691cf-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="691cf-109">CN</span><span class="sxs-lookup"><span data-stu-id="691cf-109">CN</span></span>                | <span data-ttu-id="691cf-110">MS-DS-Machine-Account-quota</span><span class="sxs-lookup"><span data-stu-id="691cf-110">MS-DS-Machine-Account-Quota</span></span>                      |
| <span data-ttu-id="691cf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="691cf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="691cf-112">ms-DS-MachineAccountQuota</span><span class="sxs-lookup"><span data-stu-id="691cf-112">ms-DS-MachineAccountQuota</span></span>                        |
| <span data-ttu-id="691cf-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="691cf-113">Size</span></span>              | <span data-ttu-id="691cf-114">4 bytes</span><span class="sxs-lookup"><span data-stu-id="691cf-114">4 bytes</span></span>                                          |
| <span data-ttu-id="691cf-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="691cf-115">Update Privilege</span></span>  | <span data-ttu-id="691cf-116">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="691cf-116">Domain administrator</span></span>                             |
| <span data-ttu-id="691cf-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="691cf-117">Update Frequency</span></span>  | <span data-ttu-id="691cf-118">Sempre que a cota de um domínio precisar ser alterada.</span><span class="sxs-lookup"><span data-stu-id="691cf-118">Whenever the quota for a domain needs to change.</span></span> |
| <span data-ttu-id="691cf-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="691cf-119">Attribute-Id</span></span>      | <span data-ttu-id="691cf-120">1.2.840.113556.1.4.1411</span><span class="sxs-lookup"><span data-stu-id="691cf-120">1.2.840.113556.1.4.1411</span></span>                          |
| <span data-ttu-id="691cf-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="691cf-121">System-Id-Guid</span></span>    | <span data-ttu-id="691cf-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="691cf-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span></span>             |
| <span data-ttu-id="691cf-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="691cf-123">Syntax</span></span>            | [<span data-ttu-id="691cf-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="691cf-124">**Enumeration**</span></span>](s-enumeration.md)             |



## <a name="implementations"></a><span data-ttu-id="691cf-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="691cf-125">Implementations</span></span>

-   [<span data-ttu-id="691cf-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="691cf-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="691cf-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="691cf-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="691cf-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="691cf-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="691cf-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="691cf-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="691cf-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="691cf-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="691cf-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="691cf-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="691cf-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="691cf-132">Windows 2000 Server</span></span>



| <span data-ttu-id="691cf-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="691cf-133">Entry</span></span> | <span data-ttu-id="691cf-134">Valor</span><span class="sxs-lookup"><span data-stu-id="691cf-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="691cf-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="691cf-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="691cf-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="691cf-137">System-Only</span></span>            | <span data-ttu-id="691cf-138">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-138">False</span></span>                                        |
| <span data-ttu-id="691cf-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="691cf-139">Is-Single-Valued</span></span>       | <span data-ttu-id="691cf-140">True</span><span class="sxs-lookup"><span data-stu-id="691cf-140">True</span></span>                                         |
| <span data-ttu-id="691cf-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="691cf-141">Is Indexed</span></span>             | <span data-ttu-id="691cf-142">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-142">False</span></span>                                        |
| <span data-ttu-id="691cf-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="691cf-143">In Global Catalog</span></span>      | <span data-ttu-id="691cf-144">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-144">False</span></span>                                        |
| <span data-ttu-id="691cf-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="691cf-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="691cf-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="691cf-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="691cf-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="691cf-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="691cf-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="691cf-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="691cf-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-149">Search-Flags</span></span>           | <span data-ttu-id="691cf-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="691cf-150">0x00000000</span></span>                                   |
| <span data-ttu-id="691cf-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-151">System-Flags</span></span>           | <span data-ttu-id="691cf-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="691cf-152">0x00000010</span></span>                                   |
| <span data-ttu-id="691cf-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="691cf-153">Classes used in</span></span>        | [<span data-ttu-id="691cf-154">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="691cf-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="691cf-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="691cf-155">Windows Server 2003</span></span>



| <span data-ttu-id="691cf-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="691cf-156">Entry</span></span> | <span data-ttu-id="691cf-157">Valor</span><span class="sxs-lookup"><span data-stu-id="691cf-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="691cf-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="691cf-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="691cf-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="691cf-160">System-Only</span></span>            | <span data-ttu-id="691cf-161">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-161">False</span></span>                                        |
| <span data-ttu-id="691cf-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="691cf-162">Is-Single-Valued</span></span>       | <span data-ttu-id="691cf-163">True</span><span class="sxs-lookup"><span data-stu-id="691cf-163">True</span></span>                                         |
| <span data-ttu-id="691cf-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="691cf-164">Is Indexed</span></span>             | <span data-ttu-id="691cf-165">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-165">False</span></span>                                        |
| <span data-ttu-id="691cf-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="691cf-166">In Global Catalog</span></span>      | <span data-ttu-id="691cf-167">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-167">False</span></span>                                        |
| <span data-ttu-id="691cf-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="691cf-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="691cf-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="691cf-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="691cf-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="691cf-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="691cf-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="691cf-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="691cf-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-172">Search-Flags</span></span>           | <span data-ttu-id="691cf-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="691cf-173">0x00000000</span></span>                                   |
| <span data-ttu-id="691cf-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-174">System-Flags</span></span>           | <span data-ttu-id="691cf-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="691cf-175">0x00000010</span></span>                                   |
| <span data-ttu-id="691cf-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="691cf-176">Classes used in</span></span>        | [<span data-ttu-id="691cf-177">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="691cf-177">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="691cf-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="691cf-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="691cf-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="691cf-179">Entry</span></span> | <span data-ttu-id="691cf-180">Valor</span><span class="sxs-lookup"><span data-stu-id="691cf-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="691cf-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="691cf-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="691cf-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="691cf-183">System-Only</span></span>            | <span data-ttu-id="691cf-184">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-184">False</span></span>                                        |
| <span data-ttu-id="691cf-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="691cf-185">Is-Single-Valued</span></span>       | <span data-ttu-id="691cf-186">True</span><span class="sxs-lookup"><span data-stu-id="691cf-186">True</span></span>                                         |
| <span data-ttu-id="691cf-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="691cf-187">Is Indexed</span></span>             | <span data-ttu-id="691cf-188">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-188">False</span></span>                                        |
| <span data-ttu-id="691cf-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="691cf-189">In Global Catalog</span></span>      | <span data-ttu-id="691cf-190">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-190">False</span></span>                                        |
| <span data-ttu-id="691cf-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="691cf-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="691cf-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="691cf-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="691cf-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="691cf-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="691cf-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="691cf-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="691cf-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-195">Search-Flags</span></span>           | <span data-ttu-id="691cf-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="691cf-196">0x00000000</span></span>                                   |
| <span data-ttu-id="691cf-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-197">System-Flags</span></span>           | <span data-ttu-id="691cf-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="691cf-198">0x00000010</span></span>                                   |
| <span data-ttu-id="691cf-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="691cf-199">Classes used in</span></span>        | [<span data-ttu-id="691cf-200">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="691cf-200">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="691cf-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="691cf-201">Windows Server 2008</span></span>



| <span data-ttu-id="691cf-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="691cf-202">Entry</span></span> | <span data-ttu-id="691cf-203">Valor</span><span class="sxs-lookup"><span data-stu-id="691cf-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="691cf-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="691cf-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="691cf-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="691cf-206">System-Only</span></span>            | <span data-ttu-id="691cf-207">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-207">False</span></span>                                        |
| <span data-ttu-id="691cf-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="691cf-208">Is-Single-Valued</span></span>       | <span data-ttu-id="691cf-209">True</span><span class="sxs-lookup"><span data-stu-id="691cf-209">True</span></span>                                         |
| <span data-ttu-id="691cf-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="691cf-210">Is Indexed</span></span>             | <span data-ttu-id="691cf-211">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-211">False</span></span>                                        |
| <span data-ttu-id="691cf-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="691cf-212">In Global Catalog</span></span>      | <span data-ttu-id="691cf-213">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-213">False</span></span>                                        |
| <span data-ttu-id="691cf-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="691cf-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="691cf-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="691cf-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="691cf-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="691cf-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="691cf-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="691cf-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="691cf-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-218">Search-Flags</span></span>           | <span data-ttu-id="691cf-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="691cf-219">0x00000000</span></span>                                   |
| <span data-ttu-id="691cf-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-220">System-Flags</span></span>           | <span data-ttu-id="691cf-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="691cf-221">0x00000010</span></span>                                   |
| <span data-ttu-id="691cf-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="691cf-222">Classes used in</span></span>        | [<span data-ttu-id="691cf-223">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="691cf-223">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="691cf-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="691cf-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="691cf-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="691cf-225">Entry</span></span> | <span data-ttu-id="691cf-226">Valor</span><span class="sxs-lookup"><span data-stu-id="691cf-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="691cf-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="691cf-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="691cf-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="691cf-229">System-Only</span></span>            | <span data-ttu-id="691cf-230">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-230">False</span></span>                                        |
| <span data-ttu-id="691cf-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="691cf-231">Is-Single-Valued</span></span>       | <span data-ttu-id="691cf-232">True</span><span class="sxs-lookup"><span data-stu-id="691cf-232">True</span></span>                                         |
| <span data-ttu-id="691cf-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="691cf-233">Is Indexed</span></span>             | <span data-ttu-id="691cf-234">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-234">False</span></span>                                        |
| <span data-ttu-id="691cf-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="691cf-235">In Global Catalog</span></span>      | <span data-ttu-id="691cf-236">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-236">False</span></span>                                        |
| <span data-ttu-id="691cf-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="691cf-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="691cf-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="691cf-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="691cf-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="691cf-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="691cf-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="691cf-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="691cf-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-241">Search-Flags</span></span>           | <span data-ttu-id="691cf-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="691cf-242">0x00000000</span></span>                                   |
| <span data-ttu-id="691cf-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-243">System-Flags</span></span>           | <span data-ttu-id="691cf-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="691cf-244">0x00000010</span></span>                                   |
| <span data-ttu-id="691cf-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="691cf-245">Classes used in</span></span>        | [<span data-ttu-id="691cf-246">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="691cf-246">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="691cf-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="691cf-247">Windows Server 2012</span></span>



| <span data-ttu-id="691cf-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="691cf-248">Entry</span></span> | <span data-ttu-id="691cf-249">Valor</span><span class="sxs-lookup"><span data-stu-id="691cf-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="691cf-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="691cf-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="691cf-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="691cf-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="691cf-252">System-Only</span></span>            | <span data-ttu-id="691cf-253">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-253">False</span></span>                                        |
| <span data-ttu-id="691cf-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="691cf-254">Is-Single-Valued</span></span>       | <span data-ttu-id="691cf-255">True</span><span class="sxs-lookup"><span data-stu-id="691cf-255">True</span></span>                                         |
| <span data-ttu-id="691cf-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="691cf-256">Is Indexed</span></span>             | <span data-ttu-id="691cf-257">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-257">False</span></span>                                        |
| <span data-ttu-id="691cf-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="691cf-258">In Global Catalog</span></span>      | <span data-ttu-id="691cf-259">Falso</span><span class="sxs-lookup"><span data-stu-id="691cf-259">False</span></span>                                        |
| <span data-ttu-id="691cf-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="691cf-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="691cf-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="691cf-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="691cf-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="691cf-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="691cf-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="691cf-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="691cf-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-264">Search-Flags</span></span>           | <span data-ttu-id="691cf-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="691cf-265">0x00000000</span></span>                                   |
| <span data-ttu-id="691cf-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="691cf-266">System-Flags</span></span>           | <span data-ttu-id="691cf-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="691cf-267">0x00000010</span></span>                                   |
| <span data-ttu-id="691cf-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="691cf-268">Classes used in</span></span>        | [<span data-ttu-id="691cf-269">**Sam-domínio**</span><span class="sxs-lookup"><span data-stu-id="691cf-269">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





