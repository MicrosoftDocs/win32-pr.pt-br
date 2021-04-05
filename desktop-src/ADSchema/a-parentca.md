---
title: Atributo pai-CA
description: O nome distinto de um objeto de autoridade de certificação (CA) para uma autoridade de certificação pai.
ms.assetid: ccb5b338-e67d-4f1b-b13c-257746ab39d1
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo pai-CA
- Esquema de AD do atributo parentCA
topic_type:
- apiref
api_name:
- Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c065c86548769ab8643a561c7aec3132728d5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087007"
---
# <a name="parent-ca-attribute"></a><span data-ttu-id="efafc-105">Atributo pai-CA</span><span class="sxs-lookup"><span data-stu-id="efafc-105">Parent-CA attribute</span></span>

<span data-ttu-id="efafc-106">O nome distinto de um objeto de autoridade de certificação (CA) para uma autoridade de certificação pai.</span><span class="sxs-lookup"><span data-stu-id="efafc-106">The distinguished name of a certification authority (CA) object for a parent CA.</span></span>



| <span data-ttu-id="efafc-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="efafc-107">Entry</span></span> | <span data-ttu-id="efafc-108">Valor</span><span class="sxs-lookup"><span data-stu-id="efafc-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="efafc-109">CN</span><span class="sxs-lookup"><span data-stu-id="efafc-109">CN</span></span>                | <span data-ttu-id="efafc-110">Pai-AC</span><span class="sxs-lookup"><span data-stu-id="efafc-110">Parent-CA</span></span>                               |
| <span data-ttu-id="efafc-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="efafc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="efafc-112">parentCA</span><span class="sxs-lookup"><span data-stu-id="efafc-112">parentCA</span></span>                                |
| <span data-ttu-id="efafc-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="efafc-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="efafc-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="efafc-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="efafc-115">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="efafc-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="efafc-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="efafc-116">Attribute-Id</span></span>      | <span data-ttu-id="efafc-117">1.2.840.113556.1.4.557</span><span class="sxs-lookup"><span data-stu-id="efafc-117">1.2.840.113556.1.4.557</span></span>                  |
| <span data-ttu-id="efafc-118">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="efafc-118">System-Id-Guid</span></span>    | <span data-ttu-id="efafc-119">5245801b-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="efafc-119">5245801b-ca6a-11d0-afff-0000f80367c1</span></span>    |
| <span data-ttu-id="efafc-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="efafc-120">Syntax</span></span>            | [<span data-ttu-id="efafc-121">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="efafc-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="efafc-122">Implementações</span><span class="sxs-lookup"><span data-stu-id="efafc-122">Implementations</span></span>

-   [<span data-ttu-id="efafc-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="efafc-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="efafc-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="efafc-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="efafc-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="efafc-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="efafc-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="efafc-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="efafc-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="efafc-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="efafc-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="efafc-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="efafc-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="efafc-129">Windows 2000 Server</span></span>



| <span data-ttu-id="efafc-130">Entrada</span><span class="sxs-lookup"><span data-stu-id="efafc-130">Entry</span></span> | <span data-ttu-id="efafc-131">Valor</span><span class="sxs-lookup"><span data-stu-id="efafc-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="efafc-132">ID do link</span><span class="sxs-lookup"><span data-stu-id="efafc-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efafc-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="efafc-134">System-Only</span></span>            | <span data-ttu-id="efafc-135">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-135">False</span></span>                                                                  |
| <span data-ttu-id="efafc-136">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efafc-136">Is-Single-Valued</span></span>       | <span data-ttu-id="efafc-137">True</span><span class="sxs-lookup"><span data-stu-id="efafc-137">True</span></span>                                                                   |
| <span data-ttu-id="efafc-138">É indexado</span><span class="sxs-lookup"><span data-stu-id="efafc-138">Is Indexed</span></span>             | <span data-ttu-id="efafc-139">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-139">False</span></span>                                                                  |
| <span data-ttu-id="efafc-140">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efafc-140">In Global Catalog</span></span>      | <span data-ttu-id="efafc-141">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-141">False</span></span>                                                                  |
| <span data-ttu-id="efafc-142">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efafc-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="efafc-143">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efafc-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="efafc-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efafc-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efafc-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-146">Search-Flags</span></span>           | <span data-ttu-id="efafc-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efafc-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="efafc-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-148">System-Flags</span></span>           | <span data-ttu-id="efafc-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efafc-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="efafc-150">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efafc-150">Classes used in</span></span>        | [<span data-ttu-id="efafc-151">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="efafc-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="efafc-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="efafc-152">Windows Server 2003</span></span>



| <span data-ttu-id="efafc-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="efafc-153">Entry</span></span> | <span data-ttu-id="efafc-154">Valor</span><span class="sxs-lookup"><span data-stu-id="efafc-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="efafc-155">ID do link</span><span class="sxs-lookup"><span data-stu-id="efafc-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efafc-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="efafc-157">System-Only</span></span>            | <span data-ttu-id="efafc-158">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-158">False</span></span>                                                                  |
| <span data-ttu-id="efafc-159">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efafc-159">Is-Single-Valued</span></span>       | <span data-ttu-id="efafc-160">True</span><span class="sxs-lookup"><span data-stu-id="efafc-160">True</span></span>                                                                   |
| <span data-ttu-id="efafc-161">É indexado</span><span class="sxs-lookup"><span data-stu-id="efafc-161">Is Indexed</span></span>             | <span data-ttu-id="efafc-162">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-162">False</span></span>                                                                  |
| <span data-ttu-id="efafc-163">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efafc-163">In Global Catalog</span></span>      | <span data-ttu-id="efafc-164">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-164">False</span></span>                                                                  |
| <span data-ttu-id="efafc-165">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efafc-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="efafc-166">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efafc-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="efafc-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efafc-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efafc-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-169">Search-Flags</span></span>           | <span data-ttu-id="efafc-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efafc-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="efafc-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-171">System-Flags</span></span>           | <span data-ttu-id="efafc-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efafc-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="efafc-173">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efafc-173">Classes used in</span></span>        | [<span data-ttu-id="efafc-174">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="efafc-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="efafc-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="efafc-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="efafc-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="efafc-176">Entry</span></span> | <span data-ttu-id="efafc-177">Valor</span><span class="sxs-lookup"><span data-stu-id="efafc-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="efafc-178">ID do link</span><span class="sxs-lookup"><span data-stu-id="efafc-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efafc-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="efafc-180">System-Only</span></span>            | <span data-ttu-id="efafc-181">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-181">False</span></span>                                                                  |
| <span data-ttu-id="efafc-182">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efafc-182">Is-Single-Valued</span></span>       | <span data-ttu-id="efafc-183">True</span><span class="sxs-lookup"><span data-stu-id="efafc-183">True</span></span>                                                                   |
| <span data-ttu-id="efafc-184">É indexado</span><span class="sxs-lookup"><span data-stu-id="efafc-184">Is Indexed</span></span>             | <span data-ttu-id="efafc-185">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-185">False</span></span>                                                                  |
| <span data-ttu-id="efafc-186">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efafc-186">In Global Catalog</span></span>      | <span data-ttu-id="efafc-187">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-187">False</span></span>                                                                  |
| <span data-ttu-id="efafc-188">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efafc-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="efafc-189">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efafc-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="efafc-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efafc-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efafc-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-192">Search-Flags</span></span>           | <span data-ttu-id="efafc-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efafc-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="efafc-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-194">System-Flags</span></span>           | <span data-ttu-id="efafc-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efafc-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="efafc-196">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efafc-196">Classes used in</span></span>        | [<span data-ttu-id="efafc-197">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="efafc-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="efafc-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efafc-198">Windows Server 2008</span></span>



| <span data-ttu-id="efafc-199">Entrada</span><span class="sxs-lookup"><span data-stu-id="efafc-199">Entry</span></span> | <span data-ttu-id="efafc-200">Valor</span><span class="sxs-lookup"><span data-stu-id="efafc-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="efafc-201">ID do link</span><span class="sxs-lookup"><span data-stu-id="efafc-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efafc-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="efafc-203">System-Only</span></span>            | <span data-ttu-id="efafc-204">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-204">False</span></span>                                                                  |
| <span data-ttu-id="efafc-205">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efafc-205">Is-Single-Valued</span></span>       | <span data-ttu-id="efafc-206">True</span><span class="sxs-lookup"><span data-stu-id="efafc-206">True</span></span>                                                                   |
| <span data-ttu-id="efafc-207">É indexado</span><span class="sxs-lookup"><span data-stu-id="efafc-207">Is Indexed</span></span>             | <span data-ttu-id="efafc-208">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-208">False</span></span>                                                                  |
| <span data-ttu-id="efafc-209">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efafc-209">In Global Catalog</span></span>      | <span data-ttu-id="efafc-210">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-210">False</span></span>                                                                  |
| <span data-ttu-id="efafc-211">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efafc-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="efafc-212">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efafc-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="efafc-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efafc-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efafc-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-215">Search-Flags</span></span>           | <span data-ttu-id="efafc-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efafc-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="efafc-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-217">System-Flags</span></span>           | <span data-ttu-id="efafc-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efafc-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="efafc-219">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efafc-219">Classes used in</span></span>        | [<span data-ttu-id="efafc-220">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="efafc-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="efafc-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="efafc-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="efafc-222">Entrada</span><span class="sxs-lookup"><span data-stu-id="efafc-222">Entry</span></span> | <span data-ttu-id="efafc-223">Valor</span><span class="sxs-lookup"><span data-stu-id="efafc-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="efafc-224">ID do link</span><span class="sxs-lookup"><span data-stu-id="efafc-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efafc-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="efafc-226">System-Only</span></span>            | <span data-ttu-id="efafc-227">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-227">False</span></span>                                                                  |
| <span data-ttu-id="efafc-228">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efafc-228">Is-Single-Valued</span></span>       | <span data-ttu-id="efafc-229">True</span><span class="sxs-lookup"><span data-stu-id="efafc-229">True</span></span>                                                                   |
| <span data-ttu-id="efafc-230">É indexado</span><span class="sxs-lookup"><span data-stu-id="efafc-230">Is Indexed</span></span>             | <span data-ttu-id="efafc-231">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-231">False</span></span>                                                                  |
| <span data-ttu-id="efafc-232">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efafc-232">In Global Catalog</span></span>      | <span data-ttu-id="efafc-233">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-233">False</span></span>                                                                  |
| <span data-ttu-id="efafc-234">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efafc-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="efafc-235">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efafc-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="efafc-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efafc-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efafc-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-238">Search-Flags</span></span>           | <span data-ttu-id="efafc-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efafc-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="efafc-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-240">System-Flags</span></span>           | <span data-ttu-id="efafc-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efafc-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="efafc-242">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efafc-242">Classes used in</span></span>        | [<span data-ttu-id="efafc-243">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="efafc-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="efafc-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="efafc-244">Windows Server 2012</span></span>



| <span data-ttu-id="efafc-245">Entrada</span><span class="sxs-lookup"><span data-stu-id="efafc-245">Entry</span></span> | <span data-ttu-id="efafc-246">Valor</span><span class="sxs-lookup"><span data-stu-id="efafc-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="efafc-247">ID do link</span><span class="sxs-lookup"><span data-stu-id="efafc-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="efafc-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="efafc-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="efafc-249">System-Only</span></span>            | <span data-ttu-id="efafc-250">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-250">False</span></span>                                                                  |
| <span data-ttu-id="efafc-251">É de valor único</span><span class="sxs-lookup"><span data-stu-id="efafc-251">Is-Single-Valued</span></span>       | <span data-ttu-id="efafc-252">True</span><span class="sxs-lookup"><span data-stu-id="efafc-252">True</span></span>                                                                   |
| <span data-ttu-id="efafc-253">É indexado</span><span class="sxs-lookup"><span data-stu-id="efafc-253">Is Indexed</span></span>             | <span data-ttu-id="efafc-254">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-254">False</span></span>                                                                  |
| <span data-ttu-id="efafc-255">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="efafc-255">In Global Catalog</span></span>      | <span data-ttu-id="efafc-256">Falso</span><span class="sxs-lookup"><span data-stu-id="efafc-256">False</span></span>                                                                  |
| <span data-ttu-id="efafc-257">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="efafc-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="efafc-258">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="efafc-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="efafc-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="efafc-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="efafc-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="efafc-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-261">Search-Flags</span></span>           | <span data-ttu-id="efafc-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="efafc-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="efafc-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="efafc-263">System-Flags</span></span>           | <span data-ttu-id="efafc-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="efafc-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="efafc-265">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="efafc-265">Classes used in</span></span>        | [<span data-ttu-id="efafc-266">**Autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="efafc-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





