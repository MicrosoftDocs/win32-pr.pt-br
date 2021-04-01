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
# <a name="ms-ds-az-domain-timeout-attribute"></a><span data-ttu-id="8dbf0-105">atributo ms-DS-AZ-Domain-Timeout</span><span class="sxs-lookup"><span data-stu-id="8dbf0-105">ms-DS-Az-Domain-Timeout attribute</span></span>

<span data-ttu-id="8dbf0-106">Tempo, em milissegundos, depois que um domínio é detectado como inacessível e antes de o DC ser tentado novamente.</span><span class="sxs-lookup"><span data-stu-id="8dbf0-106">Time, in milliseconds, after a domain is detected to be unreachable and before the DC is tried again.</span></span>



| <span data-ttu-id="8dbf0-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8dbf0-107">Entry</span></span> | <span data-ttu-id="8dbf0-108">Valor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8dbf0-109">CN</span><span class="sxs-lookup"><span data-stu-id="8dbf0-109">CN</span></span>                | <span data-ttu-id="8dbf0-110">ms-DS-AZ-Domain-Timeout</span><span class="sxs-lookup"><span data-stu-id="8dbf0-110">ms-DS-Az-Domain-Timeout</span></span>                 |
| <span data-ttu-id="8dbf0-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8dbf0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8dbf0-112">msDS-AzDomainTimeout</span><span class="sxs-lookup"><span data-stu-id="8dbf0-112">msDS-AzDomainTimeout</span></span>                    |
| <span data-ttu-id="8dbf0-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8dbf0-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="8dbf0-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8dbf0-114">Update Privilege</span></span>  | <span data-ttu-id="8dbf0-115">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="8dbf0-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="8dbf0-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8dbf0-116">Update Frequency</span></span>  | <span data-ttu-id="8dbf0-117">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="8dbf0-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="8dbf0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8dbf0-118">Attribute-Id</span></span>      | <span data-ttu-id="8dbf0-119">1.2.840.113556.1.4.1795</span><span class="sxs-lookup"><span data-stu-id="8dbf0-119">1.2.840.113556.1.4.1795</span></span>                 |
| <span data-ttu-id="8dbf0-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8dbf0-120">System-Id-Guid</span></span>    | <span data-ttu-id="8dbf0-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span><span class="sxs-lookup"><span data-stu-id="8dbf0-121">6448f56a-ca70-4e2e-b0af-d20e4ce653d0</span></span>    |
| <span data-ttu-id="8dbf0-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dbf0-122">Syntax</span></span>            | [<span data-ttu-id="8dbf0-123">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-123">**Enumeration**</span></span>](s-enumeration.md)    |



## <a name="implementations"></a><span data-ttu-id="8dbf0-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="8dbf0-124">Implementations</span></span>

-   [<span data-ttu-id="8dbf0-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8dbf0-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8dbf0-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8dbf0-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8dbf0-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8dbf0-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8dbf0-130">Windows Server 2003</span></span>



| <span data-ttu-id="8dbf0-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="8dbf0-131">Entry</span></span> | <span data-ttu-id="8dbf0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-132">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8dbf0-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="8dbf0-133">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dbf0-134">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dbf0-135">System-Only</span></span>            | <span data-ttu-id="8dbf0-136">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-136">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8dbf0-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8dbf0-138">True</span><span class="sxs-lookup"><span data-stu-id="8dbf0-138">True</span></span>                                                               |
| <span data-ttu-id="8dbf0-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="8dbf0-139">Is Indexed</span></span>             | <span data-ttu-id="8dbf0-140">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-140">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8dbf0-141">In Global Catalog</span></span>      | <span data-ttu-id="8dbf0-142">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-142">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dbf0-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8dbf0-144">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8dbf0-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dbf0-145">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dbf0-146">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-147">Search-Flags</span></span>           | <span data-ttu-id="8dbf0-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dbf0-148">0x00000000</span></span>                                                         |
| <span data-ttu-id="8dbf0-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-149">System-Flags</span></span>           | <span data-ttu-id="8dbf0-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dbf0-150">0x00000010</span></span>                                                         |
| <span data-ttu-id="8dbf0-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8dbf0-151">Classes used in</span></span>        | [<span data-ttu-id="8dbf0-152">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8dbf0-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8dbf0-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8dbf0-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="8dbf0-154">Entry</span></span> | <span data-ttu-id="8dbf0-155">Valor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-155">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8dbf0-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="8dbf0-156">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dbf0-157">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dbf0-158">System-Only</span></span>            | <span data-ttu-id="8dbf0-159">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-159">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8dbf0-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8dbf0-161">True</span><span class="sxs-lookup"><span data-stu-id="8dbf0-161">True</span></span>                                                               |
| <span data-ttu-id="8dbf0-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="8dbf0-162">Is Indexed</span></span>             | <span data-ttu-id="8dbf0-163">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-163">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8dbf0-164">In Global Catalog</span></span>      | <span data-ttu-id="8dbf0-165">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-165">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dbf0-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8dbf0-167">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8dbf0-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dbf0-168">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dbf0-169">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-170">Search-Flags</span></span>           | <span data-ttu-id="8dbf0-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dbf0-171">0x00000000</span></span>                                                         |
| <span data-ttu-id="8dbf0-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-172">System-Flags</span></span>           | <span data-ttu-id="8dbf0-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dbf0-173">0x00000010</span></span>                                                         |
| <span data-ttu-id="8dbf0-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8dbf0-174">Classes used in</span></span>        | [<span data-ttu-id="8dbf0-175">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-175">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8dbf0-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dbf0-176">Windows Server 2008</span></span>



| <span data-ttu-id="8dbf0-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="8dbf0-177">Entry</span></span> | <span data-ttu-id="8dbf0-178">Valor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8dbf0-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="8dbf0-179">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dbf0-180">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dbf0-181">System-Only</span></span>            | <span data-ttu-id="8dbf0-182">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-182">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8dbf0-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8dbf0-184">True</span><span class="sxs-lookup"><span data-stu-id="8dbf0-184">True</span></span>                                                               |
| <span data-ttu-id="8dbf0-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="8dbf0-185">Is Indexed</span></span>             | <span data-ttu-id="8dbf0-186">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-186">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8dbf0-187">In Global Catalog</span></span>      | <span data-ttu-id="8dbf0-188">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-188">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dbf0-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8dbf0-190">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8dbf0-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dbf0-191">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dbf0-192">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-193">Search-Flags</span></span>           | <span data-ttu-id="8dbf0-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dbf0-194">0x00000000</span></span>                                                         |
| <span data-ttu-id="8dbf0-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-195">System-Flags</span></span>           | <span data-ttu-id="8dbf0-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dbf0-196">0x00000010</span></span>                                                         |
| <span data-ttu-id="8dbf0-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8dbf0-197">Classes used in</span></span>        | [<span data-ttu-id="8dbf0-198">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-198">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8dbf0-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8dbf0-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8dbf0-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="8dbf0-200">Entry</span></span> | <span data-ttu-id="8dbf0-201">Valor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-201">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8dbf0-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="8dbf0-202">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dbf0-203">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dbf0-204">System-Only</span></span>            | <span data-ttu-id="8dbf0-205">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-205">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8dbf0-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8dbf0-207">True</span><span class="sxs-lookup"><span data-stu-id="8dbf0-207">True</span></span>                                                               |
| <span data-ttu-id="8dbf0-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="8dbf0-208">Is Indexed</span></span>             | <span data-ttu-id="8dbf0-209">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-209">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8dbf0-210">In Global Catalog</span></span>      | <span data-ttu-id="8dbf0-211">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-211">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dbf0-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8dbf0-213">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8dbf0-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dbf0-214">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dbf0-215">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-216">Search-Flags</span></span>           | <span data-ttu-id="8dbf0-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dbf0-217">0x00000000</span></span>                                                         |
| <span data-ttu-id="8dbf0-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-218">System-Flags</span></span>           | <span data-ttu-id="8dbf0-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dbf0-219">0x00000010</span></span>                                                         |
| <span data-ttu-id="8dbf0-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8dbf0-220">Classes used in</span></span>        | [<span data-ttu-id="8dbf0-221">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-221">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8dbf0-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8dbf0-222">Windows Server 2012</span></span>



| <span data-ttu-id="8dbf0-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="8dbf0-223">Entry</span></span> | <span data-ttu-id="8dbf0-224">Valor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-224">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="8dbf0-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="8dbf0-225">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8dbf0-226">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="8dbf0-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8dbf0-227">System-Only</span></span>            | <span data-ttu-id="8dbf0-228">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-228">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8dbf0-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8dbf0-230">True</span><span class="sxs-lookup"><span data-stu-id="8dbf0-230">True</span></span>                                                               |
| <span data-ttu-id="8dbf0-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="8dbf0-231">Is Indexed</span></span>             | <span data-ttu-id="8dbf0-232">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-232">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8dbf0-233">In Global Catalog</span></span>      | <span data-ttu-id="8dbf0-234">Falso</span><span class="sxs-lookup"><span data-stu-id="8dbf0-234">False</span></span>                                                              |
| <span data-ttu-id="8dbf0-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8dbf0-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8dbf0-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8dbf0-236">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="8dbf0-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8dbf0-237">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8dbf0-238">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="8dbf0-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-239">Search-Flags</span></span>           | <span data-ttu-id="8dbf0-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8dbf0-240">0x00000000</span></span>                                                         |
| <span data-ttu-id="8dbf0-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8dbf0-241">System-Flags</span></span>           | <span data-ttu-id="8dbf0-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8dbf0-242">0x00000010</span></span>                                                         |
| <span data-ttu-id="8dbf0-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8dbf0-243">Classes used in</span></span>        | [<span data-ttu-id="8dbf0-244">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="8dbf0-244">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> |



 

 





