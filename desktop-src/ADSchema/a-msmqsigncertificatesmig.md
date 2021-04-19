---
title: MSMQ-Sign-Certificates-atributo MiG
description: No modo misto do MSMQ, o atributo contém o valor anterior de mSMQSignCertificates. O MSMQ dá suporte à migração do MSMQ 1,0 DS para o Windows 2000 DS e o modo misto especifica um estado no qual alguns dos servidores DS não foram atualizados para o Windows 2000.
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-Sign-Certificates-esquema do AD do atributo MiG
- Esquema de AD do atributo mSMQSignCertificatesMig
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749105"
---
# <a name="msmq-sign-certificates-mig-attribute"></a><span data-ttu-id="f8d24-106">MSMQ-Sign-Certificates-atributo MiG</span><span class="sxs-lookup"><span data-stu-id="f8d24-106">MSMQ-Sign-Certificates-Mig attribute</span></span>

<span data-ttu-id="f8d24-107">No modo misto do MSMQ, o atributo contém o valor anterior de mSMQSignCertificates.</span><span class="sxs-lookup"><span data-stu-id="f8d24-107">In MSMQ mixed-mode, the attribute contains the previous value of mSMQSignCertificates.</span></span> <span data-ttu-id="f8d24-108">O MSMQ dá suporte à migração do MSMQ 1,0 DS para o Windows 2000 DS e o modo misto especifica um estado no qual alguns dos servidores DS não foram atualizados para o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f8d24-108">MSMQ supports migration from the MSMQ 1.0 DS to the Windows 2000 DS, and mixed mode specifies a state in which some of the DS severs were not upgraded to Windows 2000.</span></span>



| <span data-ttu-id="f8d24-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d24-109">Entry</span></span> | <span data-ttu-id="f8d24-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f8d24-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f8d24-111">CN</span><span class="sxs-lookup"><span data-stu-id="f8d24-111">CN</span></span>                | <span data-ttu-id="f8d24-112">MSMQ-Sign-Certificates-MiG</span><span class="sxs-lookup"><span data-stu-id="f8d24-112">MSMQ-Sign-Certificates-Mig</span></span>                            |
| <span data-ttu-id="f8d24-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f8d24-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f8d24-114">mSMQSignCertificatesMig</span><span class="sxs-lookup"><span data-stu-id="f8d24-114">mSMQSignCertificatesMig</span></span>                               |
| <span data-ttu-id="f8d24-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f8d24-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f8d24-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f8d24-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f8d24-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f8d24-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f8d24-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f8d24-118">Attribute-Id</span></span>      | <span data-ttu-id="f8d24-119">1.2.840.113556.1.4.967</span><span class="sxs-lookup"><span data-stu-id="f8d24-119">1.2.840.113556.1.4.967</span></span>                                |
| <span data-ttu-id="f8d24-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f8d24-120">System-Id-Guid</span></span>    | <span data-ttu-id="f8d24-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="f8d24-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="f8d24-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8d24-122">Syntax</span></span>            | [<span data-ttu-id="f8d24-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="f8d24-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f8d24-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="f8d24-124">Implementations</span></span>

-   [<span data-ttu-id="f8d24-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f8d24-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f8d24-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f8d24-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f8d24-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f8d24-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f8d24-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f8d24-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f8d24-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f8d24-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f8d24-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f8d24-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f8d24-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f8d24-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f8d24-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d24-132">Entry</span></span> | <span data-ttu-id="f8d24-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f8d24-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d24-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8d24-134">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8d24-135">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8d24-136">System-Only</span></span>            | <span data-ttu-id="f8d24-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-137">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8d24-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f8d24-139">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-139">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8d24-140">Is Indexed</span></span>             | <span data-ttu-id="f8d24-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-141">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8d24-142">In Global Catalog</span></span>      | <span data-ttu-id="f8d24-143">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-143">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8d24-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8d24-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8d24-145">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="f8d24-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8d24-146">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8d24-147">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-148">Search-Flags</span></span>           | <span data-ttu-id="f8d24-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8d24-149">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="f8d24-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-150">System-Flags</span></span>           | <span data-ttu-id="f8d24-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8d24-151">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="f8d24-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8d24-152">Classes used in</span></span>        | [<span data-ttu-id="f8d24-153">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="f8d24-154">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f8d24-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8d24-155">Windows Server 2003</span></span>



| <span data-ttu-id="f8d24-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d24-156">Entry</span></span> | <span data-ttu-id="f8d24-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f8d24-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d24-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8d24-158">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8d24-159">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8d24-160">System-Only</span></span>            | <span data-ttu-id="f8d24-161">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-161">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8d24-162">Is-Single-Valued</span></span>       | <span data-ttu-id="f8d24-163">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-163">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8d24-164">Is Indexed</span></span>             | <span data-ttu-id="f8d24-165">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-165">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8d24-166">In Global Catalog</span></span>      | <span data-ttu-id="f8d24-167">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-167">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8d24-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8d24-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8d24-169">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="f8d24-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8d24-170">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8d24-171">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-172">Search-Flags</span></span>           | <span data-ttu-id="f8d24-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8d24-173">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="f8d24-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-174">System-Flags</span></span>           | <span data-ttu-id="f8d24-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8d24-175">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="f8d24-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8d24-176">Classes used in</span></span>        | [<span data-ttu-id="f8d24-177">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-177">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="f8d24-178">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f8d24-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f8d24-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f8d24-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d24-180">Entry</span></span> | <span data-ttu-id="f8d24-181">Valor</span><span class="sxs-lookup"><span data-stu-id="f8d24-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d24-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8d24-182">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8d24-183">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8d24-184">System-Only</span></span>            | <span data-ttu-id="f8d24-185">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-185">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8d24-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f8d24-187">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-187">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8d24-188">Is Indexed</span></span>             | <span data-ttu-id="f8d24-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-189">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8d24-190">In Global Catalog</span></span>      | <span data-ttu-id="f8d24-191">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-191">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8d24-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8d24-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8d24-193">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="f8d24-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8d24-194">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8d24-195">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-196">Search-Flags</span></span>           | <span data-ttu-id="f8d24-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8d24-197">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="f8d24-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-198">System-Flags</span></span>           | <span data-ttu-id="f8d24-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8d24-199">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="f8d24-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8d24-200">Classes used in</span></span>        | [<span data-ttu-id="f8d24-201">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-201">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="f8d24-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f8d24-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8d24-203">Windows Server 2008</span></span>



| <span data-ttu-id="f8d24-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d24-204">Entry</span></span> | <span data-ttu-id="f8d24-205">Valor</span><span class="sxs-lookup"><span data-stu-id="f8d24-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d24-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8d24-206">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8d24-207">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8d24-208">System-Only</span></span>            | <span data-ttu-id="f8d24-209">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-209">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8d24-210">Is-Single-Valued</span></span>       | <span data-ttu-id="f8d24-211">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-211">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8d24-212">Is Indexed</span></span>             | <span data-ttu-id="f8d24-213">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-213">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8d24-214">In Global Catalog</span></span>      | <span data-ttu-id="f8d24-215">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-215">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8d24-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8d24-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8d24-217">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="f8d24-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8d24-218">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8d24-219">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-220">Search-Flags</span></span>           | <span data-ttu-id="f8d24-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8d24-221">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="f8d24-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-222">System-Flags</span></span>           | <span data-ttu-id="f8d24-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8d24-223">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="f8d24-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8d24-224">Classes used in</span></span>        | [<span data-ttu-id="f8d24-225">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-225">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="f8d24-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f8d24-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8d24-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f8d24-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d24-228">Entry</span></span> | <span data-ttu-id="f8d24-229">Valor</span><span class="sxs-lookup"><span data-stu-id="f8d24-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d24-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8d24-230">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8d24-231">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8d24-232">System-Only</span></span>            | <span data-ttu-id="f8d24-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-233">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8d24-234">Is-Single-Valued</span></span>       | <span data-ttu-id="f8d24-235">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-235">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8d24-236">Is Indexed</span></span>             | <span data-ttu-id="f8d24-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-237">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8d24-238">In Global Catalog</span></span>      | <span data-ttu-id="f8d24-239">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-239">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8d24-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8d24-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8d24-241">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="f8d24-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8d24-242">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8d24-243">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-244">Search-Flags</span></span>           | <span data-ttu-id="f8d24-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8d24-245">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="f8d24-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-246">System-Flags</span></span>           | <span data-ttu-id="f8d24-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8d24-247">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="f8d24-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8d24-248">Classes used in</span></span>        | [<span data-ttu-id="f8d24-249">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-249">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="f8d24-250">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f8d24-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f8d24-251">Windows Server 2012</span></span>



| <span data-ttu-id="f8d24-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="f8d24-252">Entry</span></span> | <span data-ttu-id="f8d24-253">Valor</span><span class="sxs-lookup"><span data-stu-id="f8d24-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d24-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="f8d24-254">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f8d24-255">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="f8d24-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="f8d24-256">System-Only</span></span>            | <span data-ttu-id="f8d24-257">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-257">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f8d24-258">Is-Single-Valued</span></span>       | <span data-ttu-id="f8d24-259">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-259">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="f8d24-260">Is Indexed</span></span>             | <span data-ttu-id="f8d24-261">Falso</span><span class="sxs-lookup"><span data-stu-id="f8d24-261">False</span></span>                                                                                         |
| <span data-ttu-id="f8d24-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f8d24-262">In Global Catalog</span></span>      | <span data-ttu-id="f8d24-263">True</span><span class="sxs-lookup"><span data-stu-id="f8d24-263">True</span></span>                                                                                          |
| <span data-ttu-id="f8d24-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f8d24-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="f8d24-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f8d24-265">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="f8d24-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f8d24-266">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f8d24-267">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="f8d24-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-268">Search-Flags</span></span>           | <span data-ttu-id="f8d24-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f8d24-269">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="f8d24-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f8d24-270">System-Flags</span></span>           | <span data-ttu-id="f8d24-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f8d24-271">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="f8d24-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f8d24-272">Classes used in</span></span>        | [<span data-ttu-id="f8d24-273">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-273">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="f8d24-274">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f8d24-274">**User**</span></span>](c-user.md)<br/> |



 

 





