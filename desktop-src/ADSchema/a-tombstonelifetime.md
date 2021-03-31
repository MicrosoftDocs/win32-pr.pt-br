---
title: Tombstone-Lifetime atributo
description: O número de dias antes que um objeto excluído seja removido dos serviços de diretório.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Esquema de Tombstone-Lifetime do atributo AD
- Esquema de AD do atributo tombstoneLifetime
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825261"
---
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="33cfc-105">Tombstone-Lifetime atributo</span><span class="sxs-lookup"><span data-stu-id="33cfc-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="33cfc-106">O número de dias antes que um objeto excluído seja removido dos serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="33cfc-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="33cfc-107">Isso ajuda a remover objetos de servidores replicados e a impedir que as restaurações reintroduzam um objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="33cfc-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="33cfc-108">Esse valor está no objeto de serviço de diretório na NIC de configuração.</span><span class="sxs-lookup"><span data-stu-id="33cfc-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="33cfc-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-109">Entry</span></span> | <span data-ttu-id="33cfc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="33cfc-111">CN</span><span class="sxs-lookup"><span data-stu-id="33cfc-111">CN</span></span>                | <span data-ttu-id="33cfc-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="33cfc-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="33cfc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="33cfc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="33cfc-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="33cfc-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="33cfc-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="33cfc-115">Size</span></span>              | <span data-ttu-id="33cfc-116">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="33cfc-116">4 bytes.</span></span> <span data-ttu-id="33cfc-117">O padrão é 60 dias quando nenhum valor é inserido.</span><span class="sxs-lookup"><span data-stu-id="33cfc-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="33cfc-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="33cfc-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="33cfc-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="33cfc-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="33cfc-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-120">Attribute-Id</span></span>      | <span data-ttu-id="33cfc-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="33cfc-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="33cfc-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="33cfc-122">System-Id-Guid</span></span>    | <span data-ttu-id="33cfc-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="33cfc-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="33cfc-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="33cfc-124">Syntax</span></span>            | [<span data-ttu-id="33cfc-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="33cfc-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="33cfc-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="33cfc-126">Implementations</span></span>

-   [<span data-ttu-id="33cfc-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="33cfc-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="33cfc-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="33cfc-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="33cfc-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="33cfc-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="33cfc-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="33cfc-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="33cfc-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="33cfc-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="33cfc-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="33cfc-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="33cfc-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="33cfc-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="33cfc-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33cfc-134">Windows 2000 Server</span></span>



| <span data-ttu-id="33cfc-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-135">Entry</span></span> | <span data-ttu-id="33cfc-136">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="33cfc-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="33cfc-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="33cfc-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-138">MAPI-Id</span></span>                | <span data-ttu-id="33cfc-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="33cfc-139">0x8145</span></span>                                           |
| <span data-ttu-id="33cfc-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="33cfc-140">System-Only</span></span>            | <span data-ttu-id="33cfc-141">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-141">False</span></span>                                            |
| <span data-ttu-id="33cfc-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33cfc-142">Is-Single-Valued</span></span>       | <span data-ttu-id="33cfc-143">True</span><span class="sxs-lookup"><span data-stu-id="33cfc-143">True</span></span>                                             |
| <span data-ttu-id="33cfc-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="33cfc-144">Is Indexed</span></span>             | <span data-ttu-id="33cfc-145">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-145">False</span></span>                                            |
| <span data-ttu-id="33cfc-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33cfc-146">In Global Catalog</span></span>      | <span data-ttu-id="33cfc-147">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-147">False</span></span>                                            |
| <span data-ttu-id="33cfc-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33cfc-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="33cfc-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33cfc-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="33cfc-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33cfc-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33cfc-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-152">Search-Flags</span></span>           | <span data-ttu-id="33cfc-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33cfc-153">0x00000000</span></span>                                       |
| <span data-ttu-id="33cfc-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-154">System-Flags</span></span>           | <span data-ttu-id="33cfc-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33cfc-155">0x00000010</span></span>                                       |
| <span data-ttu-id="33cfc-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33cfc-156">Classes used in</span></span>        | [<span data-ttu-id="33cfc-157">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="33cfc-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="33cfc-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="33cfc-158">Windows Server 2003</span></span>



| <span data-ttu-id="33cfc-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-159">Entry</span></span> | <span data-ttu-id="33cfc-160">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="33cfc-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="33cfc-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="33cfc-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-162">MAPI-Id</span></span>                | <span data-ttu-id="33cfc-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="33cfc-163">0x8145</span></span>                                           |
| <span data-ttu-id="33cfc-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="33cfc-164">System-Only</span></span>            | <span data-ttu-id="33cfc-165">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-165">False</span></span>                                            |
| <span data-ttu-id="33cfc-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33cfc-166">Is-Single-Valued</span></span>       | <span data-ttu-id="33cfc-167">True</span><span class="sxs-lookup"><span data-stu-id="33cfc-167">True</span></span>                                             |
| <span data-ttu-id="33cfc-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="33cfc-168">Is Indexed</span></span>             | <span data-ttu-id="33cfc-169">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-169">False</span></span>                                            |
| <span data-ttu-id="33cfc-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33cfc-170">In Global Catalog</span></span>      | <span data-ttu-id="33cfc-171">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-171">False</span></span>                                            |
| <span data-ttu-id="33cfc-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33cfc-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="33cfc-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33cfc-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="33cfc-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33cfc-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33cfc-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-176">Search-Flags</span></span>           | <span data-ttu-id="33cfc-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33cfc-177">0x00000000</span></span>                                       |
| <span data-ttu-id="33cfc-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-178">System-Flags</span></span>           | <span data-ttu-id="33cfc-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33cfc-179">0x00000010</span></span>                                       |
| <span data-ttu-id="33cfc-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33cfc-180">Classes used in</span></span>        | [<span data-ttu-id="33cfc-181">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="33cfc-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="33cfc-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="33cfc-182">ADAM</span></span>



| <span data-ttu-id="33cfc-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-183">Entry</span></span> | <span data-ttu-id="33cfc-184">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="33cfc-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="33cfc-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="33cfc-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-186">MAPI-Id</span></span>                | <span data-ttu-id="33cfc-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="33cfc-187">0x8145</span></span>                                           |
| <span data-ttu-id="33cfc-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="33cfc-188">System-Only</span></span>            | <span data-ttu-id="33cfc-189">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-189">False</span></span>                                            |
| <span data-ttu-id="33cfc-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33cfc-190">Is-Single-Valued</span></span>       | <span data-ttu-id="33cfc-191">True</span><span class="sxs-lookup"><span data-stu-id="33cfc-191">True</span></span>                                             |
| <span data-ttu-id="33cfc-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="33cfc-192">Is Indexed</span></span>             | <span data-ttu-id="33cfc-193">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-193">False</span></span>                                            |
| <span data-ttu-id="33cfc-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33cfc-194">In Global Catalog</span></span>      | <span data-ttu-id="33cfc-195">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-195">False</span></span>                                            |
| <span data-ttu-id="33cfc-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33cfc-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="33cfc-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33cfc-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="33cfc-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33cfc-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33cfc-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-200">Search-Flags</span></span>           | <span data-ttu-id="33cfc-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33cfc-201">0x00000000</span></span>                                       |
| <span data-ttu-id="33cfc-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-202">System-Flags</span></span>           | <span data-ttu-id="33cfc-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33cfc-203">0x00000010</span></span>                                       |
| <span data-ttu-id="33cfc-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33cfc-204">Classes used in</span></span>        | [<span data-ttu-id="33cfc-205">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="33cfc-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="33cfc-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="33cfc-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="33cfc-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-207">Entry</span></span> | <span data-ttu-id="33cfc-208">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="33cfc-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="33cfc-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="33cfc-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-210">MAPI-Id</span></span>                | <span data-ttu-id="33cfc-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="33cfc-211">0x8145</span></span>                                           |
| <span data-ttu-id="33cfc-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="33cfc-212">System-Only</span></span>            | <span data-ttu-id="33cfc-213">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-213">False</span></span>                                            |
| <span data-ttu-id="33cfc-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33cfc-214">Is-Single-Valued</span></span>       | <span data-ttu-id="33cfc-215">True</span><span class="sxs-lookup"><span data-stu-id="33cfc-215">True</span></span>                                             |
| <span data-ttu-id="33cfc-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="33cfc-216">Is Indexed</span></span>             | <span data-ttu-id="33cfc-217">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-217">False</span></span>                                            |
| <span data-ttu-id="33cfc-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33cfc-218">In Global Catalog</span></span>      | <span data-ttu-id="33cfc-219">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-219">False</span></span>                                            |
| <span data-ttu-id="33cfc-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33cfc-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="33cfc-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33cfc-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="33cfc-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33cfc-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33cfc-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-224">Search-Flags</span></span>           | <span data-ttu-id="33cfc-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33cfc-225">0x00000000</span></span>                                       |
| <span data-ttu-id="33cfc-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-226">System-Flags</span></span>           | <span data-ttu-id="33cfc-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33cfc-227">0x00000010</span></span>                                       |
| <span data-ttu-id="33cfc-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33cfc-228">Classes used in</span></span>        | [<span data-ttu-id="33cfc-229">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="33cfc-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="33cfc-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33cfc-230">Windows Server 2008</span></span>



| <span data-ttu-id="33cfc-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-231">Entry</span></span> | <span data-ttu-id="33cfc-232">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="33cfc-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="33cfc-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="33cfc-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-234">MAPI-Id</span></span>                | <span data-ttu-id="33cfc-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="33cfc-235">0x8145</span></span>                                           |
| <span data-ttu-id="33cfc-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="33cfc-236">System-Only</span></span>            | <span data-ttu-id="33cfc-237">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-237">False</span></span>                                            |
| <span data-ttu-id="33cfc-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33cfc-238">Is-Single-Valued</span></span>       | <span data-ttu-id="33cfc-239">True</span><span class="sxs-lookup"><span data-stu-id="33cfc-239">True</span></span>                                             |
| <span data-ttu-id="33cfc-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="33cfc-240">Is Indexed</span></span>             | <span data-ttu-id="33cfc-241">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-241">False</span></span>                                            |
| <span data-ttu-id="33cfc-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33cfc-242">In Global Catalog</span></span>      | <span data-ttu-id="33cfc-243">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-243">False</span></span>                                            |
| <span data-ttu-id="33cfc-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33cfc-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="33cfc-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33cfc-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="33cfc-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33cfc-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33cfc-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-248">Search-Flags</span></span>           | <span data-ttu-id="33cfc-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33cfc-249">0x00000000</span></span>                                       |
| <span data-ttu-id="33cfc-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-250">System-Flags</span></span>           | <span data-ttu-id="33cfc-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33cfc-251">0x00000010</span></span>                                       |
| <span data-ttu-id="33cfc-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33cfc-252">Classes used in</span></span>        | [<span data-ttu-id="33cfc-253">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="33cfc-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="33cfc-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33cfc-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="33cfc-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-255">Entry</span></span> | <span data-ttu-id="33cfc-256">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="33cfc-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="33cfc-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="33cfc-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-258">MAPI-Id</span></span>                | <span data-ttu-id="33cfc-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="33cfc-259">0x8145</span></span>                                           |
| <span data-ttu-id="33cfc-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="33cfc-260">System-Only</span></span>            | <span data-ttu-id="33cfc-261">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-261">False</span></span>                                            |
| <span data-ttu-id="33cfc-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33cfc-262">Is-Single-Valued</span></span>       | <span data-ttu-id="33cfc-263">True</span><span class="sxs-lookup"><span data-stu-id="33cfc-263">True</span></span>                                             |
| <span data-ttu-id="33cfc-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="33cfc-264">Is Indexed</span></span>             | <span data-ttu-id="33cfc-265">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-265">False</span></span>                                            |
| <span data-ttu-id="33cfc-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33cfc-266">In Global Catalog</span></span>      | <span data-ttu-id="33cfc-267">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-267">False</span></span>                                            |
| <span data-ttu-id="33cfc-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33cfc-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="33cfc-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33cfc-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="33cfc-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33cfc-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33cfc-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-272">Search-Flags</span></span>           | <span data-ttu-id="33cfc-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33cfc-273">0x00000000</span></span>                                       |
| <span data-ttu-id="33cfc-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-274">System-Flags</span></span>           | <span data-ttu-id="33cfc-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33cfc-275">0x00000010</span></span>                                       |
| <span data-ttu-id="33cfc-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33cfc-276">Classes used in</span></span>        | [<span data-ttu-id="33cfc-277">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="33cfc-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="33cfc-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33cfc-278">Windows Server 2012</span></span>



| <span data-ttu-id="33cfc-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="33cfc-279">Entry</span></span> | <span data-ttu-id="33cfc-280">Valor</span><span class="sxs-lookup"><span data-stu-id="33cfc-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="33cfc-281">ID do link</span><span class="sxs-lookup"><span data-stu-id="33cfc-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="33cfc-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33cfc-282">MAPI-Id</span></span>                | <span data-ttu-id="33cfc-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="33cfc-283">0x8145</span></span>                                           |
| <span data-ttu-id="33cfc-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="33cfc-284">System-Only</span></span>            | <span data-ttu-id="33cfc-285">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-285">False</span></span>                                            |
| <span data-ttu-id="33cfc-286">É de valor único</span><span class="sxs-lookup"><span data-stu-id="33cfc-286">Is-Single-Valued</span></span>       | <span data-ttu-id="33cfc-287">True</span><span class="sxs-lookup"><span data-stu-id="33cfc-287">True</span></span>                                             |
| <span data-ttu-id="33cfc-288">É indexado</span><span class="sxs-lookup"><span data-stu-id="33cfc-288">Is Indexed</span></span>             | <span data-ttu-id="33cfc-289">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-289">False</span></span>                                            |
| <span data-ttu-id="33cfc-290">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="33cfc-290">In Global Catalog</span></span>      | <span data-ttu-id="33cfc-291">Falso</span><span class="sxs-lookup"><span data-stu-id="33cfc-291">False</span></span>                                            |
| <span data-ttu-id="33cfc-292">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="33cfc-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="33cfc-293">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="33cfc-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="33cfc-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33cfc-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33cfc-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="33cfc-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-296">Search-Flags</span></span>           | <span data-ttu-id="33cfc-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33cfc-297">0x00000000</span></span>                                       |
| <span data-ttu-id="33cfc-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33cfc-298">System-Flags</span></span>           | <span data-ttu-id="33cfc-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="33cfc-299">0x00000010</span></span>                                       |
| <span data-ttu-id="33cfc-300">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="33cfc-300">Classes used in</span></span>        | [<span data-ttu-id="33cfc-301">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="33cfc-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





