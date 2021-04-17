---
title: ACS – atributo non-reserved-TX-Limit
description: A largura de banda máxima que um aplicativo de usuário pode transmitir antes que uma reserva esteja em vigor.
ms.assetid: 5ead8e5b-31e8-438e-8d1b-9aae8601dfc9
ms.tgt_platform: multiple
keywords:
- ACS-esquema não reservado-TX-limite de atributos do AD
- Esquema de AD do atributo aCSNonReservedTxLimit
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999b1775640624b7825b38ae1632d70773bc75b3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105811192"
---
# <a name="acs-non-reserved-tx-limit-attribute"></a><span data-ttu-id="2958c-105">ACS – atributo non-reserved-TX-Limit</span><span class="sxs-lookup"><span data-stu-id="2958c-105">ACS-Non-Reserved-Tx-Limit attribute</span></span>

<span data-ttu-id="2958c-106">A largura de banda máxima que um aplicativo de usuário pode transmitir antes que uma reserva esteja em vigor.</span><span class="sxs-lookup"><span data-stu-id="2958c-106">The maximum bandwidth a user application can transmit before a reservation is in place.</span></span>



| <span data-ttu-id="2958c-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="2958c-107">Entry</span></span> | <span data-ttu-id="2958c-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2958c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2958c-109">CN</span><span class="sxs-lookup"><span data-stu-id="2958c-109">CN</span></span>                | <span data-ttu-id="2958c-110">ACS-não reservado-TX-Limit</span><span class="sxs-lookup"><span data-stu-id="2958c-110">ACS-Non-Reserved-Tx-Limit</span></span>            |
| <span data-ttu-id="2958c-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="2958c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2958c-112">aCSNonReservedTxLimit</span><span class="sxs-lookup"><span data-stu-id="2958c-112">aCSNonReservedTxLimit</span></span>                |
| <span data-ttu-id="2958c-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2958c-113">Size</span></span>              | <span data-ttu-id="2958c-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="2958c-114">8 bytes</span></span>                              |
| <span data-ttu-id="2958c-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="2958c-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2958c-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="2958c-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2958c-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2958c-117">Attribute-Id</span></span>      | <span data-ttu-id="2958c-118">1.2.840.113556.1.4.780</span><span class="sxs-lookup"><span data-stu-id="2958c-118">1.2.840.113556.1.4.780</span></span>               |
| <span data-ttu-id="2958c-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="2958c-119">System-Id-Guid</span></span>    | <span data-ttu-id="2958c-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2958c-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="2958c-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="2958c-121">Syntax</span></span>            | [<span data-ttu-id="2958c-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="2958c-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="2958c-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="2958c-123">Implementations</span></span>

-   [<span data-ttu-id="2958c-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2958c-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2958c-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2958c-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2958c-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2958c-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2958c-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2958c-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2958c-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2958c-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2958c-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2958c-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2958c-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2958c-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2958c-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="2958c-131">Entry</span></span> | <span data-ttu-id="2958c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2958c-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2958c-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="2958c-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2958c-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2958c-135">System-Only</span></span>            | <span data-ttu-id="2958c-136">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-136">False</span></span>                                        |
| <span data-ttu-id="2958c-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2958c-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2958c-138">True</span><span class="sxs-lookup"><span data-stu-id="2958c-138">True</span></span>                                         |
| <span data-ttu-id="2958c-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="2958c-139">Is Indexed</span></span>             | <span data-ttu-id="2958c-140">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-140">False</span></span>                                        |
| <span data-ttu-id="2958c-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2958c-141">In Global Catalog</span></span>      | <span data-ttu-id="2958c-142">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-142">False</span></span>                                        |
| <span data-ttu-id="2958c-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2958c-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2958c-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2958c-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2958c-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2958c-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2958c-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2958c-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2958c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-147">Search-Flags</span></span>           | <span data-ttu-id="2958c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2958c-148">0x00000000</span></span>                                   |
| <span data-ttu-id="2958c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-149">System-Flags</span></span>           | <span data-ttu-id="2958c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2958c-150">0x00000010</span></span>                                   |
| <span data-ttu-id="2958c-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2958c-151">Classes used in</span></span>        | [<span data-ttu-id="2958c-152">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2958c-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2958c-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2958c-153">Windows Server 2003</span></span>



| <span data-ttu-id="2958c-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="2958c-154">Entry</span></span> | <span data-ttu-id="2958c-155">Valor</span><span class="sxs-lookup"><span data-stu-id="2958c-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2958c-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="2958c-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2958c-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2958c-158">System-Only</span></span>            | <span data-ttu-id="2958c-159">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-159">False</span></span>                                        |
| <span data-ttu-id="2958c-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2958c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2958c-161">True</span><span class="sxs-lookup"><span data-stu-id="2958c-161">True</span></span>                                         |
| <span data-ttu-id="2958c-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="2958c-162">Is Indexed</span></span>             | <span data-ttu-id="2958c-163">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-163">False</span></span>                                        |
| <span data-ttu-id="2958c-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2958c-164">In Global Catalog</span></span>      | <span data-ttu-id="2958c-165">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-165">False</span></span>                                        |
| <span data-ttu-id="2958c-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2958c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2958c-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2958c-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2958c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2958c-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2958c-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2958c-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2958c-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-170">Search-Flags</span></span>           | <span data-ttu-id="2958c-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2958c-171">0x00000000</span></span>                                   |
| <span data-ttu-id="2958c-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-172">System-Flags</span></span>           | <span data-ttu-id="2958c-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2958c-173">0x00000010</span></span>                                   |
| <span data-ttu-id="2958c-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2958c-174">Classes used in</span></span>        | [<span data-ttu-id="2958c-175">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2958c-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2958c-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2958c-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2958c-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="2958c-177">Entry</span></span> | <span data-ttu-id="2958c-178">Valor</span><span class="sxs-lookup"><span data-stu-id="2958c-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2958c-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="2958c-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2958c-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2958c-181">System-Only</span></span>            | <span data-ttu-id="2958c-182">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-182">False</span></span>                                        |
| <span data-ttu-id="2958c-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2958c-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2958c-184">True</span><span class="sxs-lookup"><span data-stu-id="2958c-184">True</span></span>                                         |
| <span data-ttu-id="2958c-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="2958c-185">Is Indexed</span></span>             | <span data-ttu-id="2958c-186">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-186">False</span></span>                                        |
| <span data-ttu-id="2958c-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2958c-187">In Global Catalog</span></span>      | <span data-ttu-id="2958c-188">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-188">False</span></span>                                        |
| <span data-ttu-id="2958c-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2958c-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2958c-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2958c-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2958c-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2958c-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2958c-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2958c-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2958c-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-193">Search-Flags</span></span>           | <span data-ttu-id="2958c-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2958c-194">0x00000000</span></span>                                   |
| <span data-ttu-id="2958c-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-195">System-Flags</span></span>           | <span data-ttu-id="2958c-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2958c-196">0x00000010</span></span>                                   |
| <span data-ttu-id="2958c-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2958c-197">Classes used in</span></span>        | [<span data-ttu-id="2958c-198">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2958c-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2958c-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2958c-199">Windows Server 2008</span></span>



| <span data-ttu-id="2958c-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="2958c-200">Entry</span></span> | <span data-ttu-id="2958c-201">Valor</span><span class="sxs-lookup"><span data-stu-id="2958c-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2958c-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="2958c-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2958c-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2958c-204">System-Only</span></span>            | <span data-ttu-id="2958c-205">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-205">False</span></span>                                        |
| <span data-ttu-id="2958c-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2958c-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2958c-207">True</span><span class="sxs-lookup"><span data-stu-id="2958c-207">True</span></span>                                         |
| <span data-ttu-id="2958c-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="2958c-208">Is Indexed</span></span>             | <span data-ttu-id="2958c-209">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-209">False</span></span>                                        |
| <span data-ttu-id="2958c-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2958c-210">In Global Catalog</span></span>      | <span data-ttu-id="2958c-211">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-211">False</span></span>                                        |
| <span data-ttu-id="2958c-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2958c-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2958c-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2958c-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2958c-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2958c-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2958c-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2958c-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2958c-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-216">Search-Flags</span></span>           | <span data-ttu-id="2958c-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2958c-217">0x00000000</span></span>                                   |
| <span data-ttu-id="2958c-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-218">System-Flags</span></span>           | <span data-ttu-id="2958c-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2958c-219">0x00000010</span></span>                                   |
| <span data-ttu-id="2958c-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2958c-220">Classes used in</span></span>        | [<span data-ttu-id="2958c-221">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2958c-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2958c-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2958c-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2958c-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="2958c-223">Entry</span></span> | <span data-ttu-id="2958c-224">Valor</span><span class="sxs-lookup"><span data-stu-id="2958c-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2958c-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="2958c-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2958c-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2958c-227">System-Only</span></span>            | <span data-ttu-id="2958c-228">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-228">False</span></span>                                        |
| <span data-ttu-id="2958c-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2958c-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2958c-230">True</span><span class="sxs-lookup"><span data-stu-id="2958c-230">True</span></span>                                         |
| <span data-ttu-id="2958c-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="2958c-231">Is Indexed</span></span>             | <span data-ttu-id="2958c-232">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-232">False</span></span>                                        |
| <span data-ttu-id="2958c-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2958c-233">In Global Catalog</span></span>      | <span data-ttu-id="2958c-234">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-234">False</span></span>                                        |
| <span data-ttu-id="2958c-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2958c-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2958c-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2958c-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2958c-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2958c-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2958c-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2958c-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2958c-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-239">Search-Flags</span></span>           | <span data-ttu-id="2958c-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2958c-240">0x00000000</span></span>                                   |
| <span data-ttu-id="2958c-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-241">System-Flags</span></span>           | <span data-ttu-id="2958c-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2958c-242">0x00000010</span></span>                                   |
| <span data-ttu-id="2958c-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2958c-243">Classes used in</span></span>        | [<span data-ttu-id="2958c-244">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2958c-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2958c-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2958c-245">Windows Server 2012</span></span>



| <span data-ttu-id="2958c-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="2958c-246">Entry</span></span> | <span data-ttu-id="2958c-247">Valor</span><span class="sxs-lookup"><span data-stu-id="2958c-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="2958c-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="2958c-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2958c-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="2958c-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2958c-250">System-Only</span></span>            | <span data-ttu-id="2958c-251">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-251">False</span></span>                                        |
| <span data-ttu-id="2958c-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="2958c-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2958c-253">True</span><span class="sxs-lookup"><span data-stu-id="2958c-253">True</span></span>                                         |
| <span data-ttu-id="2958c-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="2958c-254">Is Indexed</span></span>             | <span data-ttu-id="2958c-255">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-255">False</span></span>                                        |
| <span data-ttu-id="2958c-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="2958c-256">In Global Catalog</span></span>      | <span data-ttu-id="2958c-257">Falso</span><span class="sxs-lookup"><span data-stu-id="2958c-257">False</span></span>                                        |
| <span data-ttu-id="2958c-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="2958c-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2958c-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="2958c-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="2958c-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2958c-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="2958c-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2958c-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="2958c-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-262">Search-Flags</span></span>           | <span data-ttu-id="2958c-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2958c-263">0x00000000</span></span>                                   |
| <span data-ttu-id="2958c-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2958c-264">System-Flags</span></span>           | <span data-ttu-id="2958c-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2958c-265">0x00000010</span></span>                                   |
| <span data-ttu-id="2958c-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="2958c-266">Classes used in</span></span>        | [<span data-ttu-id="2958c-267">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="2958c-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





