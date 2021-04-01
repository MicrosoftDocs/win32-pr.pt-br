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
# <a name="sd-rights-effective-attribute"></a><span data-ttu-id="c906e-106">SD-atributo de efetivação de direitos</span><span class="sxs-lookup"><span data-stu-id="c906e-106">SD-Rights-Effective attribute</span></span>

<span data-ttu-id="c906e-107">Esse atributo construído retorna um único valor **DWORD** que pode ter até três bits definidos:</span><span class="sxs-lookup"><span data-stu-id="c906e-107">This constructed attribute returns a single **DWORD** value that can have up to three bits set:</span></span>

-   <span data-ttu-id="c906e-108">\_informações de segurança do proprietário \_</span><span class="sxs-lookup"><span data-stu-id="c906e-108">OWNER\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="c906e-109">\_informações de segurança da DACL \_</span><span class="sxs-lookup"><span data-stu-id="c906e-109">DACL\_SECURITY\_INFORMATION</span></span>
-   <span data-ttu-id="c906e-110">\_informações de segurança da SACL \_</span><span class="sxs-lookup"><span data-stu-id="c906e-110">SACL\_SECURITY\_INFORMATION</span></span>

<span data-ttu-id="c906e-111">Se um bit for definido, o usuário terá acesso de gravação à parte correspondente do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="c906e-111">If a bit is set, then the user has write access to the corresponding part of the security descriptor.</span></span> <span data-ttu-id="c906e-112">Proprietário significa proprietário e grupo.</span><span class="sxs-lookup"><span data-stu-id="c906e-112">Owner means both owner and group.</span></span>



| <span data-ttu-id="c906e-113">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-113">Entry</span></span> | <span data-ttu-id="c906e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-114">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c906e-115">CN</span><span class="sxs-lookup"><span data-stu-id="c906e-115">CN</span></span>                | <span data-ttu-id="c906e-116">SD-direitos-efetivos</span><span class="sxs-lookup"><span data-stu-id="c906e-116">SD-Rights-Effective</span></span>                  |
| <span data-ttu-id="c906e-117">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c906e-117">Ldap-Display-Name</span></span> | <span data-ttu-id="c906e-118">sDRightsEffective</span><span class="sxs-lookup"><span data-stu-id="c906e-118">sDRightsEffective</span></span>                    |
| <span data-ttu-id="c906e-119">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c906e-119">Size</span></span>              | \-                                   |
| <span data-ttu-id="c906e-120">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c906e-120">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c906e-121">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c906e-121">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c906e-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-122">Attribute-Id</span></span>      | <span data-ttu-id="c906e-123">1.2.840.113556.1.4.1304</span><span class="sxs-lookup"><span data-stu-id="c906e-123">1.2.840.113556.1.4.1304</span></span>              |
| <span data-ttu-id="c906e-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c906e-124">System-Id-Guid</span></span>    | <span data-ttu-id="c906e-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="c906e-125">c3dbafa6-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="c906e-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="c906e-126">Syntax</span></span>            | [<span data-ttu-id="c906e-127">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c906e-127">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c906e-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="c906e-128">Implementations</span></span>

-   [<span data-ttu-id="c906e-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c906e-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c906e-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c906e-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c906e-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c906e-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c906e-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c906e-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c906e-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c906e-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c906e-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c906e-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c906e-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c906e-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c906e-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c906e-136">Windows 2000 Server</span></span>



| <span data-ttu-id="c906e-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-137">Entry</span></span> | <span data-ttu-id="c906e-138">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-138">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c906e-139">ID do link</span><span class="sxs-lookup"><span data-stu-id="c906e-139">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-140">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="c906e-141">System-Only</span></span>            | <span data-ttu-id="c906e-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-142">False</span></span>                           |
| <span data-ttu-id="c906e-143">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c906e-143">Is-Single-Valued</span></span>       | <span data-ttu-id="c906e-144">True</span><span class="sxs-lookup"><span data-stu-id="c906e-144">True</span></span>                            |
| <span data-ttu-id="c906e-145">É indexado</span><span class="sxs-lookup"><span data-stu-id="c906e-145">Is Indexed</span></span>             | <span data-ttu-id="c906e-146">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-146">False</span></span>                           |
| <span data-ttu-id="c906e-147">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c906e-147">In Global Catalog</span></span>      | <span data-ttu-id="c906e-148">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-148">False</span></span>                           |
| <span data-ttu-id="c906e-149">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c906e-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="c906e-150">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c906e-150">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c906e-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c906e-151">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c906e-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c906e-152">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c906e-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-153">Search-Flags</span></span>           | <span data-ttu-id="c906e-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c906e-154">0x00000000</span></span>                      |
| <span data-ttu-id="c906e-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-155">System-Flags</span></span>           | <span data-ttu-id="c906e-156">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c906e-156">0x08000014</span></span>                      |
| <span data-ttu-id="c906e-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c906e-157">Classes used in</span></span>        | [<span data-ttu-id="c906e-158">**Início**</span><span class="sxs-lookup"><span data-stu-id="c906e-158">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c906e-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c906e-159">Windows Server 2003</span></span>



| <span data-ttu-id="c906e-160">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-160">Entry</span></span> | <span data-ttu-id="c906e-161">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-161">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c906e-162">ID do link</span><span class="sxs-lookup"><span data-stu-id="c906e-162">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c906e-164">System-Only</span></span>            | <span data-ttu-id="c906e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-165">False</span></span>                           |
| <span data-ttu-id="c906e-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c906e-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c906e-167">True</span><span class="sxs-lookup"><span data-stu-id="c906e-167">True</span></span>                            |
| <span data-ttu-id="c906e-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="c906e-168">Is Indexed</span></span>             | <span data-ttu-id="c906e-169">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-169">False</span></span>                           |
| <span data-ttu-id="c906e-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c906e-170">In Global Catalog</span></span>      | <span data-ttu-id="c906e-171">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-171">False</span></span>                           |
| <span data-ttu-id="c906e-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c906e-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c906e-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c906e-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c906e-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c906e-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c906e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c906e-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c906e-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-176">Search-Flags</span></span>           | <span data-ttu-id="c906e-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c906e-177">0x00000000</span></span>                      |
| <span data-ttu-id="c906e-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-178">System-Flags</span></span>           | <span data-ttu-id="c906e-179">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c906e-179">0x08000014</span></span>                      |
| <span data-ttu-id="c906e-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c906e-180">Classes used in</span></span>        | [<span data-ttu-id="c906e-181">**Início**</span><span class="sxs-lookup"><span data-stu-id="c906e-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c906e-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="c906e-182">ADAM</span></span>



| <span data-ttu-id="c906e-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-183">Entry</span></span> | <span data-ttu-id="c906e-184">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c906e-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="c906e-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="c906e-187">System-Only</span></span>            | <span data-ttu-id="c906e-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-188">False</span></span>                           |
| <span data-ttu-id="c906e-189">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c906e-189">Is-Single-Valued</span></span>       | <span data-ttu-id="c906e-190">True</span><span class="sxs-lookup"><span data-stu-id="c906e-190">True</span></span>                            |
| <span data-ttu-id="c906e-191">É indexado</span><span class="sxs-lookup"><span data-stu-id="c906e-191">Is Indexed</span></span>             | <span data-ttu-id="c906e-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-192">False</span></span>                           |
| <span data-ttu-id="c906e-193">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c906e-193">In Global Catalog</span></span>      | <span data-ttu-id="c906e-194">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-194">False</span></span>                           |
| <span data-ttu-id="c906e-195">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c906e-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="c906e-196">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c906e-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c906e-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c906e-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c906e-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c906e-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c906e-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-199">Search-Flags</span></span>           | <span data-ttu-id="c906e-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c906e-200">0x00000000</span></span>                      |
| <span data-ttu-id="c906e-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-201">System-Flags</span></span>           | <span data-ttu-id="c906e-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c906e-202">0x08000014</span></span>                      |
| <span data-ttu-id="c906e-203">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c906e-203">Classes used in</span></span>        | [<span data-ttu-id="c906e-204">**Início**</span><span class="sxs-lookup"><span data-stu-id="c906e-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c906e-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c906e-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c906e-206">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-206">Entry</span></span> | <span data-ttu-id="c906e-207">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c906e-208">ID do link</span><span class="sxs-lookup"><span data-stu-id="c906e-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c906e-210">System-Only</span></span>            | <span data-ttu-id="c906e-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-211">False</span></span>                           |
| <span data-ttu-id="c906e-212">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c906e-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c906e-213">True</span><span class="sxs-lookup"><span data-stu-id="c906e-213">True</span></span>                            |
| <span data-ttu-id="c906e-214">É indexado</span><span class="sxs-lookup"><span data-stu-id="c906e-214">Is Indexed</span></span>             | <span data-ttu-id="c906e-215">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-215">False</span></span>                           |
| <span data-ttu-id="c906e-216">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c906e-216">In Global Catalog</span></span>      | <span data-ttu-id="c906e-217">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-217">False</span></span>                           |
| <span data-ttu-id="c906e-218">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c906e-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c906e-219">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c906e-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c906e-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c906e-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c906e-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c906e-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c906e-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-222">Search-Flags</span></span>           | <span data-ttu-id="c906e-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c906e-223">0x00000000</span></span>                      |
| <span data-ttu-id="c906e-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-224">System-Flags</span></span>           | <span data-ttu-id="c906e-225">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c906e-225">0x08000014</span></span>                      |
| <span data-ttu-id="c906e-226">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c906e-226">Classes used in</span></span>        | [<span data-ttu-id="c906e-227">**Início**</span><span class="sxs-lookup"><span data-stu-id="c906e-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c906e-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c906e-228">Windows Server 2008</span></span>



| <span data-ttu-id="c906e-229">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-229">Entry</span></span> | <span data-ttu-id="c906e-230">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c906e-231">ID do link</span><span class="sxs-lookup"><span data-stu-id="c906e-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-232">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c906e-233">System-Only</span></span>            | <span data-ttu-id="c906e-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-234">False</span></span>                           |
| <span data-ttu-id="c906e-235">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c906e-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c906e-236">True</span><span class="sxs-lookup"><span data-stu-id="c906e-236">True</span></span>                            |
| <span data-ttu-id="c906e-237">É indexado</span><span class="sxs-lookup"><span data-stu-id="c906e-237">Is Indexed</span></span>             | <span data-ttu-id="c906e-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-238">False</span></span>                           |
| <span data-ttu-id="c906e-239">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c906e-239">In Global Catalog</span></span>      | <span data-ttu-id="c906e-240">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-240">False</span></span>                           |
| <span data-ttu-id="c906e-241">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c906e-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c906e-242">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c906e-242">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c906e-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c906e-243">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c906e-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c906e-244">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c906e-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-245">Search-Flags</span></span>           | <span data-ttu-id="c906e-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c906e-246">0x00000000</span></span>                      |
| <span data-ttu-id="c906e-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-247">System-Flags</span></span>           | <span data-ttu-id="c906e-248">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c906e-248">0x08000014</span></span>                      |
| <span data-ttu-id="c906e-249">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c906e-249">Classes used in</span></span>        | [<span data-ttu-id="c906e-250">**Início**</span><span class="sxs-lookup"><span data-stu-id="c906e-250">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c906e-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c906e-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c906e-252">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-252">Entry</span></span> | <span data-ttu-id="c906e-253">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-253">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c906e-254">ID do link</span><span class="sxs-lookup"><span data-stu-id="c906e-254">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-255">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="c906e-256">System-Only</span></span>            | <span data-ttu-id="c906e-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-257">False</span></span>                           |
| <span data-ttu-id="c906e-258">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c906e-258">Is-Single-Valued</span></span>       | <span data-ttu-id="c906e-259">True</span><span class="sxs-lookup"><span data-stu-id="c906e-259">True</span></span>                            |
| <span data-ttu-id="c906e-260">É indexado</span><span class="sxs-lookup"><span data-stu-id="c906e-260">Is Indexed</span></span>             | <span data-ttu-id="c906e-261">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-261">False</span></span>                           |
| <span data-ttu-id="c906e-262">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c906e-262">In Global Catalog</span></span>      | <span data-ttu-id="c906e-263">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-263">False</span></span>                           |
| <span data-ttu-id="c906e-264">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c906e-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="c906e-265">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c906e-265">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c906e-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c906e-266">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c906e-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c906e-267">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c906e-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-268">Search-Flags</span></span>           | <span data-ttu-id="c906e-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c906e-269">0x00000000</span></span>                      |
| <span data-ttu-id="c906e-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-270">System-Flags</span></span>           | <span data-ttu-id="c906e-271">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c906e-271">0x08000014</span></span>                      |
| <span data-ttu-id="c906e-272">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c906e-272">Classes used in</span></span>        | [<span data-ttu-id="c906e-273">**Início**</span><span class="sxs-lookup"><span data-stu-id="c906e-273">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c906e-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c906e-274">Windows Server 2012</span></span>



| <span data-ttu-id="c906e-275">Entrada</span><span class="sxs-lookup"><span data-stu-id="c906e-275">Entry</span></span> | <span data-ttu-id="c906e-276">Valor</span><span class="sxs-lookup"><span data-stu-id="c906e-276">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c906e-277">ID do link</span><span class="sxs-lookup"><span data-stu-id="c906e-277">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c906e-278">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c906e-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="c906e-279">System-Only</span></span>            | <span data-ttu-id="c906e-280">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-280">False</span></span>                           |
| <span data-ttu-id="c906e-281">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c906e-281">Is-Single-Valued</span></span>       | <span data-ttu-id="c906e-282">True</span><span class="sxs-lookup"><span data-stu-id="c906e-282">True</span></span>                            |
| <span data-ttu-id="c906e-283">É indexado</span><span class="sxs-lookup"><span data-stu-id="c906e-283">Is Indexed</span></span>             | <span data-ttu-id="c906e-284">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-284">False</span></span>                           |
| <span data-ttu-id="c906e-285">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c906e-285">In Global Catalog</span></span>      | <span data-ttu-id="c906e-286">Falso</span><span class="sxs-lookup"><span data-stu-id="c906e-286">False</span></span>                           |
| <span data-ttu-id="c906e-287">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c906e-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="c906e-288">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c906e-288">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c906e-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c906e-289">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c906e-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c906e-290">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c906e-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-291">Search-Flags</span></span>           | <span data-ttu-id="c906e-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c906e-292">0x00000000</span></span>                      |
| <span data-ttu-id="c906e-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c906e-293">System-Flags</span></span>           | <span data-ttu-id="c906e-294">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c906e-294">0x08000014</span></span>                      |
| <span data-ttu-id="c906e-295">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c906e-295">Classes used in</span></span>        | [<span data-ttu-id="c906e-296">**Início**</span><span class="sxs-lookup"><span data-stu-id="c906e-296">**Top**</span></span>](c-top.md)<br/> |



 

 





