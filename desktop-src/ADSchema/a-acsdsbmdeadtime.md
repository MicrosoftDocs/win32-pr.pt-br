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
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="84c19-105">ACS-DSBM-atributo de inatividade</span><span class="sxs-lookup"><span data-stu-id="84c19-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="84c19-106">Esse atributo contém o DSBMDeadInterval (intervalo de tempo inativo de eleição) para um domínio.</span><span class="sxs-lookup"><span data-stu-id="84c19-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="84c19-107">Se o Gerenciador de largura de banda de sub-rede designado não enviar \_ um \_ anúncio que sou DSBM durante esse intervalo, os outros gerenciadores de largura de banda de sub-rede (SBMs) no domínio elegerão um novo DSBM.</span><span class="sxs-lookup"><span data-stu-id="84c19-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="84c19-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="84c19-108">Entry</span></span> | <span data-ttu-id="84c19-109">Valor</span><span class="sxs-lookup"><span data-stu-id="84c19-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="84c19-110">CN</span><span class="sxs-lookup"><span data-stu-id="84c19-110">CN</span></span>                | <span data-ttu-id="84c19-111">ACS-DSBM-Deadtime</span><span class="sxs-lookup"><span data-stu-id="84c19-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="84c19-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="84c19-112">Ldap-Display-Name</span></span> | <span data-ttu-id="84c19-113">aCSDSBMDeadTime</span><span class="sxs-lookup"><span data-stu-id="84c19-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="84c19-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="84c19-114">Size</span></span>              | <span data-ttu-id="84c19-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="84c19-115">4 bytes</span></span>                              |
| <span data-ttu-id="84c19-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="84c19-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="84c19-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="84c19-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="84c19-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="84c19-118">Attribute-Id</span></span>      | <span data-ttu-id="84c19-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="84c19-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="84c19-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="84c19-120">System-Id-Guid</span></span>    | <span data-ttu-id="84c19-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="84c19-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="84c19-122">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84c19-122">Syntax</span></span>            | [<span data-ttu-id="84c19-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="84c19-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="84c19-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="84c19-124">Implementations</span></span>

-   [<span data-ttu-id="84c19-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="84c19-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="84c19-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="84c19-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="84c19-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="84c19-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="84c19-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="84c19-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="84c19-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="84c19-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="84c19-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="84c19-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="84c19-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="84c19-131">Windows 2000 Server</span></span>



| <span data-ttu-id="84c19-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="84c19-132">Entry</span></span> | <span data-ttu-id="84c19-133">Valor</span><span class="sxs-lookup"><span data-stu-id="84c19-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84c19-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="84c19-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84c19-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="84c19-136">System-Only</span></span>            | <span data-ttu-id="84c19-137">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-137">False</span></span>                                        |
| <span data-ttu-id="84c19-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="84c19-138">Is-Single-Valued</span></span>       | <span data-ttu-id="84c19-139">True</span><span class="sxs-lookup"><span data-stu-id="84c19-139">True</span></span>                                         |
| <span data-ttu-id="84c19-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="84c19-140">Is Indexed</span></span>             | <span data-ttu-id="84c19-141">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-141">False</span></span>                                        |
| <span data-ttu-id="84c19-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="84c19-142">In Global Catalog</span></span>      | <span data-ttu-id="84c19-143">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-143">False</span></span>                                        |
| <span data-ttu-id="84c19-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84c19-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="84c19-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="84c19-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84c19-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84c19-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="84c19-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84c19-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="84c19-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-148">Search-Flags</span></span>           | <span data-ttu-id="84c19-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84c19-149">0x00000000</span></span>                                   |
| <span data-ttu-id="84c19-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-150">System-Flags</span></span>           | <span data-ttu-id="84c19-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84c19-151">0x00000010</span></span>                                   |
| <span data-ttu-id="84c19-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="84c19-152">Classes used in</span></span>        | [<span data-ttu-id="84c19-153">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="84c19-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="84c19-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="84c19-154">Windows Server 2003</span></span>



| <span data-ttu-id="84c19-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="84c19-155">Entry</span></span> | <span data-ttu-id="84c19-156">Valor</span><span class="sxs-lookup"><span data-stu-id="84c19-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84c19-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="84c19-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84c19-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="84c19-159">System-Only</span></span>            | <span data-ttu-id="84c19-160">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-160">False</span></span>                                        |
| <span data-ttu-id="84c19-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="84c19-161">Is-Single-Valued</span></span>       | <span data-ttu-id="84c19-162">True</span><span class="sxs-lookup"><span data-stu-id="84c19-162">True</span></span>                                         |
| <span data-ttu-id="84c19-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="84c19-163">Is Indexed</span></span>             | <span data-ttu-id="84c19-164">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-164">False</span></span>                                        |
| <span data-ttu-id="84c19-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="84c19-165">In Global Catalog</span></span>      | <span data-ttu-id="84c19-166">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-166">False</span></span>                                        |
| <span data-ttu-id="84c19-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84c19-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="84c19-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="84c19-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84c19-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84c19-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="84c19-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84c19-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="84c19-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-171">Search-Flags</span></span>           | <span data-ttu-id="84c19-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84c19-172">0x00000000</span></span>                                   |
| <span data-ttu-id="84c19-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-173">System-Flags</span></span>           | <span data-ttu-id="84c19-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84c19-174">0x00000010</span></span>                                   |
| <span data-ttu-id="84c19-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="84c19-175">Classes used in</span></span>        | [<span data-ttu-id="84c19-176">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="84c19-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="84c19-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="84c19-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="84c19-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="84c19-178">Entry</span></span> | <span data-ttu-id="84c19-179">Valor</span><span class="sxs-lookup"><span data-stu-id="84c19-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84c19-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="84c19-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84c19-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="84c19-182">System-Only</span></span>            | <span data-ttu-id="84c19-183">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-183">False</span></span>                                        |
| <span data-ttu-id="84c19-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="84c19-184">Is-Single-Valued</span></span>       | <span data-ttu-id="84c19-185">True</span><span class="sxs-lookup"><span data-stu-id="84c19-185">True</span></span>                                         |
| <span data-ttu-id="84c19-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="84c19-186">Is Indexed</span></span>             | <span data-ttu-id="84c19-187">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-187">False</span></span>                                        |
| <span data-ttu-id="84c19-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="84c19-188">In Global Catalog</span></span>      | <span data-ttu-id="84c19-189">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-189">False</span></span>                                        |
| <span data-ttu-id="84c19-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84c19-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="84c19-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="84c19-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84c19-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84c19-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="84c19-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84c19-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="84c19-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-194">Search-Flags</span></span>           | <span data-ttu-id="84c19-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84c19-195">0x00000000</span></span>                                   |
| <span data-ttu-id="84c19-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-196">System-Flags</span></span>           | <span data-ttu-id="84c19-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84c19-197">0x00000010</span></span>                                   |
| <span data-ttu-id="84c19-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="84c19-198">Classes used in</span></span>        | [<span data-ttu-id="84c19-199">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="84c19-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="84c19-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84c19-200">Windows Server 2008</span></span>



| <span data-ttu-id="84c19-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="84c19-201">Entry</span></span> | <span data-ttu-id="84c19-202">Valor</span><span class="sxs-lookup"><span data-stu-id="84c19-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84c19-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="84c19-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84c19-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="84c19-205">System-Only</span></span>            | <span data-ttu-id="84c19-206">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-206">False</span></span>                                        |
| <span data-ttu-id="84c19-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="84c19-207">Is-Single-Valued</span></span>       | <span data-ttu-id="84c19-208">True</span><span class="sxs-lookup"><span data-stu-id="84c19-208">True</span></span>                                         |
| <span data-ttu-id="84c19-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="84c19-209">Is Indexed</span></span>             | <span data-ttu-id="84c19-210">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-210">False</span></span>                                        |
| <span data-ttu-id="84c19-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="84c19-211">In Global Catalog</span></span>      | <span data-ttu-id="84c19-212">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-212">False</span></span>                                        |
| <span data-ttu-id="84c19-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84c19-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="84c19-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="84c19-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84c19-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84c19-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="84c19-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84c19-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="84c19-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-217">Search-Flags</span></span>           | <span data-ttu-id="84c19-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84c19-218">0x00000000</span></span>                                   |
| <span data-ttu-id="84c19-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-219">System-Flags</span></span>           | <span data-ttu-id="84c19-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84c19-220">0x00000010</span></span>                                   |
| <span data-ttu-id="84c19-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="84c19-221">Classes used in</span></span>        | [<span data-ttu-id="84c19-222">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="84c19-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="84c19-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="84c19-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="84c19-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="84c19-224">Entry</span></span> | <span data-ttu-id="84c19-225">Valor</span><span class="sxs-lookup"><span data-stu-id="84c19-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84c19-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="84c19-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84c19-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="84c19-228">System-Only</span></span>            | <span data-ttu-id="84c19-229">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-229">False</span></span>                                        |
| <span data-ttu-id="84c19-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="84c19-230">Is-Single-Valued</span></span>       | <span data-ttu-id="84c19-231">True</span><span class="sxs-lookup"><span data-stu-id="84c19-231">True</span></span>                                         |
| <span data-ttu-id="84c19-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="84c19-232">Is Indexed</span></span>             | <span data-ttu-id="84c19-233">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-233">False</span></span>                                        |
| <span data-ttu-id="84c19-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="84c19-234">In Global Catalog</span></span>      | <span data-ttu-id="84c19-235">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-235">False</span></span>                                        |
| <span data-ttu-id="84c19-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84c19-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="84c19-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="84c19-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84c19-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84c19-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="84c19-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84c19-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="84c19-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-240">Search-Flags</span></span>           | <span data-ttu-id="84c19-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84c19-241">0x00000000</span></span>                                   |
| <span data-ttu-id="84c19-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-242">System-Flags</span></span>           | <span data-ttu-id="84c19-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84c19-243">0x00000010</span></span>                                   |
| <span data-ttu-id="84c19-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="84c19-244">Classes used in</span></span>        | [<span data-ttu-id="84c19-245">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="84c19-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="84c19-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84c19-246">Windows Server 2012</span></span>



| <span data-ttu-id="84c19-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="84c19-247">Entry</span></span> | <span data-ttu-id="84c19-248">Valor</span><span class="sxs-lookup"><span data-stu-id="84c19-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="84c19-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="84c19-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="84c19-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="84c19-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="84c19-251">System-Only</span></span>            | <span data-ttu-id="84c19-252">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-252">False</span></span>                                        |
| <span data-ttu-id="84c19-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="84c19-253">Is-Single-Valued</span></span>       | <span data-ttu-id="84c19-254">True</span><span class="sxs-lookup"><span data-stu-id="84c19-254">True</span></span>                                         |
| <span data-ttu-id="84c19-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="84c19-255">Is Indexed</span></span>             | <span data-ttu-id="84c19-256">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-256">False</span></span>                                        |
| <span data-ttu-id="84c19-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="84c19-257">In Global Catalog</span></span>      | <span data-ttu-id="84c19-258">Falso</span><span class="sxs-lookup"><span data-stu-id="84c19-258">False</span></span>                                        |
| <span data-ttu-id="84c19-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="84c19-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="84c19-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="84c19-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="84c19-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="84c19-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="84c19-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="84c19-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="84c19-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-263">Search-Flags</span></span>           | <span data-ttu-id="84c19-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="84c19-264">0x00000000</span></span>                                   |
| <span data-ttu-id="84c19-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="84c19-265">System-Flags</span></span>           | <span data-ttu-id="84c19-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="84c19-266">0x00000010</span></span>                                   |
| <span data-ttu-id="84c19-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="84c19-267">Classes used in</span></span>        | [<span data-ttu-id="84c19-268">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="84c19-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





