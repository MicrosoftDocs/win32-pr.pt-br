---
title: Package-Type atributo
description: Esse atributo descreve o tipo de instalação necessário para um pacote de aplicativo, por exemplo, MSI, EXE, CAB.
ms.assetid: 76505575-a2c9-4113-84ac-1d0689d9e0e4
ms.tgt_platform: multiple
keywords:
- Esquema de Package-Type do atributo AD
- Esquema do atributo do ADtype
topic_type:
- apiref
api_name:
- Package-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 325bb00484a3ee44cd23b98931c40fb440cdb3b1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087008"
---
# <a name="package-type-attribute"></a><span data-ttu-id="e29a0-105">Package-Type atributo</span><span class="sxs-lookup"><span data-stu-id="e29a0-105">Package-Type attribute</span></span>

<span data-ttu-id="e29a0-106">Esse atributo descreve o tipo de instalação necessário para um pacote de aplicativo, por exemplo, MSI, EXE, CAB.</span><span class="sxs-lookup"><span data-stu-id="e29a0-106">This attribute describes the type of installation required for an application package, for example, MSI, EXE, CAB.</span></span>



| <span data-ttu-id="e29a0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e29a0-107">Entry</span></span> | <span data-ttu-id="e29a0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e29a0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e29a0-109">CN</span><span class="sxs-lookup"><span data-stu-id="e29a0-109">CN</span></span>                | <span data-ttu-id="e29a0-110">Package-Type</span><span class="sxs-lookup"><span data-stu-id="e29a0-110">Package-Type</span></span>                         |
| <span data-ttu-id="e29a0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e29a0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e29a0-112">packageType</span><span class="sxs-lookup"><span data-stu-id="e29a0-112">packageType</span></span>                          |
| <span data-ttu-id="e29a0-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e29a0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="e29a0-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e29a0-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e29a0-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e29a0-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e29a0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e29a0-116">Attribute-Id</span></span>      | <span data-ttu-id="e29a0-117">1.2.840.113556.1.4.324</span><span class="sxs-lookup"><span data-stu-id="e29a0-117">1.2.840.113556.1.4.324</span></span>               |
| <span data-ttu-id="e29a0-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e29a0-118">System-Id-Guid</span></span>    | <span data-ttu-id="e29a0-119">7d6c0e96-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="e29a0-119">7d6c0e96-7e20-11d0-afd6-00c04fd930c9</span></span> |
| <span data-ttu-id="e29a0-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="e29a0-120">Syntax</span></span>            | [<span data-ttu-id="e29a0-121">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="e29a0-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e29a0-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="e29a0-122">Implementations</span></span>

-   [<span data-ttu-id="e29a0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e29a0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e29a0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e29a0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e29a0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e29a0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e29a0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e29a0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e29a0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e29a0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e29a0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e29a0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e29a0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e29a0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e29a0-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="e29a0-130">Entry</span></span> | <span data-ttu-id="e29a0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e29a0-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e29a0-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="e29a0-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29a0-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29a0-134">System-Only</span></span>            | <span data-ttu-id="e29a0-135">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-135">False</span></span>                                                            |
| <span data-ttu-id="e29a0-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e29a0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e29a0-137">True</span><span class="sxs-lookup"><span data-stu-id="e29a0-137">True</span></span>                                                             |
| <span data-ttu-id="e29a0-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="e29a0-138">Is Indexed</span></span>             | <span data-ttu-id="e29a0-139">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-139">False</span></span>                                                            |
| <span data-ttu-id="e29a0-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e29a0-140">In Global Catalog</span></span>      | <span data-ttu-id="e29a0-141">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-141">False</span></span>                                                            |
| <span data-ttu-id="e29a0-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29a0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29a0-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e29a0-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e29a0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29a0-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29a0-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-146">Search-Flags</span></span>           | <span data-ttu-id="e29a0-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29a0-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="e29a0-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-148">System-Flags</span></span>           | <span data-ttu-id="e29a0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29a0-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="e29a0-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e29a0-150">Classes used in</span></span>        | [<span data-ttu-id="e29a0-151">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e29a0-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e29a0-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e29a0-152">Windows Server 2003</span></span>



| <span data-ttu-id="e29a0-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="e29a0-153">Entry</span></span> | <span data-ttu-id="e29a0-154">Valor</span><span class="sxs-lookup"><span data-stu-id="e29a0-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e29a0-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="e29a0-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29a0-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29a0-157">System-Only</span></span>            | <span data-ttu-id="e29a0-158">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-158">False</span></span>                                                            |
| <span data-ttu-id="e29a0-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e29a0-159">Is-Single-Valued</span></span>       | <span data-ttu-id="e29a0-160">True</span><span class="sxs-lookup"><span data-stu-id="e29a0-160">True</span></span>                                                             |
| <span data-ttu-id="e29a0-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="e29a0-161">Is Indexed</span></span>             | <span data-ttu-id="e29a0-162">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-162">False</span></span>                                                            |
| <span data-ttu-id="e29a0-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e29a0-163">In Global Catalog</span></span>      | <span data-ttu-id="e29a0-164">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-164">False</span></span>                                                            |
| <span data-ttu-id="e29a0-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29a0-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29a0-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e29a0-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e29a0-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29a0-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29a0-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-169">Search-Flags</span></span>           | <span data-ttu-id="e29a0-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29a0-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="e29a0-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-171">System-Flags</span></span>           | <span data-ttu-id="e29a0-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29a0-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="e29a0-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e29a0-173">Classes used in</span></span>        | [<span data-ttu-id="e29a0-174">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e29a0-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e29a0-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e29a0-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e29a0-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="e29a0-176">Entry</span></span> | <span data-ttu-id="e29a0-177">Valor</span><span class="sxs-lookup"><span data-stu-id="e29a0-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e29a0-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="e29a0-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29a0-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29a0-180">System-Only</span></span>            | <span data-ttu-id="e29a0-181">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-181">False</span></span>                                                            |
| <span data-ttu-id="e29a0-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e29a0-182">Is-Single-Valued</span></span>       | <span data-ttu-id="e29a0-183">True</span><span class="sxs-lookup"><span data-stu-id="e29a0-183">True</span></span>                                                             |
| <span data-ttu-id="e29a0-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="e29a0-184">Is Indexed</span></span>             | <span data-ttu-id="e29a0-185">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-185">False</span></span>                                                            |
| <span data-ttu-id="e29a0-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e29a0-186">In Global Catalog</span></span>      | <span data-ttu-id="e29a0-187">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-187">False</span></span>                                                            |
| <span data-ttu-id="e29a0-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29a0-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29a0-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e29a0-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e29a0-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29a0-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29a0-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-192">Search-Flags</span></span>           | <span data-ttu-id="e29a0-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29a0-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="e29a0-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-194">System-Flags</span></span>           | <span data-ttu-id="e29a0-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29a0-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="e29a0-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e29a0-196">Classes used in</span></span>        | [<span data-ttu-id="e29a0-197">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e29a0-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e29a0-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e29a0-198">Windows Server 2008</span></span>



| <span data-ttu-id="e29a0-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="e29a0-199">Entry</span></span> | <span data-ttu-id="e29a0-200">Valor</span><span class="sxs-lookup"><span data-stu-id="e29a0-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e29a0-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="e29a0-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29a0-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29a0-203">System-Only</span></span>            | <span data-ttu-id="e29a0-204">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-204">False</span></span>                                                            |
| <span data-ttu-id="e29a0-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e29a0-205">Is-Single-Valued</span></span>       | <span data-ttu-id="e29a0-206">True</span><span class="sxs-lookup"><span data-stu-id="e29a0-206">True</span></span>                                                             |
| <span data-ttu-id="e29a0-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="e29a0-207">Is Indexed</span></span>             | <span data-ttu-id="e29a0-208">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-208">False</span></span>                                                            |
| <span data-ttu-id="e29a0-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e29a0-209">In Global Catalog</span></span>      | <span data-ttu-id="e29a0-210">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-210">False</span></span>                                                            |
| <span data-ttu-id="e29a0-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29a0-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29a0-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e29a0-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e29a0-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29a0-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29a0-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-215">Search-Flags</span></span>           | <span data-ttu-id="e29a0-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29a0-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="e29a0-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-217">System-Flags</span></span>           | <span data-ttu-id="e29a0-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29a0-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="e29a0-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e29a0-219">Classes used in</span></span>        | [<span data-ttu-id="e29a0-220">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e29a0-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e29a0-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e29a0-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e29a0-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="e29a0-222">Entry</span></span> | <span data-ttu-id="e29a0-223">Valor</span><span class="sxs-lookup"><span data-stu-id="e29a0-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e29a0-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="e29a0-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29a0-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29a0-226">System-Only</span></span>            | <span data-ttu-id="e29a0-227">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-227">False</span></span>                                                            |
| <span data-ttu-id="e29a0-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e29a0-228">Is-Single-Valued</span></span>       | <span data-ttu-id="e29a0-229">True</span><span class="sxs-lookup"><span data-stu-id="e29a0-229">True</span></span>                                                             |
| <span data-ttu-id="e29a0-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="e29a0-230">Is Indexed</span></span>             | <span data-ttu-id="e29a0-231">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-231">False</span></span>                                                            |
| <span data-ttu-id="e29a0-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e29a0-232">In Global Catalog</span></span>      | <span data-ttu-id="e29a0-233">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-233">False</span></span>                                                            |
| <span data-ttu-id="e29a0-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29a0-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29a0-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e29a0-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e29a0-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29a0-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29a0-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-238">Search-Flags</span></span>           | <span data-ttu-id="e29a0-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29a0-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="e29a0-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-240">System-Flags</span></span>           | <span data-ttu-id="e29a0-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29a0-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="e29a0-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e29a0-242">Classes used in</span></span>        | [<span data-ttu-id="e29a0-243">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e29a0-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e29a0-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e29a0-244">Windows Server 2012</span></span>



| <span data-ttu-id="e29a0-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="e29a0-245">Entry</span></span> | <span data-ttu-id="e29a0-246">Valor</span><span class="sxs-lookup"><span data-stu-id="e29a0-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="e29a0-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="e29a0-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e29a0-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="e29a0-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="e29a0-249">System-Only</span></span>            | <span data-ttu-id="e29a0-250">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-250">False</span></span>                                                            |
| <span data-ttu-id="e29a0-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e29a0-251">Is-Single-Valued</span></span>       | <span data-ttu-id="e29a0-252">True</span><span class="sxs-lookup"><span data-stu-id="e29a0-252">True</span></span>                                                             |
| <span data-ttu-id="e29a0-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="e29a0-253">Is Indexed</span></span>             | <span data-ttu-id="e29a0-254">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-254">False</span></span>                                                            |
| <span data-ttu-id="e29a0-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e29a0-255">In Global Catalog</span></span>      | <span data-ttu-id="e29a0-256">Falso</span><span class="sxs-lookup"><span data-stu-id="e29a0-256">False</span></span>                                                            |
| <span data-ttu-id="e29a0-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e29a0-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="e29a0-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e29a0-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="e29a0-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e29a0-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e29a0-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="e29a0-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-261">Search-Flags</span></span>           | <span data-ttu-id="e29a0-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e29a0-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="e29a0-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e29a0-263">System-Flags</span></span>           | <span data-ttu-id="e29a0-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e29a0-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="e29a0-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e29a0-265">Classes used in</span></span>        | [<span data-ttu-id="e29a0-266">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e29a0-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





