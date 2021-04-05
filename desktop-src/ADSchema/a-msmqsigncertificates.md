---
title: Atributo MSMQ-Sign-Certificates
description: Esse atributo contém um número de certificados. Um usuário pode gerar um certificado por computador. Para cada certificado, também mantemos um resumo.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Atributo AD do MSMQ-Sign-Certificates
- Esquema de AD do atributo mSMQSignCertificates
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825162"
---
# <a name="msmq-sign-certificates-attribute"></a><span data-ttu-id="aa71c-107">Atributo MSMQ-Sign-Certificates</span><span class="sxs-lookup"><span data-stu-id="aa71c-107">MSMQ-Sign-Certificates attribute</span></span>

<span data-ttu-id="aa71c-108">Esse atributo contém um número de certificados.</span><span class="sxs-lookup"><span data-stu-id="aa71c-108">This attribute contains a number of certificates.</span></span> <span data-ttu-id="aa71c-109">Um usuário pode gerar um certificado por computador.</span><span class="sxs-lookup"><span data-stu-id="aa71c-109">A user can generate a certificate per computer.</span></span> <span data-ttu-id="aa71c-110">Para cada certificado, também mantemos um resumo.</span><span class="sxs-lookup"><span data-stu-id="aa71c-110">For each certificate we also keep a digest.</span></span>



| <span data-ttu-id="aa71c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71c-111">Entry</span></span> | <span data-ttu-id="aa71c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="aa71c-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71c-113">CN</span><span class="sxs-lookup"><span data-stu-id="aa71c-113">CN</span></span>                | <span data-ttu-id="aa71c-114">MSMQ-assinar certificados</span><span class="sxs-lookup"><span data-stu-id="aa71c-114">MSMQ-Sign-Certificates</span></span>                                                                 |
| <span data-ttu-id="aa71c-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="aa71c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="aa71c-116">mSMQSignCertificates</span><span class="sxs-lookup"><span data-stu-id="aa71c-116">mSMQSignCertificates</span></span>                                                                   |
| <span data-ttu-id="aa71c-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="aa71c-117">Size</span></span>              | <span data-ttu-id="aa71c-118">O tipo de atributo é um BLOB, o tamanho não é limitado e os dados são mantidos em nosso próprio formato.</span><span class="sxs-lookup"><span data-stu-id="aa71c-118">The attribute type is a BLOB, size is not limited, and data is kept in our own format.</span></span> |
| <span data-ttu-id="aa71c-119">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="aa71c-119">Update Privilege</span></span>  | \-                                                                                     |
| <span data-ttu-id="aa71c-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="aa71c-120">Update Frequency</span></span>  | \-                                                                                     |
| <span data-ttu-id="aa71c-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="aa71c-121">Attribute-Id</span></span>      | <span data-ttu-id="aa71c-122">1.2.840.113556.1.4.947</span><span class="sxs-lookup"><span data-stu-id="aa71c-122">1.2.840.113556.1.4.947</span></span>                                                                 |
| <span data-ttu-id="aa71c-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="aa71c-123">System-Id-Guid</span></span>    | <span data-ttu-id="aa71c-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="aa71c-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span></span>                                                   |
| <span data-ttu-id="aa71c-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa71c-125">Syntax</span></span>            | [<span data-ttu-id="aa71c-126">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="aa71c-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                  |



## <a name="implementations"></a><span data-ttu-id="aa71c-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="aa71c-127">Implementations</span></span>

-   [<span data-ttu-id="aa71c-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="aa71c-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="aa71c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="aa71c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="aa71c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="aa71c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="aa71c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="aa71c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="aa71c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="aa71c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="aa71c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="aa71c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="aa71c-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa71c-134">Windows 2000 Server</span></span>



| <span data-ttu-id="aa71c-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71c-135">Entry</span></span> | <span data-ttu-id="aa71c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="aa71c-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71c-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="aa71c-137">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa71c-138">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa71c-139">System-Only</span></span>            | <span data-ttu-id="aa71c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-140">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="aa71c-141">Is-Single-Valued</span></span>       | <span data-ttu-id="aa71c-142">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-142">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="aa71c-143">Is Indexed</span></span>             | <span data-ttu-id="aa71c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-144">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="aa71c-145">In Global Catalog</span></span>      | <span data-ttu-id="aa71c-146">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-146">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa71c-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa71c-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="aa71c-148">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="aa71c-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa71c-149">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa71c-150">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-151">Search-Flags</span></span>           | <span data-ttu-id="aa71c-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa71c-152">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="aa71c-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-153">System-Flags</span></span>           | <span data-ttu-id="aa71c-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa71c-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="aa71c-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="aa71c-155">Classes used in</span></span>        | [<span data-ttu-id="aa71c-156">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="aa71c-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="aa71c-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa71c-158">Windows Server 2003</span></span>



| <span data-ttu-id="aa71c-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71c-159">Entry</span></span> | <span data-ttu-id="aa71c-160">Valor</span><span class="sxs-lookup"><span data-stu-id="aa71c-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71c-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="aa71c-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa71c-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa71c-163">System-Only</span></span>            | <span data-ttu-id="aa71c-164">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-164">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="aa71c-165">Is-Single-Valued</span></span>       | <span data-ttu-id="aa71c-166">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-166">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="aa71c-167">Is Indexed</span></span>             | <span data-ttu-id="aa71c-168">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-168">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="aa71c-169">In Global Catalog</span></span>      | <span data-ttu-id="aa71c-170">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-170">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa71c-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa71c-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="aa71c-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="aa71c-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa71c-173">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa71c-174">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-175">Search-Flags</span></span>           | <span data-ttu-id="aa71c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa71c-176">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="aa71c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-177">System-Flags</span></span>           | <span data-ttu-id="aa71c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa71c-178">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="aa71c-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="aa71c-179">Classes used in</span></span>        | [<span data-ttu-id="aa71c-180">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-180">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="aa71c-181">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="aa71c-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="aa71c-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="aa71c-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71c-183">Entry</span></span> | <span data-ttu-id="aa71c-184">Valor</span><span class="sxs-lookup"><span data-stu-id="aa71c-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71c-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="aa71c-185">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa71c-186">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa71c-187">System-Only</span></span>            | <span data-ttu-id="aa71c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-188">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="aa71c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="aa71c-190">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-190">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="aa71c-191">Is Indexed</span></span>             | <span data-ttu-id="aa71c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-192">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="aa71c-193">In Global Catalog</span></span>      | <span data-ttu-id="aa71c-194">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-194">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa71c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa71c-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="aa71c-196">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="aa71c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa71c-197">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa71c-198">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-199">Search-Flags</span></span>           | <span data-ttu-id="aa71c-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa71c-200">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="aa71c-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-201">System-Flags</span></span>           | <span data-ttu-id="aa71c-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa71c-202">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="aa71c-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="aa71c-203">Classes used in</span></span>        | [<span data-ttu-id="aa71c-204">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-204">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="aa71c-205">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-205">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="aa71c-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa71c-206">Windows Server 2008</span></span>



| <span data-ttu-id="aa71c-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71c-207">Entry</span></span> | <span data-ttu-id="aa71c-208">Valor</span><span class="sxs-lookup"><span data-stu-id="aa71c-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71c-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="aa71c-209">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa71c-210">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa71c-211">System-Only</span></span>            | <span data-ttu-id="aa71c-212">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-212">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="aa71c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="aa71c-214">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-214">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="aa71c-215">Is Indexed</span></span>             | <span data-ttu-id="aa71c-216">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-216">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="aa71c-217">In Global Catalog</span></span>      | <span data-ttu-id="aa71c-218">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-218">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa71c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa71c-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="aa71c-220">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="aa71c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa71c-221">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa71c-222">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-223">Search-Flags</span></span>           | <span data-ttu-id="aa71c-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa71c-224">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="aa71c-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-225">System-Flags</span></span>           | <span data-ttu-id="aa71c-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa71c-226">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="aa71c-227">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="aa71c-227">Classes used in</span></span>        | [<span data-ttu-id="aa71c-228">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="aa71c-229">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="aa71c-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa71c-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="aa71c-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71c-231">Entry</span></span> | <span data-ttu-id="aa71c-232">Valor</span><span class="sxs-lookup"><span data-stu-id="aa71c-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71c-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="aa71c-233">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa71c-234">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa71c-235">System-Only</span></span>            | <span data-ttu-id="aa71c-236">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-236">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-237">É de valor único</span><span class="sxs-lookup"><span data-stu-id="aa71c-237">Is-Single-Valued</span></span>       | <span data-ttu-id="aa71c-238">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-238">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-239">É indexado</span><span class="sxs-lookup"><span data-stu-id="aa71c-239">Is Indexed</span></span>             | <span data-ttu-id="aa71c-240">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-240">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-241">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="aa71c-241">In Global Catalog</span></span>      | <span data-ttu-id="aa71c-242">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-242">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-243">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa71c-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa71c-244">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="aa71c-244">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="aa71c-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa71c-245">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa71c-246">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-247">Search-Flags</span></span>           | <span data-ttu-id="aa71c-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa71c-248">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="aa71c-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-249">System-Flags</span></span>           | <span data-ttu-id="aa71c-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa71c-250">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="aa71c-251">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="aa71c-251">Classes used in</span></span>        | [<span data-ttu-id="aa71c-252">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-252">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="aa71c-253">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-253">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="aa71c-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aa71c-254">Windows Server 2012</span></span>



| <span data-ttu-id="aa71c-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa71c-255">Entry</span></span> | <span data-ttu-id="aa71c-256">Valor</span><span class="sxs-lookup"><span data-stu-id="aa71c-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa71c-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="aa71c-257">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="aa71c-258">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="aa71c-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="aa71c-259">System-Only</span></span>            | <span data-ttu-id="aa71c-260">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-260">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-261">É de valor único</span><span class="sxs-lookup"><span data-stu-id="aa71c-261">Is-Single-Valued</span></span>       | <span data-ttu-id="aa71c-262">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-262">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-263">É indexado</span><span class="sxs-lookup"><span data-stu-id="aa71c-263">Is Indexed</span></span>             | <span data-ttu-id="aa71c-264">Falso</span><span class="sxs-lookup"><span data-stu-id="aa71c-264">False</span></span>                                                                                         |
| <span data-ttu-id="aa71c-265">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="aa71c-265">In Global Catalog</span></span>      | <span data-ttu-id="aa71c-266">True</span><span class="sxs-lookup"><span data-stu-id="aa71c-266">True</span></span>                                                                                          |
| <span data-ttu-id="aa71c-267">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="aa71c-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="aa71c-268">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="aa71c-268">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="aa71c-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="aa71c-269">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="aa71c-270">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="aa71c-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-271">Search-Flags</span></span>           | <span data-ttu-id="aa71c-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="aa71c-272">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="aa71c-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="aa71c-273">System-Flags</span></span>           | <span data-ttu-id="aa71c-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="aa71c-274">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="aa71c-275">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="aa71c-275">Classes used in</span></span>        | [<span data-ttu-id="aa71c-276">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-276">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="aa71c-277">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="aa71c-277">**User**</span></span>](c-user.md)<br/> |



 

 





