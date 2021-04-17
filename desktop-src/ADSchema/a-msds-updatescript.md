---
title: atributo ms-DS-UpdateScript
description: Isso é usado para manter o script com as instruções de reestruturação de domínio.
ms.assetid: a9dd205d-f6c3-4eeb-95dc-491bfe30ab8b
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-UpdateScript
- atributo msDS-UpdateScript do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-UpdateScript
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7809bf6fdbaabb38976068d1998cacfb12bdaf3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755730"
---
# <a name="ms-ds-updatescript-attribute"></a><span data-ttu-id="5dda1-105">atributo ms-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="5dda1-105">ms-DS-UpdateScript attribute</span></span>

<span data-ttu-id="5dda1-106">Isso é usado para manter o script com as instruções de reestruturação de domínio.</span><span class="sxs-lookup"><span data-stu-id="5dda1-106">This is used to hold the script with the domain restructure instructions.</span></span>



| <span data-ttu-id="5dda1-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dda1-107">Entry</span></span> | <span data-ttu-id="5dda1-108">Valor</span><span class="sxs-lookup"><span data-stu-id="5dda1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5dda1-109">CN</span><span class="sxs-lookup"><span data-stu-id="5dda1-109">CN</span></span>                | <span data-ttu-id="5dda1-110">ms-DS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="5dda1-110">ms-DS-UpdateScript</span></span>                          |
| <span data-ttu-id="5dda1-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5dda1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5dda1-112">msDS-UpdateScript</span><span class="sxs-lookup"><span data-stu-id="5dda1-112">msDS-UpdateScript</span></span>                           |
| <span data-ttu-id="5dda1-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5dda1-113">Size</span></span>              | <span data-ttu-id="5dda1-114">Tamanho máximo de 10 mil bytes.</span><span class="sxs-lookup"><span data-stu-id="5dda1-114">Maximum size 10K bytes.</span></span>                     |
| <span data-ttu-id="5dda1-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5dda1-115">Update Privilege</span></span>  | <span data-ttu-id="5dda1-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5dda1-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="5dda1-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5dda1-117">Update Frequency</span></span>  | <span data-ttu-id="5dda1-118">Somente durante a reestruturação do domínio.</span><span class="sxs-lookup"><span data-stu-id="5dda1-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="5dda1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5dda1-119">Attribute-Id</span></span>      | <span data-ttu-id="5dda1-120">1.2.840.113556.1.4.1721</span><span class="sxs-lookup"><span data-stu-id="5dda1-120">1.2.840.113556.1.4.1721</span></span>                     |
| <span data-ttu-id="5dda1-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5dda1-121">System-Id-Guid</span></span>    | <span data-ttu-id="5dda1-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span><span class="sxs-lookup"><span data-stu-id="5dda1-122">146eb639-bb9f-4fc1-a825-e29e00c77920</span></span>        |
| <span data-ttu-id="5dda1-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dda1-123">Syntax</span></span>            | [<span data-ttu-id="5dda1-124">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="5dda1-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5dda1-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="5dda1-125">Implementations</span></span>

-   [<span data-ttu-id="5dda1-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5dda1-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5dda1-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5dda1-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5dda1-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5dda1-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5dda1-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5dda1-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5dda1-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5dda1-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5dda1-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5dda1-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="5dda1-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5dda1-132">Windows Server 2003</span></span>



| <span data-ttu-id="5dda1-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dda1-133">Entry</span></span> | <span data-ttu-id="5dda1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="5dda1-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5dda1-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="5dda1-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dda1-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dda1-137">System-Only</span></span>            | <span data-ttu-id="5dda1-138">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-138">False</span></span>                                                         |
| <span data-ttu-id="5dda1-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5dda1-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5dda1-140">True</span><span class="sxs-lookup"><span data-stu-id="5dda1-140">True</span></span>                                                          |
| <span data-ttu-id="5dda1-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="5dda1-141">Is Indexed</span></span>             | <span data-ttu-id="5dda1-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-142">False</span></span>                                                         |
| <span data-ttu-id="5dda1-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5dda1-143">In Global Catalog</span></span>      | <span data-ttu-id="5dda1-144">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-144">False</span></span>                                                         |
| <span data-ttu-id="5dda1-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5dda1-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dda1-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5dda1-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5dda1-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dda1-147">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dda1-148">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-149">Search-Flags</span></span>           | <span data-ttu-id="5dda1-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dda1-150">0x00000000</span></span>                                                    |
| <span data-ttu-id="5dda1-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-151">System-Flags</span></span>           | <span data-ttu-id="5dda1-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dda1-152">0x00000010</span></span>                                                    |
| <span data-ttu-id="5dda1-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5dda1-153">Classes used in</span></span>        | [<span data-ttu-id="5dda1-154">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="5dda1-154">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5dda1-155">ADAM</span><span class="sxs-lookup"><span data-stu-id="5dda1-155">ADAM</span></span>



| <span data-ttu-id="5dda1-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dda1-156">Entry</span></span> | <span data-ttu-id="5dda1-157">Valor</span><span class="sxs-lookup"><span data-stu-id="5dda1-157">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5dda1-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="5dda1-158">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dda1-159">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dda1-160">System-Only</span></span>            | <span data-ttu-id="5dda1-161">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-161">False</span></span>                                                         |
| <span data-ttu-id="5dda1-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5dda1-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5dda1-163">True</span><span class="sxs-lookup"><span data-stu-id="5dda1-163">True</span></span>                                                          |
| <span data-ttu-id="5dda1-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="5dda1-164">Is Indexed</span></span>             | <span data-ttu-id="5dda1-165">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-165">False</span></span>                                                         |
| <span data-ttu-id="5dda1-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5dda1-166">In Global Catalog</span></span>      | <span data-ttu-id="5dda1-167">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-167">False</span></span>                                                         |
| <span data-ttu-id="5dda1-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5dda1-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dda1-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5dda1-169">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5dda1-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dda1-170">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dda1-171">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-172">Search-Flags</span></span>           | <span data-ttu-id="5dda1-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dda1-173">0x00000000</span></span>                                                    |
| <span data-ttu-id="5dda1-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-174">System-Flags</span></span>           | <span data-ttu-id="5dda1-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dda1-175">0x00000010</span></span>                                                    |
| <span data-ttu-id="5dda1-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5dda1-176">Classes used in</span></span>        | [<span data-ttu-id="5dda1-177">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="5dda1-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5dda1-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5dda1-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5dda1-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dda1-179">Entry</span></span> | <span data-ttu-id="5dda1-180">Valor</span><span class="sxs-lookup"><span data-stu-id="5dda1-180">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5dda1-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="5dda1-181">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dda1-182">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dda1-183">System-Only</span></span>            | <span data-ttu-id="5dda1-184">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-184">False</span></span>                                                         |
| <span data-ttu-id="5dda1-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5dda1-185">Is-Single-Valued</span></span>       | <span data-ttu-id="5dda1-186">True</span><span class="sxs-lookup"><span data-stu-id="5dda1-186">True</span></span>                                                          |
| <span data-ttu-id="5dda1-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="5dda1-187">Is Indexed</span></span>             | <span data-ttu-id="5dda1-188">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-188">False</span></span>                                                         |
| <span data-ttu-id="5dda1-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5dda1-189">In Global Catalog</span></span>      | <span data-ttu-id="5dda1-190">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-190">False</span></span>                                                         |
| <span data-ttu-id="5dda1-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5dda1-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dda1-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5dda1-192">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5dda1-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dda1-193">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dda1-194">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-195">Search-Flags</span></span>           | <span data-ttu-id="5dda1-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dda1-196">0x00000000</span></span>                                                    |
| <span data-ttu-id="5dda1-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-197">System-Flags</span></span>           | <span data-ttu-id="5dda1-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dda1-198">0x00000010</span></span>                                                    |
| <span data-ttu-id="5dda1-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5dda1-199">Classes used in</span></span>        | [<span data-ttu-id="5dda1-200">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="5dda1-200">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5dda1-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dda1-201">Windows Server 2008</span></span>



| <span data-ttu-id="5dda1-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dda1-202">Entry</span></span> | <span data-ttu-id="5dda1-203">Valor</span><span class="sxs-lookup"><span data-stu-id="5dda1-203">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5dda1-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="5dda1-204">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dda1-205">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dda1-206">System-Only</span></span>            | <span data-ttu-id="5dda1-207">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-207">False</span></span>                                                         |
| <span data-ttu-id="5dda1-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5dda1-208">Is-Single-Valued</span></span>       | <span data-ttu-id="5dda1-209">True</span><span class="sxs-lookup"><span data-stu-id="5dda1-209">True</span></span>                                                          |
| <span data-ttu-id="5dda1-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="5dda1-210">Is Indexed</span></span>             | <span data-ttu-id="5dda1-211">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-211">False</span></span>                                                         |
| <span data-ttu-id="5dda1-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5dda1-212">In Global Catalog</span></span>      | <span data-ttu-id="5dda1-213">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-213">False</span></span>                                                         |
| <span data-ttu-id="5dda1-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5dda1-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dda1-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5dda1-215">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5dda1-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dda1-216">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dda1-217">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-218">Search-Flags</span></span>           | <span data-ttu-id="5dda1-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dda1-219">0x00000000</span></span>                                                    |
| <span data-ttu-id="5dda1-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-220">System-Flags</span></span>           | <span data-ttu-id="5dda1-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dda1-221">0x00000010</span></span>                                                    |
| <span data-ttu-id="5dda1-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5dda1-222">Classes used in</span></span>        | [<span data-ttu-id="5dda1-223">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="5dda1-223">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5dda1-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5dda1-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5dda1-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dda1-225">Entry</span></span> | <span data-ttu-id="5dda1-226">Valor</span><span class="sxs-lookup"><span data-stu-id="5dda1-226">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5dda1-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="5dda1-227">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dda1-228">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dda1-229">System-Only</span></span>            | <span data-ttu-id="5dda1-230">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-230">False</span></span>                                                         |
| <span data-ttu-id="5dda1-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5dda1-231">Is-Single-Valued</span></span>       | <span data-ttu-id="5dda1-232">True</span><span class="sxs-lookup"><span data-stu-id="5dda1-232">True</span></span>                                                          |
| <span data-ttu-id="5dda1-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="5dda1-233">Is Indexed</span></span>             | <span data-ttu-id="5dda1-234">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-234">False</span></span>                                                         |
| <span data-ttu-id="5dda1-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5dda1-235">In Global Catalog</span></span>      | <span data-ttu-id="5dda1-236">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-236">False</span></span>                                                         |
| <span data-ttu-id="5dda1-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5dda1-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dda1-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5dda1-238">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5dda1-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dda1-239">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dda1-240">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-241">Search-Flags</span></span>           | <span data-ttu-id="5dda1-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dda1-242">0x00000000</span></span>                                                    |
| <span data-ttu-id="5dda1-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-243">System-Flags</span></span>           | <span data-ttu-id="5dda1-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dda1-244">0x00000010</span></span>                                                    |
| <span data-ttu-id="5dda1-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5dda1-245">Classes used in</span></span>        | [<span data-ttu-id="5dda1-246">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="5dda1-246">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5dda1-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5dda1-247">Windows Server 2012</span></span>



| <span data-ttu-id="5dda1-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="5dda1-248">Entry</span></span> | <span data-ttu-id="5dda1-249">Valor</span><span class="sxs-lookup"><span data-stu-id="5dda1-249">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5dda1-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="5dda1-250">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5dda1-251">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="5dda1-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="5dda1-252">System-Only</span></span>            | <span data-ttu-id="5dda1-253">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-253">False</span></span>                                                         |
| <span data-ttu-id="5dda1-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5dda1-254">Is-Single-Valued</span></span>       | <span data-ttu-id="5dda1-255">True</span><span class="sxs-lookup"><span data-stu-id="5dda1-255">True</span></span>                                                          |
| <span data-ttu-id="5dda1-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="5dda1-256">Is Indexed</span></span>             | <span data-ttu-id="5dda1-257">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-257">False</span></span>                                                         |
| <span data-ttu-id="5dda1-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5dda1-258">In Global Catalog</span></span>      | <span data-ttu-id="5dda1-259">Falso</span><span class="sxs-lookup"><span data-stu-id="5dda1-259">False</span></span>                                                         |
| <span data-ttu-id="5dda1-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5dda1-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="5dda1-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5dda1-261">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="5dda1-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5dda1-262">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5dda1-263">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="5dda1-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-264">Search-Flags</span></span>           | <span data-ttu-id="5dda1-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5dda1-265">0x00000000</span></span>                                                    |
| <span data-ttu-id="5dda1-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5dda1-266">System-Flags</span></span>           | <span data-ttu-id="5dda1-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5dda1-267">0x00000010</span></span>                                                    |
| <span data-ttu-id="5dda1-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5dda1-268">Classes used in</span></span>        | [<span data-ttu-id="5dda1-269">**Entre referências-contêiner**</span><span class="sxs-lookup"><span data-stu-id="5dda1-269">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





