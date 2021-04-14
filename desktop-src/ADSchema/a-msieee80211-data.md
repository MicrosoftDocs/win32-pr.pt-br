---
title: MS-IEEE-80211-atributo de dados
description: Armazena uma lista de configurações de rede preferenciais em Política de Grupo para redes sem fio.
ms.assetid: 8e5ae2c6-c048-419d-a684-e450a2445a0e
ms.tgt_platform: multiple
keywords:
- MS-IEEE-80211-esquema de atributos de dados do AD
- msieee80211-esquema de AD do atributo de dados
topic_type:
- apiref
api_name:
- ms-ieee-80211-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a53138e15a15e4fafecb998b87ef8b4df71fb2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499983"
---
# <a name="ms-ieee-80211-data-attribute"></a><span data-ttu-id="57f65-105">MS-IEEE-80211-atributo de dados</span><span class="sxs-lookup"><span data-stu-id="57f65-105">ms-ieee-80211-Data attribute</span></span>

<span data-ttu-id="57f65-106">Armazena uma lista de configurações de rede preferenciais em Política de Grupo para redes sem fio.</span><span class="sxs-lookup"><span data-stu-id="57f65-106">Stores a list of preferred network configurations in Group Policy for wireless networks.</span></span>



| <span data-ttu-id="57f65-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="57f65-107">Entry</span></span> | <span data-ttu-id="57f65-108">Valor</span><span class="sxs-lookup"><span data-stu-id="57f65-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="57f65-109">CN</span><span class="sxs-lookup"><span data-stu-id="57f65-109">CN</span></span>                | <span data-ttu-id="57f65-110">MS-IEEE-80211-data</span><span class="sxs-lookup"><span data-stu-id="57f65-110">ms-ieee-80211-Data</span></span>                                                               |
| <span data-ttu-id="57f65-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="57f65-111">Ldap-Display-Name</span></span> | <span data-ttu-id="57f65-112">msieee80211-dados</span><span class="sxs-lookup"><span data-stu-id="57f65-112">msieee80211-Data</span></span>                                                                 |
| <span data-ttu-id="57f65-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="57f65-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="57f65-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="57f65-114">Update Privilege</span></span>  | <span data-ttu-id="57f65-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="57f65-115">Domain administrator</span></span>                                                             |
| <span data-ttu-id="57f65-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="57f65-116">Update Frequency</span></span>  | <span data-ttu-id="57f65-117">Cada vez que um administrador de domínio altera a diretiva de rede sem fio para um domínio ou unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="57f65-117">Each time a Domain Admin changes the wireless network policy for a domain or OU.</span></span> |
| <span data-ttu-id="57f65-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="57f65-118">Attribute-Id</span></span>      | <span data-ttu-id="57f65-119">1.2.840.113556.1.4.1821</span><span class="sxs-lookup"><span data-stu-id="57f65-119">1.2.840.113556.1.4.1821</span></span>                                                          |
| <span data-ttu-id="57f65-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="57f65-120">System-Id-Guid</span></span>    | <span data-ttu-id="57f65-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span><span class="sxs-lookup"><span data-stu-id="57f65-121">0e0d0938-2658-4580-a9f6-7a0ac7b566cb</span></span>                                             |
| <span data-ttu-id="57f65-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="57f65-122">Syntax</span></span>            | [<span data-ttu-id="57f65-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="57f65-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                            |



## <a name="implementations"></a><span data-ttu-id="57f65-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="57f65-124">Implementations</span></span>

-   [<span data-ttu-id="57f65-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="57f65-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="57f65-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="57f65-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="57f65-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="57f65-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="57f65-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="57f65-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="57f65-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="57f65-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="57f65-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57f65-130">Windows Server 2003</span></span>



| <span data-ttu-id="57f65-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="57f65-131">Entry</span></span> | <span data-ttu-id="57f65-132">Valor</span><span class="sxs-lookup"><span data-stu-id="57f65-132">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="57f65-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="57f65-133">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57f65-134">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="57f65-135">System-Only</span></span>            | <span data-ttu-id="57f65-136">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-136">False</span></span>                                                           |
| <span data-ttu-id="57f65-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57f65-137">Is-Single-Valued</span></span>       | <span data-ttu-id="57f65-138">True</span><span class="sxs-lookup"><span data-stu-id="57f65-138">True</span></span>                                                            |
| <span data-ttu-id="57f65-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="57f65-139">Is Indexed</span></span>             | <span data-ttu-id="57f65-140">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-140">False</span></span>                                                           |
| <span data-ttu-id="57f65-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57f65-141">In Global Catalog</span></span>      | <span data-ttu-id="57f65-142">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-142">False</span></span>                                                           |
| <span data-ttu-id="57f65-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57f65-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="57f65-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57f65-144">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="57f65-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57f65-145">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57f65-146">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-147">Search-Flags</span></span>           | <span data-ttu-id="57f65-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57f65-148">0x00000000</span></span>                                                      |
| <span data-ttu-id="57f65-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-149">System-Flags</span></span>           | <span data-ttu-id="57f65-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57f65-150">0x00000010</span></span>                                                      |
| <span data-ttu-id="57f65-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57f65-151">Classes used in</span></span>        | [<span data-ttu-id="57f65-152">**MS-IEEE-80211-política**</span><span class="sxs-lookup"><span data-stu-id="57f65-152">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="57f65-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="57f65-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="57f65-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="57f65-154">Entry</span></span> | <span data-ttu-id="57f65-155">Valor</span><span class="sxs-lookup"><span data-stu-id="57f65-155">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="57f65-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="57f65-156">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57f65-157">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="57f65-158">System-Only</span></span>            | <span data-ttu-id="57f65-159">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-159">False</span></span>                                                           |
| <span data-ttu-id="57f65-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57f65-160">Is-Single-Valued</span></span>       | <span data-ttu-id="57f65-161">True</span><span class="sxs-lookup"><span data-stu-id="57f65-161">True</span></span>                                                            |
| <span data-ttu-id="57f65-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="57f65-162">Is Indexed</span></span>             | <span data-ttu-id="57f65-163">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-163">False</span></span>                                                           |
| <span data-ttu-id="57f65-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57f65-164">In Global Catalog</span></span>      | <span data-ttu-id="57f65-165">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-165">False</span></span>                                                           |
| <span data-ttu-id="57f65-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57f65-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="57f65-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57f65-167">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="57f65-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57f65-168">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57f65-169">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-170">Search-Flags</span></span>           | <span data-ttu-id="57f65-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57f65-171">0x00000000</span></span>                                                      |
| <span data-ttu-id="57f65-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-172">System-Flags</span></span>           | <span data-ttu-id="57f65-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57f65-173">0x00000010</span></span>                                                      |
| <span data-ttu-id="57f65-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57f65-174">Classes used in</span></span>        | [<span data-ttu-id="57f65-175">**MS-IEEE-80211-política**</span><span class="sxs-lookup"><span data-stu-id="57f65-175">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="57f65-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57f65-176">Windows Server 2008</span></span>



| <span data-ttu-id="57f65-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="57f65-177">Entry</span></span> | <span data-ttu-id="57f65-178">Valor</span><span class="sxs-lookup"><span data-stu-id="57f65-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="57f65-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="57f65-179">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57f65-180">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="57f65-181">System-Only</span></span>            | <span data-ttu-id="57f65-182">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-182">False</span></span>                                                           |
| <span data-ttu-id="57f65-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57f65-183">Is-Single-Valued</span></span>       | <span data-ttu-id="57f65-184">True</span><span class="sxs-lookup"><span data-stu-id="57f65-184">True</span></span>                                                            |
| <span data-ttu-id="57f65-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="57f65-185">Is Indexed</span></span>             | <span data-ttu-id="57f65-186">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-186">False</span></span>                                                           |
| <span data-ttu-id="57f65-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57f65-187">In Global Catalog</span></span>      | <span data-ttu-id="57f65-188">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-188">False</span></span>                                                           |
| <span data-ttu-id="57f65-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57f65-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="57f65-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57f65-190">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="57f65-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57f65-191">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57f65-192">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-193">Search-Flags</span></span>           | <span data-ttu-id="57f65-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57f65-194">0x00000000</span></span>                                                      |
| <span data-ttu-id="57f65-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-195">System-Flags</span></span>           | <span data-ttu-id="57f65-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57f65-196">0x00000010</span></span>                                                      |
| <span data-ttu-id="57f65-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57f65-197">Classes used in</span></span>        | [<span data-ttu-id="57f65-198">**MS-IEEE-80211-política**</span><span class="sxs-lookup"><span data-stu-id="57f65-198">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="57f65-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="57f65-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="57f65-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="57f65-200">Entry</span></span> | <span data-ttu-id="57f65-201">Valor</span><span class="sxs-lookup"><span data-stu-id="57f65-201">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="57f65-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="57f65-202">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57f65-203">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="57f65-204">System-Only</span></span>            | <span data-ttu-id="57f65-205">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-205">False</span></span>                                                           |
| <span data-ttu-id="57f65-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57f65-206">Is-Single-Valued</span></span>       | <span data-ttu-id="57f65-207">True</span><span class="sxs-lookup"><span data-stu-id="57f65-207">True</span></span>                                                            |
| <span data-ttu-id="57f65-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="57f65-208">Is Indexed</span></span>             | <span data-ttu-id="57f65-209">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-209">False</span></span>                                                           |
| <span data-ttu-id="57f65-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57f65-210">In Global Catalog</span></span>      | <span data-ttu-id="57f65-211">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-211">False</span></span>                                                           |
| <span data-ttu-id="57f65-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57f65-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="57f65-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57f65-213">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="57f65-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57f65-214">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57f65-215">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-216">Search-Flags</span></span>           | <span data-ttu-id="57f65-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57f65-217">0x00000000</span></span>                                                      |
| <span data-ttu-id="57f65-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-218">System-Flags</span></span>           | <span data-ttu-id="57f65-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57f65-219">0x00000010</span></span>                                                      |
| <span data-ttu-id="57f65-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57f65-220">Classes used in</span></span>        | [<span data-ttu-id="57f65-221">**MS-IEEE-80211-política**</span><span class="sxs-lookup"><span data-stu-id="57f65-221">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="57f65-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="57f65-222">Windows Server 2012</span></span>



| <span data-ttu-id="57f65-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="57f65-223">Entry</span></span> | <span data-ttu-id="57f65-224">Valor</span><span class="sxs-lookup"><span data-stu-id="57f65-224">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="57f65-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="57f65-225">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57f65-226">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="57f65-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="57f65-227">System-Only</span></span>            | <span data-ttu-id="57f65-228">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-228">False</span></span>                                                           |
| <span data-ttu-id="57f65-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57f65-229">Is-Single-Valued</span></span>       | <span data-ttu-id="57f65-230">True</span><span class="sxs-lookup"><span data-stu-id="57f65-230">True</span></span>                                                            |
| <span data-ttu-id="57f65-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="57f65-231">Is Indexed</span></span>             | <span data-ttu-id="57f65-232">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-232">False</span></span>                                                           |
| <span data-ttu-id="57f65-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57f65-233">In Global Catalog</span></span>      | <span data-ttu-id="57f65-234">Falso</span><span class="sxs-lookup"><span data-stu-id="57f65-234">False</span></span>                                                           |
| <span data-ttu-id="57f65-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57f65-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="57f65-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57f65-236">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="57f65-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57f65-237">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57f65-238">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="57f65-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-239">Search-Flags</span></span>           | <span data-ttu-id="57f65-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57f65-240">0x00000000</span></span>                                                      |
| <span data-ttu-id="57f65-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57f65-241">System-Flags</span></span>           | <span data-ttu-id="57f65-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57f65-242">0x00000010</span></span>                                                      |
| <span data-ttu-id="57f65-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57f65-243">Classes used in</span></span>        | [<span data-ttu-id="57f65-244">**MS-IEEE-80211-política**</span><span class="sxs-lookup"><span data-stu-id="57f65-244">**ms-ieee-80211-Policy**</span></span>](c-msieee80211-policy.md)<br/> |



 

 





