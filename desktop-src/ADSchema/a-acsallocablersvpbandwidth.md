---
title: ACS-allocable-RSVP-atributo de largura de banda
description: A largura de banda máxima que pode ser reservada.
ms.assetid: 18d9a5c5-e44c-49e9-a8f0-9386a7b1ff97
ms.tgt_platform: multiple
keywords:
- ACS-allocable-RSVP-atributo de largura de banda do esquema do AD
- Esquema de AD do atributo aCSAllocableRSVPBandwidth
topic_type:
- apiref
api_name:
- ACS-Allocable-RSVP-Bandwidth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6bfe98d30fb8ef959f2e75d078b3a04b325b6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825449"
---
# <a name="acs-allocable-rsvp-bandwidth-attribute"></a><span data-ttu-id="fef2d-105">ACS-allocable-RSVP-atributo de largura de banda</span><span class="sxs-lookup"><span data-stu-id="fef2d-105">ACS-Allocable-RSVP-Bandwidth attribute</span></span>

<span data-ttu-id="fef2d-106">A largura de banda máxima que pode ser reservada.</span><span class="sxs-lookup"><span data-stu-id="fef2d-106">The maximum bandwidth that can be reserved.</span></span>



| <span data-ttu-id="fef2d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="fef2d-107">Entry</span></span> | <span data-ttu-id="fef2d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="fef2d-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="fef2d-109">CN</span><span class="sxs-lookup"><span data-stu-id="fef2d-109">CN</span></span>                | <span data-ttu-id="fef2d-110">ACS-allocable-RSVP-largura de banda</span><span class="sxs-lookup"><span data-stu-id="fef2d-110">ACS-Allocable-RSVP-Bandwidth</span></span>         |
| <span data-ttu-id="fef2d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="fef2d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fef2d-112">aCSAllocableRSVPBandwidth</span><span class="sxs-lookup"><span data-stu-id="fef2d-112">aCSAllocableRSVPBandwidth</span></span>            |
| <span data-ttu-id="fef2d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="fef2d-113">Size</span></span>              | <span data-ttu-id="fef2d-114">8 bytes</span><span class="sxs-lookup"><span data-stu-id="fef2d-114">8 bytes</span></span>                              |
| <span data-ttu-id="fef2d-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="fef2d-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="fef2d-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="fef2d-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="fef2d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fef2d-117">Attribute-Id</span></span>      | <span data-ttu-id="fef2d-118">1.2.840.113556.1.4.766</span><span class="sxs-lookup"><span data-stu-id="fef2d-118">1.2.840.113556.1.4.766</span></span>               |
| <span data-ttu-id="fef2d-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="fef2d-119">System-Id-Guid</span></span>    | <span data-ttu-id="fef2d-120">7f561283-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fef2d-120">7f561283-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="fef2d-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="fef2d-121">Syntax</span></span>            | [<span data-ttu-id="fef2d-122">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="fef2d-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="fef2d-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="fef2d-123">Implementations</span></span>

-   [<span data-ttu-id="fef2d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fef2d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fef2d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fef2d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fef2d-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fef2d-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fef2d-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fef2d-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fef2d-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fef2d-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fef2d-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fef2d-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fef2d-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fef2d-130">Windows 2000 Server</span></span>



| <span data-ttu-id="fef2d-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="fef2d-131">Entry</span></span> | <span data-ttu-id="fef2d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="fef2d-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef2d-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="fef2d-133">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef2d-134">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef2d-135">System-Only</span></span>            | <span data-ttu-id="fef2d-136">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-136">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fef2d-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fef2d-138">True</span><span class="sxs-lookup"><span data-stu-id="fef2d-138">True</span></span>                                                                                                       |
| <span data-ttu-id="fef2d-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="fef2d-139">Is Indexed</span></span>             | <span data-ttu-id="fef2d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-140">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fef2d-141">In Global Catalog</span></span>      | <span data-ttu-id="fef2d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-142">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fef2d-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef2d-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fef2d-144">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="fef2d-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef2d-145">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef2d-146">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-147">Search-Flags</span></span>           | <span data-ttu-id="fef2d-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef2d-148">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-149">System-Flags</span></span>           | <span data-ttu-id="fef2d-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef2d-150">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fef2d-151">Classes used in</span></span>        | [<span data-ttu-id="fef2d-152">**ACS-limites de recursos**</span><span class="sxs-lookup"><span data-stu-id="fef2d-152">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="fef2d-153">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="fef2d-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fef2d-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fef2d-154">Windows Server 2003</span></span>



| <span data-ttu-id="fef2d-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="fef2d-155">Entry</span></span> | <span data-ttu-id="fef2d-156">Valor</span><span class="sxs-lookup"><span data-stu-id="fef2d-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef2d-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="fef2d-157">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef2d-158">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef2d-159">System-Only</span></span>            | <span data-ttu-id="fef2d-160">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-160">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fef2d-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fef2d-162">True</span><span class="sxs-lookup"><span data-stu-id="fef2d-162">True</span></span>                                                                                                       |
| <span data-ttu-id="fef2d-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="fef2d-163">Is Indexed</span></span>             | <span data-ttu-id="fef2d-164">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-164">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fef2d-165">In Global Catalog</span></span>      | <span data-ttu-id="fef2d-166">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-166">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fef2d-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef2d-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fef2d-168">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="fef2d-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef2d-169">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef2d-170">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-171">Search-Flags</span></span>           | <span data-ttu-id="fef2d-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef2d-172">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-173">System-Flags</span></span>           | <span data-ttu-id="fef2d-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef2d-174">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fef2d-175">Classes used in</span></span>        | [<span data-ttu-id="fef2d-176">**ACS-limites de recursos**</span><span class="sxs-lookup"><span data-stu-id="fef2d-176">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="fef2d-177">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="fef2d-177">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fef2d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fef2d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fef2d-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="fef2d-179">Entry</span></span> | <span data-ttu-id="fef2d-180">Valor</span><span class="sxs-lookup"><span data-stu-id="fef2d-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef2d-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="fef2d-181">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef2d-182">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef2d-183">System-Only</span></span>            | <span data-ttu-id="fef2d-184">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-184">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fef2d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="fef2d-186">True</span><span class="sxs-lookup"><span data-stu-id="fef2d-186">True</span></span>                                                                                                       |
| <span data-ttu-id="fef2d-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="fef2d-187">Is Indexed</span></span>             | <span data-ttu-id="fef2d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-188">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fef2d-189">In Global Catalog</span></span>      | <span data-ttu-id="fef2d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-190">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fef2d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef2d-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fef2d-192">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="fef2d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef2d-193">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef2d-194">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-195">Search-Flags</span></span>           | <span data-ttu-id="fef2d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef2d-196">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-197">System-Flags</span></span>           | <span data-ttu-id="fef2d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef2d-198">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fef2d-199">Classes used in</span></span>        | [<span data-ttu-id="fef2d-200">**ACS-limites de recursos**</span><span class="sxs-lookup"><span data-stu-id="fef2d-200">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="fef2d-201">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="fef2d-201">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fef2d-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fef2d-202">Windows Server 2008</span></span>



| <span data-ttu-id="fef2d-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="fef2d-203">Entry</span></span> | <span data-ttu-id="fef2d-204">Valor</span><span class="sxs-lookup"><span data-stu-id="fef2d-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef2d-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="fef2d-205">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef2d-206">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef2d-207">System-Only</span></span>            | <span data-ttu-id="fef2d-208">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-208">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fef2d-209">Is-Single-Valued</span></span>       | <span data-ttu-id="fef2d-210">True</span><span class="sxs-lookup"><span data-stu-id="fef2d-210">True</span></span>                                                                                                       |
| <span data-ttu-id="fef2d-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="fef2d-211">Is Indexed</span></span>             | <span data-ttu-id="fef2d-212">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-212">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fef2d-213">In Global Catalog</span></span>      | <span data-ttu-id="fef2d-214">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-214">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fef2d-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef2d-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fef2d-216">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="fef2d-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef2d-217">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef2d-218">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-219">Search-Flags</span></span>           | <span data-ttu-id="fef2d-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef2d-220">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-221">System-Flags</span></span>           | <span data-ttu-id="fef2d-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef2d-222">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fef2d-223">Classes used in</span></span>        | [<span data-ttu-id="fef2d-224">**ACS-limites de recursos**</span><span class="sxs-lookup"><span data-stu-id="fef2d-224">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="fef2d-225">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="fef2d-225">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fef2d-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fef2d-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fef2d-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="fef2d-227">Entry</span></span> | <span data-ttu-id="fef2d-228">Valor</span><span class="sxs-lookup"><span data-stu-id="fef2d-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef2d-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="fef2d-229">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef2d-230">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef2d-231">System-Only</span></span>            | <span data-ttu-id="fef2d-232">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-232">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fef2d-233">Is-Single-Valued</span></span>       | <span data-ttu-id="fef2d-234">True</span><span class="sxs-lookup"><span data-stu-id="fef2d-234">True</span></span>                                                                                                       |
| <span data-ttu-id="fef2d-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="fef2d-235">Is Indexed</span></span>             | <span data-ttu-id="fef2d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-236">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fef2d-237">In Global Catalog</span></span>      | <span data-ttu-id="fef2d-238">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-238">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fef2d-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef2d-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fef2d-240">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="fef2d-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef2d-241">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef2d-242">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-243">Search-Flags</span></span>           | <span data-ttu-id="fef2d-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef2d-244">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-245">System-Flags</span></span>           | <span data-ttu-id="fef2d-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef2d-246">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fef2d-247">Classes used in</span></span>        | [<span data-ttu-id="fef2d-248">**ACS-limites de recursos**</span><span class="sxs-lookup"><span data-stu-id="fef2d-248">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="fef2d-249">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="fef2d-249">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fef2d-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fef2d-250">Windows Server 2012</span></span>



| <span data-ttu-id="fef2d-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="fef2d-251">Entry</span></span> | <span data-ttu-id="fef2d-252">Valor</span><span class="sxs-lookup"><span data-stu-id="fef2d-252">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fef2d-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="fef2d-253">Link-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fef2d-254">MAPI-Id</span></span>                | \-                                                                                                         |
| <span data-ttu-id="fef2d-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="fef2d-255">System-Only</span></span>            | <span data-ttu-id="fef2d-256">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-256">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="fef2d-257">Is-Single-Valued</span></span>       | <span data-ttu-id="fef2d-258">True</span><span class="sxs-lookup"><span data-stu-id="fef2d-258">True</span></span>                                                                                                       |
| <span data-ttu-id="fef2d-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="fef2d-259">Is Indexed</span></span>             | <span data-ttu-id="fef2d-260">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-260">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="fef2d-261">In Global Catalog</span></span>      | <span data-ttu-id="fef2d-262">Falso</span><span class="sxs-lookup"><span data-stu-id="fef2d-262">False</span></span>                                                                                                      |
| <span data-ttu-id="fef2d-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="fef2d-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="fef2d-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="fef2d-264">O:BAG:BAD:S:</span></span>                                                                                               |
| <span data-ttu-id="fef2d-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fef2d-265">Range-Lower</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fef2d-266">Range-Upper</span></span>            | \-                                                                                                         |
| <span data-ttu-id="fef2d-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-267">Search-Flags</span></span>           | <span data-ttu-id="fef2d-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fef2d-268">0x00000000</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fef2d-269">System-Flags</span></span>           | <span data-ttu-id="fef2d-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fef2d-270">0x00000010</span></span>                                                                                                 |
| <span data-ttu-id="fef2d-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="fef2d-271">Classes used in</span></span>        | [<span data-ttu-id="fef2d-272">**ACS-limites de recursos**</span><span class="sxs-lookup"><span data-stu-id="fef2d-272">**ACS-Resource-Limits**</span></span>](c-acsresourcelimits.md)<br/> [<span data-ttu-id="fef2d-273">**ACS-sub-rede**</span><span class="sxs-lookup"><span data-stu-id="fef2d-273">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





