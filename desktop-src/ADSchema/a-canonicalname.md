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
# <a name="canonical-name-attribute"></a><span data-ttu-id="7feb2-105">Canonical-Name atributo</span><span class="sxs-lookup"><span data-stu-id="7feb2-105">Canonical-Name attribute</span></span>

<span data-ttu-id="7feb2-106">O nome do objeto no formato canônico.</span><span class="sxs-lookup"><span data-stu-id="7feb2-106">The name of the object in canonical format.</span></span> <span data-ttu-id="7feb2-107">myserver2.fabrikam.com/users/jeffsmith é um exemplo de um nome distinto em formato canônico.</span><span class="sxs-lookup"><span data-stu-id="7feb2-107">myserver2.fabrikam.com/users/jeffsmith is an example of a distinguished name in canonical format.</span></span> <span data-ttu-id="7feb2-108">Este é um atributo construído.</span><span class="sxs-lookup"><span data-stu-id="7feb2-108">This is a constructed attribute.</span></span> <span data-ttu-id="7feb2-109">Os resultados retornados são idênticos aos retornados pela seguinte função de Active Directory: DsCrackNames (nulo, \_ sinalizador de nome DS \_ \_ \_ somente sintático, nome do FQDN do DS \_ \_ 1779 \_ , \_ nome canônico do DS \_ ,...).</span><span class="sxs-lookup"><span data-stu-id="7feb2-109">The results returned are identical to those returned by the following Active Directory function: DsCrackNames(NULL, DS\_NAME\_FLAG\_SYNTACTICAL\_ONLY, DS\_FQDN\_1779\_NAME, DS\_CANONICAL\_NAME, ...).</span></span>

<span data-ttu-id="7feb2-110">Para obter mais informações sobre formatos de nome, consulte [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span><span class="sxs-lookup"><span data-stu-id="7feb2-110">For more information about name formats, see [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).</span></span>



| <span data-ttu-id="7feb2-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-111">Entry</span></span> | <span data-ttu-id="7feb2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7feb2-113">CN</span><span class="sxs-lookup"><span data-stu-id="7feb2-113">CN</span></span>                | <span data-ttu-id="7feb2-114">Canonical-Name</span><span class="sxs-lookup"><span data-stu-id="7feb2-114">Canonical-Name</span></span>                              |
| <span data-ttu-id="7feb2-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7feb2-115">Ldap-Display-Name</span></span> | <span data-ttu-id="7feb2-116">canonicalName</span><span class="sxs-lookup"><span data-stu-id="7feb2-116">canonicalName</span></span>                               |
| <span data-ttu-id="7feb2-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7feb2-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="7feb2-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7feb2-118">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="7feb2-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7feb2-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7feb2-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-120">Attribute-Id</span></span>      | <span data-ttu-id="7feb2-121">1.2.840.113556.1.4.916</span><span class="sxs-lookup"><span data-stu-id="7feb2-121">1.2.840.113556.1.4.916</span></span>                      |
| <span data-ttu-id="7feb2-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7feb2-122">System-Id-Guid</span></span>    | <span data-ttu-id="7feb2-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="7feb2-123">9a7ad945-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="7feb2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="7feb2-124">Syntax</span></span>            | [<span data-ttu-id="7feb2-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7feb2-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7feb2-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="7feb2-126">Implementations</span></span>

-   [<span data-ttu-id="7feb2-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7feb2-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7feb2-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7feb2-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7feb2-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7feb2-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7feb2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7feb2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7feb2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7feb2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7feb2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7feb2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7feb2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7feb2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7feb2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7feb2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="7feb2-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-135">Entry</span></span> | <span data-ttu-id="7feb2-136">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7feb2-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="7feb2-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-138">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="7feb2-139">System-Only</span></span>            | <span data-ttu-id="7feb2-140">True</span><span class="sxs-lookup"><span data-stu-id="7feb2-140">True</span></span>                            |
| <span data-ttu-id="7feb2-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7feb2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="7feb2-142">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-142">False</span></span>                           |
| <span data-ttu-id="7feb2-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="7feb2-143">Is Indexed</span></span>             | <span data-ttu-id="7feb2-144">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-144">False</span></span>                           |
| <span data-ttu-id="7feb2-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7feb2-145">In Global Catalog</span></span>      | <span data-ttu-id="7feb2-146">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-146">False</span></span>                           |
| <span data-ttu-id="7feb2-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7feb2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="7feb2-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7feb2-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7feb2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7feb2-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7feb2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7feb2-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7feb2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-151">Search-Flags</span></span>           | <span data-ttu-id="7feb2-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7feb2-152">0x00000000</span></span>                      |
| <span data-ttu-id="7feb2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-153">System-Flags</span></span>           | <span data-ttu-id="7feb2-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7feb2-154">0x08000014</span></span>                      |
| <span data-ttu-id="7feb2-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7feb2-155">Classes used in</span></span>        | [<span data-ttu-id="7feb2-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="7feb2-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7feb2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7feb2-157">Windows Server 2003</span></span>



| <span data-ttu-id="7feb2-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-158">Entry</span></span> | <span data-ttu-id="7feb2-159">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7feb2-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="7feb2-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="7feb2-162">System-Only</span></span>            | <span data-ttu-id="7feb2-163">True</span><span class="sxs-lookup"><span data-stu-id="7feb2-163">True</span></span>                            |
| <span data-ttu-id="7feb2-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7feb2-164">Is-Single-Valued</span></span>       | <span data-ttu-id="7feb2-165">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-165">False</span></span>                           |
| <span data-ttu-id="7feb2-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="7feb2-166">Is Indexed</span></span>             | <span data-ttu-id="7feb2-167">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-167">False</span></span>                           |
| <span data-ttu-id="7feb2-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7feb2-168">In Global Catalog</span></span>      | <span data-ttu-id="7feb2-169">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-169">False</span></span>                           |
| <span data-ttu-id="7feb2-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7feb2-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="7feb2-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7feb2-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7feb2-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7feb2-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7feb2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7feb2-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7feb2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-174">Search-Flags</span></span>           | <span data-ttu-id="7feb2-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7feb2-175">0x00000000</span></span>                      |
| <span data-ttu-id="7feb2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-176">System-Flags</span></span>           | <span data-ttu-id="7feb2-177">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7feb2-177">0x08000014</span></span>                      |
| <span data-ttu-id="7feb2-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7feb2-178">Classes used in</span></span>        | [<span data-ttu-id="7feb2-179">**Início**</span><span class="sxs-lookup"><span data-stu-id="7feb2-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7feb2-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="7feb2-180">ADAM</span></span>



| <span data-ttu-id="7feb2-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-181">Entry</span></span> | <span data-ttu-id="7feb2-182">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7feb2-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="7feb2-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-184">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="7feb2-185">System-Only</span></span>            | <span data-ttu-id="7feb2-186">True</span><span class="sxs-lookup"><span data-stu-id="7feb2-186">True</span></span>                            |
| <span data-ttu-id="7feb2-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7feb2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="7feb2-188">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-188">False</span></span>                           |
| <span data-ttu-id="7feb2-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="7feb2-189">Is Indexed</span></span>             | <span data-ttu-id="7feb2-190">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-190">False</span></span>                           |
| <span data-ttu-id="7feb2-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7feb2-191">In Global Catalog</span></span>      | <span data-ttu-id="7feb2-192">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-192">False</span></span>                           |
| <span data-ttu-id="7feb2-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7feb2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="7feb2-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7feb2-194">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7feb2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7feb2-195">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7feb2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7feb2-196">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7feb2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-197">Search-Flags</span></span>           | <span data-ttu-id="7feb2-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7feb2-198">0x00000000</span></span>                      |
| <span data-ttu-id="7feb2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-199">System-Flags</span></span>           | <span data-ttu-id="7feb2-200">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7feb2-200">0x08000014</span></span>                      |
| <span data-ttu-id="7feb2-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7feb2-201">Classes used in</span></span>        | [<span data-ttu-id="7feb2-202">**Início**</span><span class="sxs-lookup"><span data-stu-id="7feb2-202">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7feb2-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7feb2-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7feb2-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-204">Entry</span></span> | <span data-ttu-id="7feb2-205">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-205">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7feb2-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="7feb2-206">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-207">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="7feb2-208">System-Only</span></span>            | <span data-ttu-id="7feb2-209">True</span><span class="sxs-lookup"><span data-stu-id="7feb2-209">True</span></span>                            |
| <span data-ttu-id="7feb2-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7feb2-210">Is-Single-Valued</span></span>       | <span data-ttu-id="7feb2-211">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-211">False</span></span>                           |
| <span data-ttu-id="7feb2-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="7feb2-212">Is Indexed</span></span>             | <span data-ttu-id="7feb2-213">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-213">False</span></span>                           |
| <span data-ttu-id="7feb2-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7feb2-214">In Global Catalog</span></span>      | <span data-ttu-id="7feb2-215">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-215">False</span></span>                           |
| <span data-ttu-id="7feb2-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7feb2-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="7feb2-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7feb2-217">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7feb2-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7feb2-218">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7feb2-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7feb2-219">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7feb2-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-220">Search-Flags</span></span>           | <span data-ttu-id="7feb2-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7feb2-221">0x00000000</span></span>                      |
| <span data-ttu-id="7feb2-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-222">System-Flags</span></span>           | <span data-ttu-id="7feb2-223">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7feb2-223">0x08000014</span></span>                      |
| <span data-ttu-id="7feb2-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7feb2-224">Classes used in</span></span>        | [<span data-ttu-id="7feb2-225">**Início**</span><span class="sxs-lookup"><span data-stu-id="7feb2-225">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7feb2-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7feb2-226">Windows Server 2008</span></span>



| <span data-ttu-id="7feb2-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-227">Entry</span></span> | <span data-ttu-id="7feb2-228">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-228">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7feb2-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="7feb2-229">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="7feb2-231">System-Only</span></span>            | <span data-ttu-id="7feb2-232">True</span><span class="sxs-lookup"><span data-stu-id="7feb2-232">True</span></span>                            |
| <span data-ttu-id="7feb2-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7feb2-233">Is-Single-Valued</span></span>       | <span data-ttu-id="7feb2-234">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-234">False</span></span>                           |
| <span data-ttu-id="7feb2-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="7feb2-235">Is Indexed</span></span>             | <span data-ttu-id="7feb2-236">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-236">False</span></span>                           |
| <span data-ttu-id="7feb2-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7feb2-237">In Global Catalog</span></span>      | <span data-ttu-id="7feb2-238">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-238">False</span></span>                           |
| <span data-ttu-id="7feb2-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7feb2-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="7feb2-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7feb2-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7feb2-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7feb2-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7feb2-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7feb2-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7feb2-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-243">Search-Flags</span></span>           | <span data-ttu-id="7feb2-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7feb2-244">0x00000000</span></span>                      |
| <span data-ttu-id="7feb2-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-245">System-Flags</span></span>           | <span data-ttu-id="7feb2-246">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7feb2-246">0x08000014</span></span>                      |
| <span data-ttu-id="7feb2-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7feb2-247">Classes used in</span></span>        | [<span data-ttu-id="7feb2-248">**Início**</span><span class="sxs-lookup"><span data-stu-id="7feb2-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7feb2-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7feb2-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7feb2-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-250">Entry</span></span> | <span data-ttu-id="7feb2-251">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7feb2-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="7feb2-252">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-253">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="7feb2-254">System-Only</span></span>            | <span data-ttu-id="7feb2-255">True</span><span class="sxs-lookup"><span data-stu-id="7feb2-255">True</span></span>                            |
| <span data-ttu-id="7feb2-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7feb2-256">Is-Single-Valued</span></span>       | <span data-ttu-id="7feb2-257">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-257">False</span></span>                           |
| <span data-ttu-id="7feb2-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="7feb2-258">Is Indexed</span></span>             | <span data-ttu-id="7feb2-259">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-259">False</span></span>                           |
| <span data-ttu-id="7feb2-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7feb2-260">In Global Catalog</span></span>      | <span data-ttu-id="7feb2-261">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-261">False</span></span>                           |
| <span data-ttu-id="7feb2-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7feb2-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="7feb2-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7feb2-263">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7feb2-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7feb2-264">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7feb2-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7feb2-265">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7feb2-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-266">Search-Flags</span></span>           | <span data-ttu-id="7feb2-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7feb2-267">0x00000000</span></span>                      |
| <span data-ttu-id="7feb2-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-268">System-Flags</span></span>           | <span data-ttu-id="7feb2-269">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7feb2-269">0x08000014</span></span>                      |
| <span data-ttu-id="7feb2-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7feb2-270">Classes used in</span></span>        | [<span data-ttu-id="7feb2-271">**Início**</span><span class="sxs-lookup"><span data-stu-id="7feb2-271">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7feb2-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7feb2-272">Windows Server 2012</span></span>



| <span data-ttu-id="7feb2-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="7feb2-273">Entry</span></span> | <span data-ttu-id="7feb2-274">Valor</span><span class="sxs-lookup"><span data-stu-id="7feb2-274">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="7feb2-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="7feb2-275">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7feb2-276">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="7feb2-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="7feb2-277">System-Only</span></span>            | <span data-ttu-id="7feb2-278">True</span><span class="sxs-lookup"><span data-stu-id="7feb2-278">True</span></span>                            |
| <span data-ttu-id="7feb2-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7feb2-279">Is-Single-Valued</span></span>       | <span data-ttu-id="7feb2-280">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-280">False</span></span>                           |
| <span data-ttu-id="7feb2-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="7feb2-281">Is Indexed</span></span>             | <span data-ttu-id="7feb2-282">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-282">False</span></span>                           |
| <span data-ttu-id="7feb2-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7feb2-283">In Global Catalog</span></span>      | <span data-ttu-id="7feb2-284">Falso</span><span class="sxs-lookup"><span data-stu-id="7feb2-284">False</span></span>                           |
| <span data-ttu-id="7feb2-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7feb2-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="7feb2-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7feb2-286">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="7feb2-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7feb2-287">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="7feb2-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7feb2-288">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="7feb2-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-289">Search-Flags</span></span>           | <span data-ttu-id="7feb2-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7feb2-290">0x00000000</span></span>                      |
| <span data-ttu-id="7feb2-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7feb2-291">System-Flags</span></span>           | <span data-ttu-id="7feb2-292">0x08000014</span><span class="sxs-lookup"><span data-stu-id="7feb2-292">0x08000014</span></span>                      |
| <span data-ttu-id="7feb2-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7feb2-293">Classes used in</span></span>        | [<span data-ttu-id="7feb2-294">**Início**</span><span class="sxs-lookup"><span data-stu-id="7feb2-294">**Top**</span></span>](c-top.md)<br/> |



 

