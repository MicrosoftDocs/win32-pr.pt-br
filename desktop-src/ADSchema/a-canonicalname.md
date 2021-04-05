---
title: Canonical-Name atributo
description: O nome do objeto no formato canônico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Esquema de Canonical-Name do atributo AD
- atributo canônico do esquema do AD
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825412"
---
# <a name="canonical-name-attribute"></a><span data-ttu-id="c69bd-105">Canonical-Name atributo</span><span class="sxs-lookup"><span data-stu-id="c69bd-105">Canonical-Name attribute</span></span>

<span data-ttu-id="c69bd-106">O nome do objeto no formato canônico.</span><span class="sxs-lookup"><span data-stu-id="c69bd-106">The name of the object in canonical format.</span></span> <span data-ttu-id="c69bd-107">myserver2.fabrikam.com/users/jeffsmith é um exemplo de um nome distinto em formato canônico.</span><span class="sxs-lookup"><span data-stu-id="c69bd-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="c69bd-108">Este é um atributo construído.</span><span class="sxs-lookup"><span data-stu-id="c69bd-108">This is a constructed attribute.</span></span> <span data-ttu-id="c69bd-109">Os resultados retornados são idênticos aos retornados pela seguinte função de Active Directory: DsCrackNames (nulo, \_ sinalizador de nome DS \_ \_ \_ somente sintático, nome do FQDN do DS \_ \_ 1779 \_ , \_ nome canônico do DS \_ ,...).</span><span class="sxs-lookup"><span data-stu-id="c69bd-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="c69bd-110">Para obter mais informações sobre formatos de nome, consulte [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span><span class="sxs-lookup"><span data-stu-id="c69bd-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="c69bd-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-111">Entry</span></span> | <span data-ttu-id="c69bd-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c69bd-113">CN</span><span class="sxs-lookup"><span data-stu-id="c69bd-113">CN</span></span>                | <span data-ttu-id="c69bd-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="c69bd-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="c69bd-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c69bd-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c69bd-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="c69bd-116">canonicalName</span></span>                               |
| <span data-ttu-id="c69bd-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c69bd-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="c69bd-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c69bd-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c69bd-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c69bd-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c69bd-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-120">Attribute-Id</span></span>      | <span data-ttu-id="c69bd-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="c69bd-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="c69bd-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c69bd-122">System-Id-Guid</span></span>    | <span data-ttu-id="c69bd-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="c69bd-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="c69bd-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="c69bd-124">Syntax</span></span>            | [<span data-ttu-id="c69bd-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="c69bd-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c69bd-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="c69bd-126">Implementations</span></span>

-   [<span data-ttu-id="c69bd-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c69bd-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c69bd-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c69bd-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c69bd-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c69bd-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c69bd-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c69bd-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c69bd-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c69bd-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c69bd-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c69bd-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c69bd-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c69bd-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c69bd-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c69bd-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c69bd-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-135">Entry</span></span> | <span data-ttu-id="c69bd-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c69bd-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="c69bd-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69bd-139">System-Only</span></span>            | <span data-ttu-id="c69bd-140">True</span><span class="sxs-lookup"><span data-stu-id="c69bd-140">True</span></span>                            |
| <span data-ttu-id="c69bd-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c69bd-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c69bd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-142">False</span></span>                           |
| <span data-ttu-id="c69bd-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="c69bd-143">Is Indexed</span></span>             | <span data-ttu-id="c69bd-144">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-144">False</span></span>                           |
| <span data-ttu-id="c69bd-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c69bd-145">In Global Catalog</span></span>      | <span data-ttu-id="c69bd-146">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-146">False</span></span>                           |
| <span data-ttu-id="c69bd-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c69bd-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69bd-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c69bd-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c69bd-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69bd-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c69bd-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69bd-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c69bd-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-151">Search-Flags</span></span>           | <span data-ttu-id="c69bd-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69bd-152">0x00000000</span></span>                      |
| <span data-ttu-id="c69bd-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-153">System-Flags</span></span>           | <span data-ttu-id="c69bd-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c69bd-154">0x08000014</span></span>                      |
| <span data-ttu-id="c69bd-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c69bd-155">Classes used in</span></span>        | [<span data-ttu-id="c69bd-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="c69bd-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c69bd-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c69bd-157">Windows Server 2003</span></span>



| <span data-ttu-id="c69bd-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-158">Entry</span></span> | <span data-ttu-id="c69bd-159">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c69bd-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="c69bd-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69bd-162">System-Only</span></span>            | <span data-ttu-id="c69bd-163">True</span><span class="sxs-lookup"><span data-stu-id="c69bd-163">True</span></span>                            |
| <span data-ttu-id="c69bd-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c69bd-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c69bd-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-165">False</span></span>                           |
| <span data-ttu-id="c69bd-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="c69bd-166">Is Indexed</span></span>             | <span data-ttu-id="c69bd-167">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-167">False</span></span>                           |
| <span data-ttu-id="c69bd-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c69bd-168">In Global Catalog</span></span>      | <span data-ttu-id="c69bd-169">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-169">False</span></span>                           |
| <span data-ttu-id="c69bd-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c69bd-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69bd-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c69bd-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c69bd-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69bd-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c69bd-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69bd-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c69bd-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-174">Search-Flags</span></span>           | <span data-ttu-id="c69bd-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69bd-175">0x00000000</span></span>                      |
| <span data-ttu-id="c69bd-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-176">System-Flags</span></span>           | <span data-ttu-id="c69bd-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c69bd-177">0x08000014</span></span>                      |
| <span data-ttu-id="c69bd-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c69bd-178">Classes used in</span></span>        | [<span data-ttu-id="c69bd-179">**Início**</span><span class="sxs-lookup"><span data-stu-id="c69bd-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c69bd-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="c69bd-180">ADAM</span></span>



| <span data-ttu-id="c69bd-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-181">Entry</span></span> | <span data-ttu-id="c69bd-182">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c69bd-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="c69bd-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69bd-185">System-Only</span></span>            | <span data-ttu-id="c69bd-186">True</span><span class="sxs-lookup"><span data-stu-id="c69bd-186">True</span></span>                            |
| <span data-ttu-id="c69bd-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c69bd-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c69bd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-188">False</span></span>                           |
| <span data-ttu-id="c69bd-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="c69bd-189">Is Indexed</span></span>             | <span data-ttu-id="c69bd-190">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-190">False</span></span>                           |
| <span data-ttu-id="c69bd-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c69bd-191">In Global Catalog</span></span>      | <span data-ttu-id="c69bd-192">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-192">False</span></span>                           |
| <span data-ttu-id="c69bd-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c69bd-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69bd-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c69bd-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c69bd-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69bd-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c69bd-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69bd-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c69bd-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-197">Search-Flags</span></span>           | <span data-ttu-id="c69bd-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69bd-198">0x00000000</span></span>                      |
| <span data-ttu-id="c69bd-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-199">System-Flags</span></span>           | <span data-ttu-id="c69bd-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c69bd-200">0x08000014</span></span>                      |
| <span data-ttu-id="c69bd-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c69bd-201">Classes used in</span></span>        | [<span data-ttu-id="c69bd-202">**Início**</span><span class="sxs-lookup"><span data-stu-id="c69bd-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c69bd-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c69bd-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c69bd-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-204">Entry</span></span> | <span data-ttu-id="c69bd-205">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c69bd-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="c69bd-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69bd-208">System-Only</span></span>            | <span data-ttu-id="c69bd-209">True</span><span class="sxs-lookup"><span data-stu-id="c69bd-209">True</span></span>                            |
| <span data-ttu-id="c69bd-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c69bd-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c69bd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-211">False</span></span>                           |
| <span data-ttu-id="c69bd-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="c69bd-212">Is Indexed</span></span>             | <span data-ttu-id="c69bd-213">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-213">False</span></span>                           |
| <span data-ttu-id="c69bd-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c69bd-214">In Global Catalog</span></span>      | <span data-ttu-id="c69bd-215">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-215">False</span></span>                           |
| <span data-ttu-id="c69bd-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c69bd-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69bd-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c69bd-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c69bd-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69bd-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c69bd-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69bd-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c69bd-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-220">Search-Flags</span></span>           | <span data-ttu-id="c69bd-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69bd-221">0x00000000</span></span>                      |
| <span data-ttu-id="c69bd-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-222">System-Flags</span></span>           | <span data-ttu-id="c69bd-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c69bd-223">0x08000014</span></span>                      |
| <span data-ttu-id="c69bd-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c69bd-224">Classes used in</span></span>        | [<span data-ttu-id="c69bd-225">**Início**</span><span class="sxs-lookup"><span data-stu-id="c69bd-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c69bd-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c69bd-226">Windows Server 2008</span></span>



| <span data-ttu-id="c69bd-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-227">Entry</span></span> | <span data-ttu-id="c69bd-228">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c69bd-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="c69bd-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69bd-231">System-Only</span></span>            | <span data-ttu-id="c69bd-232">True</span><span class="sxs-lookup"><span data-stu-id="c69bd-232">True</span></span>                            |
| <span data-ttu-id="c69bd-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c69bd-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c69bd-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-234">False</span></span>                           |
| <span data-ttu-id="c69bd-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="c69bd-235">Is Indexed</span></span>             | <span data-ttu-id="c69bd-236">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-236">False</span></span>                           |
| <span data-ttu-id="c69bd-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c69bd-237">In Global Catalog</span></span>      | <span data-ttu-id="c69bd-238">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-238">False</span></span>                           |
| <span data-ttu-id="c69bd-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c69bd-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69bd-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c69bd-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c69bd-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69bd-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c69bd-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69bd-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c69bd-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-243">Search-Flags</span></span>           | <span data-ttu-id="c69bd-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69bd-244">0x00000000</span></span>                      |
| <span data-ttu-id="c69bd-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-245">System-Flags</span></span>           | <span data-ttu-id="c69bd-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c69bd-246">0x08000014</span></span>                      |
| <span data-ttu-id="c69bd-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c69bd-247">Classes used in</span></span>        | [<span data-ttu-id="c69bd-248">**Início**</span><span class="sxs-lookup"><span data-stu-id="c69bd-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c69bd-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c69bd-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c69bd-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-250">Entry</span></span> | <span data-ttu-id="c69bd-251">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c69bd-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="c69bd-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69bd-254">System-Only</span></span>            | <span data-ttu-id="c69bd-255">True</span><span class="sxs-lookup"><span data-stu-id="c69bd-255">True</span></span>                            |
| <span data-ttu-id="c69bd-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c69bd-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c69bd-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-257">False</span></span>                           |
| <span data-ttu-id="c69bd-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="c69bd-258">Is Indexed</span></span>             | <span data-ttu-id="c69bd-259">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-259">False</span></span>                           |
| <span data-ttu-id="c69bd-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c69bd-260">In Global Catalog</span></span>      | <span data-ttu-id="c69bd-261">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-261">False</span></span>                           |
| <span data-ttu-id="c69bd-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c69bd-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69bd-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c69bd-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c69bd-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69bd-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c69bd-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69bd-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c69bd-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-266">Search-Flags</span></span>           | <span data-ttu-id="c69bd-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69bd-267">0x00000000</span></span>                      |
| <span data-ttu-id="c69bd-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-268">System-Flags</span></span>           | <span data-ttu-id="c69bd-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c69bd-269">0x08000014</span></span>                      |
| <span data-ttu-id="c69bd-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c69bd-270">Classes used in</span></span>        | [<span data-ttu-id="c69bd-271">**Início**</span><span class="sxs-lookup"><span data-stu-id="c69bd-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c69bd-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c69bd-272">Windows Server 2012</span></span>



| <span data-ttu-id="c69bd-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="c69bd-273">Entry</span></span> | <span data-ttu-id="c69bd-274">Valor</span><span class="sxs-lookup"><span data-stu-id="c69bd-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c69bd-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="c69bd-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c69bd-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="c69bd-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="c69bd-277">System-Only</span></span>            | <span data-ttu-id="c69bd-278">True</span><span class="sxs-lookup"><span data-stu-id="c69bd-278">True</span></span>                            |
| <span data-ttu-id="c69bd-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c69bd-279">Is-Single-Valued</span></span>       | <span data-ttu-id="c69bd-280">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-280">False</span></span>                           |
| <span data-ttu-id="c69bd-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="c69bd-281">Is Indexed</span></span>             | <span data-ttu-id="c69bd-282">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-282">False</span></span>                           |
| <span data-ttu-id="c69bd-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c69bd-283">In Global Catalog</span></span>      | <span data-ttu-id="c69bd-284">Falso</span><span class="sxs-lookup"><span data-stu-id="c69bd-284">False</span></span>                           |
| <span data-ttu-id="c69bd-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c69bd-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="c69bd-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c69bd-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c69bd-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c69bd-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="c69bd-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c69bd-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="c69bd-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-289">Search-Flags</span></span>           | <span data-ttu-id="c69bd-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c69bd-290">0x00000000</span></span>                      |
| <span data-ttu-id="c69bd-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c69bd-291">System-Flags</span></span>           | <span data-ttu-id="c69bd-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="c69bd-292">0x08000014</span></span>                      |
| <span data-ttu-id="c69bd-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c69bd-293">Classes used in</span></span>        | [<span data-ttu-id="c69bd-294">**Início**</span><span class="sxs-lookup"><span data-stu-id="c69bd-294">**Top**</span></span>](c-top.md)<br/> |



 

