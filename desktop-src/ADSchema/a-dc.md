---
title: Domain-Component atributo
description: O atributo de nomenclatura para objetos de domínio e DNS. Geralmente exibido como DC DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Esquema de Domain-Component do atributo AD
- Esquema de AD do atributo de DC
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086712"
---
# <a name="domain-component-attribute"></a><span data-ttu-id="3e066-106">Domain-Component atributo</span><span class="sxs-lookup"><span data-stu-id="3e066-106">Domain-Component attribute</span></span>

<span data-ttu-id="3e066-107">O atributo de nomenclatura para objetos de domínio e DNS.</span><span class="sxs-lookup"><span data-stu-id="3e066-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="3e066-108">Geralmente exibido como DC = DomainName.</span><span class="sxs-lookup"><span data-stu-id="3e066-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="3e066-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-109">Entry</span></span> | <span data-ttu-id="3e066-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3e066-111">CN</span><span class="sxs-lookup"><span data-stu-id="3e066-111">CN</span></span>                | <span data-ttu-id="3e066-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="3e066-112">Domain-Component</span></span>                            |
| <span data-ttu-id="3e066-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3e066-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3e066-114">dc</span><span class="sxs-lookup"><span data-stu-id="3e066-114">dc</span></span>                                          |
| <span data-ttu-id="3e066-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3e066-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3e066-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3e066-116">Update Privilege</span></span>  | <span data-ttu-id="3e066-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="3e066-117">Domain administrator</span></span>                        |
| <span data-ttu-id="3e066-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3e066-118">Update Frequency</span></span>  | <span data-ttu-id="3e066-119">Quando o domínio é criado.</span><span class="sxs-lookup"><span data-stu-id="3e066-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="3e066-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-120">Attribute-Id</span></span>      | <span data-ttu-id="3e066-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="3e066-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="3e066-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3e066-122">System-Id-Guid</span></span>    | <span data-ttu-id="3e066-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="3e066-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="3e066-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e066-124">Syntax</span></span>            | [<span data-ttu-id="3e066-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3e066-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3e066-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="3e066-126">Implementations</span></span>

-   [<span data-ttu-id="3e066-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3e066-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3e066-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3e066-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3e066-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3e066-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3e066-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3e066-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3e066-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3e066-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3e066-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3e066-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3e066-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e066-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3e066-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3e066-134">Windows 2000 Server</span></span>



| <span data-ttu-id="3e066-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-135">Entry</span></span> | <span data-ttu-id="3e066-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e066-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e066-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e066-139">System-Only</span></span>            | <span data-ttu-id="3e066-140">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e066-141">Is-Single-Valued</span></span>       | <span data-ttu-id="3e066-142">True</span><span class="sxs-lookup"><span data-stu-id="3e066-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e066-143">Is Indexed</span></span>             | <span data-ttu-id="3e066-144">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e066-145">In Global Catalog</span></span>      | <span data-ttu-id="3e066-146">True</span><span class="sxs-lookup"><span data-stu-id="3e066-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e066-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e066-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e066-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3e066-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e066-149">Range-Lower</span></span>            | <span data-ttu-id="3e066-150">1</span><span class="sxs-lookup"><span data-stu-id="3e066-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="3e066-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e066-151">Range-Upper</span></span>            | <span data-ttu-id="3e066-152">255</span><span class="sxs-lookup"><span data-stu-id="3e066-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="3e066-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-153">Search-Flags</span></span>           | <span data-ttu-id="3e066-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e066-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3e066-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-155">System-Flags</span></span>           | <span data-ttu-id="3e066-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3e066-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3e066-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e066-157">Classes used in</span></span>        | [<span data-ttu-id="3e066-158">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3e066-159">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3e066-160">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3e066-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3e066-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e066-161">Windows Server 2003</span></span>



| <span data-ttu-id="3e066-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-162">Entry</span></span> | <span data-ttu-id="3e066-163">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e066-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e066-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e066-166">System-Only</span></span>            | <span data-ttu-id="3e066-167">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e066-168">Is-Single-Valued</span></span>       | <span data-ttu-id="3e066-169">True</span><span class="sxs-lookup"><span data-stu-id="3e066-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e066-170">Is Indexed</span></span>             | <span data-ttu-id="3e066-171">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e066-172">In Global Catalog</span></span>      | <span data-ttu-id="3e066-173">True</span><span class="sxs-lookup"><span data-stu-id="3e066-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e066-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e066-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e066-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3e066-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e066-176">Range-Lower</span></span>            | <span data-ttu-id="3e066-177">1</span><span class="sxs-lookup"><span data-stu-id="3e066-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="3e066-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e066-178">Range-Upper</span></span>            | <span data-ttu-id="3e066-179">255</span><span class="sxs-lookup"><span data-stu-id="3e066-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="3e066-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-180">Search-Flags</span></span>           | <span data-ttu-id="3e066-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e066-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3e066-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-182">System-Flags</span></span>           | <span data-ttu-id="3e066-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3e066-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3e066-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e066-184">Classes used in</span></span>        | [<span data-ttu-id="3e066-185">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3e066-186">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3e066-187">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3e066-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3e066-188">ADAM</span><span class="sxs-lookup"><span data-stu-id="3e066-188">ADAM</span></span>



| <span data-ttu-id="3e066-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-189">Entry</span></span> | <span data-ttu-id="3e066-190">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="3e066-191">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e066-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="3e066-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="3e066-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e066-193">System-Only</span></span>            | <span data-ttu-id="3e066-194">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-194">False</span></span>                                 |
| <span data-ttu-id="3e066-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e066-195">Is-Single-Valued</span></span>       | <span data-ttu-id="3e066-196">True</span><span class="sxs-lookup"><span data-stu-id="3e066-196">True</span></span>                                  |
| <span data-ttu-id="3e066-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e066-197">Is Indexed</span></span>             | <span data-ttu-id="3e066-198">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-198">False</span></span>                                 |
| <span data-ttu-id="3e066-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e066-199">In Global Catalog</span></span>      | <span data-ttu-id="3e066-200">True</span><span class="sxs-lookup"><span data-stu-id="3e066-200">True</span></span>                                  |
| <span data-ttu-id="3e066-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e066-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e066-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e066-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="3e066-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e066-203">Range-Lower</span></span>            | <span data-ttu-id="3e066-204">1</span><span class="sxs-lookup"><span data-stu-id="3e066-204">1</span></span>                                     |
| <span data-ttu-id="3e066-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e066-205">Range-Upper</span></span>            | <span data-ttu-id="3e066-206">255</span><span class="sxs-lookup"><span data-stu-id="3e066-206">255</span></span>                                   |
| <span data-ttu-id="3e066-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-207">Search-Flags</span></span>           | <span data-ttu-id="3e066-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e066-208">0x00000000</span></span>                            |
| <span data-ttu-id="3e066-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-209">System-Flags</span></span>           | <span data-ttu-id="3e066-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3e066-210">0x00000012</span></span>                            |
| <span data-ttu-id="3e066-211">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e066-211">Classes used in</span></span>        | [<span data-ttu-id="3e066-212">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3e066-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3e066-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3e066-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3e066-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-214">Entry</span></span> | <span data-ttu-id="3e066-215">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e066-216">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e066-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e066-218">System-Only</span></span>            | <span data-ttu-id="3e066-219">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e066-220">Is-Single-Valued</span></span>       | <span data-ttu-id="3e066-221">True</span><span class="sxs-lookup"><span data-stu-id="3e066-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e066-222">Is Indexed</span></span>             | <span data-ttu-id="3e066-223">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e066-224">In Global Catalog</span></span>      | <span data-ttu-id="3e066-225">True</span><span class="sxs-lookup"><span data-stu-id="3e066-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e066-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e066-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e066-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3e066-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e066-228">Range-Lower</span></span>            | <span data-ttu-id="3e066-229">1</span><span class="sxs-lookup"><span data-stu-id="3e066-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="3e066-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e066-230">Range-Upper</span></span>            | <span data-ttu-id="3e066-231">255</span><span class="sxs-lookup"><span data-stu-id="3e066-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="3e066-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-232">Search-Flags</span></span>           | <span data-ttu-id="3e066-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e066-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3e066-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-234">System-Flags</span></span>           | <span data-ttu-id="3e066-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3e066-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3e066-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e066-236">Classes used in</span></span>        | [<span data-ttu-id="3e066-237">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3e066-238">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3e066-239">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3e066-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3e066-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e066-240">Windows Server 2008</span></span>



| <span data-ttu-id="3e066-241">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-241">Entry</span></span> | <span data-ttu-id="3e066-242">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e066-243">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e066-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e066-245">System-Only</span></span>            | <span data-ttu-id="3e066-246">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-247">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e066-247">Is-Single-Valued</span></span>       | <span data-ttu-id="3e066-248">True</span><span class="sxs-lookup"><span data-stu-id="3e066-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-249">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e066-249">Is Indexed</span></span>             | <span data-ttu-id="3e066-250">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-251">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e066-251">In Global Catalog</span></span>      | <span data-ttu-id="3e066-252">True</span><span class="sxs-lookup"><span data-stu-id="3e066-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e066-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e066-254">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e066-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3e066-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e066-255">Range-Lower</span></span>            | <span data-ttu-id="3e066-256">1</span><span class="sxs-lookup"><span data-stu-id="3e066-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="3e066-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e066-257">Range-Upper</span></span>            | <span data-ttu-id="3e066-258">255</span><span class="sxs-lookup"><span data-stu-id="3e066-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="3e066-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-259">Search-Flags</span></span>           | <span data-ttu-id="3e066-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e066-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3e066-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-261">System-Flags</span></span>           | <span data-ttu-id="3e066-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3e066-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3e066-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e066-263">Classes used in</span></span>        | [<span data-ttu-id="3e066-264">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3e066-265">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3e066-266">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3e066-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3e066-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3e066-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3e066-268">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-268">Entry</span></span> | <span data-ttu-id="3e066-269">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e066-270">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e066-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e066-272">System-Only</span></span>            | <span data-ttu-id="3e066-273">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-274">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e066-274">Is-Single-Valued</span></span>       | <span data-ttu-id="3e066-275">True</span><span class="sxs-lookup"><span data-stu-id="3e066-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-276">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e066-276">Is Indexed</span></span>             | <span data-ttu-id="3e066-277">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-278">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e066-278">In Global Catalog</span></span>      | <span data-ttu-id="3e066-279">True</span><span class="sxs-lookup"><span data-stu-id="3e066-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e066-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e066-281">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e066-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3e066-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e066-282">Range-Lower</span></span>            | <span data-ttu-id="3e066-283">1</span><span class="sxs-lookup"><span data-stu-id="3e066-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="3e066-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e066-284">Range-Upper</span></span>            | <span data-ttu-id="3e066-285">255</span><span class="sxs-lookup"><span data-stu-id="3e066-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="3e066-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-286">Search-Flags</span></span>           | <span data-ttu-id="3e066-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e066-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3e066-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-288">System-Flags</span></span>           | <span data-ttu-id="3e066-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3e066-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3e066-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e066-290">Classes used in</span></span>        | [<span data-ttu-id="3e066-291">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3e066-292">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3e066-293">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3e066-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3e066-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e066-294">Windows Server 2012</span></span>



| <span data-ttu-id="3e066-295">Entrada</span><span class="sxs-lookup"><span data-stu-id="3e066-295">Entry</span></span> | <span data-ttu-id="3e066-296">Valor</span><span class="sxs-lookup"><span data-stu-id="3e066-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e066-297">ID do link</span><span class="sxs-lookup"><span data-stu-id="3e066-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3e066-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3e066-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="3e066-299">System-Only</span></span>            | <span data-ttu-id="3e066-300">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-301">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3e066-301">Is-Single-Valued</span></span>       | <span data-ttu-id="3e066-302">True</span><span class="sxs-lookup"><span data-stu-id="3e066-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-303">É indexado</span><span class="sxs-lookup"><span data-stu-id="3e066-303">Is Indexed</span></span>             | <span data-ttu-id="3e066-304">Falso</span><span class="sxs-lookup"><span data-stu-id="3e066-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="3e066-305">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3e066-305">In Global Catalog</span></span>      | <span data-ttu-id="3e066-306">True</span><span class="sxs-lookup"><span data-stu-id="3e066-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="3e066-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3e066-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="3e066-308">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3e066-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3e066-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3e066-309">Range-Lower</span></span>            | <span data-ttu-id="3e066-310">1</span><span class="sxs-lookup"><span data-stu-id="3e066-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="3e066-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3e066-311">Range-Upper</span></span>            | <span data-ttu-id="3e066-312">255</span><span class="sxs-lookup"><span data-stu-id="3e066-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="3e066-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-313">Search-Flags</span></span>           | <span data-ttu-id="3e066-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3e066-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3e066-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3e066-315">System-Flags</span></span>           | <span data-ttu-id="3e066-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3e066-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3e066-317">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3e066-317">Classes used in</span></span>        | [<span data-ttu-id="3e066-318">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3e066-319">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3e066-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3e066-320">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3e066-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 





