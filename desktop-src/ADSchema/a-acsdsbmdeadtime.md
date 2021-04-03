---
title: ACS-DSBM-atributo de inatividade
description: Esse atributo contém o DSBMDeadInterval (intervalo de tempo inativo de eleição) para um domínio.
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- ACS-DSBM-inatividade do esquema de atributo do AD
- Esquema de AD do atributo aCSDSBMDeadTime
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8b1c980175dc985c3a718d15323be0b8d1b411
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086776"
---
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="c0d63-105">ACS-DSBM-atributo de inatividade</span><span class="sxs-lookup"><span data-stu-id="c0d63-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="c0d63-106">Esse atributo contém o DSBMDeadInterval (intervalo de tempo inativo de eleição) para um domínio.</span><span class="sxs-lookup"><span data-stu-id="c0d63-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="c0d63-107">Se o Gerenciador de largura de banda de sub-rede designado não enviar \_ um \_ anúncio que sou DSBM durante esse intervalo, os outros gerenciadores de largura de banda de sub-rede (SBMs) no domínio elegerão um novo DSBM.</span><span class="sxs-lookup"><span data-stu-id="c0d63-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="c0d63-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0d63-108">Entry</span></span> | <span data-ttu-id="c0d63-109">Valor</span><span class="sxs-lookup"><span data-stu-id="c0d63-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c0d63-110">CN</span><span class="sxs-lookup"><span data-stu-id="c0d63-110">CN</span></span>                | <span data-ttu-id="c0d63-111">ACS-DSBM-Deadtime</span><span class="sxs-lookup"><span data-stu-id="c0d63-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="c0d63-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c0d63-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c0d63-113">aCSDSBMDeadTime</span><span class="sxs-lookup"><span data-stu-id="c0d63-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="c0d63-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c0d63-114">Size</span></span>              | <span data-ttu-id="c0d63-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="c0d63-115">4 bytes</span></span>                              |
| <span data-ttu-id="c0d63-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c0d63-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c0d63-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c0d63-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c0d63-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c0d63-118">Attribute-Id</span></span>      | <span data-ttu-id="c0d63-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="c0d63-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="c0d63-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c0d63-120">System-Id-Guid</span></span>    | <span data-ttu-id="c0d63-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c0d63-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="c0d63-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0d63-122">Syntax</span></span>            | [<span data-ttu-id="c0d63-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c0d63-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c0d63-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="c0d63-124">Implementations</span></span>

-   [<span data-ttu-id="c0d63-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c0d63-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c0d63-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c0d63-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c0d63-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c0d63-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c0d63-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c0d63-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c0d63-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c0d63-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c0d63-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c0d63-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c0d63-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c0d63-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c0d63-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0d63-132">Entry</span></span> | <span data-ttu-id="c0d63-133">Valor</span><span class="sxs-lookup"><span data-stu-id="c0d63-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c0d63-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="c0d63-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0d63-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0d63-136">System-Only</span></span>            | <span data-ttu-id="c0d63-137">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-137">False</span></span>                                        |
| <span data-ttu-id="c0d63-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c0d63-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c0d63-139">True</span><span class="sxs-lookup"><span data-stu-id="c0d63-139">True</span></span>                                         |
| <span data-ttu-id="c0d63-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="c0d63-140">Is Indexed</span></span>             | <span data-ttu-id="c0d63-141">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-141">False</span></span>                                        |
| <span data-ttu-id="c0d63-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0d63-142">In Global Catalog</span></span>      | <span data-ttu-id="c0d63-143">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-143">False</span></span>                                        |
| <span data-ttu-id="c0d63-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0d63-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0d63-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c0d63-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c0d63-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0d63-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0d63-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-148">Search-Flags</span></span>           | <span data-ttu-id="c0d63-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0d63-149">0x00000000</span></span>                                   |
| <span data-ttu-id="c0d63-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-150">System-Flags</span></span>           | <span data-ttu-id="c0d63-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0d63-151">0x00000010</span></span>                                   |
| <span data-ttu-id="c0d63-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c0d63-152">Classes used in</span></span>        | [<span data-ttu-id="c0d63-153">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="c0d63-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c0d63-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0d63-154">Windows Server 2003</span></span>



| <span data-ttu-id="c0d63-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0d63-155">Entry</span></span> | <span data-ttu-id="c0d63-156">Valor</span><span class="sxs-lookup"><span data-stu-id="c0d63-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c0d63-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="c0d63-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0d63-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0d63-159">System-Only</span></span>            | <span data-ttu-id="c0d63-160">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-160">False</span></span>                                        |
| <span data-ttu-id="c0d63-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c0d63-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c0d63-162">True</span><span class="sxs-lookup"><span data-stu-id="c0d63-162">True</span></span>                                         |
| <span data-ttu-id="c0d63-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="c0d63-163">Is Indexed</span></span>             | <span data-ttu-id="c0d63-164">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-164">False</span></span>                                        |
| <span data-ttu-id="c0d63-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0d63-165">In Global Catalog</span></span>      | <span data-ttu-id="c0d63-166">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-166">False</span></span>                                        |
| <span data-ttu-id="c0d63-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0d63-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0d63-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c0d63-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c0d63-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0d63-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0d63-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-171">Search-Flags</span></span>           | <span data-ttu-id="c0d63-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0d63-172">0x00000000</span></span>                                   |
| <span data-ttu-id="c0d63-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-173">System-Flags</span></span>           | <span data-ttu-id="c0d63-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0d63-174">0x00000010</span></span>                                   |
| <span data-ttu-id="c0d63-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c0d63-175">Classes used in</span></span>        | [<span data-ttu-id="c0d63-176">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="c0d63-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c0d63-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c0d63-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c0d63-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0d63-178">Entry</span></span> | <span data-ttu-id="c0d63-179">Valor</span><span class="sxs-lookup"><span data-stu-id="c0d63-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c0d63-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="c0d63-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0d63-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0d63-182">System-Only</span></span>            | <span data-ttu-id="c0d63-183">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-183">False</span></span>                                        |
| <span data-ttu-id="c0d63-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c0d63-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c0d63-185">True</span><span class="sxs-lookup"><span data-stu-id="c0d63-185">True</span></span>                                         |
| <span data-ttu-id="c0d63-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="c0d63-186">Is Indexed</span></span>             | <span data-ttu-id="c0d63-187">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-187">False</span></span>                                        |
| <span data-ttu-id="c0d63-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0d63-188">In Global Catalog</span></span>      | <span data-ttu-id="c0d63-189">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-189">False</span></span>                                        |
| <span data-ttu-id="c0d63-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0d63-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0d63-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c0d63-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c0d63-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0d63-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0d63-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-194">Search-Flags</span></span>           | <span data-ttu-id="c0d63-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0d63-195">0x00000000</span></span>                                   |
| <span data-ttu-id="c0d63-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-196">System-Flags</span></span>           | <span data-ttu-id="c0d63-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0d63-197">0x00000010</span></span>                                   |
| <span data-ttu-id="c0d63-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c0d63-198">Classes used in</span></span>        | [<span data-ttu-id="c0d63-199">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="c0d63-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c0d63-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0d63-200">Windows Server 2008</span></span>



| <span data-ttu-id="c0d63-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0d63-201">Entry</span></span> | <span data-ttu-id="c0d63-202">Valor</span><span class="sxs-lookup"><span data-stu-id="c0d63-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c0d63-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="c0d63-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0d63-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0d63-205">System-Only</span></span>            | <span data-ttu-id="c0d63-206">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-206">False</span></span>                                        |
| <span data-ttu-id="c0d63-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c0d63-207">Is-Single-Valued</span></span>       | <span data-ttu-id="c0d63-208">True</span><span class="sxs-lookup"><span data-stu-id="c0d63-208">True</span></span>                                         |
| <span data-ttu-id="c0d63-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="c0d63-209">Is Indexed</span></span>             | <span data-ttu-id="c0d63-210">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-210">False</span></span>                                        |
| <span data-ttu-id="c0d63-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0d63-211">In Global Catalog</span></span>      | <span data-ttu-id="c0d63-212">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-212">False</span></span>                                        |
| <span data-ttu-id="c0d63-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0d63-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0d63-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c0d63-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c0d63-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0d63-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0d63-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-217">Search-Flags</span></span>           | <span data-ttu-id="c0d63-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0d63-218">0x00000000</span></span>                                   |
| <span data-ttu-id="c0d63-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-219">System-Flags</span></span>           | <span data-ttu-id="c0d63-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0d63-220">0x00000010</span></span>                                   |
| <span data-ttu-id="c0d63-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c0d63-221">Classes used in</span></span>        | [<span data-ttu-id="c0d63-222">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="c0d63-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c0d63-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0d63-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c0d63-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0d63-224">Entry</span></span> | <span data-ttu-id="c0d63-225">Valor</span><span class="sxs-lookup"><span data-stu-id="c0d63-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c0d63-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="c0d63-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0d63-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0d63-228">System-Only</span></span>            | <span data-ttu-id="c0d63-229">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-229">False</span></span>                                        |
| <span data-ttu-id="c0d63-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c0d63-230">Is-Single-Valued</span></span>       | <span data-ttu-id="c0d63-231">True</span><span class="sxs-lookup"><span data-stu-id="c0d63-231">True</span></span>                                         |
| <span data-ttu-id="c0d63-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="c0d63-232">Is Indexed</span></span>             | <span data-ttu-id="c0d63-233">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-233">False</span></span>                                        |
| <span data-ttu-id="c0d63-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0d63-234">In Global Catalog</span></span>      | <span data-ttu-id="c0d63-235">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-235">False</span></span>                                        |
| <span data-ttu-id="c0d63-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0d63-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0d63-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c0d63-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c0d63-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0d63-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0d63-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-240">Search-Flags</span></span>           | <span data-ttu-id="c0d63-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0d63-241">0x00000000</span></span>                                   |
| <span data-ttu-id="c0d63-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-242">System-Flags</span></span>           | <span data-ttu-id="c0d63-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0d63-243">0x00000010</span></span>                                   |
| <span data-ttu-id="c0d63-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c0d63-244">Classes used in</span></span>        | [<span data-ttu-id="c0d63-245">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="c0d63-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c0d63-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0d63-246">Windows Server 2012</span></span>



| <span data-ttu-id="c0d63-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="c0d63-247">Entry</span></span> | <span data-ttu-id="c0d63-248">Valor</span><span class="sxs-lookup"><span data-stu-id="c0d63-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="c0d63-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="c0d63-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0d63-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="c0d63-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0d63-251">System-Only</span></span>            | <span data-ttu-id="c0d63-252">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-252">False</span></span>                                        |
| <span data-ttu-id="c0d63-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c0d63-253">Is-Single-Valued</span></span>       | <span data-ttu-id="c0d63-254">True</span><span class="sxs-lookup"><span data-stu-id="c0d63-254">True</span></span>                                         |
| <span data-ttu-id="c0d63-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="c0d63-255">Is Indexed</span></span>             | <span data-ttu-id="c0d63-256">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-256">False</span></span>                                        |
| <span data-ttu-id="c0d63-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0d63-257">In Global Catalog</span></span>      | <span data-ttu-id="c0d63-258">Falso</span><span class="sxs-lookup"><span data-stu-id="c0d63-258">False</span></span>                                        |
| <span data-ttu-id="c0d63-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c0d63-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0d63-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c0d63-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="c0d63-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0d63-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0d63-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="c0d63-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-263">Search-Flags</span></span>           | <span data-ttu-id="c0d63-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0d63-264">0x00000000</span></span>                                   |
| <span data-ttu-id="c0d63-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0d63-265">System-Flags</span></span>           | <span data-ttu-id="c0d63-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c0d63-266">0x00000010</span></span>                                   |
| <span data-ttu-id="c0d63-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c0d63-267">Classes used in</span></span>        | [<span data-ttu-id="c0d63-268">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="c0d63-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





