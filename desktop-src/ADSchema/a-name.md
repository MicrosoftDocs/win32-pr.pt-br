---
title: Atributo RDN
description: O nome distinto relativo (RDN) de um objeto.
ms.assetid: 07fe0e81-1b18-4dbb-abca-a059a8bf993e
ms.tgt_platform: multiple
keywords:
- Esquema de atributos do atributo RDN
- atributo de nome esquema do AD
topic_type:
- apiref
api_name:
- RDN
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe49bd525d0fa3f4ed95874f2020d9d2a5eb9554
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755471"
---
# <a name="rdn-attribute"></a><span data-ttu-id="8a335-105">Atributo RDN</span><span class="sxs-lookup"><span data-stu-id="8a335-105">RDN attribute</span></span>

<span data-ttu-id="8a335-106">O nome distinto relativo (RDN) de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8a335-106">The Relative Distinguished Name (RDN) of an object.</span></span> <span data-ttu-id="8a335-107">Um RDN é a parte relativa de um DN (nome distinto), que identifica exclusivamente um objeto LDAP.</span><span class="sxs-lookup"><span data-stu-id="8a335-107">An RDN is the relative portion of a distinguished name (DN), which uniquely identifies an LDAP object.</span></span>



| <span data-ttu-id="8a335-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-108">Entry</span></span> | <span data-ttu-id="8a335-109">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-109">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="8a335-110">CN</span><span class="sxs-lookup"><span data-stu-id="8a335-110">CN</span></span>                | <span data-ttu-id="8a335-111">RDN</span><span class="sxs-lookup"><span data-stu-id="8a335-111">RDN</span></span>                                            |
| <span data-ttu-id="8a335-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="8a335-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8a335-113">name</span><span class="sxs-lookup"><span data-stu-id="8a335-113">name</span></span>                                           |
| <span data-ttu-id="8a335-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="8a335-114">Size</span></span>              | \-                                             |
| <span data-ttu-id="8a335-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="8a335-115">Update Privilege</span></span>  | <span data-ttu-id="8a335-116">Esse valor é definido pelo administrador do esquema.</span><span class="sxs-lookup"><span data-stu-id="8a335-116">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="8a335-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="8a335-117">Update Frequency</span></span>  | \-                                             |
| <span data-ttu-id="8a335-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-118">Attribute-Id</span></span>      | <span data-ttu-id="8a335-119">1.2.840.113556.1.4.1</span><span class="sxs-lookup"><span data-stu-id="8a335-119">1.2.840.113556.1.4.1</span></span>                           |
| <span data-ttu-id="8a335-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="8a335-120">System-Id-Guid</span></span>    | <span data-ttu-id="8a335-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8a335-121">bf967a0e-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="8a335-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a335-122">Syntax</span></span>            | [<span data-ttu-id="8a335-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="8a335-123">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="8a335-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="8a335-124">Implementations</span></span>

-   [<span data-ttu-id="8a335-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8a335-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8a335-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a335-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a335-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8a335-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8a335-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a335-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a335-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a335-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a335-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a335-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a335-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a335-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8a335-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a335-132">Windows 2000 Server</span></span>



| <span data-ttu-id="8a335-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-133">Entry</span></span> | <span data-ttu-id="8a335-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a335-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a335-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a335-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-136">MAPI-Id</span></span>                | <span data-ttu-id="8a335-137">0x8202</span><span class="sxs-lookup"><span data-stu-id="8a335-137">0x8202</span></span>                          |
| <span data-ttu-id="8a335-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a335-138">System-Only</span></span>            | <span data-ttu-id="8a335-139">True</span><span class="sxs-lookup"><span data-stu-id="8a335-139">True</span></span>                            |
| <span data-ttu-id="8a335-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a335-140">Is-Single-Valued</span></span>       | <span data-ttu-id="8a335-141">True</span><span class="sxs-lookup"><span data-stu-id="8a335-141">True</span></span>                            |
| <span data-ttu-id="8a335-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a335-142">Is Indexed</span></span>             | <span data-ttu-id="8a335-143">True</span><span class="sxs-lookup"><span data-stu-id="8a335-143">True</span></span>                            |
| <span data-ttu-id="8a335-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a335-144">In Global Catalog</span></span>      | <span data-ttu-id="8a335-145">True</span><span class="sxs-lookup"><span data-stu-id="8a335-145">True</span></span>                            |
| <span data-ttu-id="8a335-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a335-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a335-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a335-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a335-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a335-148">Range-Lower</span></span>            | <span data-ttu-id="8a335-149">1</span><span class="sxs-lookup"><span data-stu-id="8a335-149">1</span></span>                               |
| <span data-ttu-id="8a335-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a335-150">Range-Upper</span></span>            | <span data-ttu-id="8a335-151">255</span><span class="sxs-lookup"><span data-stu-id="8a335-151">255</span></span>                             |
| <span data-ttu-id="8a335-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-152">Search-Flags</span></span>           | <span data-ttu-id="8a335-153">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="8a335-153">0x0000000D</span></span>                      |
| <span data-ttu-id="8a335-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-154">System-Flags</span></span>           | <span data-ttu-id="8a335-155">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8a335-155">0x00000012</span></span>                      |
| <span data-ttu-id="8a335-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a335-156">Classes used in</span></span>        | [<span data-ttu-id="8a335-157">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a335-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8a335-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a335-158">Windows Server 2003</span></span>



| <span data-ttu-id="8a335-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-159">Entry</span></span> | <span data-ttu-id="8a335-160">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a335-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a335-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a335-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-162">MAPI-Id</span></span>                | <span data-ttu-id="8a335-163">0x8202</span><span class="sxs-lookup"><span data-stu-id="8a335-163">0x8202</span></span>                          |
| <span data-ttu-id="8a335-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a335-164">System-Only</span></span>            | <span data-ttu-id="8a335-165">True</span><span class="sxs-lookup"><span data-stu-id="8a335-165">True</span></span>                            |
| <span data-ttu-id="8a335-166">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a335-166">Is-Single-Valued</span></span>       | <span data-ttu-id="8a335-167">True</span><span class="sxs-lookup"><span data-stu-id="8a335-167">True</span></span>                            |
| <span data-ttu-id="8a335-168">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a335-168">Is Indexed</span></span>             | <span data-ttu-id="8a335-169">True</span><span class="sxs-lookup"><span data-stu-id="8a335-169">True</span></span>                            |
| <span data-ttu-id="8a335-170">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a335-170">In Global Catalog</span></span>      | <span data-ttu-id="8a335-171">True</span><span class="sxs-lookup"><span data-stu-id="8a335-171">True</span></span>                            |
| <span data-ttu-id="8a335-172">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a335-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a335-173">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a335-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a335-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a335-174">Range-Lower</span></span>            | <span data-ttu-id="8a335-175">1</span><span class="sxs-lookup"><span data-stu-id="8a335-175">1</span></span>                               |
| <span data-ttu-id="8a335-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a335-176">Range-Upper</span></span>            | <span data-ttu-id="8a335-177">255</span><span class="sxs-lookup"><span data-stu-id="8a335-177">255</span></span>                             |
| <span data-ttu-id="8a335-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-178">Search-Flags</span></span>           | <span data-ttu-id="8a335-179">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="8a335-179">0x0000000D</span></span>                      |
| <span data-ttu-id="8a335-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-180">System-Flags</span></span>           | <span data-ttu-id="8a335-181">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8a335-181">0x00000012</span></span>                      |
| <span data-ttu-id="8a335-182">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a335-182">Classes used in</span></span>        | [<span data-ttu-id="8a335-183">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a335-183">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8a335-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="8a335-184">ADAM</span></span>



| <span data-ttu-id="8a335-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-185">Entry</span></span> | <span data-ttu-id="8a335-186">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a335-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a335-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a335-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-188">MAPI-Id</span></span>                | <span data-ttu-id="8a335-189">0x8202</span><span class="sxs-lookup"><span data-stu-id="8a335-189">0x8202</span></span>                          |
| <span data-ttu-id="8a335-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a335-190">System-Only</span></span>            | <span data-ttu-id="8a335-191">True</span><span class="sxs-lookup"><span data-stu-id="8a335-191">True</span></span>                            |
| <span data-ttu-id="8a335-192">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a335-192">Is-Single-Valued</span></span>       | <span data-ttu-id="8a335-193">True</span><span class="sxs-lookup"><span data-stu-id="8a335-193">True</span></span>                            |
| <span data-ttu-id="8a335-194">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a335-194">Is Indexed</span></span>             | <span data-ttu-id="8a335-195">True</span><span class="sxs-lookup"><span data-stu-id="8a335-195">True</span></span>                            |
| <span data-ttu-id="8a335-196">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a335-196">In Global Catalog</span></span>      | <span data-ttu-id="8a335-197">True</span><span class="sxs-lookup"><span data-stu-id="8a335-197">True</span></span>                            |
| <span data-ttu-id="8a335-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a335-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a335-199">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a335-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a335-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a335-200">Range-Lower</span></span>            | <span data-ttu-id="8a335-201">1</span><span class="sxs-lookup"><span data-stu-id="8a335-201">1</span></span>                               |
| <span data-ttu-id="8a335-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a335-202">Range-Upper</span></span>            | <span data-ttu-id="8a335-203">255</span><span class="sxs-lookup"><span data-stu-id="8a335-203">255</span></span>                             |
| <span data-ttu-id="8a335-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-204">Search-Flags</span></span>           | <span data-ttu-id="8a335-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="8a335-205">0x0000000D</span></span>                      |
| <span data-ttu-id="8a335-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-206">System-Flags</span></span>           | <span data-ttu-id="8a335-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8a335-207">0x00000012</span></span>                      |
| <span data-ttu-id="8a335-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a335-208">Classes used in</span></span>        | [<span data-ttu-id="8a335-209">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a335-209">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a335-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a335-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a335-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-211">Entry</span></span> | <span data-ttu-id="8a335-212">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a335-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a335-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a335-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-214">MAPI-Id</span></span>                | <span data-ttu-id="8a335-215">0x8202</span><span class="sxs-lookup"><span data-stu-id="8a335-215">0x8202</span></span>                          |
| <span data-ttu-id="8a335-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a335-216">System-Only</span></span>            | <span data-ttu-id="8a335-217">True</span><span class="sxs-lookup"><span data-stu-id="8a335-217">True</span></span>                            |
| <span data-ttu-id="8a335-218">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a335-218">Is-Single-Valued</span></span>       | <span data-ttu-id="8a335-219">True</span><span class="sxs-lookup"><span data-stu-id="8a335-219">True</span></span>                            |
| <span data-ttu-id="8a335-220">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a335-220">Is Indexed</span></span>             | <span data-ttu-id="8a335-221">True</span><span class="sxs-lookup"><span data-stu-id="8a335-221">True</span></span>                            |
| <span data-ttu-id="8a335-222">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a335-222">In Global Catalog</span></span>      | <span data-ttu-id="8a335-223">True</span><span class="sxs-lookup"><span data-stu-id="8a335-223">True</span></span>                            |
| <span data-ttu-id="8a335-224">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a335-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a335-225">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a335-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a335-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a335-226">Range-Lower</span></span>            | <span data-ttu-id="8a335-227">1</span><span class="sxs-lookup"><span data-stu-id="8a335-227">1</span></span>                               |
| <span data-ttu-id="8a335-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a335-228">Range-Upper</span></span>            | <span data-ttu-id="8a335-229">255</span><span class="sxs-lookup"><span data-stu-id="8a335-229">255</span></span>                             |
| <span data-ttu-id="8a335-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-230">Search-Flags</span></span>           | <span data-ttu-id="8a335-231">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="8a335-231">0x0000000D</span></span>                      |
| <span data-ttu-id="8a335-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-232">System-Flags</span></span>           | <span data-ttu-id="8a335-233">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8a335-233">0x00000012</span></span>                      |
| <span data-ttu-id="8a335-234">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a335-234">Classes used in</span></span>        | [<span data-ttu-id="8a335-235">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a335-235">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8a335-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a335-236">Windows Server 2008</span></span>



| <span data-ttu-id="8a335-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-237">Entry</span></span> | <span data-ttu-id="8a335-238">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a335-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a335-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a335-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-240">MAPI-Id</span></span>                | <span data-ttu-id="8a335-241">0x8202</span><span class="sxs-lookup"><span data-stu-id="8a335-241">0x8202</span></span>                          |
| <span data-ttu-id="8a335-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a335-242">System-Only</span></span>            | <span data-ttu-id="8a335-243">True</span><span class="sxs-lookup"><span data-stu-id="8a335-243">True</span></span>                            |
| <span data-ttu-id="8a335-244">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a335-244">Is-Single-Valued</span></span>       | <span data-ttu-id="8a335-245">True</span><span class="sxs-lookup"><span data-stu-id="8a335-245">True</span></span>                            |
| <span data-ttu-id="8a335-246">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a335-246">Is Indexed</span></span>             | <span data-ttu-id="8a335-247">True</span><span class="sxs-lookup"><span data-stu-id="8a335-247">True</span></span>                            |
| <span data-ttu-id="8a335-248">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a335-248">In Global Catalog</span></span>      | <span data-ttu-id="8a335-249">True</span><span class="sxs-lookup"><span data-stu-id="8a335-249">True</span></span>                            |
| <span data-ttu-id="8a335-250">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a335-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a335-251">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a335-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a335-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a335-252">Range-Lower</span></span>            | <span data-ttu-id="8a335-253">1</span><span class="sxs-lookup"><span data-stu-id="8a335-253">1</span></span>                               |
| <span data-ttu-id="8a335-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a335-254">Range-Upper</span></span>            | <span data-ttu-id="8a335-255">255</span><span class="sxs-lookup"><span data-stu-id="8a335-255">255</span></span>                             |
| <span data-ttu-id="8a335-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-256">Search-Flags</span></span>           | <span data-ttu-id="8a335-257">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="8a335-257">0x0000000D</span></span>                      |
| <span data-ttu-id="8a335-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-258">System-Flags</span></span>           | <span data-ttu-id="8a335-259">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8a335-259">0x00000012</span></span>                      |
| <span data-ttu-id="8a335-260">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a335-260">Classes used in</span></span>        | [<span data-ttu-id="8a335-261">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a335-261">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a335-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a335-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a335-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-263">Entry</span></span> | <span data-ttu-id="8a335-264">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a335-265">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a335-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a335-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-266">MAPI-Id</span></span>                | <span data-ttu-id="8a335-267">0x8202</span><span class="sxs-lookup"><span data-stu-id="8a335-267">0x8202</span></span>                          |
| <span data-ttu-id="8a335-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a335-268">System-Only</span></span>            | <span data-ttu-id="8a335-269">True</span><span class="sxs-lookup"><span data-stu-id="8a335-269">True</span></span>                            |
| <span data-ttu-id="8a335-270">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a335-270">Is-Single-Valued</span></span>       | <span data-ttu-id="8a335-271">True</span><span class="sxs-lookup"><span data-stu-id="8a335-271">True</span></span>                            |
| <span data-ttu-id="8a335-272">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a335-272">Is Indexed</span></span>             | <span data-ttu-id="8a335-273">True</span><span class="sxs-lookup"><span data-stu-id="8a335-273">True</span></span>                            |
| <span data-ttu-id="8a335-274">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a335-274">In Global Catalog</span></span>      | <span data-ttu-id="8a335-275">True</span><span class="sxs-lookup"><span data-stu-id="8a335-275">True</span></span>                            |
| <span data-ttu-id="8a335-276">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a335-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a335-277">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a335-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a335-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a335-278">Range-Lower</span></span>            | <span data-ttu-id="8a335-279">1</span><span class="sxs-lookup"><span data-stu-id="8a335-279">1</span></span>                               |
| <span data-ttu-id="8a335-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a335-280">Range-Upper</span></span>            | <span data-ttu-id="8a335-281">255</span><span class="sxs-lookup"><span data-stu-id="8a335-281">255</span></span>                             |
| <span data-ttu-id="8a335-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-282">Search-Flags</span></span>           | <span data-ttu-id="8a335-283">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="8a335-283">0x0000000D</span></span>                      |
| <span data-ttu-id="8a335-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-284">System-Flags</span></span>           | <span data-ttu-id="8a335-285">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8a335-285">0x00000012</span></span>                      |
| <span data-ttu-id="8a335-286">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a335-286">Classes used in</span></span>        | [<span data-ttu-id="8a335-287">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a335-287">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8a335-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a335-288">Windows Server 2012</span></span>



| <span data-ttu-id="8a335-289">Entrada</span><span class="sxs-lookup"><span data-stu-id="8a335-289">Entry</span></span> | <span data-ttu-id="8a335-290">Valor</span><span class="sxs-lookup"><span data-stu-id="8a335-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8a335-291">ID do link</span><span class="sxs-lookup"><span data-stu-id="8a335-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8a335-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a335-292">MAPI-Id</span></span>                | <span data-ttu-id="8a335-293">0x8202</span><span class="sxs-lookup"><span data-stu-id="8a335-293">0x8202</span></span>                          |
| <span data-ttu-id="8a335-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a335-294">System-Only</span></span>            | <span data-ttu-id="8a335-295">True</span><span class="sxs-lookup"><span data-stu-id="8a335-295">True</span></span>                            |
| <span data-ttu-id="8a335-296">É de valor único</span><span class="sxs-lookup"><span data-stu-id="8a335-296">Is-Single-Valued</span></span>       | <span data-ttu-id="8a335-297">True</span><span class="sxs-lookup"><span data-stu-id="8a335-297">True</span></span>                            |
| <span data-ttu-id="8a335-298">É indexado</span><span class="sxs-lookup"><span data-stu-id="8a335-298">Is Indexed</span></span>             | <span data-ttu-id="8a335-299">True</span><span class="sxs-lookup"><span data-stu-id="8a335-299">True</span></span>                            |
| <span data-ttu-id="8a335-300">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="8a335-300">In Global Catalog</span></span>      | <span data-ttu-id="8a335-301">True</span><span class="sxs-lookup"><span data-stu-id="8a335-301">True</span></span>                            |
| <span data-ttu-id="8a335-302">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="8a335-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a335-303">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="8a335-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8a335-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a335-304">Range-Lower</span></span>            | <span data-ttu-id="8a335-305">1</span><span class="sxs-lookup"><span data-stu-id="8a335-305">1</span></span>                               |
| <span data-ttu-id="8a335-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a335-306">Range-Upper</span></span>            | <span data-ttu-id="8a335-307">255</span><span class="sxs-lookup"><span data-stu-id="8a335-307">255</span></span>                             |
| <span data-ttu-id="8a335-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-308">Search-Flags</span></span>           | <span data-ttu-id="8a335-309">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="8a335-309">0x0000000D</span></span>                      |
| <span data-ttu-id="8a335-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a335-310">System-Flags</span></span>           | <span data-ttu-id="8a335-311">0x00000012</span><span class="sxs-lookup"><span data-stu-id="8a335-311">0x00000012</span></span>                      |
| <span data-ttu-id="8a335-312">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="8a335-312">Classes used in</span></span>        | [<span data-ttu-id="8a335-313">**Início**</span><span class="sxs-lookup"><span data-stu-id="8a335-313">**Top**</span></span>](c-top.md)<br/> |



 

 





