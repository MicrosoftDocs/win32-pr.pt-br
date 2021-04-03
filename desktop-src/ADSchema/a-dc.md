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
# <a name="domain-component-attribute"></a><span data-ttu-id="3f54d-106">Domain-Component atributo</span><span class="sxs-lookup"><span data-stu-id="3f54d-106">Domain-Component attribute</span></span>

<span data-ttu-id="3f54d-107">O atributo de nomenclatura para objetos de domínio e DNS.</span><span class="sxs-lookup"><span data-stu-id="3f54d-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="3f54d-108">Geralmente exibido como DC = DomainName.</span><span class="sxs-lookup"><span data-stu-id="3f54d-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="3f54d-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-109">Entry</span></span> | <span data-ttu-id="3f54d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3f54d-111">CN</span><span class="sxs-lookup"><span data-stu-id="3f54d-111">CN</span></span>                | <span data-ttu-id="3f54d-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="3f54d-112">Domain-Component</span></span>                            |
| <span data-ttu-id="3f54d-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="3f54d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="3f54d-114">dc</span><span class="sxs-lookup"><span data-stu-id="3f54d-114">dc</span></span>                                          |
| <span data-ttu-id="3f54d-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="3f54d-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="3f54d-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="3f54d-116">Update Privilege</span></span>  | <span data-ttu-id="3f54d-117">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="3f54d-117">Domain administrator</span></span>                        |
| <span data-ttu-id="3f54d-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="3f54d-118">Update Frequency</span></span>  | <span data-ttu-id="3f54d-119">Quando o domínio é criado.</span><span class="sxs-lookup"><span data-stu-id="3f54d-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="3f54d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-120">Attribute-Id</span></span>      | <span data-ttu-id="3f54d-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="3f54d-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="3f54d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="3f54d-122">System-Id-Guid</span></span>    | <span data-ttu-id="3f54d-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="3f54d-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="3f54d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f54d-124">Syntax</span></span>            | [<span data-ttu-id="3f54d-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="3f54d-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3f54d-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="3f54d-126">Implementations</span></span>

-   [<span data-ttu-id="3f54d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3f54d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3f54d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3f54d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3f54d-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="3f54d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="3f54d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3f54d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3f54d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3f54d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3f54d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3f54d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3f54d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3f54d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3f54d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3f54d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="3f54d-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-135">Entry</span></span> | <span data-ttu-id="3f54d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f54d-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f54d-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f54d-139">System-Only</span></span>            | <span data-ttu-id="3f54d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f54d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="3f54d-142">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f54d-143">Is Indexed</span></span>             | <span data-ttu-id="3f54d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f54d-145">In Global Catalog</span></span>      | <span data-ttu-id="3f54d-146">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f54d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f54d-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f54d-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3f54d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f54d-149">Range-Lower</span></span>            | <span data-ttu-id="3f54d-150">1</span><span class="sxs-lookup"><span data-stu-id="3f54d-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="3f54d-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f54d-151">Range-Upper</span></span>            | <span data-ttu-id="3f54d-152">255</span><span class="sxs-lookup"><span data-stu-id="3f54d-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="3f54d-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-153">Search-Flags</span></span>           | <span data-ttu-id="3f54d-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f54d-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-155">System-Flags</span></span>           | <span data-ttu-id="3f54d-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3f54d-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-157">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f54d-157">Classes used in</span></span>        | [<span data-ttu-id="3f54d-158">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3f54d-159">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3f54d-160">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3f54d-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3f54d-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3f54d-161">Windows Server 2003</span></span>



| <span data-ttu-id="3f54d-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-162">Entry</span></span> | <span data-ttu-id="3f54d-163">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f54d-164">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f54d-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f54d-166">System-Only</span></span>            | <span data-ttu-id="3f54d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f54d-168">Is-Single-Valued</span></span>       | <span data-ttu-id="3f54d-169">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f54d-170">Is Indexed</span></span>             | <span data-ttu-id="3f54d-171">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f54d-172">In Global Catalog</span></span>      | <span data-ttu-id="3f54d-173">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f54d-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f54d-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f54d-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3f54d-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f54d-176">Range-Lower</span></span>            | <span data-ttu-id="3f54d-177">1</span><span class="sxs-lookup"><span data-stu-id="3f54d-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="3f54d-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f54d-178">Range-Upper</span></span>            | <span data-ttu-id="3f54d-179">255</span><span class="sxs-lookup"><span data-stu-id="3f54d-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="3f54d-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-180">Search-Flags</span></span>           | <span data-ttu-id="3f54d-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f54d-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-182">System-Flags</span></span>           | <span data-ttu-id="3f54d-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3f54d-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f54d-184">Classes used in</span></span>        | [<span data-ttu-id="3f54d-185">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3f54d-186">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3f54d-187">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3f54d-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="3f54d-188">ADAM</span><span class="sxs-lookup"><span data-stu-id="3f54d-188">ADAM</span></span>



| <span data-ttu-id="3f54d-189">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-189">Entry</span></span> | <span data-ttu-id="3f54d-190">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="3f54d-191">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f54d-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="3f54d-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="3f54d-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f54d-193">System-Only</span></span>            | <span data-ttu-id="3f54d-194">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-194">False</span></span>                                 |
| <span data-ttu-id="3f54d-195">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f54d-195">Is-Single-Valued</span></span>       | <span data-ttu-id="3f54d-196">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-196">True</span></span>                                  |
| <span data-ttu-id="3f54d-197">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f54d-197">Is Indexed</span></span>             | <span data-ttu-id="3f54d-198">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-198">False</span></span>                                 |
| <span data-ttu-id="3f54d-199">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f54d-199">In Global Catalog</span></span>      | <span data-ttu-id="3f54d-200">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-200">True</span></span>                                  |
| <span data-ttu-id="3f54d-201">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f54d-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f54d-202">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f54d-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="3f54d-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f54d-203">Range-Lower</span></span>            | <span data-ttu-id="3f54d-204">1</span><span class="sxs-lookup"><span data-stu-id="3f54d-204">1</span></span>                                     |
| <span data-ttu-id="3f54d-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f54d-205">Range-Upper</span></span>            | <span data-ttu-id="3f54d-206">255</span><span class="sxs-lookup"><span data-stu-id="3f54d-206">255</span></span>                                   |
| <span data-ttu-id="3f54d-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-207">Search-Flags</span></span>           | <span data-ttu-id="3f54d-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f54d-208">0x00000000</span></span>                            |
| <span data-ttu-id="3f54d-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-209">System-Flags</span></span>           | <span data-ttu-id="3f54d-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3f54d-210">0x00000012</span></span>                            |
| <span data-ttu-id="3f54d-211">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f54d-211">Classes used in</span></span>        | [<span data-ttu-id="3f54d-212">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3f54d-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3f54d-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3f54d-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3f54d-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-214">Entry</span></span> | <span data-ttu-id="3f54d-215">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f54d-216">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f54d-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f54d-218">System-Only</span></span>            | <span data-ttu-id="3f54d-219">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f54d-220">Is-Single-Valued</span></span>       | <span data-ttu-id="3f54d-221">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f54d-222">Is Indexed</span></span>             | <span data-ttu-id="3f54d-223">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f54d-224">In Global Catalog</span></span>      | <span data-ttu-id="3f54d-225">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f54d-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f54d-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f54d-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3f54d-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f54d-228">Range-Lower</span></span>            | <span data-ttu-id="3f54d-229">1</span><span class="sxs-lookup"><span data-stu-id="3f54d-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="3f54d-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f54d-230">Range-Upper</span></span>            | <span data-ttu-id="3f54d-231">255</span><span class="sxs-lookup"><span data-stu-id="3f54d-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="3f54d-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-232">Search-Flags</span></span>           | <span data-ttu-id="3f54d-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f54d-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-234">System-Flags</span></span>           | <span data-ttu-id="3f54d-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3f54d-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f54d-236">Classes used in</span></span>        | [<span data-ttu-id="3f54d-237">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3f54d-238">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3f54d-239">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3f54d-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3f54d-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f54d-240">Windows Server 2008</span></span>



| <span data-ttu-id="3f54d-241">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-241">Entry</span></span> | <span data-ttu-id="3f54d-242">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f54d-243">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f54d-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f54d-245">System-Only</span></span>            | <span data-ttu-id="3f54d-246">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-247">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f54d-247">Is-Single-Valued</span></span>       | <span data-ttu-id="3f54d-248">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-249">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f54d-249">Is Indexed</span></span>             | <span data-ttu-id="3f54d-250">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-251">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f54d-251">In Global Catalog</span></span>      | <span data-ttu-id="3f54d-252">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-253">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f54d-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f54d-254">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f54d-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3f54d-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f54d-255">Range-Lower</span></span>            | <span data-ttu-id="3f54d-256">1</span><span class="sxs-lookup"><span data-stu-id="3f54d-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="3f54d-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f54d-257">Range-Upper</span></span>            | <span data-ttu-id="3f54d-258">255</span><span class="sxs-lookup"><span data-stu-id="3f54d-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="3f54d-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-259">Search-Flags</span></span>           | <span data-ttu-id="3f54d-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f54d-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-261">System-Flags</span></span>           | <span data-ttu-id="3f54d-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3f54d-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-263">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f54d-263">Classes used in</span></span>        | [<span data-ttu-id="3f54d-264">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3f54d-265">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3f54d-266">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3f54d-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3f54d-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f54d-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3f54d-268">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-268">Entry</span></span> | <span data-ttu-id="3f54d-269">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f54d-270">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f54d-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f54d-272">System-Only</span></span>            | <span data-ttu-id="3f54d-273">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-274">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f54d-274">Is-Single-Valued</span></span>       | <span data-ttu-id="3f54d-275">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-276">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f54d-276">Is Indexed</span></span>             | <span data-ttu-id="3f54d-277">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-278">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f54d-278">In Global Catalog</span></span>      | <span data-ttu-id="3f54d-279">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-280">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f54d-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f54d-281">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f54d-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3f54d-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f54d-282">Range-Lower</span></span>            | <span data-ttu-id="3f54d-283">1</span><span class="sxs-lookup"><span data-stu-id="3f54d-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="3f54d-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f54d-284">Range-Upper</span></span>            | <span data-ttu-id="3f54d-285">255</span><span class="sxs-lookup"><span data-stu-id="3f54d-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="3f54d-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-286">Search-Flags</span></span>           | <span data-ttu-id="3f54d-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f54d-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-288">System-Flags</span></span>           | <span data-ttu-id="3f54d-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3f54d-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f54d-290">Classes used in</span></span>        | [<span data-ttu-id="3f54d-291">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3f54d-292">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3f54d-293">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3f54d-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3f54d-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f54d-294">Windows Server 2012</span></span>



| <span data-ttu-id="3f54d-295">Entrada</span><span class="sxs-lookup"><span data-stu-id="3f54d-295">Entry</span></span> | <span data-ttu-id="3f54d-296">Valor</span><span class="sxs-lookup"><span data-stu-id="3f54d-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f54d-297">ID do link</span><span class="sxs-lookup"><span data-stu-id="3f54d-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3f54d-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="3f54d-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="3f54d-299">System-Only</span></span>            | <span data-ttu-id="3f54d-300">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-301">É de valor único</span><span class="sxs-lookup"><span data-stu-id="3f54d-301">Is-Single-Valued</span></span>       | <span data-ttu-id="3f54d-302">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-303">É indexado</span><span class="sxs-lookup"><span data-stu-id="3f54d-303">Is Indexed</span></span>             | <span data-ttu-id="3f54d-304">Falso</span><span class="sxs-lookup"><span data-stu-id="3f54d-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="3f54d-305">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="3f54d-305">In Global Catalog</span></span>      | <span data-ttu-id="3f54d-306">True</span><span class="sxs-lookup"><span data-stu-id="3f54d-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="3f54d-307">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="3f54d-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="3f54d-308">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="3f54d-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="3f54d-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3f54d-309">Range-Lower</span></span>            | <span data-ttu-id="3f54d-310">1</span><span class="sxs-lookup"><span data-stu-id="3f54d-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="3f54d-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3f54d-311">Range-Upper</span></span>            | <span data-ttu-id="3f54d-312">255</span><span class="sxs-lookup"><span data-stu-id="3f54d-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="3f54d-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-313">Search-Flags</span></span>           | <span data-ttu-id="3f54d-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3f54d-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3f54d-315">System-Flags</span></span>           | <span data-ttu-id="3f54d-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="3f54d-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="3f54d-317">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="3f54d-317">Classes used in</span></span>        | [<span data-ttu-id="3f54d-318">**Nó DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="3f54d-319">**Zona DNS**</span><span class="sxs-lookup"><span data-stu-id="3f54d-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="3f54d-320">**Controlador**</span><span class="sxs-lookup"><span data-stu-id="3f54d-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 





