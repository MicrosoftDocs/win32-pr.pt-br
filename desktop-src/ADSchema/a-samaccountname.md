---
title: SAM-atributo de nome de conta
description: O nome de logon usado para dar suporte a clientes e servidores que executam versões anteriores do sistema operacional, como o Windows NT 4,0, o Windows 95, o Windows 98 e o LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- SAM-Account-Name atributo AD Schema
- Esquema do atributo do sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825278"
---
# <a name="sam-account-name-attribute"></a><span data-ttu-id="bb102-105">SAM-atributo de nome de conta</span><span class="sxs-lookup"><span data-stu-id="bb102-105">SAM-Account-Name attribute</span></span>

<span data-ttu-id="bb102-106">O nome de logon usado para dar suporte a clientes e servidores que executam versões anteriores do sistema operacional, como o Windows NT 4,0, o Windows 95, o Windows 98 e o LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="bb102-106">The logon name used to support clients and servers running earlier versions of the operating system, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span>

<span data-ttu-id="bb102-107">Esse atributo deve ter 20 caracteres ou menos para dar suporte a clientes anteriores e não pode conter nenhum destes caracteres:</span><span class="sxs-lookup"><span data-stu-id="bb102-107">This attribute must be 20 characters or less to support earlier clients, and cannot contain any of these characters:</span></span>

-   <span data-ttu-id="bb102-108">"/ \\ \[ \] : ; \| = , + \* ?</span><span class="sxs-lookup"><span data-stu-id="bb102-108">"/ \\ \[ \] : ; \| = , + \* ?</span></span> <span data-ttu-id="bb102-109">< ></span><span class="sxs-lookup"><span data-stu-id="bb102-109">< ></span></span>



| <span data-ttu-id="bb102-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb102-110">Entry</span></span> | <span data-ttu-id="bb102-111">Valor</span><span class="sxs-lookup"><span data-stu-id="bb102-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb102-112">CN</span><span class="sxs-lookup"><span data-stu-id="bb102-112">CN</span></span>                | <span data-ttu-id="bb102-113">SAM-Account-Name</span><span class="sxs-lookup"><span data-stu-id="bb102-113">SAM-Account-Name</span></span>                                                                         |
| <span data-ttu-id="bb102-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bb102-114">Ldap-Display-Name</span></span> | <span data-ttu-id="bb102-115">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="bb102-115">sAMAccountName</span></span>                                                                           |
| <span data-ttu-id="bb102-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bb102-116">Size</span></span>              | <span data-ttu-id="bb102-117">20 caracteres ou menos.</span><span class="sxs-lookup"><span data-stu-id="bb102-117">20 characters or less.</span></span>                                                                   |
| <span data-ttu-id="bb102-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bb102-118">Update Privilege</span></span>  | <span data-ttu-id="bb102-119">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="bb102-119">Domain administrator</span></span>                                                                     |
| <span data-ttu-id="bb102-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bb102-120">Update Frequency</span></span>  | <span data-ttu-id="bb102-121">Esse valor deve ser atribuído quando o registro de conta é criado e não deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="bb102-121">This value should be assigned when the account record is created, and should not change.</span></span> |
| <span data-ttu-id="bb102-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bb102-122">Attribute-Id</span></span>      | <span data-ttu-id="bb102-123">1.2.840.113556.1.4.221</span><span class="sxs-lookup"><span data-stu-id="bb102-123">1.2.840.113556.1.4.221</span></span>                                                                   |
| <span data-ttu-id="bb102-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bb102-124">System-Id-Guid</span></span>    | <span data-ttu-id="bb102-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="bb102-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span></span>                                                     |
| <span data-ttu-id="bb102-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb102-126">Syntax</span></span>            | [<span data-ttu-id="bb102-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bb102-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                              |



## <a name="implementations"></a><span data-ttu-id="bb102-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="bb102-128">Implementations</span></span>

-   [<span data-ttu-id="bb102-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bb102-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bb102-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bb102-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bb102-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bb102-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bb102-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bb102-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bb102-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bb102-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bb102-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bb102-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bb102-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb102-135">Windows 2000 Server</span></span>



| <span data-ttu-id="bb102-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb102-136">Entry</span></span> | <span data-ttu-id="bb102-137">Valor</span><span class="sxs-lookup"><span data-stu-id="bb102-137">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb102-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb102-138">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb102-139">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb102-140">System-Only</span></span>            | <span data-ttu-id="bb102-141">Falso</span><span class="sxs-lookup"><span data-stu-id="bb102-141">False</span></span>                                                        |
| <span data-ttu-id="bb102-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb102-142">Is-Single-Valued</span></span>       | <span data-ttu-id="bb102-143">True</span><span class="sxs-lookup"><span data-stu-id="bb102-143">True</span></span>                                                         |
| <span data-ttu-id="bb102-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb102-144">Is Indexed</span></span>             | <span data-ttu-id="bb102-145">True</span><span class="sxs-lookup"><span data-stu-id="bb102-145">True</span></span>                                                         |
| <span data-ttu-id="bb102-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb102-146">In Global Catalog</span></span>      | <span data-ttu-id="bb102-147">True</span><span class="sxs-lookup"><span data-stu-id="bb102-147">True</span></span>                                                         |
| <span data-ttu-id="bb102-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb102-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb102-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb102-149">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb102-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb102-150">Range-Lower</span></span>            | <span data-ttu-id="bb102-151">0</span><span class="sxs-lookup"><span data-stu-id="bb102-151">0</span></span>                                                            |
| <span data-ttu-id="bb102-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb102-152">Range-Upper</span></span>            | <span data-ttu-id="bb102-153">256</span><span class="sxs-lookup"><span data-stu-id="bb102-153">256</span></span>                                                          |
| <span data-ttu-id="bb102-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-154">Search-Flags</span></span>           | <span data-ttu-id="bb102-155">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb102-155">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb102-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-156">System-Flags</span></span>           | <span data-ttu-id="bb102-157">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb102-157">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb102-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb102-158">Classes used in</span></span>        | [<span data-ttu-id="bb102-159">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="bb102-159">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bb102-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb102-160">Windows Server 2003</span></span>



| <span data-ttu-id="bb102-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb102-161">Entry</span></span> | <span data-ttu-id="bb102-162">Valor</span><span class="sxs-lookup"><span data-stu-id="bb102-162">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb102-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb102-163">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb102-164">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb102-165">System-Only</span></span>            | <span data-ttu-id="bb102-166">Falso</span><span class="sxs-lookup"><span data-stu-id="bb102-166">False</span></span>                                                        |
| <span data-ttu-id="bb102-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb102-167">Is-Single-Valued</span></span>       | <span data-ttu-id="bb102-168">True</span><span class="sxs-lookup"><span data-stu-id="bb102-168">True</span></span>                                                         |
| <span data-ttu-id="bb102-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb102-169">Is Indexed</span></span>             | <span data-ttu-id="bb102-170">True</span><span class="sxs-lookup"><span data-stu-id="bb102-170">True</span></span>                                                         |
| <span data-ttu-id="bb102-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb102-171">In Global Catalog</span></span>      | <span data-ttu-id="bb102-172">True</span><span class="sxs-lookup"><span data-stu-id="bb102-172">True</span></span>                                                         |
| <span data-ttu-id="bb102-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb102-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb102-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb102-174">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb102-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb102-175">Range-Lower</span></span>            | <span data-ttu-id="bb102-176">0</span><span class="sxs-lookup"><span data-stu-id="bb102-176">0</span></span>                                                            |
| <span data-ttu-id="bb102-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb102-177">Range-Upper</span></span>            | <span data-ttu-id="bb102-178">256</span><span class="sxs-lookup"><span data-stu-id="bb102-178">256</span></span>                                                          |
| <span data-ttu-id="bb102-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-179">Search-Flags</span></span>           | <span data-ttu-id="bb102-180">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb102-180">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb102-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-181">System-Flags</span></span>           | <span data-ttu-id="bb102-182">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb102-182">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb102-183">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb102-183">Classes used in</span></span>        | [<span data-ttu-id="bb102-184">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="bb102-184">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bb102-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bb102-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bb102-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb102-186">Entry</span></span> | <span data-ttu-id="bb102-187">Valor</span><span class="sxs-lookup"><span data-stu-id="bb102-187">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb102-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb102-188">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb102-189">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb102-190">System-Only</span></span>            | <span data-ttu-id="bb102-191">Falso</span><span class="sxs-lookup"><span data-stu-id="bb102-191">False</span></span>                                                        |
| <span data-ttu-id="bb102-192">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb102-192">Is-Single-Valued</span></span>       | <span data-ttu-id="bb102-193">True</span><span class="sxs-lookup"><span data-stu-id="bb102-193">True</span></span>                                                         |
| <span data-ttu-id="bb102-194">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb102-194">Is Indexed</span></span>             | <span data-ttu-id="bb102-195">True</span><span class="sxs-lookup"><span data-stu-id="bb102-195">True</span></span>                                                         |
| <span data-ttu-id="bb102-196">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb102-196">In Global Catalog</span></span>      | <span data-ttu-id="bb102-197">True</span><span class="sxs-lookup"><span data-stu-id="bb102-197">True</span></span>                                                         |
| <span data-ttu-id="bb102-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb102-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb102-199">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb102-199">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb102-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb102-200">Range-Lower</span></span>            | <span data-ttu-id="bb102-201">0</span><span class="sxs-lookup"><span data-stu-id="bb102-201">0</span></span>                                                            |
| <span data-ttu-id="bb102-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb102-202">Range-Upper</span></span>            | <span data-ttu-id="bb102-203">256</span><span class="sxs-lookup"><span data-stu-id="bb102-203">256</span></span>                                                          |
| <span data-ttu-id="bb102-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-204">Search-Flags</span></span>           | <span data-ttu-id="bb102-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb102-205">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb102-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-206">System-Flags</span></span>           | <span data-ttu-id="bb102-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb102-207">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb102-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb102-208">Classes used in</span></span>        | [<span data-ttu-id="bb102-209">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="bb102-209">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bb102-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb102-210">Windows Server 2008</span></span>



| <span data-ttu-id="bb102-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb102-211">Entry</span></span> | <span data-ttu-id="bb102-212">Valor</span><span class="sxs-lookup"><span data-stu-id="bb102-212">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb102-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb102-213">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb102-214">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb102-215">System-Only</span></span>            | <span data-ttu-id="bb102-216">Falso</span><span class="sxs-lookup"><span data-stu-id="bb102-216">False</span></span>                                                        |
| <span data-ttu-id="bb102-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb102-217">Is-Single-Valued</span></span>       | <span data-ttu-id="bb102-218">True</span><span class="sxs-lookup"><span data-stu-id="bb102-218">True</span></span>                                                         |
| <span data-ttu-id="bb102-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb102-219">Is Indexed</span></span>             | <span data-ttu-id="bb102-220">True</span><span class="sxs-lookup"><span data-stu-id="bb102-220">True</span></span>                                                         |
| <span data-ttu-id="bb102-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb102-221">In Global Catalog</span></span>      | <span data-ttu-id="bb102-222">True</span><span class="sxs-lookup"><span data-stu-id="bb102-222">True</span></span>                                                         |
| <span data-ttu-id="bb102-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb102-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb102-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb102-224">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb102-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb102-225">Range-Lower</span></span>            | <span data-ttu-id="bb102-226">0</span><span class="sxs-lookup"><span data-stu-id="bb102-226">0</span></span>                                                            |
| <span data-ttu-id="bb102-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb102-227">Range-Upper</span></span>            | <span data-ttu-id="bb102-228">256</span><span class="sxs-lookup"><span data-stu-id="bb102-228">256</span></span>                                                          |
| <span data-ttu-id="bb102-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-229">Search-Flags</span></span>           | <span data-ttu-id="bb102-230">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb102-230">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb102-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-231">System-Flags</span></span>           | <span data-ttu-id="bb102-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb102-232">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb102-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb102-233">Classes used in</span></span>        | [<span data-ttu-id="bb102-234">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="bb102-234">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bb102-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb102-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bb102-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb102-236">Entry</span></span> | <span data-ttu-id="bb102-237">Valor</span><span class="sxs-lookup"><span data-stu-id="bb102-237">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb102-238">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb102-238">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb102-239">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb102-240">System-Only</span></span>            | <span data-ttu-id="bb102-241">Falso</span><span class="sxs-lookup"><span data-stu-id="bb102-241">False</span></span>                                                        |
| <span data-ttu-id="bb102-242">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb102-242">Is-Single-Valued</span></span>       | <span data-ttu-id="bb102-243">True</span><span class="sxs-lookup"><span data-stu-id="bb102-243">True</span></span>                                                         |
| <span data-ttu-id="bb102-244">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb102-244">Is Indexed</span></span>             | <span data-ttu-id="bb102-245">True</span><span class="sxs-lookup"><span data-stu-id="bb102-245">True</span></span>                                                         |
| <span data-ttu-id="bb102-246">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb102-246">In Global Catalog</span></span>      | <span data-ttu-id="bb102-247">True</span><span class="sxs-lookup"><span data-stu-id="bb102-247">True</span></span>                                                         |
| <span data-ttu-id="bb102-248">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb102-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb102-249">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb102-249">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb102-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb102-250">Range-Lower</span></span>            | <span data-ttu-id="bb102-251">0</span><span class="sxs-lookup"><span data-stu-id="bb102-251">0</span></span>                                                            |
| <span data-ttu-id="bb102-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb102-252">Range-Upper</span></span>            | <span data-ttu-id="bb102-253">256</span><span class="sxs-lookup"><span data-stu-id="bb102-253">256</span></span>                                                          |
| <span data-ttu-id="bb102-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-254">Search-Flags</span></span>           | <span data-ttu-id="bb102-255">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb102-255">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb102-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-256">System-Flags</span></span>           | <span data-ttu-id="bb102-257">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb102-257">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb102-258">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb102-258">Classes used in</span></span>        | [<span data-ttu-id="bb102-259">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="bb102-259">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bb102-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bb102-260">Windows Server 2012</span></span>



| <span data-ttu-id="bb102-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="bb102-261">Entry</span></span> | <span data-ttu-id="bb102-262">Valor</span><span class="sxs-lookup"><span data-stu-id="bb102-262">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="bb102-263">ID do link</span><span class="sxs-lookup"><span data-stu-id="bb102-263">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bb102-264">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="bb102-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="bb102-265">System-Only</span></span>            | <span data-ttu-id="bb102-266">Falso</span><span class="sxs-lookup"><span data-stu-id="bb102-266">False</span></span>                                                        |
| <span data-ttu-id="bb102-267">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bb102-267">Is-Single-Valued</span></span>       | <span data-ttu-id="bb102-268">True</span><span class="sxs-lookup"><span data-stu-id="bb102-268">True</span></span>                                                         |
| <span data-ttu-id="bb102-269">É indexado</span><span class="sxs-lookup"><span data-stu-id="bb102-269">Is Indexed</span></span>             | <span data-ttu-id="bb102-270">True</span><span class="sxs-lookup"><span data-stu-id="bb102-270">True</span></span>                                                         |
| <span data-ttu-id="bb102-271">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bb102-271">In Global Catalog</span></span>      | <span data-ttu-id="bb102-272">True</span><span class="sxs-lookup"><span data-stu-id="bb102-272">True</span></span>                                                         |
| <span data-ttu-id="bb102-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bb102-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="bb102-274">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bb102-274">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="bb102-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bb102-275">Range-Lower</span></span>            | <span data-ttu-id="bb102-276">0</span><span class="sxs-lookup"><span data-stu-id="bb102-276">0</span></span>                                                            |
| <span data-ttu-id="bb102-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bb102-277">Range-Upper</span></span>            | <span data-ttu-id="bb102-278">256</span><span class="sxs-lookup"><span data-stu-id="bb102-278">256</span></span>                                                          |
| <span data-ttu-id="bb102-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-279">Search-Flags</span></span>           | <span data-ttu-id="bb102-280">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="bb102-280">0x0000000D</span></span>                                                   |
| <span data-ttu-id="bb102-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bb102-281">System-Flags</span></span>           | <span data-ttu-id="bb102-282">0x00000012</span><span class="sxs-lookup"><span data-stu-id="bb102-282">0x00000012</span></span>                                                   |
| <span data-ttu-id="bb102-283">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bb102-283">Classes used in</span></span>        | [<span data-ttu-id="bb102-284">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="bb102-284">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





