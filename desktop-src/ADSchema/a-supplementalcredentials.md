---
title: Supplemental-Credentials atributo
description: Credenciais armazenadas para uso na autenticação. A versão criptografada da senha do usuário. Esse atributo não é legível nem gravável.
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- Esquema de Supplemental-Credentials do atributo AD
- Esquema de AD do atributo supplementalCredentials
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19a73b3ae3cf19745fc995a59c336b72d264e78
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499950"
---
# <a name="supplemental-credentials-attribute"></a><span data-ttu-id="5c38c-107">Supplemental-Credentials atributo</span><span class="sxs-lookup"><span data-stu-id="5c38c-107">Supplemental-Credentials attribute</span></span>

<span data-ttu-id="5c38c-108">Credenciais armazenadas para uso na autenticação.</span><span class="sxs-lookup"><span data-stu-id="5c38c-108">Stored credentials for use in authenticating.</span></span> <span data-ttu-id="5c38c-109">A versão criptografada da senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c38c-109">The encrypted version of the user's password.</span></span> <span data-ttu-id="5c38c-110">Esse atributo não é legível nem gravável.</span><span class="sxs-lookup"><span data-stu-id="5c38c-110">This attribute is neither readable nor writable.</span></span>



| <span data-ttu-id="5c38c-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-111">Entry</span></span> | <span data-ttu-id="5c38c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="5c38c-113">CN</span><span class="sxs-lookup"><span data-stu-id="5c38c-113">CN</span></span>                | <span data-ttu-id="5c38c-114">Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="5c38c-114">Supplemental-Credentials</span></span>                              |
| <span data-ttu-id="5c38c-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5c38c-115">Ldap-Display-Name</span></span> | <span data-ttu-id="5c38c-116">supplementalCredentials</span><span class="sxs-lookup"><span data-stu-id="5c38c-116">supplementalCredentials</span></span>                               |
| <span data-ttu-id="5c38c-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5c38c-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="5c38c-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5c38c-118">Update Privilege</span></span>  | <span data-ttu-id="5c38c-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5c38c-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="5c38c-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5c38c-120">Update Frequency</span></span>  | <span data-ttu-id="5c38c-121">Quando a senha do usuário é alterada.</span><span class="sxs-lookup"><span data-stu-id="5c38c-121">When the user's password changes.</span></span>                     |
| <span data-ttu-id="5c38c-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-122">Attribute-Id</span></span>      | <span data-ttu-id="5c38c-123">1.2.840.113556.1.4.125</span><span class="sxs-lookup"><span data-stu-id="5c38c-123">1.2.840.113556.1.4.125</span></span>                                |
| <span data-ttu-id="5c38c-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5c38c-124">System-Id-Guid</span></span>    | <span data-ttu-id="5c38c-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5c38c-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="5c38c-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c38c-126">Syntax</span></span>            | [<span data-ttu-id="5c38c-127">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="5c38c-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="5c38c-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="5c38c-128">Implementations</span></span>

-   [<span data-ttu-id="5c38c-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5c38c-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5c38c-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5c38c-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5c38c-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5c38c-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5c38c-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5c38c-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5c38c-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5c38c-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5c38c-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5c38c-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5c38c-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5c38c-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5c38c-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c38c-136">Windows 2000 Server</span></span>



| <span data-ttu-id="5c38c-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-137">Entry</span></span> | <span data-ttu-id="5c38c-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-138">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c38c-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c38c-139">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-140">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c38c-141">System-Only</span></span>            | <span data-ttu-id="5c38c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-142">False</span></span>                                                        |
| <span data-ttu-id="5c38c-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c38c-143">Is-Single-Valued</span></span>       | <span data-ttu-id="5c38c-144">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-144">False</span></span>                                                        |
| <span data-ttu-id="5c38c-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c38c-145">Is Indexed</span></span>             | <span data-ttu-id="5c38c-146">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-146">False</span></span>                                                        |
| <span data-ttu-id="5c38c-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c38c-147">In Global Catalog</span></span>      | <span data-ttu-id="5c38c-148">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-148">False</span></span>                                                        |
| <span data-ttu-id="5c38c-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c38c-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c38c-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c38c-150">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5c38c-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c38c-151">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c38c-152">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-153">Search-Flags</span></span>           | <span data-ttu-id="5c38c-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c38c-154">0x00000000</span></span>                                                   |
| <span data-ttu-id="5c38c-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-155">System-Flags</span></span>           | <span data-ttu-id="5c38c-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c38c-156">0x00000010</span></span>                                                   |
| <span data-ttu-id="5c38c-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c38c-157">Classes used in</span></span>        | [<span data-ttu-id="5c38c-158">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="5c38c-158">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5c38c-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c38c-159">Windows Server 2003</span></span>



| <span data-ttu-id="5c38c-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-160">Entry</span></span> | <span data-ttu-id="5c38c-161">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-161">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c38c-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c38c-162">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-163">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c38c-164">System-Only</span></span>            | <span data-ttu-id="5c38c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-165">False</span></span>                                                        |
| <span data-ttu-id="5c38c-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c38c-166">Is-Single-Valued</span></span>       | <span data-ttu-id="5c38c-167">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-167">False</span></span>                                                        |
| <span data-ttu-id="5c38c-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c38c-168">Is Indexed</span></span>             | <span data-ttu-id="5c38c-169">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-169">False</span></span>                                                        |
| <span data-ttu-id="5c38c-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c38c-170">In Global Catalog</span></span>      | <span data-ttu-id="5c38c-171">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-171">False</span></span>                                                        |
| <span data-ttu-id="5c38c-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c38c-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c38c-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c38c-173">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5c38c-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c38c-174">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c38c-175">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-176">Search-Flags</span></span>           | <span data-ttu-id="5c38c-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c38c-177">0x00000000</span></span>                                                   |
| <span data-ttu-id="5c38c-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-178">System-Flags</span></span>           | <span data-ttu-id="5c38c-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c38c-179">0x00000010</span></span>                                                   |
| <span data-ttu-id="5c38c-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c38c-180">Classes used in</span></span>        | [<span data-ttu-id="5c38c-181">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="5c38c-181">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5c38c-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="5c38c-182">ADAM</span></span>



| <span data-ttu-id="5c38c-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-183">Entry</span></span> | <span data-ttu-id="5c38c-184">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-184">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c38c-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c38c-185">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-186">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c38c-187">System-Only</span></span>            | <span data-ttu-id="5c38c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-188">False</span></span>                                                        |
| <span data-ttu-id="5c38c-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c38c-189">Is-Single-Valued</span></span>       | <span data-ttu-id="5c38c-190">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-190">False</span></span>                                                        |
| <span data-ttu-id="5c38c-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c38c-191">Is Indexed</span></span>             | <span data-ttu-id="5c38c-192">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-192">False</span></span>                                                        |
| <span data-ttu-id="5c38c-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c38c-193">In Global Catalog</span></span>      | <span data-ttu-id="5c38c-194">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-194">False</span></span>                                                        |
| <span data-ttu-id="5c38c-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c38c-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c38c-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c38c-196">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5c38c-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c38c-197">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c38c-198">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-199">Search-Flags</span></span>           | <span data-ttu-id="5c38c-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c38c-200">0x00000000</span></span>                                                   |
| <span data-ttu-id="5c38c-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-201">System-Flags</span></span>           | <span data-ttu-id="5c38c-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c38c-202">0x00000010</span></span>                                                   |
| <span data-ttu-id="5c38c-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c38c-203">Classes used in</span></span>        | [<span data-ttu-id="5c38c-204">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="5c38c-204">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5c38c-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5c38c-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5c38c-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-206">Entry</span></span> | <span data-ttu-id="5c38c-207">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-207">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c38c-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c38c-208">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-209">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c38c-210">System-Only</span></span>            | <span data-ttu-id="5c38c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-211">False</span></span>                                                        |
| <span data-ttu-id="5c38c-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c38c-212">Is-Single-Valued</span></span>       | <span data-ttu-id="5c38c-213">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-213">False</span></span>                                                        |
| <span data-ttu-id="5c38c-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c38c-214">Is Indexed</span></span>             | <span data-ttu-id="5c38c-215">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-215">False</span></span>                                                        |
| <span data-ttu-id="5c38c-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c38c-216">In Global Catalog</span></span>      | <span data-ttu-id="5c38c-217">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-217">False</span></span>                                                        |
| <span data-ttu-id="5c38c-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c38c-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c38c-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c38c-219">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5c38c-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c38c-220">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c38c-221">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-222">Search-Flags</span></span>           | <span data-ttu-id="5c38c-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c38c-223">0x00000000</span></span>                                                   |
| <span data-ttu-id="5c38c-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-224">System-Flags</span></span>           | <span data-ttu-id="5c38c-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c38c-225">0x00000010</span></span>                                                   |
| <span data-ttu-id="5c38c-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c38c-226">Classes used in</span></span>        | [<span data-ttu-id="5c38c-227">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="5c38c-227">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5c38c-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c38c-228">Windows Server 2008</span></span>



| <span data-ttu-id="5c38c-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-229">Entry</span></span> | <span data-ttu-id="5c38c-230">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-230">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c38c-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c38c-231">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-232">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c38c-233">System-Only</span></span>            | <span data-ttu-id="5c38c-234">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-234">False</span></span>                                                        |
| <span data-ttu-id="5c38c-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c38c-235">Is-Single-Valued</span></span>       | <span data-ttu-id="5c38c-236">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-236">False</span></span>                                                        |
| <span data-ttu-id="5c38c-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c38c-237">Is Indexed</span></span>             | <span data-ttu-id="5c38c-238">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-238">False</span></span>                                                        |
| <span data-ttu-id="5c38c-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c38c-239">In Global Catalog</span></span>      | <span data-ttu-id="5c38c-240">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-240">False</span></span>                                                        |
| <span data-ttu-id="5c38c-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c38c-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c38c-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c38c-242">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5c38c-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c38c-243">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c38c-244">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-245">Search-Flags</span></span>           | <span data-ttu-id="5c38c-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c38c-246">0x00000000</span></span>                                                   |
| <span data-ttu-id="5c38c-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-247">System-Flags</span></span>           | <span data-ttu-id="5c38c-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c38c-248">0x00000010</span></span>                                                   |
| <span data-ttu-id="5c38c-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c38c-249">Classes used in</span></span>        | [<span data-ttu-id="5c38c-250">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="5c38c-250">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5c38c-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c38c-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5c38c-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-252">Entry</span></span> | <span data-ttu-id="5c38c-253">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-253">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c38c-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c38c-254">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-255">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c38c-256">System-Only</span></span>            | <span data-ttu-id="5c38c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-257">False</span></span>                                                        |
| <span data-ttu-id="5c38c-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c38c-258">Is-Single-Valued</span></span>       | <span data-ttu-id="5c38c-259">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-259">False</span></span>                                                        |
| <span data-ttu-id="5c38c-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c38c-260">Is Indexed</span></span>             | <span data-ttu-id="5c38c-261">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-261">False</span></span>                                                        |
| <span data-ttu-id="5c38c-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c38c-262">In Global Catalog</span></span>      | <span data-ttu-id="5c38c-263">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-263">False</span></span>                                                        |
| <span data-ttu-id="5c38c-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c38c-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c38c-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c38c-265">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5c38c-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c38c-266">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c38c-267">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-268">Search-Flags</span></span>           | <span data-ttu-id="5c38c-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c38c-269">0x00000000</span></span>                                                   |
| <span data-ttu-id="5c38c-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-270">System-Flags</span></span>           | <span data-ttu-id="5c38c-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c38c-271">0x00000010</span></span>                                                   |
| <span data-ttu-id="5c38c-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c38c-272">Classes used in</span></span>        | [<span data-ttu-id="5c38c-273">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="5c38c-273">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5c38c-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c38c-274">Windows Server 2012</span></span>



| <span data-ttu-id="5c38c-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="5c38c-275">Entry</span></span> | <span data-ttu-id="5c38c-276">Valor</span><span class="sxs-lookup"><span data-stu-id="5c38c-276">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="5c38c-277">ID do link</span><span class="sxs-lookup"><span data-stu-id="5c38c-277">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c38c-278">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="5c38c-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c38c-279">System-Only</span></span>            | <span data-ttu-id="5c38c-280">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-280">False</span></span>                                                        |
| <span data-ttu-id="5c38c-281">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5c38c-281">Is-Single-Valued</span></span>       | <span data-ttu-id="5c38c-282">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-282">False</span></span>                                                        |
| <span data-ttu-id="5c38c-283">É indexado</span><span class="sxs-lookup"><span data-stu-id="5c38c-283">Is Indexed</span></span>             | <span data-ttu-id="5c38c-284">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-284">False</span></span>                                                        |
| <span data-ttu-id="5c38c-285">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5c38c-285">In Global Catalog</span></span>      | <span data-ttu-id="5c38c-286">Falso</span><span class="sxs-lookup"><span data-stu-id="5c38c-286">False</span></span>                                                        |
| <span data-ttu-id="5c38c-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5c38c-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c38c-288">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5c38c-288">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="5c38c-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c38c-289">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c38c-290">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="5c38c-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-291">Search-Flags</span></span>           | <span data-ttu-id="5c38c-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c38c-292">0x00000000</span></span>                                                   |
| <span data-ttu-id="5c38c-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c38c-293">System-Flags</span></span>           | <span data-ttu-id="5c38c-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c38c-294">0x00000010</span></span>                                                   |
| <span data-ttu-id="5c38c-295">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5c38c-295">Classes used in</span></span>        | [<span data-ttu-id="5c38c-296">**Segurança-principal**</span><span class="sxs-lookup"><span data-stu-id="5c38c-296">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





