---
title: SD-atributo de efetivação de direitos
description: Esse atributo construído retorna um único valor DWORD que pode ter até três bits definir segurança do \_ proprietário \_ INFORMATIONDACL \_ segurança \_ INFORMATIONSACL \_ informações de segurança \_ se um bit for definido, o usuário terá acesso de gravação à parte correspondente do descritor de segurança. Proprietário significa proprietário e grupo.
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- SD-esquema do atributo do AD com direitos efetivos
- Esquema de AD do atributo sDRightsEffective
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac449cd18b3fb75a61f04fffc266c290b7763295
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825089"
---
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="8cfae-106">SD-atributo de efetivação de direitos</span><span class="sxs-lookup"><span data-stu-id="8cfae-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="8cfae-107">Esse atributo construído retorna um único valor **DWORD** que pode ter até três bits definidos:</span><span class="sxs-lookup"><span data-stu-id="8cfae-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="8cfae-108">\_informações de segurança do proprietário \_</span><span class="sxs-lookup"><span data-stu-id="8cfae-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="8cfae-109">\_informações de segurança da DACL \_</span><span class="sxs-lookup"><span data-stu-id="8cfae-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="8cfae-110">\_informações de segurança da SACL \_</span><span class="sxs-lookup"><span data-stu-id="8cfae-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="8cfae-111">Se um bit for definido, o usuário terá acesso de gravação à parte correspondente do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="8cfae-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="8cfae-112">Proprietário significa proprietário e grupo.</span><span class="sxs-lookup"><span data-stu-id="8cfae-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="8cfae-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-113">Entry</span></span> | <span data-ttu-id="8cfae-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8cfae-115">CN</span><span class="sxs-lookup"><span data-stu-id="8cfae-115">CN</span></span>                | <span data-ttu-id="8cfae-116">SD-direitos-efetivos</span><span class="sxs-lookup"><span data-stu-id="8cfae-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="8cfae-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8cfae-117">Ldap-Display-Name</span></span> | <span data-ttu-id="8cfae-118">sDRightsEffective</span><span class="sxs-lookup"><span data-stu-id="8cfae-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="8cfae-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8cfae-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="8cfae-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8cfae-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8cfae-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8cfae-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8cfae-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-122">Attribute-Id</span></span>      | <span data-ttu-id="8cfae-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="8cfae-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="8cfae-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8cfae-124">System-Id-Guid</span></span>    | <span data-ttu-id="8cfae-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="8cfae-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="8cfae-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cfae-126">Syntax</span></span>            | [<span data-ttu-id="8cfae-127">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="8cfae-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8cfae-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="8cfae-128">Implementations</span></span>

-   [<span data-ttu-id="8cfae-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8cfae-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8cfae-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8cfae-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8cfae-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8cfae-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8cfae-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8cfae-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8cfae-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8cfae-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8cfae-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8cfae-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8cfae-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8cfae-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8cfae-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cfae-136">Windows 2000 Server</span></span>



| <span data-ttu-id="8cfae-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-137">Entry</span></span> | <span data-ttu-id="8cfae-138">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8cfae-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cfae-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cfae-141">System-Only</span></span>            | <span data-ttu-id="8cfae-142">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-142">False</span></span>                           |
| <span data-ttu-id="8cfae-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cfae-143">Is-Single-Valued</span></span>       | <span data-ttu-id="8cfae-144">True</span><span class="sxs-lookup"><span data-stu-id="8cfae-144">True</span></span>                            |
| <span data-ttu-id="8cfae-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cfae-145">Is Indexed</span></span>             | <span data-ttu-id="8cfae-146">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-146">False</span></span>                           |
| <span data-ttu-id="8cfae-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cfae-147">In Global Catalog</span></span>      | <span data-ttu-id="8cfae-148">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-148">False</span></span>                           |
| <span data-ttu-id="8cfae-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cfae-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cfae-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cfae-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8cfae-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cfae-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8cfae-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cfae-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8cfae-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-153">Search-Flags</span></span>           | <span data-ttu-id="8cfae-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cfae-154">0x00000000</span></span>                      |
| <span data-ttu-id="8cfae-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-155">System-Flags</span></span>           | <span data-ttu-id="8cfae-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8cfae-156">0x08000014</span></span>                      |
| <span data-ttu-id="8cfae-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cfae-157">Classes used in</span></span>        | [<span data-ttu-id="8cfae-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="8cfae-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8cfae-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cfae-159">Windows Server 2003</span></span>



| <span data-ttu-id="8cfae-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-160">Entry</span></span> | <span data-ttu-id="8cfae-161">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8cfae-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cfae-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cfae-164">System-Only</span></span>            | <span data-ttu-id="8cfae-165">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-165">False</span></span>                           |
| <span data-ttu-id="8cfae-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cfae-166">Is-Single-Valued</span></span>       | <span data-ttu-id="8cfae-167">True</span><span class="sxs-lookup"><span data-stu-id="8cfae-167">True</span></span>                            |
| <span data-ttu-id="8cfae-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cfae-168">Is Indexed</span></span>             | <span data-ttu-id="8cfae-169">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-169">False</span></span>                           |
| <span data-ttu-id="8cfae-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cfae-170">In Global Catalog</span></span>      | <span data-ttu-id="8cfae-171">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-171">False</span></span>                           |
| <span data-ttu-id="8cfae-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cfae-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cfae-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cfae-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8cfae-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cfae-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8cfae-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cfae-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8cfae-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-176">Search-Flags</span></span>           | <span data-ttu-id="8cfae-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cfae-177">0x00000000</span></span>                      |
| <span data-ttu-id="8cfae-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-178">System-Flags</span></span>           | <span data-ttu-id="8cfae-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8cfae-179">0x08000014</span></span>                      |
| <span data-ttu-id="8cfae-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cfae-180">Classes used in</span></span>        | [<span data-ttu-id="8cfae-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="8cfae-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8cfae-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="8cfae-182">ADAM</span></span>



| <span data-ttu-id="8cfae-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-183">Entry</span></span> | <span data-ttu-id="8cfae-184">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8cfae-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cfae-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cfae-187">System-Only</span></span>            | <span data-ttu-id="8cfae-188">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-188">False</span></span>                           |
| <span data-ttu-id="8cfae-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cfae-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8cfae-190">True</span><span class="sxs-lookup"><span data-stu-id="8cfae-190">True</span></span>                            |
| <span data-ttu-id="8cfae-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cfae-191">Is Indexed</span></span>             | <span data-ttu-id="8cfae-192">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-192">False</span></span>                           |
| <span data-ttu-id="8cfae-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cfae-193">In Global Catalog</span></span>      | <span data-ttu-id="8cfae-194">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-194">False</span></span>                           |
| <span data-ttu-id="8cfae-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cfae-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cfae-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cfae-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8cfae-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cfae-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8cfae-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cfae-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8cfae-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-199">Search-Flags</span></span>           | <span data-ttu-id="8cfae-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cfae-200">0x00000000</span></span>                      |
| <span data-ttu-id="8cfae-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-201">System-Flags</span></span>           | <span data-ttu-id="8cfae-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8cfae-202">0x08000014</span></span>                      |
| <span data-ttu-id="8cfae-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cfae-203">Classes used in</span></span>        | [<span data-ttu-id="8cfae-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="8cfae-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8cfae-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8cfae-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8cfae-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-206">Entry</span></span> | <span data-ttu-id="8cfae-207">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8cfae-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cfae-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cfae-210">System-Only</span></span>            | <span data-ttu-id="8cfae-211">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-211">False</span></span>                           |
| <span data-ttu-id="8cfae-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cfae-212">Is-Single-Valued</span></span>       | <span data-ttu-id="8cfae-213">True</span><span class="sxs-lookup"><span data-stu-id="8cfae-213">True</span></span>                            |
| <span data-ttu-id="8cfae-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cfae-214">Is Indexed</span></span>             | <span data-ttu-id="8cfae-215">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-215">False</span></span>                           |
| <span data-ttu-id="8cfae-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cfae-216">In Global Catalog</span></span>      | <span data-ttu-id="8cfae-217">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-217">False</span></span>                           |
| <span data-ttu-id="8cfae-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cfae-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cfae-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cfae-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8cfae-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cfae-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8cfae-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cfae-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8cfae-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-222">Search-Flags</span></span>           | <span data-ttu-id="8cfae-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cfae-223">0x00000000</span></span>                      |
| <span data-ttu-id="8cfae-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-224">System-Flags</span></span>           | <span data-ttu-id="8cfae-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8cfae-225">0x08000014</span></span>                      |
| <span data-ttu-id="8cfae-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cfae-226">Classes used in</span></span>        | [<span data-ttu-id="8cfae-227">**Início**</span><span class="sxs-lookup"><span data-stu-id="8cfae-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8cfae-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cfae-228">Windows Server 2008</span></span>



| <span data-ttu-id="8cfae-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-229">Entry</span></span> | <span data-ttu-id="8cfae-230">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8cfae-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cfae-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cfae-233">System-Only</span></span>            | <span data-ttu-id="8cfae-234">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-234">False</span></span>                           |
| <span data-ttu-id="8cfae-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cfae-235">Is-Single-Valued</span></span>       | <span data-ttu-id="8cfae-236">True</span><span class="sxs-lookup"><span data-stu-id="8cfae-236">True</span></span>                            |
| <span data-ttu-id="8cfae-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cfae-237">Is Indexed</span></span>             | <span data-ttu-id="8cfae-238">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-238">False</span></span>                           |
| <span data-ttu-id="8cfae-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cfae-239">In Global Catalog</span></span>      | <span data-ttu-id="8cfae-240">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-240">False</span></span>                           |
| <span data-ttu-id="8cfae-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cfae-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cfae-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cfae-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8cfae-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cfae-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8cfae-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cfae-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8cfae-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-245">Search-Flags</span></span>           | <span data-ttu-id="8cfae-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cfae-246">0x00000000</span></span>                      |
| <span data-ttu-id="8cfae-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-247">System-Flags</span></span>           | <span data-ttu-id="8cfae-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8cfae-248">0x08000014</span></span>                      |
| <span data-ttu-id="8cfae-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cfae-249">Classes used in</span></span>        | [<span data-ttu-id="8cfae-250">**Início**</span><span class="sxs-lookup"><span data-stu-id="8cfae-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8cfae-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cfae-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8cfae-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-252">Entry</span></span> | <span data-ttu-id="8cfae-253">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8cfae-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cfae-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cfae-256">System-Only</span></span>            | <span data-ttu-id="8cfae-257">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-257">False</span></span>                           |
| <span data-ttu-id="8cfae-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cfae-258">Is-Single-Valued</span></span>       | <span data-ttu-id="8cfae-259">True</span><span class="sxs-lookup"><span data-stu-id="8cfae-259">True</span></span>                            |
| <span data-ttu-id="8cfae-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cfae-260">Is Indexed</span></span>             | <span data-ttu-id="8cfae-261">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-261">False</span></span>                           |
| <span data-ttu-id="8cfae-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cfae-262">In Global Catalog</span></span>      | <span data-ttu-id="8cfae-263">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-263">False</span></span>                           |
| <span data-ttu-id="8cfae-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cfae-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cfae-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cfae-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8cfae-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cfae-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8cfae-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cfae-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8cfae-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-268">Search-Flags</span></span>           | <span data-ttu-id="8cfae-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cfae-269">0x00000000</span></span>                      |
| <span data-ttu-id="8cfae-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-270">System-Flags</span></span>           | <span data-ttu-id="8cfae-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8cfae-271">0x08000014</span></span>                      |
| <span data-ttu-id="8cfae-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cfae-272">Classes used in</span></span>        | [<span data-ttu-id="8cfae-273">**Início**</span><span class="sxs-lookup"><span data-stu-id="8cfae-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8cfae-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cfae-274">Windows Server 2012</span></span>



| <span data-ttu-id="8cfae-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="8cfae-275">Entry</span></span> | <span data-ttu-id="8cfae-276">Valor</span><span class="sxs-lookup"><span data-stu-id="8cfae-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8cfae-277">ID do link</span><span class="sxs-lookup"><span data-stu-id="8cfae-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cfae-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8cfae-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cfae-279">System-Only</span></span>            | <span data-ttu-id="8cfae-280">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-280">False</span></span>                           |
| <span data-ttu-id="8cfae-281">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8cfae-281">Is-Single-Valued</span></span>       | <span data-ttu-id="8cfae-282">True</span><span class="sxs-lookup"><span data-stu-id="8cfae-282">True</span></span>                            |
| <span data-ttu-id="8cfae-283">É indexado</span><span class="sxs-lookup"><span data-stu-id="8cfae-283">Is Indexed</span></span>             | <span data-ttu-id="8cfae-284">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-284">False</span></span>                           |
| <span data-ttu-id="8cfae-285">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8cfae-285">In Global Catalog</span></span>      | <span data-ttu-id="8cfae-286">Falso</span><span class="sxs-lookup"><span data-stu-id="8cfae-286">False</span></span>                           |
| <span data-ttu-id="8cfae-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8cfae-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cfae-288">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8cfae-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8cfae-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cfae-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="8cfae-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cfae-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="8cfae-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-291">Search-Flags</span></span>           | <span data-ttu-id="8cfae-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cfae-292">0x00000000</span></span>                      |
| <span data-ttu-id="8cfae-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cfae-293">System-Flags</span></span>           | <span data-ttu-id="8cfae-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8cfae-294">0x08000014</span></span>                      |
| <span data-ttu-id="8cfae-295">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8cfae-295">Classes used in</span></span>        | [<span data-ttu-id="8cfae-296">**Início**</span><span class="sxs-lookup"><span data-stu-id="8cfae-296">**Top**</span></span>](c-top.md)<br/> |



 

 





