---
title: ms-DS-Preferred-GC-atributo de site
description: O atributo ms-DS-Preferred-GC-site é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.
ms.assetid: f42d3787-4063-4804-a7b5-4798516ad47e
ms.tgt_platform: multiple
keywords:
- ms-DS-preferível-GC-esquema do AD do atributo do site
- msDS-Preferred-GC-site atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Preferred-GC-Site
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172e12758ba0b365fa195cb4e1384c161cea3d14
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104163648"
---
# <a name="ms-ds-preferred-gc-site-attribute"></a><span data-ttu-id="f5d11-105">ms-DS-Preferred-GC-atributo de site</span><span class="sxs-lookup"><span data-stu-id="f5d11-105">ms-DS-Preferred-GC-Site attribute</span></span>

<span data-ttu-id="f5d11-106">O atributo **MS-DS-Preferred-GC-site** é usado pelo gerente de contas de segurança para a expansão de grupo durante a avaliação do token.</span><span class="sxs-lookup"><span data-stu-id="f5d11-106">The **ms-DS-Preferred-GC-Site** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="f5d11-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d11-107">Entry</span></span> | <span data-ttu-id="f5d11-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d11-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="f5d11-109">CN</span><span class="sxs-lookup"><span data-stu-id="f5d11-109">CN</span></span>                | <span data-ttu-id="f5d11-110">ms-DS-Preferred-GC-site</span><span class="sxs-lookup"><span data-stu-id="f5d11-110">ms-DS-Preferred-GC-Site</span></span>                 |
| <span data-ttu-id="f5d11-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f5d11-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f5d11-112">msDS-Preferred-GC-site</span><span class="sxs-lookup"><span data-stu-id="f5d11-112">msDS-Preferred-GC-Site</span></span>                  |
| <span data-ttu-id="f5d11-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f5d11-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="f5d11-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f5d11-114">Update Privilege</span></span>  | <span data-ttu-id="f5d11-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="f5d11-115">Domain administrator</span></span>                    |
| <span data-ttu-id="f5d11-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f5d11-116">Update Frequency</span></span>  | <span data-ttu-id="f5d11-117">A critério do administrador.</span><span class="sxs-lookup"><span data-stu-id="f5d11-117">At the administrator's discretion.</span></span>      |
| <span data-ttu-id="f5d11-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f5d11-118">Attribute-Id</span></span>      | <span data-ttu-id="f5d11-119">1.2.840.113556.1.4.1444</span><span class="sxs-lookup"><span data-stu-id="f5d11-119">1.2.840.113556.1.4.1444</span></span>                 |
| <span data-ttu-id="f5d11-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f5d11-120">System-Id-Guid</span></span>    | <span data-ttu-id="f5d11-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span><span class="sxs-lookup"><span data-stu-id="f5d11-121">d921b50a-0ab2-42cd-87f6-09cf83a91854</span></span>    |
| <span data-ttu-id="f5d11-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5d11-122">Syntax</span></span>            | [<span data-ttu-id="f5d11-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="f5d11-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="f5d11-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="f5d11-124">Implementations</span></span>

-   [<span data-ttu-id="f5d11-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f5d11-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f5d11-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f5d11-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f5d11-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f5d11-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f5d11-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f5d11-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f5d11-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f5d11-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f5d11-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f5d11-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f5d11-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5d11-131">Windows Server 2003</span></span>



| <span data-ttu-id="f5d11-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d11-132">Entry</span></span> | <span data-ttu-id="f5d11-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d11-133">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5d11-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5d11-134">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5d11-135">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5d11-136">System-Only</span></span>            | <span data-ttu-id="f5d11-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-137">False</span></span>                                                       |
| <span data-ttu-id="f5d11-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5d11-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f5d11-139">True</span><span class="sxs-lookup"><span data-stu-id="f5d11-139">True</span></span>                                                        |
| <span data-ttu-id="f5d11-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5d11-140">Is Indexed</span></span>             | <span data-ttu-id="f5d11-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-141">False</span></span>                                                       |
| <span data-ttu-id="f5d11-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5d11-142">In Global Catalog</span></span>      | <span data-ttu-id="f5d11-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-143">False</span></span>                                                       |
| <span data-ttu-id="f5d11-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5d11-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5d11-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5d11-145">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="f5d11-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5d11-146">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5d11-147">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-148">Search-Flags</span></span>           | <span data-ttu-id="f5d11-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5d11-149">0x00000000</span></span>                                                  |
| <span data-ttu-id="f5d11-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-150">System-Flags</span></span>           | <span data-ttu-id="f5d11-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5d11-151">0x00000010</span></span>                                                  |
| <span data-ttu-id="f5d11-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5d11-152">Classes used in</span></span>        | [<span data-ttu-id="f5d11-153">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="f5d11-153">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f5d11-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="f5d11-154">ADAM</span></span>



| <span data-ttu-id="f5d11-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d11-155">Entry</span></span> | <span data-ttu-id="f5d11-156">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d11-156">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5d11-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5d11-157">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5d11-158">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5d11-159">System-Only</span></span>            | <span data-ttu-id="f5d11-160">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-160">False</span></span>                                                       |
| <span data-ttu-id="f5d11-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5d11-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f5d11-162">True</span><span class="sxs-lookup"><span data-stu-id="f5d11-162">True</span></span>                                                        |
| <span data-ttu-id="f5d11-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5d11-163">Is Indexed</span></span>             | <span data-ttu-id="f5d11-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-164">False</span></span>                                                       |
| <span data-ttu-id="f5d11-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5d11-165">In Global Catalog</span></span>      | <span data-ttu-id="f5d11-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-166">False</span></span>                                                       |
| <span data-ttu-id="f5d11-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5d11-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5d11-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5d11-168">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="f5d11-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5d11-169">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5d11-170">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-171">Search-Flags</span></span>           | <span data-ttu-id="f5d11-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5d11-172">0x00000000</span></span>                                                  |
| <span data-ttu-id="f5d11-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-173">System-Flags</span></span>           | <span data-ttu-id="f5d11-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5d11-174">0x00000010</span></span>                                                  |
| <span data-ttu-id="f5d11-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5d11-175">Classes used in</span></span>        | [<span data-ttu-id="f5d11-176">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="f5d11-176">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f5d11-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f5d11-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f5d11-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d11-178">Entry</span></span> | <span data-ttu-id="f5d11-179">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d11-179">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5d11-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5d11-180">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5d11-181">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5d11-182">System-Only</span></span>            | <span data-ttu-id="f5d11-183">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-183">False</span></span>                                                       |
| <span data-ttu-id="f5d11-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5d11-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f5d11-185">True</span><span class="sxs-lookup"><span data-stu-id="f5d11-185">True</span></span>                                                        |
| <span data-ttu-id="f5d11-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5d11-186">Is Indexed</span></span>             | <span data-ttu-id="f5d11-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-187">False</span></span>                                                       |
| <span data-ttu-id="f5d11-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5d11-188">In Global Catalog</span></span>      | <span data-ttu-id="f5d11-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-189">False</span></span>                                                       |
| <span data-ttu-id="f5d11-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5d11-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5d11-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5d11-191">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="f5d11-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5d11-192">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5d11-193">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-194">Search-Flags</span></span>           | <span data-ttu-id="f5d11-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5d11-195">0x00000000</span></span>                                                  |
| <span data-ttu-id="f5d11-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-196">System-Flags</span></span>           | <span data-ttu-id="f5d11-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5d11-197">0x00000010</span></span>                                                  |
| <span data-ttu-id="f5d11-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5d11-198">Classes used in</span></span>        | [<span data-ttu-id="f5d11-199">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="f5d11-199">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f5d11-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5d11-200">Windows Server 2008</span></span>



| <span data-ttu-id="f5d11-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d11-201">Entry</span></span> | <span data-ttu-id="f5d11-202">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d11-202">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5d11-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5d11-203">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5d11-204">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5d11-205">System-Only</span></span>            | <span data-ttu-id="f5d11-206">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-206">False</span></span>                                                       |
| <span data-ttu-id="f5d11-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5d11-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f5d11-208">True</span><span class="sxs-lookup"><span data-stu-id="f5d11-208">True</span></span>                                                        |
| <span data-ttu-id="f5d11-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5d11-209">Is Indexed</span></span>             | <span data-ttu-id="f5d11-210">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-210">False</span></span>                                                       |
| <span data-ttu-id="f5d11-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5d11-211">In Global Catalog</span></span>      | <span data-ttu-id="f5d11-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-212">False</span></span>                                                       |
| <span data-ttu-id="f5d11-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5d11-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5d11-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5d11-214">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="f5d11-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5d11-215">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5d11-216">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-217">Search-Flags</span></span>           | <span data-ttu-id="f5d11-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5d11-218">0x00000000</span></span>                                                  |
| <span data-ttu-id="f5d11-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-219">System-Flags</span></span>           | <span data-ttu-id="f5d11-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5d11-220">0x00000010</span></span>                                                  |
| <span data-ttu-id="f5d11-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5d11-221">Classes used in</span></span>        | [<span data-ttu-id="f5d11-222">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="f5d11-222">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f5d11-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f5d11-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f5d11-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d11-224">Entry</span></span> | <span data-ttu-id="f5d11-225">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d11-225">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5d11-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5d11-226">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5d11-227">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5d11-228">System-Only</span></span>            | <span data-ttu-id="f5d11-229">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-229">False</span></span>                                                       |
| <span data-ttu-id="f5d11-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5d11-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f5d11-231">True</span><span class="sxs-lookup"><span data-stu-id="f5d11-231">True</span></span>                                                        |
| <span data-ttu-id="f5d11-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5d11-232">Is Indexed</span></span>             | <span data-ttu-id="f5d11-233">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-233">False</span></span>                                                       |
| <span data-ttu-id="f5d11-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5d11-234">In Global Catalog</span></span>      | <span data-ttu-id="f5d11-235">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-235">False</span></span>                                                       |
| <span data-ttu-id="f5d11-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5d11-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5d11-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5d11-237">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="f5d11-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5d11-238">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5d11-239">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-240">Search-Flags</span></span>           | <span data-ttu-id="f5d11-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5d11-241">0x00000000</span></span>                                                  |
| <span data-ttu-id="f5d11-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-242">System-Flags</span></span>           | <span data-ttu-id="f5d11-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5d11-243">0x00000010</span></span>                                                  |
| <span data-ttu-id="f5d11-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5d11-244">Classes used in</span></span>        | [<span data-ttu-id="f5d11-245">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="f5d11-245">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f5d11-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5d11-246">Windows Server 2012</span></span>



| <span data-ttu-id="f5d11-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="f5d11-247">Entry</span></span> | <span data-ttu-id="f5d11-248">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d11-248">Value</span></span> |
|------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5d11-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="f5d11-249">Link-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f5d11-250">MAPI-Id</span></span>                | \-                                                          |
| <span data-ttu-id="f5d11-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f5d11-251">System-Only</span></span>            | <span data-ttu-id="f5d11-252">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-252">False</span></span>                                                       |
| <span data-ttu-id="f5d11-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f5d11-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f5d11-254">True</span><span class="sxs-lookup"><span data-stu-id="f5d11-254">True</span></span>                                                        |
| <span data-ttu-id="f5d11-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="f5d11-255">Is Indexed</span></span>             | <span data-ttu-id="f5d11-256">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-256">False</span></span>                                                       |
| <span data-ttu-id="f5d11-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f5d11-257">In Global Catalog</span></span>      | <span data-ttu-id="f5d11-258">Falso</span><span class="sxs-lookup"><span data-stu-id="f5d11-258">False</span></span>                                                       |
| <span data-ttu-id="f5d11-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f5d11-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f5d11-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f5d11-260">O:BAG:BAD:S:</span></span>                                                |
| <span data-ttu-id="f5d11-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f5d11-261">Range-Lower</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f5d11-262">Range-Upper</span></span>            | \-                                                          |
| <span data-ttu-id="f5d11-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-263">Search-Flags</span></span>           | <span data-ttu-id="f5d11-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f5d11-264">0x00000000</span></span>                                                  |
| <span data-ttu-id="f5d11-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f5d11-265">System-Flags</span></span>           | <span data-ttu-id="f5d11-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f5d11-266">0x00000010</span></span>                                                  |
| <span data-ttu-id="f5d11-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f5d11-267">Classes used in</span></span>        | [<span data-ttu-id="f5d11-268">**NTDS – configurações de site**</span><span class="sxs-lookup"><span data-stu-id="f5d11-268">**NTDS-Site-Settings**</span></span>](c-ntdssitesettings.md)<br/> |



 

 





