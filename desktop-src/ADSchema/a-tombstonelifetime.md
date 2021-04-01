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
# <a name="tombstone-lifetime-attribute"></a><span data-ttu-id="dff8e-105">Tombstone-Lifetime atributo</span><span class="sxs-lookup"><span data-stu-id="dff8e-105">Tombstone-Lifetime attribute</span></span>

<span data-ttu-id="dff8e-106">O número de dias antes que um objeto excluído seja removido dos serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="dff8e-106">The number of days before a deleted object is removed from the directory services.</span></span> <span data-ttu-id="dff8e-107">Isso ajuda a remover objetos de servidores replicados e a impedir que as restaurações reintroduzam um objeto excluído.</span><span class="sxs-lookup"><span data-stu-id="dff8e-107">This assists in removing objects from replicated servers and preventing restores from reintroducing a deleted object.</span></span> <span data-ttu-id="dff8e-108">Esse valor está no objeto de serviço de diretório na NIC de configuração.</span><span class="sxs-lookup"><span data-stu-id="dff8e-108">This value is in the Directory Service object in the configuration NIC.</span></span>



| <span data-ttu-id="dff8e-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-109">Entry</span></span> | <span data-ttu-id="dff8e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-110">Value</span></span> |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="dff8e-111">CN</span><span class="sxs-lookup"><span data-stu-id="dff8e-111">CN</span></span>                | <span data-ttu-id="dff8e-112">Tombstone-Lifetime</span><span class="sxs-lookup"><span data-stu-id="dff8e-112">Tombstone-Lifetime</span></span>                                        |
| <span data-ttu-id="dff8e-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="dff8e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dff8e-114">tombstoneLifetime</span><span class="sxs-lookup"><span data-stu-id="dff8e-114">tombstoneLifetime</span></span>                                         |
| <span data-ttu-id="dff8e-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="dff8e-115">Size</span></span>              | <span data-ttu-id="dff8e-116">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="dff8e-116">4 bytes.</span></span> <span data-ttu-id="dff8e-117">O padrão é 60 dias quando nenhum valor é inserido.</span><span class="sxs-lookup"><span data-stu-id="dff8e-117">The default is 60 days when no value is entered.</span></span> |
| <span data-ttu-id="dff8e-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="dff8e-118">Update Privilege</span></span>  | \-                                                        |
| <span data-ttu-id="dff8e-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="dff8e-119">Update Frequency</span></span>  | \-                                                        |
| <span data-ttu-id="dff8e-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-120">Attribute-Id</span></span>      | <span data-ttu-id="dff8e-121">1.2.840.113556.1.2.54</span><span class="sxs-lookup"><span data-stu-id="dff8e-121">1.2.840.113556.1.2.54</span></span>                                     |
| <span data-ttu-id="dff8e-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="dff8e-122">System-Id-Guid</span></span>    | <span data-ttu-id="dff8e-123">16c3a860-1273-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="dff8e-123">16c3a860-1273-11d0-a060-00aa006c33ed</span></span>                      |
| <span data-ttu-id="dff8e-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="dff8e-124">Syntax</span></span>            | [<span data-ttu-id="dff8e-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="dff8e-125">**Enumeration**</span></span>](s-enumeration.md)                      |



## <a name="implementations"></a><span data-ttu-id="dff8e-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="dff8e-126">Implementations</span></span>

-   [<span data-ttu-id="dff8e-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dff8e-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dff8e-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dff8e-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dff8e-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="dff8e-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dff8e-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dff8e-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dff8e-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dff8e-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dff8e-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dff8e-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dff8e-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dff8e-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dff8e-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dff8e-134">Windows 2000 Server</span></span>



| <span data-ttu-id="dff8e-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-135">Entry</span></span> | <span data-ttu-id="dff8e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-136">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dff8e-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="dff8e-137">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dff8e-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-138">MAPI-Id</span></span>                | <span data-ttu-id="dff8e-139">0x8145</span><span class="sxs-lookup"><span data-stu-id="dff8e-139">0x8145</span></span>                                           |
| <span data-ttu-id="dff8e-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="dff8e-140">System-Only</span></span>            | <span data-ttu-id="dff8e-141">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-141">False</span></span>                                            |
| <span data-ttu-id="dff8e-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dff8e-142">Is-Single-Valued</span></span>       | <span data-ttu-id="dff8e-143">True</span><span class="sxs-lookup"><span data-stu-id="dff8e-143">True</span></span>                                             |
| <span data-ttu-id="dff8e-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="dff8e-144">Is Indexed</span></span>             | <span data-ttu-id="dff8e-145">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-145">False</span></span>                                            |
| <span data-ttu-id="dff8e-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dff8e-146">In Global Catalog</span></span>      | <span data-ttu-id="dff8e-147">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-147">False</span></span>                                            |
| <span data-ttu-id="dff8e-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dff8e-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="dff8e-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dff8e-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dff8e-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dff8e-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dff8e-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-152">Search-Flags</span></span>           | <span data-ttu-id="dff8e-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff8e-153">0x00000000</span></span>                                       |
| <span data-ttu-id="dff8e-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-154">System-Flags</span></span>           | <span data-ttu-id="dff8e-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dff8e-155">0x00000010</span></span>                                       |
| <span data-ttu-id="dff8e-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dff8e-156">Classes used in</span></span>        | [<span data-ttu-id="dff8e-157">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="dff8e-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dff8e-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dff8e-158">Windows Server 2003</span></span>



| <span data-ttu-id="dff8e-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-159">Entry</span></span> | <span data-ttu-id="dff8e-160">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dff8e-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="dff8e-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dff8e-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-162">MAPI-Id</span></span>                | <span data-ttu-id="dff8e-163">0x8145</span><span class="sxs-lookup"><span data-stu-id="dff8e-163">0x8145</span></span>                                           |
| <span data-ttu-id="dff8e-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="dff8e-164">System-Only</span></span>            | <span data-ttu-id="dff8e-165">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-165">False</span></span>                                            |
| <span data-ttu-id="dff8e-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dff8e-166">Is-Single-Valued</span></span>       | <span data-ttu-id="dff8e-167">True</span><span class="sxs-lookup"><span data-stu-id="dff8e-167">True</span></span>                                             |
| <span data-ttu-id="dff8e-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="dff8e-168">Is Indexed</span></span>             | <span data-ttu-id="dff8e-169">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-169">False</span></span>                                            |
| <span data-ttu-id="dff8e-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dff8e-170">In Global Catalog</span></span>      | <span data-ttu-id="dff8e-171">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-171">False</span></span>                                            |
| <span data-ttu-id="dff8e-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dff8e-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="dff8e-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dff8e-173">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dff8e-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dff8e-174">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dff8e-175">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-176">Search-Flags</span></span>           | <span data-ttu-id="dff8e-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff8e-177">0x00000000</span></span>                                       |
| <span data-ttu-id="dff8e-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-178">System-Flags</span></span>           | <span data-ttu-id="dff8e-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dff8e-179">0x00000010</span></span>                                       |
| <span data-ttu-id="dff8e-180">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dff8e-180">Classes used in</span></span>        | [<span data-ttu-id="dff8e-181">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="dff8e-181">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dff8e-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="dff8e-182">ADAM</span></span>



| <span data-ttu-id="dff8e-183">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-183">Entry</span></span> | <span data-ttu-id="dff8e-184">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-184">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dff8e-185">ID do link</span><span class="sxs-lookup"><span data-stu-id="dff8e-185">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dff8e-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-186">MAPI-Id</span></span>                | <span data-ttu-id="dff8e-187">0x8145</span><span class="sxs-lookup"><span data-stu-id="dff8e-187">0x8145</span></span>                                           |
| <span data-ttu-id="dff8e-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="dff8e-188">System-Only</span></span>            | <span data-ttu-id="dff8e-189">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-189">False</span></span>                                            |
| <span data-ttu-id="dff8e-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dff8e-190">Is-Single-Valued</span></span>       | <span data-ttu-id="dff8e-191">True</span><span class="sxs-lookup"><span data-stu-id="dff8e-191">True</span></span>                                             |
| <span data-ttu-id="dff8e-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="dff8e-192">Is Indexed</span></span>             | <span data-ttu-id="dff8e-193">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-193">False</span></span>                                            |
| <span data-ttu-id="dff8e-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dff8e-194">In Global Catalog</span></span>      | <span data-ttu-id="dff8e-195">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-195">False</span></span>                                            |
| <span data-ttu-id="dff8e-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dff8e-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="dff8e-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dff8e-197">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dff8e-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dff8e-198">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dff8e-199">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-200">Search-Flags</span></span>           | <span data-ttu-id="dff8e-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff8e-201">0x00000000</span></span>                                       |
| <span data-ttu-id="dff8e-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-202">System-Flags</span></span>           | <span data-ttu-id="dff8e-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dff8e-203">0x00000010</span></span>                                       |
| <span data-ttu-id="dff8e-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dff8e-204">Classes used in</span></span>        | [<span data-ttu-id="dff8e-205">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="dff8e-205">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dff8e-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dff8e-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dff8e-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-207">Entry</span></span> | <span data-ttu-id="dff8e-208">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-208">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dff8e-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="dff8e-209">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dff8e-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-210">MAPI-Id</span></span>                | <span data-ttu-id="dff8e-211">0x8145</span><span class="sxs-lookup"><span data-stu-id="dff8e-211">0x8145</span></span>                                           |
| <span data-ttu-id="dff8e-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="dff8e-212">System-Only</span></span>            | <span data-ttu-id="dff8e-213">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-213">False</span></span>                                            |
| <span data-ttu-id="dff8e-214">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dff8e-214">Is-Single-Valued</span></span>       | <span data-ttu-id="dff8e-215">True</span><span class="sxs-lookup"><span data-stu-id="dff8e-215">True</span></span>                                             |
| <span data-ttu-id="dff8e-216">É indexado</span><span class="sxs-lookup"><span data-stu-id="dff8e-216">Is Indexed</span></span>             | <span data-ttu-id="dff8e-217">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-217">False</span></span>                                            |
| <span data-ttu-id="dff8e-218">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dff8e-218">In Global Catalog</span></span>      | <span data-ttu-id="dff8e-219">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-219">False</span></span>                                            |
| <span data-ttu-id="dff8e-220">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dff8e-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="dff8e-221">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dff8e-221">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dff8e-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dff8e-222">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dff8e-223">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-224">Search-Flags</span></span>           | <span data-ttu-id="dff8e-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff8e-225">0x00000000</span></span>                                       |
| <span data-ttu-id="dff8e-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-226">System-Flags</span></span>           | <span data-ttu-id="dff8e-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dff8e-227">0x00000010</span></span>                                       |
| <span data-ttu-id="dff8e-228">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dff8e-228">Classes used in</span></span>        | [<span data-ttu-id="dff8e-229">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="dff8e-229">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dff8e-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dff8e-230">Windows Server 2008</span></span>



| <span data-ttu-id="dff8e-231">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-231">Entry</span></span> | <span data-ttu-id="dff8e-232">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-232">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dff8e-233">ID do link</span><span class="sxs-lookup"><span data-stu-id="dff8e-233">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dff8e-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-234">MAPI-Id</span></span>                | <span data-ttu-id="dff8e-235">0x8145</span><span class="sxs-lookup"><span data-stu-id="dff8e-235">0x8145</span></span>                                           |
| <span data-ttu-id="dff8e-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="dff8e-236">System-Only</span></span>            | <span data-ttu-id="dff8e-237">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-237">False</span></span>                                            |
| <span data-ttu-id="dff8e-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dff8e-238">Is-Single-Valued</span></span>       | <span data-ttu-id="dff8e-239">True</span><span class="sxs-lookup"><span data-stu-id="dff8e-239">True</span></span>                                             |
| <span data-ttu-id="dff8e-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="dff8e-240">Is Indexed</span></span>             | <span data-ttu-id="dff8e-241">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-241">False</span></span>                                            |
| <span data-ttu-id="dff8e-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dff8e-242">In Global Catalog</span></span>      | <span data-ttu-id="dff8e-243">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-243">False</span></span>                                            |
| <span data-ttu-id="dff8e-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dff8e-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="dff8e-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dff8e-245">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dff8e-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dff8e-246">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dff8e-247">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-248">Search-Flags</span></span>           | <span data-ttu-id="dff8e-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff8e-249">0x00000000</span></span>                                       |
| <span data-ttu-id="dff8e-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-250">System-Flags</span></span>           | <span data-ttu-id="dff8e-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dff8e-251">0x00000010</span></span>                                       |
| <span data-ttu-id="dff8e-252">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dff8e-252">Classes used in</span></span>        | [<span data-ttu-id="dff8e-253">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="dff8e-253">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dff8e-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dff8e-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dff8e-255">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-255">Entry</span></span> | <span data-ttu-id="dff8e-256">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-256">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dff8e-257">ID do link</span><span class="sxs-lookup"><span data-stu-id="dff8e-257">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dff8e-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-258">MAPI-Id</span></span>                | <span data-ttu-id="dff8e-259">0x8145</span><span class="sxs-lookup"><span data-stu-id="dff8e-259">0x8145</span></span>                                           |
| <span data-ttu-id="dff8e-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="dff8e-260">System-Only</span></span>            | <span data-ttu-id="dff8e-261">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-261">False</span></span>                                            |
| <span data-ttu-id="dff8e-262">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dff8e-262">Is-Single-Valued</span></span>       | <span data-ttu-id="dff8e-263">True</span><span class="sxs-lookup"><span data-stu-id="dff8e-263">True</span></span>                                             |
| <span data-ttu-id="dff8e-264">É indexado</span><span class="sxs-lookup"><span data-stu-id="dff8e-264">Is Indexed</span></span>             | <span data-ttu-id="dff8e-265">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-265">False</span></span>                                            |
| <span data-ttu-id="dff8e-266">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dff8e-266">In Global Catalog</span></span>      | <span data-ttu-id="dff8e-267">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-267">False</span></span>                                            |
| <span data-ttu-id="dff8e-268">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dff8e-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="dff8e-269">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dff8e-269">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dff8e-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dff8e-270">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dff8e-271">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-272">Search-Flags</span></span>           | <span data-ttu-id="dff8e-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff8e-273">0x00000000</span></span>                                       |
| <span data-ttu-id="dff8e-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-274">System-Flags</span></span>           | <span data-ttu-id="dff8e-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dff8e-275">0x00000010</span></span>                                       |
| <span data-ttu-id="dff8e-276">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dff8e-276">Classes used in</span></span>        | [<span data-ttu-id="dff8e-277">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="dff8e-277">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dff8e-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dff8e-278">Windows Server 2012</span></span>



| <span data-ttu-id="dff8e-279">Entrada</span><span class="sxs-lookup"><span data-stu-id="dff8e-279">Entry</span></span> | <span data-ttu-id="dff8e-280">Valor</span><span class="sxs-lookup"><span data-stu-id="dff8e-280">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="dff8e-281">ID do link</span><span class="sxs-lookup"><span data-stu-id="dff8e-281">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="dff8e-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dff8e-282">MAPI-Id</span></span>                | <span data-ttu-id="dff8e-283">0x8145</span><span class="sxs-lookup"><span data-stu-id="dff8e-283">0x8145</span></span>                                           |
| <span data-ttu-id="dff8e-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="dff8e-284">System-Only</span></span>            | <span data-ttu-id="dff8e-285">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-285">False</span></span>                                            |
| <span data-ttu-id="dff8e-286">É de valor único</span><span class="sxs-lookup"><span data-stu-id="dff8e-286">Is-Single-Valued</span></span>       | <span data-ttu-id="dff8e-287">True</span><span class="sxs-lookup"><span data-stu-id="dff8e-287">True</span></span>                                             |
| <span data-ttu-id="dff8e-288">É indexado</span><span class="sxs-lookup"><span data-stu-id="dff8e-288">Is Indexed</span></span>             | <span data-ttu-id="dff8e-289">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-289">False</span></span>                                            |
| <span data-ttu-id="dff8e-290">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="dff8e-290">In Global Catalog</span></span>      | <span data-ttu-id="dff8e-291">Falso</span><span class="sxs-lookup"><span data-stu-id="dff8e-291">False</span></span>                                            |
| <span data-ttu-id="dff8e-292">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="dff8e-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="dff8e-293">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="dff8e-293">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="dff8e-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dff8e-294">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dff8e-295">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="dff8e-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-296">Search-Flags</span></span>           | <span data-ttu-id="dff8e-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dff8e-297">0x00000000</span></span>                                       |
| <span data-ttu-id="dff8e-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dff8e-298">System-Flags</span></span>           | <span data-ttu-id="dff8e-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dff8e-299">0x00000010</span></span>                                       |
| <span data-ttu-id="dff8e-300">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="dff8e-300">Classes used in</span></span>        | [<span data-ttu-id="dff8e-301">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="dff8e-301">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





