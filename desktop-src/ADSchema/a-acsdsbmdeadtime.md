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
# <a name="acs-dsbm-deadtime-attribute"></a><span data-ttu-id="0d42f-105">ACS-DSBM-atributo de inatividade</span><span class="sxs-lookup"><span data-stu-id="0d42f-105">ACS-DSBM-DeadTime attribute</span></span>

<span data-ttu-id="0d42f-106">Esse atributo contém o DSBMDeadInterval (intervalo de tempo inativo de eleição) para um domínio.</span><span class="sxs-lookup"><span data-stu-id="0d42f-106">This attribute contains the election dead time interval (DSBMDeadInterval) for a domain.</span></span> <span data-ttu-id="0d42f-107">Se o Gerenciador de largura de banda de sub-rede designado não enviar \_ um \_ anúncio que sou DSBM durante esse intervalo, os outros gerenciadores de largura de banda de sub-rede (SBMs) no domínio elegerão um novo DSBM.</span><span class="sxs-lookup"><span data-stu-id="0d42f-107">If the Designated Subnet Bandwidth Manager does not send out an I\_AM\_DSBM advertisement during this interval, then the other Subnet Bandwidth Managers (SBMs) in the domain elect a new DSBM.</span></span>



| <span data-ttu-id="0d42f-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d42f-108">Entry</span></span> | <span data-ttu-id="0d42f-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0d42f-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="0d42f-110">CN</span><span class="sxs-lookup"><span data-stu-id="0d42f-110">CN</span></span>                | <span data-ttu-id="0d42f-111">ACS-DSBM-Deadtime</span><span class="sxs-lookup"><span data-stu-id="0d42f-111">ACS-DSBM-DeadTime</span></span>                    |
| <span data-ttu-id="0d42f-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0d42f-112">Ldap-Display-Name</span></span> | <span data-ttu-id="0d42f-113">aCSDSBMDeadTime</span><span class="sxs-lookup"><span data-stu-id="0d42f-113">aCSDSBMDeadTime</span></span>                      |
| <span data-ttu-id="0d42f-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0d42f-114">Size</span></span>              | <span data-ttu-id="0d42f-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="0d42f-115">4 bytes</span></span>                              |
| <span data-ttu-id="0d42f-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0d42f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="0d42f-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0d42f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="0d42f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0d42f-118">Attribute-Id</span></span>      | <span data-ttu-id="0d42f-119">1.2.840.113556.1.4.778</span><span class="sxs-lookup"><span data-stu-id="0d42f-119">1.2.840.113556.1.4.778</span></span>               |
| <span data-ttu-id="0d42f-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0d42f-120">System-Id-Guid</span></span>    | <span data-ttu-id="0d42f-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0d42f-121">1cb355a0-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="0d42f-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d42f-122">Syntax</span></span>            | [<span data-ttu-id="0d42f-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="0d42f-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="0d42f-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="0d42f-124">Implementations</span></span>

-   [<span data-ttu-id="0d42f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0d42f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0d42f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0d42f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0d42f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0d42f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0d42f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0d42f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0d42f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0d42f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0d42f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0d42f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0d42f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0d42f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0d42f-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d42f-132">Entry</span></span> | <span data-ttu-id="0d42f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0d42f-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0d42f-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d42f-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d42f-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d42f-136">System-Only</span></span>            | <span data-ttu-id="0d42f-137">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-137">False</span></span>                                        |
| <span data-ttu-id="0d42f-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d42f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0d42f-139">True</span><span class="sxs-lookup"><span data-stu-id="0d42f-139">True</span></span>                                         |
| <span data-ttu-id="0d42f-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d42f-140">Is Indexed</span></span>             | <span data-ttu-id="0d42f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-141">False</span></span>                                        |
| <span data-ttu-id="0d42f-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d42f-142">In Global Catalog</span></span>      | <span data-ttu-id="0d42f-143">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-143">False</span></span>                                        |
| <span data-ttu-id="0d42f-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d42f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d42f-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d42f-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0d42f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d42f-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d42f-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-148">Search-Flags</span></span>           | <span data-ttu-id="0d42f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d42f-149">0x00000000</span></span>                                   |
| <span data-ttu-id="0d42f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-150">System-Flags</span></span>           | <span data-ttu-id="0d42f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d42f-151">0x00000010</span></span>                                   |
| <span data-ttu-id="0d42f-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d42f-152">Classes used in</span></span>        | [<span data-ttu-id="0d42f-153">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="0d42f-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0d42f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d42f-154">Windows Server 2003</span></span>



| <span data-ttu-id="0d42f-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d42f-155">Entry</span></span> | <span data-ttu-id="0d42f-156">Valor</span><span class="sxs-lookup"><span data-stu-id="0d42f-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0d42f-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d42f-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d42f-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d42f-159">System-Only</span></span>            | <span data-ttu-id="0d42f-160">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-160">False</span></span>                                        |
| <span data-ttu-id="0d42f-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d42f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0d42f-162">True</span><span class="sxs-lookup"><span data-stu-id="0d42f-162">True</span></span>                                         |
| <span data-ttu-id="0d42f-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d42f-163">Is Indexed</span></span>             | <span data-ttu-id="0d42f-164">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-164">False</span></span>                                        |
| <span data-ttu-id="0d42f-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d42f-165">In Global Catalog</span></span>      | <span data-ttu-id="0d42f-166">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-166">False</span></span>                                        |
| <span data-ttu-id="0d42f-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d42f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d42f-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d42f-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0d42f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d42f-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d42f-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-171">Search-Flags</span></span>           | <span data-ttu-id="0d42f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d42f-172">0x00000000</span></span>                                   |
| <span data-ttu-id="0d42f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-173">System-Flags</span></span>           | <span data-ttu-id="0d42f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d42f-174">0x00000010</span></span>                                   |
| <span data-ttu-id="0d42f-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d42f-175">Classes used in</span></span>        | [<span data-ttu-id="0d42f-176">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="0d42f-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0d42f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0d42f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0d42f-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d42f-178">Entry</span></span> | <span data-ttu-id="0d42f-179">Valor</span><span class="sxs-lookup"><span data-stu-id="0d42f-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0d42f-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d42f-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d42f-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d42f-182">System-Only</span></span>            | <span data-ttu-id="0d42f-183">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-183">False</span></span>                                        |
| <span data-ttu-id="0d42f-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d42f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0d42f-185">True</span><span class="sxs-lookup"><span data-stu-id="0d42f-185">True</span></span>                                         |
| <span data-ttu-id="0d42f-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d42f-186">Is Indexed</span></span>             | <span data-ttu-id="0d42f-187">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-187">False</span></span>                                        |
| <span data-ttu-id="0d42f-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d42f-188">In Global Catalog</span></span>      | <span data-ttu-id="0d42f-189">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-189">False</span></span>                                        |
| <span data-ttu-id="0d42f-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d42f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d42f-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d42f-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0d42f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d42f-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d42f-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-194">Search-Flags</span></span>           | <span data-ttu-id="0d42f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d42f-195">0x00000000</span></span>                                   |
| <span data-ttu-id="0d42f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-196">System-Flags</span></span>           | <span data-ttu-id="0d42f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d42f-197">0x00000010</span></span>                                   |
| <span data-ttu-id="0d42f-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d42f-198">Classes used in</span></span>        | [<span data-ttu-id="0d42f-199">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="0d42f-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0d42f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d42f-200">Windows Server 2008</span></span>



| <span data-ttu-id="0d42f-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d42f-201">Entry</span></span> | <span data-ttu-id="0d42f-202">Valor</span><span class="sxs-lookup"><span data-stu-id="0d42f-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0d42f-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d42f-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d42f-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d42f-205">System-Only</span></span>            | <span data-ttu-id="0d42f-206">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-206">False</span></span>                                        |
| <span data-ttu-id="0d42f-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d42f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0d42f-208">True</span><span class="sxs-lookup"><span data-stu-id="0d42f-208">True</span></span>                                         |
| <span data-ttu-id="0d42f-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d42f-209">Is Indexed</span></span>             | <span data-ttu-id="0d42f-210">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-210">False</span></span>                                        |
| <span data-ttu-id="0d42f-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d42f-211">In Global Catalog</span></span>      | <span data-ttu-id="0d42f-212">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-212">False</span></span>                                        |
| <span data-ttu-id="0d42f-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d42f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d42f-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d42f-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0d42f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d42f-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d42f-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-217">Search-Flags</span></span>           | <span data-ttu-id="0d42f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d42f-218">0x00000000</span></span>                                   |
| <span data-ttu-id="0d42f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-219">System-Flags</span></span>           | <span data-ttu-id="0d42f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d42f-220">0x00000010</span></span>                                   |
| <span data-ttu-id="0d42f-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d42f-221">Classes used in</span></span>        | [<span data-ttu-id="0d42f-222">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="0d42f-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0d42f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0d42f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0d42f-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d42f-224">Entry</span></span> | <span data-ttu-id="0d42f-225">Valor</span><span class="sxs-lookup"><span data-stu-id="0d42f-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0d42f-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d42f-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d42f-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d42f-228">System-Only</span></span>            | <span data-ttu-id="0d42f-229">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-229">False</span></span>                                        |
| <span data-ttu-id="0d42f-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d42f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0d42f-231">True</span><span class="sxs-lookup"><span data-stu-id="0d42f-231">True</span></span>                                         |
| <span data-ttu-id="0d42f-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d42f-232">Is Indexed</span></span>             | <span data-ttu-id="0d42f-233">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-233">False</span></span>                                        |
| <span data-ttu-id="0d42f-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d42f-234">In Global Catalog</span></span>      | <span data-ttu-id="0d42f-235">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-235">False</span></span>                                        |
| <span data-ttu-id="0d42f-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d42f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d42f-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d42f-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0d42f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d42f-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d42f-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-240">Search-Flags</span></span>           | <span data-ttu-id="0d42f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d42f-241">0x00000000</span></span>                                   |
| <span data-ttu-id="0d42f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-242">System-Flags</span></span>           | <span data-ttu-id="0d42f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d42f-243">0x00000010</span></span>                                   |
| <span data-ttu-id="0d42f-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d42f-244">Classes used in</span></span>        | [<span data-ttu-id="0d42f-245">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="0d42f-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0d42f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d42f-246">Windows Server 2012</span></span>



| <span data-ttu-id="0d42f-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d42f-247">Entry</span></span> | <span data-ttu-id="0d42f-248">Valor</span><span class="sxs-lookup"><span data-stu-id="0d42f-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="0d42f-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="0d42f-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0d42f-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="0d42f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="0d42f-251">System-Only</span></span>            | <span data-ttu-id="0d42f-252">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-252">False</span></span>                                        |
| <span data-ttu-id="0d42f-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0d42f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="0d42f-254">True</span><span class="sxs-lookup"><span data-stu-id="0d42f-254">True</span></span>                                         |
| <span data-ttu-id="0d42f-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="0d42f-255">Is Indexed</span></span>             | <span data-ttu-id="0d42f-256">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-256">False</span></span>                                        |
| <span data-ttu-id="0d42f-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0d42f-257">In Global Catalog</span></span>      | <span data-ttu-id="0d42f-258">Falso</span><span class="sxs-lookup"><span data-stu-id="0d42f-258">False</span></span>                                        |
| <span data-ttu-id="0d42f-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0d42f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="0d42f-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0d42f-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="0d42f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0d42f-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0d42f-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="0d42f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-263">Search-Flags</span></span>           | <span data-ttu-id="0d42f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0d42f-264">0x00000000</span></span>                                   |
| <span data-ttu-id="0d42f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0d42f-265">System-Flags</span></span>           | <span data-ttu-id="0d42f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0d42f-266">0x00000010</span></span>                                   |
| <span data-ttu-id="0d42f-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0d42f-267">Classes used in</span></span>        | [<span data-ttu-id="0d42f-268">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="0d42f-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





