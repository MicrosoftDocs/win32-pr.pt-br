---
title: atributo ms-DS-AZ-Domain-Timeout
description: Tempo, em milissegundos, depois que um domínio é detectado como inacessível e antes de o DC ser tentado novamente.
ms.assetid: b2523faa-7cf1-4325-a3fa-70c5f568adaa
ms.tgt_platform: multiple
keywords:
- ms-DS-AZ-Domain-timeout atributo AD Schema
- atributo msDS-AzDomainTimeout do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Az-Domain-Timeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce6f457977de1124438fa4b54e4a84d1cb6d54e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825210"
---
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="250f4-105">atributo ms-DS-AZ-Domain-Timeout</span><span class="sxs-lookup"><span data-stu-id="250f4-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="250f4-106">Tempo, em milissegundos, depois que um domínio é detectado como inacessível e antes de o DC ser tentado novamente.</span><span class="sxs-lookup"><span data-stu-id="250f4-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="250f4-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="250f4-107">Entry</span></span> | <span data-ttu-id="250f4-108">Valor</span><span class="sxs-lookup"><span data-stu-id="250f4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="250f4-109">CN</span><span class="sxs-lookup"><span data-stu-id="250f4-109">CN</span></span>                | <span data-ttu-id="250f4-110">ms-DS-AZ-Domain-Timeout</span><span class="sxs-lookup"><span data-stu-id="250f4-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="250f4-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="250f4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="250f4-112">msDS-AzDomainTimeout</span><span class="sxs-lookup"><span data-stu-id="250f4-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="250f4-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="250f4-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="250f4-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="250f4-114">Update Privilege</span></span>  | <span data-ttu-id="250f4-115">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="250f4-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="250f4-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="250f4-116">Update Frequency</span></span>  | <span data-ttu-id="250f4-117">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="250f4-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="250f4-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="250f4-118">Attribute-Id</span></span>      | <span data-ttu-id="250f4-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="250f4-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="250f4-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="250f4-120">System-Id-Guid</span></span>    | <span data-ttu-id="250f4-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="250f4-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="250f4-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="250f4-122">Syntax</span></span>            | [<span data-ttu-id="250f4-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="250f4-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="250f4-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="250f4-124">Implementations</span></span>

-   [<span data-ttu-id="250f4-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="250f4-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="250f4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="250f4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="250f4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="250f4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="250f4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="250f4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="250f4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="250f4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="250f4-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="250f4-130">Windows Server 2003</span></span>



| <span data-ttu-id="250f4-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="250f4-131">Entry</span></span> | <span data-ttu-id="250f4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="250f4-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="250f4-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="250f4-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="250f4-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="250f4-135">System-Only</span></span>            | <span data-ttu-id="250f4-136">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-136">False</span></span>                                                              |
| <span data-ttu-id="250f4-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="250f4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="250f4-138">True</span><span class="sxs-lookup"><span data-stu-id="250f4-138">True</span></span>                                                               |
| <span data-ttu-id="250f4-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="250f4-139">Is Indexed</span></span>             | <span data-ttu-id="250f4-140">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-140">False</span></span>                                                              |
| <span data-ttu-id="250f4-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="250f4-141">In Global Catalog</span></span>      | <span data-ttu-id="250f4-142">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-142">False</span></span>                                                              |
| <span data-ttu-id="250f4-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="250f4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="250f4-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="250f4-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="250f4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="250f4-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="250f4-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-147">Search-Flags</span></span>           | <span data-ttu-id="250f4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="250f4-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="250f4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-149">System-Flags</span></span>           | <span data-ttu-id="250f4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="250f4-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="250f4-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="250f4-151">Classes used in</span></span>        | [<span data-ttu-id="250f4-152">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="250f4-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="250f4-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="250f4-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="250f4-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="250f4-154">Entry</span></span> | <span data-ttu-id="250f4-155">Valor</span><span class="sxs-lookup"><span data-stu-id="250f4-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="250f4-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="250f4-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="250f4-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="250f4-158">System-Only</span></span>            | <span data-ttu-id="250f4-159">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-159">False</span></span>                                                              |
| <span data-ttu-id="250f4-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="250f4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="250f4-161">True</span><span class="sxs-lookup"><span data-stu-id="250f4-161">True</span></span>                                                               |
| <span data-ttu-id="250f4-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="250f4-162">Is Indexed</span></span>             | <span data-ttu-id="250f4-163">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-163">False</span></span>                                                              |
| <span data-ttu-id="250f4-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="250f4-164">In Global Catalog</span></span>      | <span data-ttu-id="250f4-165">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-165">False</span></span>                                                              |
| <span data-ttu-id="250f4-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="250f4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="250f4-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="250f4-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="250f4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="250f4-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="250f4-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-170">Search-Flags</span></span>           | <span data-ttu-id="250f4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="250f4-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="250f4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-172">System-Flags</span></span>           | <span data-ttu-id="250f4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="250f4-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="250f4-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="250f4-174">Classes used in</span></span>        | [<span data-ttu-id="250f4-175">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="250f4-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="250f4-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="250f4-176">Windows Server 2008</span></span>



| <span data-ttu-id="250f4-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="250f4-177">Entry</span></span> | <span data-ttu-id="250f4-178">Valor</span><span class="sxs-lookup"><span data-stu-id="250f4-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="250f4-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="250f4-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="250f4-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="250f4-181">System-Only</span></span>            | <span data-ttu-id="250f4-182">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-182">False</span></span>                                                              |
| <span data-ttu-id="250f4-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="250f4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="250f4-184">True</span><span class="sxs-lookup"><span data-stu-id="250f4-184">True</span></span>                                                               |
| <span data-ttu-id="250f4-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="250f4-185">Is Indexed</span></span>             | <span data-ttu-id="250f4-186">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-186">False</span></span>                                                              |
| <span data-ttu-id="250f4-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="250f4-187">In Global Catalog</span></span>      | <span data-ttu-id="250f4-188">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-188">False</span></span>                                                              |
| <span data-ttu-id="250f4-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="250f4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="250f4-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="250f4-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="250f4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="250f4-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="250f4-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-193">Search-Flags</span></span>           | <span data-ttu-id="250f4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="250f4-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="250f4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-195">System-Flags</span></span>           | <span data-ttu-id="250f4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="250f4-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="250f4-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="250f4-197">Classes used in</span></span>        | [<span data-ttu-id="250f4-198">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="250f4-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="250f4-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="250f4-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="250f4-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="250f4-200">Entry</span></span> | <span data-ttu-id="250f4-201">Valor</span><span class="sxs-lookup"><span data-stu-id="250f4-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="250f4-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="250f4-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="250f4-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="250f4-204">System-Only</span></span>            | <span data-ttu-id="250f4-205">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-205">False</span></span>                                                              |
| <span data-ttu-id="250f4-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="250f4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="250f4-207">True</span><span class="sxs-lookup"><span data-stu-id="250f4-207">True</span></span>                                                               |
| <span data-ttu-id="250f4-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="250f4-208">Is Indexed</span></span>             | <span data-ttu-id="250f4-209">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-209">False</span></span>                                                              |
| <span data-ttu-id="250f4-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="250f4-210">In Global Catalog</span></span>      | <span data-ttu-id="250f4-211">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-211">False</span></span>                                                              |
| <span data-ttu-id="250f4-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="250f4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="250f4-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="250f4-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="250f4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="250f4-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="250f4-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-216">Search-Flags</span></span>           | <span data-ttu-id="250f4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="250f4-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="250f4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-218">System-Flags</span></span>           | <span data-ttu-id="250f4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="250f4-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="250f4-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="250f4-220">Classes used in</span></span>        | [<span data-ttu-id="250f4-221">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="250f4-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="250f4-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="250f4-222">Windows Server 2012</span></span>



| <span data-ttu-id="250f4-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="250f4-223">Entry</span></span> | <span data-ttu-id="250f4-224">Valor</span><span class="sxs-lookup"><span data-stu-id="250f4-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="250f4-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="250f4-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="250f4-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="250f4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="250f4-227">System-Only</span></span>            | <span data-ttu-id="250f4-228">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-228">False</span></span>                                                              |
| <span data-ttu-id="250f4-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="250f4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="250f4-230">True</span><span class="sxs-lookup"><span data-stu-id="250f4-230">True</span></span>                                                               |
| <span data-ttu-id="250f4-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="250f4-231">Is Indexed</span></span>             | <span data-ttu-id="250f4-232">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-232">False</span></span>                                                              |
| <span data-ttu-id="250f4-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="250f4-233">In Global Catalog</span></span>      | <span data-ttu-id="250f4-234">Falso</span><span class="sxs-lookup"><span data-stu-id="250f4-234">False</span></span>                                                              |
| <span data-ttu-id="250f4-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="250f4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="250f4-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="250f4-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="250f4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="250f4-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="250f4-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="250f4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-239">Search-Flags</span></span>           | <span data-ttu-id="250f4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="250f4-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="250f4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="250f4-241">System-Flags</span></span>           | <span data-ttu-id="250f4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="250f4-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="250f4-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="250f4-243">Classes used in</span></span>        | [<span data-ttu-id="250f4-244">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="250f4-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





