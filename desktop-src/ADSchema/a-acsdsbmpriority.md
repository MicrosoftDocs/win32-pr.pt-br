---
title: ACS-DSBM-atributo de prioridade
description: Esses atributos contêm a prioridade para esse Gerenciador de largura de banda de sub-rede (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-esquema de atributo de prioridade do AD
- Esquema de AD do atributo aCSDSBMPriority
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087177"
---
# <a name="acs-dsbm-priority-attribute"></a><span data-ttu-id="77d46-105">ACS-DSBM-atributo de prioridade</span><span class="sxs-lookup"><span data-stu-id="77d46-105">ACS-DSBM-Priority attribute</span></span>

<span data-ttu-id="77d46-106">Esses atributos contêm a prioridade para esse Gerenciador de largura de banda de sub-rede (SBM).</span><span class="sxs-lookup"><span data-stu-id="77d46-106">This attributes contains the priority for this Subnet Bandwidth Manager (SBM).</span></span> <span data-ttu-id="77d46-107">Quando um novo DSBM (Gerenciador de largura de banda de sub-rede) designado precisa ser eleito, esse valor é enviado para outros SBMs no domínio como parte de uma mensagem de DSBM \_ disposta.</span><span class="sxs-lookup"><span data-stu-id="77d46-107">When a new Designated Subnet Bandwidth Manager (DSBM) needs to be elected, this value is sent to other SBMs in the domain as part of a DSBM\_willing message.</span></span> <span data-ttu-id="77d46-108">O SBM com a prioridade mais alta é eleito como o novo DSBM.</span><span class="sxs-lookup"><span data-stu-id="77d46-108">The SBM with the highest priority is elected as the new DSBM.</span></span>



| <span data-ttu-id="77d46-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="77d46-109">Entry</span></span> | <span data-ttu-id="77d46-110">Valor</span><span class="sxs-lookup"><span data-stu-id="77d46-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="77d46-111">CN</span><span class="sxs-lookup"><span data-stu-id="77d46-111">CN</span></span>                | <span data-ttu-id="77d46-112">ACS-DSBM-Priority</span><span class="sxs-lookup"><span data-stu-id="77d46-112">ACS-DSBM-Priority</span></span>                    |
| <span data-ttu-id="77d46-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="77d46-113">Ldap-Display-Name</span></span> | <span data-ttu-id="77d46-114">aCSDSBMPriority</span><span class="sxs-lookup"><span data-stu-id="77d46-114">aCSDSBMPriority</span></span>                      |
| <span data-ttu-id="77d46-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="77d46-115">Size</span></span>              | <span data-ttu-id="77d46-116">4 bytes</span><span class="sxs-lookup"><span data-stu-id="77d46-116">4 bytes</span></span>                              |
| <span data-ttu-id="77d46-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="77d46-117">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="77d46-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="77d46-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="77d46-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="77d46-119">Attribute-Id</span></span>      | <span data-ttu-id="77d46-120">1.2.840.113556.1.4.776</span><span class="sxs-lookup"><span data-stu-id="77d46-120">1.2.840.113556.1.4.776</span></span>               |
| <span data-ttu-id="77d46-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="77d46-121">System-Id-Guid</span></span>    | <span data-ttu-id="77d46-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="77d46-122">1cb3559e-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="77d46-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="77d46-123">Syntax</span></span>            | [<span data-ttu-id="77d46-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="77d46-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="77d46-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="77d46-125">Implementations</span></span>

-   [<span data-ttu-id="77d46-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="77d46-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="77d46-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="77d46-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="77d46-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="77d46-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="77d46-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="77d46-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="77d46-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="77d46-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="77d46-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="77d46-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="77d46-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77d46-132">Windows 2000 Server</span></span>



| <span data-ttu-id="77d46-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="77d46-133">Entry</span></span> | <span data-ttu-id="77d46-134">Valor</span><span class="sxs-lookup"><span data-stu-id="77d46-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77d46-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="77d46-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77d46-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="77d46-137">System-Only</span></span>            | <span data-ttu-id="77d46-138">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-138">False</span></span>                                        |
| <span data-ttu-id="77d46-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77d46-139">Is-Single-Valued</span></span>       | <span data-ttu-id="77d46-140">True</span><span class="sxs-lookup"><span data-stu-id="77d46-140">True</span></span>                                         |
| <span data-ttu-id="77d46-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="77d46-141">Is Indexed</span></span>             | <span data-ttu-id="77d46-142">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-142">False</span></span>                                        |
| <span data-ttu-id="77d46-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77d46-143">In Global Catalog</span></span>      | <span data-ttu-id="77d46-144">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-144">False</span></span>                                        |
| <span data-ttu-id="77d46-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77d46-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="77d46-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77d46-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77d46-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77d46-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77d46-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77d46-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77d46-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-149">Search-Flags</span></span>           | <span data-ttu-id="77d46-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77d46-150">0x00000000</span></span>                                   |
| <span data-ttu-id="77d46-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-151">System-Flags</span></span>           | <span data-ttu-id="77d46-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77d46-152">0x00000010</span></span>                                   |
| <span data-ttu-id="77d46-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77d46-153">Classes used in</span></span>        | [<span data-ttu-id="77d46-154">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="77d46-154">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="77d46-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77d46-155">Windows Server 2003</span></span>



| <span data-ttu-id="77d46-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="77d46-156">Entry</span></span> | <span data-ttu-id="77d46-157">Valor</span><span class="sxs-lookup"><span data-stu-id="77d46-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77d46-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="77d46-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77d46-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="77d46-160">System-Only</span></span>            | <span data-ttu-id="77d46-161">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-161">False</span></span>                                        |
| <span data-ttu-id="77d46-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77d46-162">Is-Single-Valued</span></span>       | <span data-ttu-id="77d46-163">True</span><span class="sxs-lookup"><span data-stu-id="77d46-163">True</span></span>                                         |
| <span data-ttu-id="77d46-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="77d46-164">Is Indexed</span></span>             | <span data-ttu-id="77d46-165">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-165">False</span></span>                                        |
| <span data-ttu-id="77d46-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77d46-166">In Global Catalog</span></span>      | <span data-ttu-id="77d46-167">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-167">False</span></span>                                        |
| <span data-ttu-id="77d46-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77d46-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="77d46-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77d46-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77d46-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77d46-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77d46-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77d46-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77d46-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-172">Search-Flags</span></span>           | <span data-ttu-id="77d46-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77d46-173">0x00000000</span></span>                                   |
| <span data-ttu-id="77d46-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-174">System-Flags</span></span>           | <span data-ttu-id="77d46-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77d46-175">0x00000010</span></span>                                   |
| <span data-ttu-id="77d46-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77d46-176">Classes used in</span></span>        | [<span data-ttu-id="77d46-177">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="77d46-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="77d46-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="77d46-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="77d46-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="77d46-179">Entry</span></span> | <span data-ttu-id="77d46-180">Valor</span><span class="sxs-lookup"><span data-stu-id="77d46-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77d46-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="77d46-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77d46-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="77d46-183">System-Only</span></span>            | <span data-ttu-id="77d46-184">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-184">False</span></span>                                        |
| <span data-ttu-id="77d46-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77d46-185">Is-Single-Valued</span></span>       | <span data-ttu-id="77d46-186">True</span><span class="sxs-lookup"><span data-stu-id="77d46-186">True</span></span>                                         |
| <span data-ttu-id="77d46-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="77d46-187">Is Indexed</span></span>             | <span data-ttu-id="77d46-188">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-188">False</span></span>                                        |
| <span data-ttu-id="77d46-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77d46-189">In Global Catalog</span></span>      | <span data-ttu-id="77d46-190">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-190">False</span></span>                                        |
| <span data-ttu-id="77d46-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77d46-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="77d46-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77d46-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77d46-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77d46-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77d46-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77d46-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77d46-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-195">Search-Flags</span></span>           | <span data-ttu-id="77d46-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77d46-196">0x00000000</span></span>                                   |
| <span data-ttu-id="77d46-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-197">System-Flags</span></span>           | <span data-ttu-id="77d46-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77d46-198">0x00000010</span></span>                                   |
| <span data-ttu-id="77d46-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77d46-199">Classes used in</span></span>        | [<span data-ttu-id="77d46-200">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="77d46-200">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="77d46-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77d46-201">Windows Server 2008</span></span>



| <span data-ttu-id="77d46-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="77d46-202">Entry</span></span> | <span data-ttu-id="77d46-203">Valor</span><span class="sxs-lookup"><span data-stu-id="77d46-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77d46-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="77d46-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77d46-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="77d46-206">System-Only</span></span>            | <span data-ttu-id="77d46-207">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-207">False</span></span>                                        |
| <span data-ttu-id="77d46-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77d46-208">Is-Single-Valued</span></span>       | <span data-ttu-id="77d46-209">True</span><span class="sxs-lookup"><span data-stu-id="77d46-209">True</span></span>                                         |
| <span data-ttu-id="77d46-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="77d46-210">Is Indexed</span></span>             | <span data-ttu-id="77d46-211">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-211">False</span></span>                                        |
| <span data-ttu-id="77d46-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77d46-212">In Global Catalog</span></span>      | <span data-ttu-id="77d46-213">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-213">False</span></span>                                        |
| <span data-ttu-id="77d46-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77d46-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="77d46-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77d46-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77d46-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77d46-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77d46-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77d46-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77d46-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-218">Search-Flags</span></span>           | <span data-ttu-id="77d46-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77d46-219">0x00000000</span></span>                                   |
| <span data-ttu-id="77d46-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-220">System-Flags</span></span>           | <span data-ttu-id="77d46-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77d46-221">0x00000010</span></span>                                   |
| <span data-ttu-id="77d46-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77d46-222">Classes used in</span></span>        | [<span data-ttu-id="77d46-223">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="77d46-223">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="77d46-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77d46-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="77d46-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="77d46-225">Entry</span></span> | <span data-ttu-id="77d46-226">Valor</span><span class="sxs-lookup"><span data-stu-id="77d46-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77d46-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="77d46-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77d46-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="77d46-229">System-Only</span></span>            | <span data-ttu-id="77d46-230">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-230">False</span></span>                                        |
| <span data-ttu-id="77d46-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77d46-231">Is-Single-Valued</span></span>       | <span data-ttu-id="77d46-232">True</span><span class="sxs-lookup"><span data-stu-id="77d46-232">True</span></span>                                         |
| <span data-ttu-id="77d46-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="77d46-233">Is Indexed</span></span>             | <span data-ttu-id="77d46-234">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-234">False</span></span>                                        |
| <span data-ttu-id="77d46-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77d46-235">In Global Catalog</span></span>      | <span data-ttu-id="77d46-236">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-236">False</span></span>                                        |
| <span data-ttu-id="77d46-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77d46-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="77d46-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77d46-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77d46-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77d46-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77d46-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77d46-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77d46-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-241">Search-Flags</span></span>           | <span data-ttu-id="77d46-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77d46-242">0x00000000</span></span>                                   |
| <span data-ttu-id="77d46-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-243">System-Flags</span></span>           | <span data-ttu-id="77d46-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77d46-244">0x00000010</span></span>                                   |
| <span data-ttu-id="77d46-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77d46-245">Classes used in</span></span>        | [<span data-ttu-id="77d46-246">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="77d46-246">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="77d46-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77d46-247">Windows Server 2012</span></span>



| <span data-ttu-id="77d46-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="77d46-248">Entry</span></span> | <span data-ttu-id="77d46-249">Valor</span><span class="sxs-lookup"><span data-stu-id="77d46-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="77d46-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="77d46-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77d46-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="77d46-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="77d46-252">System-Only</span></span>            | <span data-ttu-id="77d46-253">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-253">False</span></span>                                        |
| <span data-ttu-id="77d46-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77d46-254">Is-Single-Valued</span></span>       | <span data-ttu-id="77d46-255">True</span><span class="sxs-lookup"><span data-stu-id="77d46-255">True</span></span>                                         |
| <span data-ttu-id="77d46-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="77d46-256">Is Indexed</span></span>             | <span data-ttu-id="77d46-257">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-257">False</span></span>                                        |
| <span data-ttu-id="77d46-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77d46-258">In Global Catalog</span></span>      | <span data-ttu-id="77d46-259">Falso</span><span class="sxs-lookup"><span data-stu-id="77d46-259">False</span></span>                                        |
| <span data-ttu-id="77d46-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77d46-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="77d46-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77d46-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="77d46-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77d46-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="77d46-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77d46-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="77d46-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-264">Search-Flags</span></span>           | <span data-ttu-id="77d46-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77d46-265">0x00000000</span></span>                                   |
| <span data-ttu-id="77d46-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77d46-266">System-Flags</span></span>           | <span data-ttu-id="77d46-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77d46-267">0x00000010</span></span>                                   |
| <span data-ttu-id="77d46-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77d46-268">Classes used in</span></span>        | [<span data-ttu-id="77d46-269">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="77d46-269">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





