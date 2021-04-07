---
title: atributo de afinidade ms-DS-site-Affinity
description: O atributo ms-DS-site-Affinity é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de afinidade do MS-DS-site-Affinity
- msDS-site-Affinity atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825348"
---
# <a name="ms-ds-site-affinity-attribute"></a><span data-ttu-id="a5ccd-105">atributo de afinidade ms-DS-site-Affinity</span><span class="sxs-lookup"><span data-stu-id="a5ccd-105">ms-DS-Site-Affinity attribute</span></span>

<span data-ttu-id="a5ccd-106">O atributo **MS-DS-site-Affinity** é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.</span><span class="sxs-lookup"><span data-stu-id="a5ccd-106">The **ms-DS-Site-Affinity** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="a5ccd-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5ccd-107">Entry</span></span> | <span data-ttu-id="a5ccd-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5ccd-109">CN</span><span class="sxs-lookup"><span data-stu-id="a5ccd-109">CN</span></span>                | <span data-ttu-id="a5ccd-110">ms-DS-site-Affinity</span><span class="sxs-lookup"><span data-stu-id="a5ccd-110">ms-DS-Site-Affinity</span></span>                                                                     |
| <span data-ttu-id="a5ccd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a5ccd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a5ccd-112">msDS-afinidade de site</span><span class="sxs-lookup"><span data-stu-id="a5ccd-112">msDS-Site-Affinity</span></span>                                                                      |
| <span data-ttu-id="a5ccd-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a5ccd-113">Size</span></span>              | <span data-ttu-id="a5ccd-114">BLOB binário de valores múltiplos, em que cada valor é sizeof (GUID) + sizeof ( \_ inteiro grande).</span><span class="sxs-lookup"><span data-stu-id="a5ccd-114">Multiple-valued binary BLOB, where each value is sizeof(GUID) + sizeof(LARGE\_INTEGER).</span></span> |
| <span data-ttu-id="a5ccd-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a5ccd-115">Update Privilege</span></span>  | \-                                                                                      |
| <span data-ttu-id="a5ccd-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a5ccd-116">Update Frequency</span></span>  | <span data-ttu-id="a5ccd-117">Por padrão, uma vez a cada três meses.</span><span class="sxs-lookup"><span data-stu-id="a5ccd-117">By default once every three months.</span></span>                                                     |
| <span data-ttu-id="a5ccd-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a5ccd-118">Attribute-Id</span></span>      | <span data-ttu-id="a5ccd-119">1.2.840.113556.1.4.1443</span><span class="sxs-lookup"><span data-stu-id="a5ccd-119">1.2.840.113556.1.4.1443</span></span>                                                                 |
| <span data-ttu-id="a5ccd-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a5ccd-120">System-Id-Guid</span></span>    | <span data-ttu-id="a5ccd-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span><span class="sxs-lookup"><span data-stu-id="a5ccd-121">c17c5602-bcb7-46f0-9656-6370ca884b72</span></span>                                                    |
| <span data-ttu-id="a5ccd-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5ccd-122">Syntax</span></span>            | [<span data-ttu-id="a5ccd-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                   |



## <a name="implementations"></a><span data-ttu-id="a5ccd-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="a5ccd-124">Implementations</span></span>

-   [<span data-ttu-id="a5ccd-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a5ccd-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a5ccd-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a5ccd-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a5ccd-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a5ccd-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5ccd-130">Windows Server 2003</span></span>



| <span data-ttu-id="a5ccd-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5ccd-131">Entry</span></span> | <span data-ttu-id="a5ccd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a5ccd-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5ccd-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5ccd-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5ccd-135">System-Only</span></span>            | <span data-ttu-id="a5ccd-136">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-136">False</span></span>                             |
| <span data-ttu-id="a5ccd-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5ccd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="a5ccd-138">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-138">False</span></span>                             |
| <span data-ttu-id="a5ccd-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5ccd-139">Is Indexed</span></span>             | <span data-ttu-id="a5ccd-140">True</span><span class="sxs-lookup"><span data-stu-id="a5ccd-140">True</span></span>                              |
| <span data-ttu-id="a5ccd-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5ccd-141">In Global Catalog</span></span>      | <span data-ttu-id="a5ccd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-142">False</span></span>                             |
| <span data-ttu-id="a5ccd-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5ccd-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5ccd-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a5ccd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5ccd-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5ccd-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-147">Search-Flags</span></span>           | <span data-ttu-id="a5ccd-148">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a5ccd-148">0x00000001</span></span>                        |
| <span data-ttu-id="a5ccd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-149">System-Flags</span></span>           | <span data-ttu-id="a5ccd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5ccd-150">0x00000010</span></span>                        |
| <span data-ttu-id="a5ccd-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5ccd-151">Classes used in</span></span>        | [<span data-ttu-id="a5ccd-152">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a5ccd-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a5ccd-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a5ccd-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5ccd-154">Entry</span></span> | <span data-ttu-id="a5ccd-155">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a5ccd-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5ccd-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5ccd-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5ccd-158">System-Only</span></span>            | <span data-ttu-id="a5ccd-159">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-159">False</span></span>                             |
| <span data-ttu-id="a5ccd-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5ccd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="a5ccd-161">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-161">False</span></span>                             |
| <span data-ttu-id="a5ccd-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5ccd-162">Is Indexed</span></span>             | <span data-ttu-id="a5ccd-163">True</span><span class="sxs-lookup"><span data-stu-id="a5ccd-163">True</span></span>                              |
| <span data-ttu-id="a5ccd-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5ccd-164">In Global Catalog</span></span>      | <span data-ttu-id="a5ccd-165">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-165">False</span></span>                             |
| <span data-ttu-id="a5ccd-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5ccd-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5ccd-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a5ccd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5ccd-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5ccd-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-170">Search-Flags</span></span>           | <span data-ttu-id="a5ccd-171">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a5ccd-171">0x00000001</span></span>                        |
| <span data-ttu-id="a5ccd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-172">System-Flags</span></span>           | <span data-ttu-id="a5ccd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5ccd-173">0x00000010</span></span>                        |
| <span data-ttu-id="a5ccd-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5ccd-174">Classes used in</span></span>        | [<span data-ttu-id="a5ccd-175">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a5ccd-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5ccd-176">Windows Server 2008</span></span>



| <span data-ttu-id="a5ccd-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5ccd-177">Entry</span></span> | <span data-ttu-id="a5ccd-178">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a5ccd-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5ccd-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5ccd-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5ccd-181">System-Only</span></span>            | <span data-ttu-id="a5ccd-182">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-182">False</span></span>                             |
| <span data-ttu-id="a5ccd-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5ccd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="a5ccd-184">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-184">False</span></span>                             |
| <span data-ttu-id="a5ccd-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5ccd-185">Is Indexed</span></span>             | <span data-ttu-id="a5ccd-186">True</span><span class="sxs-lookup"><span data-stu-id="a5ccd-186">True</span></span>                              |
| <span data-ttu-id="a5ccd-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5ccd-187">In Global Catalog</span></span>      | <span data-ttu-id="a5ccd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-188">False</span></span>                             |
| <span data-ttu-id="a5ccd-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5ccd-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5ccd-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a5ccd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5ccd-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5ccd-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-193">Search-Flags</span></span>           | <span data-ttu-id="a5ccd-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a5ccd-194">0x00000001</span></span>                        |
| <span data-ttu-id="a5ccd-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-195">System-Flags</span></span>           | <span data-ttu-id="a5ccd-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5ccd-196">0x00000010</span></span>                        |
| <span data-ttu-id="a5ccd-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5ccd-197">Classes used in</span></span>        | [<span data-ttu-id="a5ccd-198">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a5ccd-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5ccd-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a5ccd-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5ccd-200">Entry</span></span> | <span data-ttu-id="a5ccd-201">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a5ccd-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5ccd-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5ccd-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5ccd-204">System-Only</span></span>            | <span data-ttu-id="a5ccd-205">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-205">False</span></span>                             |
| <span data-ttu-id="a5ccd-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5ccd-206">Is-Single-Valued</span></span>       | <span data-ttu-id="a5ccd-207">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-207">False</span></span>                             |
| <span data-ttu-id="a5ccd-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5ccd-208">Is Indexed</span></span>             | <span data-ttu-id="a5ccd-209">True</span><span class="sxs-lookup"><span data-stu-id="a5ccd-209">True</span></span>                              |
| <span data-ttu-id="a5ccd-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5ccd-210">In Global Catalog</span></span>      | <span data-ttu-id="a5ccd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-211">False</span></span>                             |
| <span data-ttu-id="a5ccd-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5ccd-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5ccd-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a5ccd-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5ccd-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5ccd-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-216">Search-Flags</span></span>           | <span data-ttu-id="a5ccd-217">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a5ccd-217">0x00000001</span></span>                        |
| <span data-ttu-id="a5ccd-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-218">System-Flags</span></span>           | <span data-ttu-id="a5ccd-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5ccd-219">0x00000010</span></span>                        |
| <span data-ttu-id="a5ccd-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5ccd-220">Classes used in</span></span>        | [<span data-ttu-id="a5ccd-221">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a5ccd-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5ccd-222">Windows Server 2012</span></span>



| <span data-ttu-id="a5ccd-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5ccd-223">Entry</span></span> | <span data-ttu-id="a5ccd-224">Valor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="a5ccd-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="a5ccd-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5ccd-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="a5ccd-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5ccd-227">System-Only</span></span>            | <span data-ttu-id="a5ccd-228">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-228">False</span></span>                             |
| <span data-ttu-id="a5ccd-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a5ccd-229">Is-Single-Valued</span></span>       | <span data-ttu-id="a5ccd-230">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-230">False</span></span>                             |
| <span data-ttu-id="a5ccd-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="a5ccd-231">Is Indexed</span></span>             | <span data-ttu-id="a5ccd-232">True</span><span class="sxs-lookup"><span data-stu-id="a5ccd-232">True</span></span>                              |
| <span data-ttu-id="a5ccd-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a5ccd-233">In Global Catalog</span></span>      | <span data-ttu-id="a5ccd-234">Falso</span><span class="sxs-lookup"><span data-stu-id="a5ccd-234">False</span></span>                             |
| <span data-ttu-id="a5ccd-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a5ccd-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5ccd-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a5ccd-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="a5ccd-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5ccd-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5ccd-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="a5ccd-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-239">Search-Flags</span></span>           | <span data-ttu-id="a5ccd-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a5ccd-240">0x00000001</span></span>                        |
| <span data-ttu-id="a5ccd-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5ccd-241">System-Flags</span></span>           | <span data-ttu-id="a5ccd-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5ccd-242">0x00000010</span></span>                        |
| <span data-ttu-id="a5ccd-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a5ccd-243">Classes used in</span></span>        | [<span data-ttu-id="a5ccd-244">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="a5ccd-244">**User**</span></span>](c-user.md)<br/> |



 

 





