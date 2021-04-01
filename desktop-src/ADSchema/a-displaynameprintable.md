---
title: Nome de exibição-atributo imprimível
description: O nome de exibição imprimível de um objeto.
ms.assetid: e8e5ff25-66dd-4c74-9571-9ec765d6d1af
ms.tgt_platform: multiple
keywords:
- Display-Name-imprimível atributo AD Schema
- Esquema de AD do atributo displayNamePrintable
topic_type:
- apiref
api_name:
- Display-Name-Printable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eff05c2279f026e3a94b707b522509b4801ff27
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825407"
---
# <a name="display-name-printable-attribute"></a><span data-ttu-id="5bf22-105">Nome de exibição-atributo imprimível</span><span class="sxs-lookup"><span data-stu-id="5bf22-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="5bf22-106">O nome de exibição imprimível de um objeto.</span><span class="sxs-lookup"><span data-stu-id="5bf22-106">The printable display name for an object.</span></span> <span data-ttu-id="5bf22-107">O nome de exibição imprimível geralmente é a combinação do nome do usuário, do início do meio e do sobrenome.</span><span class="sxs-lookup"><span data-stu-id="5bf22-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="5bf22-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bf22-108">Entry</span></span> | <span data-ttu-id="5bf22-109">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf22-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="5bf22-110">CN</span><span class="sxs-lookup"><span data-stu-id="5bf22-110">CN</span></span>                | <span data-ttu-id="5bf22-111">Nome de exibição-imprimível</span><span class="sxs-lookup"><span data-stu-id="5bf22-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="5bf22-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="5bf22-112">Ldap-Display-Name</span></span> | <span data-ttu-id="5bf22-113">displayNamePrintable</span><span class="sxs-lookup"><span data-stu-id="5bf22-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="5bf22-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="5bf22-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="5bf22-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="5bf22-115">Update Privilege</span></span>  | <span data-ttu-id="5bf22-116">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="5bf22-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="5bf22-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="5bf22-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="5bf22-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5bf22-118">Attribute-Id</span></span>      | <span data-ttu-id="5bf22-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="5bf22-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="5bf22-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="5bf22-120">System-Id-Guid</span></span>    | <span data-ttu-id="5bf22-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5bf22-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="5bf22-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bf22-122">Syntax</span></span>            | [<span data-ttu-id="5bf22-123">**Cadeia de caracteres (IA5)**</span><span class="sxs-lookup"><span data-stu-id="5bf22-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="5bf22-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="5bf22-124">Implementations</span></span>

-   [<span data-ttu-id="5bf22-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5bf22-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5bf22-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5bf22-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5bf22-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5bf22-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5bf22-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5bf22-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5bf22-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5bf22-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5bf22-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5bf22-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5bf22-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bf22-131">Windows 2000 Server</span></span>



| <span data-ttu-id="5bf22-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bf22-132">Entry</span></span> | <span data-ttu-id="5bf22-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf22-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5bf22-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bf22-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5bf22-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bf22-135">MAPI-Id</span></span>                | <span data-ttu-id="5bf22-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="5bf22-136">0x39FF</span></span>                          |
| <span data-ttu-id="5bf22-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bf22-137">System-Only</span></span>            | <span data-ttu-id="5bf22-138">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-138">False</span></span>                           |
| <span data-ttu-id="5bf22-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bf22-139">Is-Single-Valued</span></span>       | <span data-ttu-id="5bf22-140">True</span><span class="sxs-lookup"><span data-stu-id="5bf22-140">True</span></span>                            |
| <span data-ttu-id="5bf22-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bf22-141">Is Indexed</span></span>             | <span data-ttu-id="5bf22-142">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-142">False</span></span>                           |
| <span data-ttu-id="5bf22-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bf22-143">In Global Catalog</span></span>      | <span data-ttu-id="5bf22-144">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-144">False</span></span>                           |
| <span data-ttu-id="5bf22-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bf22-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bf22-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bf22-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5bf22-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bf22-147">Range-Lower</span></span>            | <span data-ttu-id="5bf22-148">1</span><span class="sxs-lookup"><span data-stu-id="5bf22-148">1</span></span>                               |
| <span data-ttu-id="5bf22-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bf22-149">Range-Upper</span></span>            | <span data-ttu-id="5bf22-150">256</span><span class="sxs-lookup"><span data-stu-id="5bf22-150">256</span></span>                             |
| <span data-ttu-id="5bf22-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-151">Search-Flags</span></span>           | <span data-ttu-id="5bf22-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bf22-152">0x00000000</span></span>                      |
| <span data-ttu-id="5bf22-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-153">System-Flags</span></span>           | <span data-ttu-id="5bf22-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bf22-154">0x00000010</span></span>                      |
| <span data-ttu-id="5bf22-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bf22-155">Classes used in</span></span>        | [<span data-ttu-id="5bf22-156">**Início**</span><span class="sxs-lookup"><span data-stu-id="5bf22-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5bf22-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5bf22-157">Windows Server 2003</span></span>



| <span data-ttu-id="5bf22-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bf22-158">Entry</span></span> | <span data-ttu-id="5bf22-159">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf22-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5bf22-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bf22-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5bf22-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bf22-161">MAPI-Id</span></span>                | <span data-ttu-id="5bf22-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="5bf22-162">0x39FF</span></span>                          |
| <span data-ttu-id="5bf22-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bf22-163">System-Only</span></span>            | <span data-ttu-id="5bf22-164">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-164">False</span></span>                           |
| <span data-ttu-id="5bf22-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bf22-165">Is-Single-Valued</span></span>       | <span data-ttu-id="5bf22-166">True</span><span class="sxs-lookup"><span data-stu-id="5bf22-166">True</span></span>                            |
| <span data-ttu-id="5bf22-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bf22-167">Is Indexed</span></span>             | <span data-ttu-id="5bf22-168">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-168">False</span></span>                           |
| <span data-ttu-id="5bf22-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bf22-169">In Global Catalog</span></span>      | <span data-ttu-id="5bf22-170">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-170">False</span></span>                           |
| <span data-ttu-id="5bf22-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bf22-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bf22-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bf22-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5bf22-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bf22-173">Range-Lower</span></span>            | <span data-ttu-id="5bf22-174">1</span><span class="sxs-lookup"><span data-stu-id="5bf22-174">1</span></span>                               |
| <span data-ttu-id="5bf22-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bf22-175">Range-Upper</span></span>            | <span data-ttu-id="5bf22-176">256</span><span class="sxs-lookup"><span data-stu-id="5bf22-176">256</span></span>                             |
| <span data-ttu-id="5bf22-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-177">Search-Flags</span></span>           | <span data-ttu-id="5bf22-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bf22-178">0x00000000</span></span>                      |
| <span data-ttu-id="5bf22-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-179">System-Flags</span></span>           | <span data-ttu-id="5bf22-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bf22-180">0x00000010</span></span>                      |
| <span data-ttu-id="5bf22-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bf22-181">Classes used in</span></span>        | [<span data-ttu-id="5bf22-182">**Início**</span><span class="sxs-lookup"><span data-stu-id="5bf22-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5bf22-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5bf22-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5bf22-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bf22-184">Entry</span></span> | <span data-ttu-id="5bf22-185">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf22-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5bf22-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bf22-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5bf22-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bf22-187">MAPI-Id</span></span>                | <span data-ttu-id="5bf22-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="5bf22-188">0x39FF</span></span>                          |
| <span data-ttu-id="5bf22-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bf22-189">System-Only</span></span>            | <span data-ttu-id="5bf22-190">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-190">False</span></span>                           |
| <span data-ttu-id="5bf22-191">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bf22-191">Is-Single-Valued</span></span>       | <span data-ttu-id="5bf22-192">True</span><span class="sxs-lookup"><span data-stu-id="5bf22-192">True</span></span>                            |
| <span data-ttu-id="5bf22-193">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bf22-193">Is Indexed</span></span>             | <span data-ttu-id="5bf22-194">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-194">False</span></span>                           |
| <span data-ttu-id="5bf22-195">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bf22-195">In Global Catalog</span></span>      | <span data-ttu-id="5bf22-196">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-196">False</span></span>                           |
| <span data-ttu-id="5bf22-197">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bf22-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bf22-198">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bf22-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5bf22-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bf22-199">Range-Lower</span></span>            | <span data-ttu-id="5bf22-200">1</span><span class="sxs-lookup"><span data-stu-id="5bf22-200">1</span></span>                               |
| <span data-ttu-id="5bf22-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bf22-201">Range-Upper</span></span>            | <span data-ttu-id="5bf22-202">256</span><span class="sxs-lookup"><span data-stu-id="5bf22-202">256</span></span>                             |
| <span data-ttu-id="5bf22-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-203">Search-Flags</span></span>           | <span data-ttu-id="5bf22-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bf22-204">0x00000000</span></span>                      |
| <span data-ttu-id="5bf22-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-205">System-Flags</span></span>           | <span data-ttu-id="5bf22-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bf22-206">0x00000010</span></span>                      |
| <span data-ttu-id="5bf22-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bf22-207">Classes used in</span></span>        | [<span data-ttu-id="5bf22-208">**Início**</span><span class="sxs-lookup"><span data-stu-id="5bf22-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5bf22-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bf22-209">Windows Server 2008</span></span>



| <span data-ttu-id="5bf22-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bf22-210">Entry</span></span> | <span data-ttu-id="5bf22-211">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf22-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5bf22-212">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bf22-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5bf22-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bf22-213">MAPI-Id</span></span>                | <span data-ttu-id="5bf22-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="5bf22-214">0x39FF</span></span>                          |
| <span data-ttu-id="5bf22-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bf22-215">System-Only</span></span>            | <span data-ttu-id="5bf22-216">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-216">False</span></span>                           |
| <span data-ttu-id="5bf22-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bf22-217">Is-Single-Valued</span></span>       | <span data-ttu-id="5bf22-218">True</span><span class="sxs-lookup"><span data-stu-id="5bf22-218">True</span></span>                            |
| <span data-ttu-id="5bf22-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bf22-219">Is Indexed</span></span>             | <span data-ttu-id="5bf22-220">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-220">False</span></span>                           |
| <span data-ttu-id="5bf22-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bf22-221">In Global Catalog</span></span>      | <span data-ttu-id="5bf22-222">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-222">False</span></span>                           |
| <span data-ttu-id="5bf22-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bf22-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bf22-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bf22-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5bf22-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bf22-225">Range-Lower</span></span>            | <span data-ttu-id="5bf22-226">1</span><span class="sxs-lookup"><span data-stu-id="5bf22-226">1</span></span>                               |
| <span data-ttu-id="5bf22-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bf22-227">Range-Upper</span></span>            | <span data-ttu-id="5bf22-228">256</span><span class="sxs-lookup"><span data-stu-id="5bf22-228">256</span></span>                             |
| <span data-ttu-id="5bf22-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-229">Search-Flags</span></span>           | <span data-ttu-id="5bf22-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bf22-230">0x00000000</span></span>                      |
| <span data-ttu-id="5bf22-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-231">System-Flags</span></span>           | <span data-ttu-id="5bf22-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bf22-232">0x00000010</span></span>                      |
| <span data-ttu-id="5bf22-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bf22-233">Classes used in</span></span>        | [<span data-ttu-id="5bf22-234">**Início**</span><span class="sxs-lookup"><span data-stu-id="5bf22-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5bf22-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5bf22-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5bf22-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bf22-236">Entry</span></span> | <span data-ttu-id="5bf22-237">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf22-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5bf22-238">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bf22-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5bf22-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bf22-239">MAPI-Id</span></span>                | <span data-ttu-id="5bf22-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="5bf22-240">0x39FF</span></span>                          |
| <span data-ttu-id="5bf22-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bf22-241">System-Only</span></span>            | <span data-ttu-id="5bf22-242">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-242">False</span></span>                           |
| <span data-ttu-id="5bf22-243">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bf22-243">Is-Single-Valued</span></span>       | <span data-ttu-id="5bf22-244">True</span><span class="sxs-lookup"><span data-stu-id="5bf22-244">True</span></span>                            |
| <span data-ttu-id="5bf22-245">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bf22-245">Is Indexed</span></span>             | <span data-ttu-id="5bf22-246">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-246">False</span></span>                           |
| <span data-ttu-id="5bf22-247">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bf22-247">In Global Catalog</span></span>      | <span data-ttu-id="5bf22-248">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-248">False</span></span>                           |
| <span data-ttu-id="5bf22-249">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bf22-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bf22-250">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bf22-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5bf22-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bf22-251">Range-Lower</span></span>            | <span data-ttu-id="5bf22-252">1</span><span class="sxs-lookup"><span data-stu-id="5bf22-252">1</span></span>                               |
| <span data-ttu-id="5bf22-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bf22-253">Range-Upper</span></span>            | <span data-ttu-id="5bf22-254">256</span><span class="sxs-lookup"><span data-stu-id="5bf22-254">256</span></span>                             |
| <span data-ttu-id="5bf22-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-255">Search-Flags</span></span>           | <span data-ttu-id="5bf22-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bf22-256">0x00000000</span></span>                      |
| <span data-ttu-id="5bf22-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-257">System-Flags</span></span>           | <span data-ttu-id="5bf22-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bf22-258">0x00000010</span></span>                      |
| <span data-ttu-id="5bf22-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bf22-259">Classes used in</span></span>        | [<span data-ttu-id="5bf22-260">**Início**</span><span class="sxs-lookup"><span data-stu-id="5bf22-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5bf22-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5bf22-261">Windows Server 2012</span></span>



| <span data-ttu-id="5bf22-262">Entrada</span><span class="sxs-lookup"><span data-stu-id="5bf22-262">Entry</span></span> | <span data-ttu-id="5bf22-263">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf22-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="5bf22-264">ID do link</span><span class="sxs-lookup"><span data-stu-id="5bf22-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="5bf22-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5bf22-265">MAPI-Id</span></span>                | <span data-ttu-id="5bf22-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="5bf22-266">0x39FF</span></span>                          |
| <span data-ttu-id="5bf22-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="5bf22-267">System-Only</span></span>            | <span data-ttu-id="5bf22-268">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-268">False</span></span>                           |
| <span data-ttu-id="5bf22-269">É de valor único</span><span class="sxs-lookup"><span data-stu-id="5bf22-269">Is-Single-Valued</span></span>       | <span data-ttu-id="5bf22-270">True</span><span class="sxs-lookup"><span data-stu-id="5bf22-270">True</span></span>                            |
| <span data-ttu-id="5bf22-271">É indexado</span><span class="sxs-lookup"><span data-stu-id="5bf22-271">Is Indexed</span></span>             | <span data-ttu-id="5bf22-272">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-272">False</span></span>                           |
| <span data-ttu-id="5bf22-273">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="5bf22-273">In Global Catalog</span></span>      | <span data-ttu-id="5bf22-274">Falso</span><span class="sxs-lookup"><span data-stu-id="5bf22-274">False</span></span>                           |
| <span data-ttu-id="5bf22-275">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="5bf22-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="5bf22-276">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="5bf22-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="5bf22-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5bf22-277">Range-Lower</span></span>            | <span data-ttu-id="5bf22-278">1</span><span class="sxs-lookup"><span data-stu-id="5bf22-278">1</span></span>                               |
| <span data-ttu-id="5bf22-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5bf22-279">Range-Upper</span></span>            | <span data-ttu-id="5bf22-280">256</span><span class="sxs-lookup"><span data-stu-id="5bf22-280">256</span></span>                             |
| <span data-ttu-id="5bf22-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-281">Search-Flags</span></span>           | <span data-ttu-id="5bf22-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5bf22-282">0x00000000</span></span>                      |
| <span data-ttu-id="5bf22-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5bf22-283">System-Flags</span></span>           | <span data-ttu-id="5bf22-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5bf22-284">0x00000010</span></span>                      |
| <span data-ttu-id="5bf22-285">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="5bf22-285">Classes used in</span></span>        | [<span data-ttu-id="5bf22-286">**Início**</span><span class="sxs-lookup"><span data-stu-id="5bf22-286">**Top**</span></span>](c-top.md)<br/> |



 

 





