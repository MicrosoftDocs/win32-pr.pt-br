---
title: Given-Name atributo
description: Contém o nome fornecido (nome) do usuário.
ms.assetid: acffe751-9911-4e80-8a26-351a21a6385e
ms.tgt_platform: multiple
keywords:
- Esquema de Given-Name do atributo AD
- Esquema de AD do atributo especificado
topic_type:
- apiref
api_name:
- Given-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76ab181c6aaf03c2a497be1718df789bfddc6b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825246"
---
# <a name="given-name-attribute"></a><span data-ttu-id="0c97e-105">Given-Name atributo</span><span class="sxs-lookup"><span data-stu-id="0c97e-105">Given-Name attribute</span></span>

<span data-ttu-id="0c97e-106">Contém o nome fornecido (nome) do usuário.</span><span class="sxs-lookup"><span data-stu-id="0c97e-106">Contains the given name (first name) of the user.</span></span>



| <span data-ttu-id="0c97e-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c97e-107">Entry</span></span> | <span data-ttu-id="0c97e-108">Valor</span><span class="sxs-lookup"><span data-stu-id="0c97e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0c97e-109">CN</span><span class="sxs-lookup"><span data-stu-id="0c97e-109">CN</span></span>                | <span data-ttu-id="0c97e-110">Given-Name</span><span class="sxs-lookup"><span data-stu-id="0c97e-110">Given-Name</span></span>                                  |
| <span data-ttu-id="0c97e-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="0c97e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0c97e-112">givenName</span><span class="sxs-lookup"><span data-stu-id="0c97e-112">givenName</span></span>                                   |
| <span data-ttu-id="0c97e-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="0c97e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0c97e-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="0c97e-114">Update Privilege</span></span>  | <span data-ttu-id="0c97e-115">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="0c97e-115">Domain administrator or account owner.</span></span>      |
| <span data-ttu-id="0c97e-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="0c97e-116">Update Frequency</span></span>  | <span data-ttu-id="0c97e-117">Quando o registro do usuário é criado.</span><span class="sxs-lookup"><span data-stu-id="0c97e-117">When the user's record is created.</span></span>          |
| <span data-ttu-id="0c97e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0c97e-118">Attribute-Id</span></span>      | <span data-ttu-id="0c97e-119">2.5.4.42</span><span class="sxs-lookup"><span data-stu-id="0c97e-119">2.5.4.42</span></span>                                    |
| <span data-ttu-id="0c97e-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="0c97e-120">System-Id-Guid</span></span>    | <span data-ttu-id="0c97e-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="0c97e-121">f0f8ff8e-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="0c97e-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c97e-122">Syntax</span></span>            | [<span data-ttu-id="0c97e-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="0c97e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0c97e-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="0c97e-124">Implementations</span></span>

-   [<span data-ttu-id="0c97e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0c97e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0c97e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0c97e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0c97e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0c97e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0c97e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0c97e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0c97e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0c97e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0c97e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0c97e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0c97e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c97e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0c97e-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c97e-132">Entry</span></span> | <span data-ttu-id="0c97e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="0c97e-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0c97e-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c97e-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="0c97e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c97e-135">MAPI-Id</span></span>                | <span data-ttu-id="0c97e-136">0x3A06</span><span class="sxs-lookup"><span data-stu-id="0c97e-136">0x3A06</span></span>                                                             |
| <span data-ttu-id="0c97e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c97e-137">System-Only</span></span>            | <span data-ttu-id="0c97e-138">Falso</span><span class="sxs-lookup"><span data-stu-id="0c97e-138">False</span></span>                                                              |
| <span data-ttu-id="0c97e-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c97e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="0c97e-140">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-140">True</span></span>                                                               |
| <span data-ttu-id="0c97e-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c97e-141">Is Indexed</span></span>             | <span data-ttu-id="0c97e-142">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-142">True</span></span>                                                               |
| <span data-ttu-id="0c97e-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c97e-143">In Global Catalog</span></span>      | <span data-ttu-id="0c97e-144">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-144">True</span></span>                                                               |
| <span data-ttu-id="0c97e-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c97e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c97e-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c97e-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="0c97e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c97e-147">Range-Lower</span></span>            | <span data-ttu-id="0c97e-148">1</span><span class="sxs-lookup"><span data-stu-id="0c97e-148">1</span></span>                                                                  |
| <span data-ttu-id="0c97e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c97e-149">Range-Upper</span></span>            | <span data-ttu-id="0c97e-150">64</span><span class="sxs-lookup"><span data-stu-id="0c97e-150">64</span></span>                                                                 |
| <span data-ttu-id="0c97e-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-151">Search-Flags</span></span>           | <span data-ttu-id="0c97e-152">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c97e-152">0x00000005</span></span>                                                         |
| <span data-ttu-id="0c97e-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-153">System-Flags</span></span>           | <span data-ttu-id="0c97e-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c97e-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="0c97e-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c97e-155">Classes used in</span></span>        | [<span data-ttu-id="0c97e-156">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c97e-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0c97e-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0c97e-157">Windows Server 2003</span></span>



| <span data-ttu-id="0c97e-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c97e-158">Entry</span></span> | <span data-ttu-id="0c97e-159">Valor</span><span class="sxs-lookup"><span data-stu-id="0c97e-159">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c97e-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c97e-160">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c97e-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c97e-161">MAPI-Id</span></span>                | <span data-ttu-id="0c97e-162">0x3A06</span><span class="sxs-lookup"><span data-stu-id="0c97e-162">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="0c97e-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c97e-163">System-Only</span></span>            | <span data-ttu-id="0c97e-164">Falso</span><span class="sxs-lookup"><span data-stu-id="0c97e-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c97e-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c97e-165">Is-Single-Valued</span></span>       | <span data-ttu-id="0c97e-166">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-166">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c97e-167">Is Indexed</span></span>             | <span data-ttu-id="0c97e-168">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c97e-169">In Global Catalog</span></span>      | <span data-ttu-id="0c97e-170">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-170">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c97e-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c97e-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c97e-172">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c97e-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c97e-173">Range-Lower</span></span>            | <span data-ttu-id="0c97e-174">1</span><span class="sxs-lookup"><span data-stu-id="0c97e-174">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c97e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c97e-175">Range-Upper</span></span>            | <span data-ttu-id="0c97e-176">64</span><span class="sxs-lookup"><span data-stu-id="0c97e-176">64</span></span>                                                                                                                     |
| <span data-ttu-id="0c97e-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-177">Search-Flags</span></span>           | <span data-ttu-id="0c97e-178">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c97e-178">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-179">System-Flags</span></span>           | <span data-ttu-id="0c97e-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c97e-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c97e-181">Classes used in</span></span>        | [<span data-ttu-id="0c97e-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c97e-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c97e-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c97e-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0c97e-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0c97e-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0c97e-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c97e-185">Entry</span></span> | <span data-ttu-id="0c97e-186">Valor</span><span class="sxs-lookup"><span data-stu-id="0c97e-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c97e-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c97e-187">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c97e-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c97e-188">MAPI-Id</span></span>                | <span data-ttu-id="0c97e-189">0x3A06</span><span class="sxs-lookup"><span data-stu-id="0c97e-189">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="0c97e-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c97e-190">System-Only</span></span>            | <span data-ttu-id="0c97e-191">Falso</span><span class="sxs-lookup"><span data-stu-id="0c97e-191">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c97e-192">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c97e-192">Is-Single-Valued</span></span>       | <span data-ttu-id="0c97e-193">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-193">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-194">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c97e-194">Is Indexed</span></span>             | <span data-ttu-id="0c97e-195">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-195">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-196">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c97e-196">In Global Catalog</span></span>      | <span data-ttu-id="0c97e-197">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-197">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c97e-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c97e-199">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c97e-199">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c97e-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c97e-200">Range-Lower</span></span>            | <span data-ttu-id="0c97e-201">1</span><span class="sxs-lookup"><span data-stu-id="0c97e-201">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c97e-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c97e-202">Range-Upper</span></span>            | <span data-ttu-id="0c97e-203">64</span><span class="sxs-lookup"><span data-stu-id="0c97e-203">64</span></span>                                                                                                                     |
| <span data-ttu-id="0c97e-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-204">Search-Flags</span></span>           | <span data-ttu-id="0c97e-205">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c97e-205">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-206">System-Flags</span></span>           | <span data-ttu-id="0c97e-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c97e-207">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c97e-208">Classes used in</span></span>        | [<span data-ttu-id="0c97e-209">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c97e-209">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c97e-210">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c97e-210">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0c97e-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c97e-211">Windows Server 2008</span></span>



| <span data-ttu-id="0c97e-212">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c97e-212">Entry</span></span> | <span data-ttu-id="0c97e-213">Valor</span><span class="sxs-lookup"><span data-stu-id="0c97e-213">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c97e-214">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c97e-214">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c97e-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c97e-215">MAPI-Id</span></span>                | <span data-ttu-id="0c97e-216">0x3A06</span><span class="sxs-lookup"><span data-stu-id="0c97e-216">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="0c97e-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c97e-217">System-Only</span></span>            | <span data-ttu-id="0c97e-218">Falso</span><span class="sxs-lookup"><span data-stu-id="0c97e-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c97e-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c97e-219">Is-Single-Valued</span></span>       | <span data-ttu-id="0c97e-220">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c97e-221">Is Indexed</span></span>             | <span data-ttu-id="0c97e-222">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-222">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c97e-223">In Global Catalog</span></span>      | <span data-ttu-id="0c97e-224">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c97e-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c97e-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c97e-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c97e-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c97e-227">Range-Lower</span></span>            | <span data-ttu-id="0c97e-228">1</span><span class="sxs-lookup"><span data-stu-id="0c97e-228">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c97e-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c97e-229">Range-Upper</span></span>            | <span data-ttu-id="0c97e-230">64</span><span class="sxs-lookup"><span data-stu-id="0c97e-230">64</span></span>                                                                                                                     |
| <span data-ttu-id="0c97e-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-231">Search-Flags</span></span>           | <span data-ttu-id="0c97e-232">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c97e-232">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-233">System-Flags</span></span>           | <span data-ttu-id="0c97e-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c97e-234">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-235">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c97e-235">Classes used in</span></span>        | [<span data-ttu-id="0c97e-236">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c97e-236">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c97e-237">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c97e-237">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0c97e-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c97e-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0c97e-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c97e-239">Entry</span></span> | <span data-ttu-id="0c97e-240">Valor</span><span class="sxs-lookup"><span data-stu-id="0c97e-240">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c97e-241">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c97e-241">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c97e-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c97e-242">MAPI-Id</span></span>                | <span data-ttu-id="0c97e-243">0x3A06</span><span class="sxs-lookup"><span data-stu-id="0c97e-243">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="0c97e-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c97e-244">System-Only</span></span>            | <span data-ttu-id="0c97e-245">Falso</span><span class="sxs-lookup"><span data-stu-id="0c97e-245">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c97e-246">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c97e-246">Is-Single-Valued</span></span>       | <span data-ttu-id="0c97e-247">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-247">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-248">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c97e-248">Is Indexed</span></span>             | <span data-ttu-id="0c97e-249">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-249">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-250">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c97e-250">In Global Catalog</span></span>      | <span data-ttu-id="0c97e-251">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-251">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c97e-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c97e-253">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c97e-253">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c97e-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c97e-254">Range-Lower</span></span>            | <span data-ttu-id="0c97e-255">1</span><span class="sxs-lookup"><span data-stu-id="0c97e-255">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c97e-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c97e-256">Range-Upper</span></span>            | <span data-ttu-id="0c97e-257">64</span><span class="sxs-lookup"><span data-stu-id="0c97e-257">64</span></span>                                                                                                                     |
| <span data-ttu-id="0c97e-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-258">Search-Flags</span></span>           | <span data-ttu-id="0c97e-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c97e-259">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-260">System-Flags</span></span>           | <span data-ttu-id="0c97e-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c97e-261">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-262">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c97e-262">Classes used in</span></span>        | [<span data-ttu-id="0c97e-263">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c97e-263">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c97e-264">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c97e-264">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0c97e-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c97e-265">Windows Server 2012</span></span>



| <span data-ttu-id="0c97e-266">Entrada</span><span class="sxs-lookup"><span data-stu-id="0c97e-266">Entry</span></span> | <span data-ttu-id="0c97e-267">Valor</span><span class="sxs-lookup"><span data-stu-id="0c97e-267">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c97e-268">ID do link</span><span class="sxs-lookup"><span data-stu-id="0c97e-268">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="0c97e-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0c97e-269">MAPI-Id</span></span>                | <span data-ttu-id="0c97e-270">0x3A06</span><span class="sxs-lookup"><span data-stu-id="0c97e-270">0x3A06</span></span>                                                                                                                 |
| <span data-ttu-id="0c97e-271">System-Only</span><span class="sxs-lookup"><span data-stu-id="0c97e-271">System-Only</span></span>            | <span data-ttu-id="0c97e-272">Falso</span><span class="sxs-lookup"><span data-stu-id="0c97e-272">False</span></span>                                                                                                                  |
| <span data-ttu-id="0c97e-273">É de valor único</span><span class="sxs-lookup"><span data-stu-id="0c97e-273">Is-Single-Valued</span></span>       | <span data-ttu-id="0c97e-274">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-274">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-275">É indexado</span><span class="sxs-lookup"><span data-stu-id="0c97e-275">Is Indexed</span></span>             | <span data-ttu-id="0c97e-276">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-277">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="0c97e-277">In Global Catalog</span></span>      | <span data-ttu-id="0c97e-278">True</span><span class="sxs-lookup"><span data-stu-id="0c97e-278">True</span></span>                                                                                                                   |
| <span data-ttu-id="0c97e-279">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="0c97e-279">NT-Security-Descriptor</span></span> | <span data-ttu-id="0c97e-280">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="0c97e-280">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="0c97e-281">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0c97e-281">Range-Lower</span></span>            | <span data-ttu-id="0c97e-282">1</span><span class="sxs-lookup"><span data-stu-id="0c97e-282">1</span></span>                                                                                                                      |
| <span data-ttu-id="0c97e-283">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0c97e-283">Range-Upper</span></span>            | <span data-ttu-id="0c97e-284">64</span><span class="sxs-lookup"><span data-stu-id="0c97e-284">64</span></span>                                                                                                                     |
| <span data-ttu-id="0c97e-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-285">Search-Flags</span></span>           | <span data-ttu-id="0c97e-286">0x00000005</span><span class="sxs-lookup"><span data-stu-id="0c97e-286">0x00000005</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0c97e-287">System-Flags</span></span>           | <span data-ttu-id="0c97e-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0c97e-288">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="0c97e-289">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="0c97e-289">Classes used in</span></span>        | [<span data-ttu-id="0c97e-290">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="0c97e-290">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="0c97e-291">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="0c97e-291">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





