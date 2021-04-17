---
title: MSMQ-Digests atributo
description: Uma matriz de resumos dos certificados correspondentes no atributo mSMQ-Sign-Certificates. Eles são usados para mapear um resumo em um certificado.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- Esquema de MSMQ-Digests do atributo AD
- Esquema de AD do atributo mSMQDigests
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755891"
---
# <a name="msmq-digests-attribute"></a><span data-ttu-id="a8597-106">MSMQ-Digests atributo</span><span class="sxs-lookup"><span data-stu-id="a8597-106">MSMQ-Digests attribute</span></span>

<span data-ttu-id="a8597-107">Uma matriz de resumos dos certificados correspondentes no atributo mSMQ-Sign-Certificates.</span><span class="sxs-lookup"><span data-stu-id="a8597-107">An array of digests of the corresponding certificates in attribute mSMQ-Sign-Certificates.</span></span> <span data-ttu-id="a8597-108">Eles são usados para mapear um resumo em um certificado.</span><span class="sxs-lookup"><span data-stu-id="a8597-108">They are used for mapping a digest into a certificate.</span></span>



| <span data-ttu-id="a8597-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8597-109">Entry</span></span> | <span data-ttu-id="a8597-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a8597-111">CN</span><span class="sxs-lookup"><span data-stu-id="a8597-111">CN</span></span>                | <span data-ttu-id="a8597-112">MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="a8597-112">MSMQ-Digests</span></span>                                          |
| <span data-ttu-id="a8597-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a8597-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a8597-114">mSMQDigests</span><span class="sxs-lookup"><span data-stu-id="a8597-114">mSMQDigests</span></span>                                           |
| <span data-ttu-id="a8597-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a8597-115">Size</span></span>              | <span data-ttu-id="a8597-116">Cada resumo é 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="a8597-116">Each digest is 16 bytes.</span></span>                              |
| <span data-ttu-id="a8597-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a8597-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="a8597-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a8597-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="a8597-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a8597-119">Attribute-Id</span></span>      | <span data-ttu-id="a8597-120">1.2.840.113556.1.4.948</span><span class="sxs-lookup"><span data-stu-id="a8597-120">1.2.840.113556.1.4.948</span></span>                                |
| <span data-ttu-id="a8597-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a8597-121">System-Id-Guid</span></span>    | <span data-ttu-id="a8597-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="a8597-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="a8597-123">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8597-123">Syntax</span></span>            | [<span data-ttu-id="a8597-124">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="a8597-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="a8597-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="a8597-125">Implementations</span></span>

-   [<span data-ttu-id="a8597-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a8597-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a8597-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a8597-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a8597-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a8597-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a8597-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a8597-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a8597-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a8597-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a8597-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a8597-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a8597-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a8597-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a8597-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8597-133">Entry</span></span> | <span data-ttu-id="a8597-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8597-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="a8597-135">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8597-136">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8597-137">System-Only</span></span>            | <span data-ttu-id="a8597-138">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-138">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a8597-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a8597-140">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-140">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="a8597-141">Is Indexed</span></span>             | <span data-ttu-id="a8597-142">True</span><span class="sxs-lookup"><span data-stu-id="a8597-142">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a8597-143">In Global Catalog</span></span>      | <span data-ttu-id="a8597-144">True</span><span class="sxs-lookup"><span data-stu-id="a8597-144">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8597-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8597-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a8597-146">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="a8597-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8597-147">Range-Lower</span></span>            | <span data-ttu-id="a8597-148">16</span><span class="sxs-lookup"><span data-stu-id="a8597-148">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8597-149">Range-Upper</span></span>            | <span data-ttu-id="a8597-150">16</span><span class="sxs-lookup"><span data-stu-id="a8597-150">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-151">Search-Flags</span></span>           | <span data-ttu-id="a8597-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8597-152">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="a8597-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-153">System-Flags</span></span>           | <span data-ttu-id="a8597-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8597-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="a8597-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a8597-155">Classes used in</span></span>        | [<span data-ttu-id="a8597-156">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="a8597-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a8597-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8597-158">Windows Server 2003</span></span>



| <span data-ttu-id="a8597-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8597-159">Entry</span></span> | <span data-ttu-id="a8597-160">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8597-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="a8597-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8597-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8597-163">System-Only</span></span>            | <span data-ttu-id="a8597-164">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-164">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a8597-165">Is-Single-Valued</span></span>       | <span data-ttu-id="a8597-166">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-166">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="a8597-167">Is Indexed</span></span>             | <span data-ttu-id="a8597-168">True</span><span class="sxs-lookup"><span data-stu-id="a8597-168">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a8597-169">In Global Catalog</span></span>      | <span data-ttu-id="a8597-170">True</span><span class="sxs-lookup"><span data-stu-id="a8597-170">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8597-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8597-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a8597-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="a8597-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8597-173">Range-Lower</span></span>            | <span data-ttu-id="a8597-174">16</span><span class="sxs-lookup"><span data-stu-id="a8597-174">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8597-175">Range-Upper</span></span>            | <span data-ttu-id="a8597-176">16</span><span class="sxs-lookup"><span data-stu-id="a8597-176">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-177">Search-Flags</span></span>           | <span data-ttu-id="a8597-178">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8597-178">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="a8597-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-179">System-Flags</span></span>           | <span data-ttu-id="a8597-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8597-180">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="a8597-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a8597-181">Classes used in</span></span>        | [<span data-ttu-id="a8597-182">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-182">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="a8597-183">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a8597-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a8597-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a8597-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8597-185">Entry</span></span> | <span data-ttu-id="a8597-186">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-186">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8597-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="a8597-187">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8597-188">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8597-189">System-Only</span></span>            | <span data-ttu-id="a8597-190">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-190">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a8597-191">Is-Single-Valued</span></span>       | <span data-ttu-id="a8597-192">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-192">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="a8597-193">Is Indexed</span></span>             | <span data-ttu-id="a8597-194">True</span><span class="sxs-lookup"><span data-stu-id="a8597-194">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a8597-195">In Global Catalog</span></span>      | <span data-ttu-id="a8597-196">True</span><span class="sxs-lookup"><span data-stu-id="a8597-196">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8597-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8597-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a8597-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="a8597-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8597-199">Range-Lower</span></span>            | <span data-ttu-id="a8597-200">16</span><span class="sxs-lookup"><span data-stu-id="a8597-200">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8597-201">Range-Upper</span></span>            | <span data-ttu-id="a8597-202">16</span><span class="sxs-lookup"><span data-stu-id="a8597-202">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-203">Search-Flags</span></span>           | <span data-ttu-id="a8597-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8597-204">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="a8597-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-205">System-Flags</span></span>           | <span data-ttu-id="a8597-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8597-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="a8597-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a8597-207">Classes used in</span></span>        | [<span data-ttu-id="a8597-208">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-208">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="a8597-209">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a8597-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8597-210">Windows Server 2008</span></span>



| <span data-ttu-id="a8597-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8597-211">Entry</span></span> | <span data-ttu-id="a8597-212">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8597-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="a8597-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8597-214">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8597-215">System-Only</span></span>            | <span data-ttu-id="a8597-216">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-216">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a8597-217">Is-Single-Valued</span></span>       | <span data-ttu-id="a8597-218">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-218">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="a8597-219">Is Indexed</span></span>             | <span data-ttu-id="a8597-220">True</span><span class="sxs-lookup"><span data-stu-id="a8597-220">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a8597-221">In Global Catalog</span></span>      | <span data-ttu-id="a8597-222">True</span><span class="sxs-lookup"><span data-stu-id="a8597-222">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8597-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8597-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a8597-224">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="a8597-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8597-225">Range-Lower</span></span>            | <span data-ttu-id="a8597-226">16</span><span class="sxs-lookup"><span data-stu-id="a8597-226">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8597-227">Range-Upper</span></span>            | <span data-ttu-id="a8597-228">16</span><span class="sxs-lookup"><span data-stu-id="a8597-228">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-229">Search-Flags</span></span>           | <span data-ttu-id="a8597-230">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8597-230">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="a8597-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-231">System-Flags</span></span>           | <span data-ttu-id="a8597-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8597-232">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="a8597-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a8597-233">Classes used in</span></span>        | [<span data-ttu-id="a8597-234">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-234">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="a8597-235">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-235">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a8597-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8597-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a8597-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8597-237">Entry</span></span> | <span data-ttu-id="a8597-238">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8597-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="a8597-239">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8597-240">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8597-241">System-Only</span></span>            | <span data-ttu-id="a8597-242">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-242">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-243">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a8597-243">Is-Single-Valued</span></span>       | <span data-ttu-id="a8597-244">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-244">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-245">É indexado</span><span class="sxs-lookup"><span data-stu-id="a8597-245">Is Indexed</span></span>             | <span data-ttu-id="a8597-246">True</span><span class="sxs-lookup"><span data-stu-id="a8597-246">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-247">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a8597-247">In Global Catalog</span></span>      | <span data-ttu-id="a8597-248">True</span><span class="sxs-lookup"><span data-stu-id="a8597-248">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8597-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8597-250">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a8597-250">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="a8597-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8597-251">Range-Lower</span></span>            | <span data-ttu-id="a8597-252">16</span><span class="sxs-lookup"><span data-stu-id="a8597-252">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8597-253">Range-Upper</span></span>            | <span data-ttu-id="a8597-254">16</span><span class="sxs-lookup"><span data-stu-id="a8597-254">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-255">Search-Flags</span></span>           | <span data-ttu-id="a8597-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8597-256">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="a8597-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-257">System-Flags</span></span>           | <span data-ttu-id="a8597-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8597-258">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="a8597-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a8597-259">Classes used in</span></span>        | [<span data-ttu-id="a8597-260">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-260">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="a8597-261">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-261">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a8597-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8597-262">Windows Server 2012</span></span>



| <span data-ttu-id="a8597-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="a8597-263">Entry</span></span> | <span data-ttu-id="a8597-264">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8597-265">ID do link</span><span class="sxs-lookup"><span data-stu-id="a8597-265">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a8597-266">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="a8597-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="a8597-267">System-Only</span></span>            | <span data-ttu-id="a8597-268">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-268">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-269">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a8597-269">Is-Single-Valued</span></span>       | <span data-ttu-id="a8597-270">Falso</span><span class="sxs-lookup"><span data-stu-id="a8597-270">False</span></span>                                                                                         |
| <span data-ttu-id="a8597-271">É indexado</span><span class="sxs-lookup"><span data-stu-id="a8597-271">Is Indexed</span></span>             | <span data-ttu-id="a8597-272">True</span><span class="sxs-lookup"><span data-stu-id="a8597-272">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-273">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a8597-273">In Global Catalog</span></span>      | <span data-ttu-id="a8597-274">True</span><span class="sxs-lookup"><span data-stu-id="a8597-274">True</span></span>                                                                                          |
| <span data-ttu-id="a8597-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a8597-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="a8597-276">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a8597-276">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="a8597-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a8597-277">Range-Lower</span></span>            | <span data-ttu-id="a8597-278">16</span><span class="sxs-lookup"><span data-stu-id="a8597-278">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a8597-279">Range-Upper</span></span>            | <span data-ttu-id="a8597-280">16</span><span class="sxs-lookup"><span data-stu-id="a8597-280">16</span></span>                                                                                            |
| <span data-ttu-id="a8597-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-281">Search-Flags</span></span>           | <span data-ttu-id="a8597-282">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a8597-282">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="a8597-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a8597-283">System-Flags</span></span>           | <span data-ttu-id="a8597-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a8597-284">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="a8597-285">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a8597-285">Classes used in</span></span>        | [<span data-ttu-id="a8597-286">**MSMQ-migrado-usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-286">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="a8597-287">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a8597-287">**User**</span></span>](c-user.md)<br/> |



 

 





