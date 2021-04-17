---
title: DS-Heuristics atributo
description: Contém configurações globais para toda a floresta.
ms.assetid: d5fd990b-7bbf-4ede-a3af-7f3f7ac959b3
ms.tgt_platform: multiple
keywords:
- Esquema de DS-Heuristics do atributo AD
- Esquema de AD do atributo dSHeuristics
topic_type:
- apiref
api_name:
- DS-Heuristics
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65922b580975ec05877ae33d213ff3a3675ec72f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105811188"
---
# <a name="ds-heuristics-attribute"></a><span data-ttu-id="7bb40-105">DS-Heuristics atributo</span><span class="sxs-lookup"><span data-stu-id="7bb40-105">DS-Heuristics attribute</span></span>

<span data-ttu-id="7bb40-106">Contém configurações globais para toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="7bb40-106">Contains global settings for the entire forest.</span></span>

<span data-ttu-id="7bb40-107">Há informações sobre os bits de exclusão de adminSDholder disponíveis no site de ajuda e suporte da Microsoft em um número de artigo [817433, as permissões delegadas não estão disponíveis e a herança é desabilitada automaticamente](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span><span class="sxs-lookup"><span data-stu-id="7bb40-107">There is information about adminSDholder exclusion bits available on the Microsoft Help and Support website in an article number [817433, Delegated permissions are not available and inheritance is automatically disabled](https://support.microsoft.com/default.aspx?scid=kb;EN-US;817433).</span></span>



| <span data-ttu-id="7bb40-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-108">Entry</span></span> | <span data-ttu-id="7bb40-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="7bb40-110">CN</span><span class="sxs-lookup"><span data-stu-id="7bb40-110">CN</span></span>                | <span data-ttu-id="7bb40-111">DS-Heuristics</span><span class="sxs-lookup"><span data-stu-id="7bb40-111">DS-Heuristics</span></span>                               |
| <span data-ttu-id="7bb40-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="7bb40-112">Ldap-Display-Name</span></span> | <span data-ttu-id="7bb40-113">dSHeuristics</span><span class="sxs-lookup"><span data-stu-id="7bb40-113">dSHeuristics</span></span>                                |
| <span data-ttu-id="7bb40-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="7bb40-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="7bb40-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="7bb40-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="7bb40-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="7bb40-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="7bb40-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-117">Attribute-Id</span></span>      | <span data-ttu-id="7bb40-118">1.2.840.113556.1.2.212</span><span class="sxs-lookup"><span data-stu-id="7bb40-118">1.2.840.113556.1.2.212</span></span>                      |
| <span data-ttu-id="7bb40-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="7bb40-119">System-Id-Guid</span></span>    | <span data-ttu-id="7bb40-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="7bb40-120">f0f8ff86-1191-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="7bb40-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bb40-121">Syntax</span></span>            | [<span data-ttu-id="7bb40-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="7bb40-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="7bb40-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="7bb40-123">Implementations</span></span>

-   [<span data-ttu-id="7bb40-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7bb40-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7bb40-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7bb40-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7bb40-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="7bb40-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="7bb40-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7bb40-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7bb40-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7bb40-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7bb40-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7bb40-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7bb40-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7bb40-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7bb40-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bb40-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7bb40-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-132">Entry</span></span> | <span data-ttu-id="7bb40-133">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-133">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7bb40-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bb40-134">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-135">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bb40-136">System-Only</span></span>            | <span data-ttu-id="7bb40-137">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-137">False</span></span>                                            |
| <span data-ttu-id="7bb40-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bb40-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7bb40-139">True</span><span class="sxs-lookup"><span data-stu-id="7bb40-139">True</span></span>                                             |
| <span data-ttu-id="7bb40-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bb40-140">Is Indexed</span></span>             | <span data-ttu-id="7bb40-141">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-141">False</span></span>                                            |
| <span data-ttu-id="7bb40-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bb40-142">In Global Catalog</span></span>      | <span data-ttu-id="7bb40-143">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-143">False</span></span>                                            |
| <span data-ttu-id="7bb40-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bb40-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bb40-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bb40-145">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7bb40-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bb40-146">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bb40-147">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-148">Search-Flags</span></span>           | <span data-ttu-id="7bb40-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb40-149">0x00000000</span></span>                                       |
| <span data-ttu-id="7bb40-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-150">System-Flags</span></span>           | <span data-ttu-id="7bb40-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bb40-151">0x00000010</span></span>                                       |
| <span data-ttu-id="7bb40-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bb40-152">Classes used in</span></span>        | [<span data-ttu-id="7bb40-153">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="7bb40-153">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7bb40-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7bb40-154">Windows Server 2003</span></span>



| <span data-ttu-id="7bb40-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-155">Entry</span></span> | <span data-ttu-id="7bb40-156">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-156">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7bb40-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bb40-157">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-158">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bb40-159">System-Only</span></span>            | <span data-ttu-id="7bb40-160">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-160">False</span></span>                                            |
| <span data-ttu-id="7bb40-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bb40-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7bb40-162">True</span><span class="sxs-lookup"><span data-stu-id="7bb40-162">True</span></span>                                             |
| <span data-ttu-id="7bb40-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bb40-163">Is Indexed</span></span>             | <span data-ttu-id="7bb40-164">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-164">False</span></span>                                            |
| <span data-ttu-id="7bb40-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bb40-165">In Global Catalog</span></span>      | <span data-ttu-id="7bb40-166">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-166">False</span></span>                                            |
| <span data-ttu-id="7bb40-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bb40-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bb40-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bb40-168">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7bb40-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bb40-169">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bb40-170">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-171">Search-Flags</span></span>           | <span data-ttu-id="7bb40-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb40-172">0x00000000</span></span>                                       |
| <span data-ttu-id="7bb40-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-173">System-Flags</span></span>           | <span data-ttu-id="7bb40-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bb40-174">0x00000010</span></span>                                       |
| <span data-ttu-id="7bb40-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bb40-175">Classes used in</span></span>        | [<span data-ttu-id="7bb40-176">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="7bb40-176">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="7bb40-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="7bb40-177">ADAM</span></span>



| <span data-ttu-id="7bb40-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-178">Entry</span></span> | <span data-ttu-id="7bb40-179">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-179">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7bb40-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bb40-180">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-181">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bb40-182">System-Only</span></span>            | <span data-ttu-id="7bb40-183">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-183">False</span></span>                                            |
| <span data-ttu-id="7bb40-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bb40-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7bb40-185">True</span><span class="sxs-lookup"><span data-stu-id="7bb40-185">True</span></span>                                             |
| <span data-ttu-id="7bb40-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bb40-186">Is Indexed</span></span>             | <span data-ttu-id="7bb40-187">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-187">False</span></span>                                            |
| <span data-ttu-id="7bb40-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bb40-188">In Global Catalog</span></span>      | <span data-ttu-id="7bb40-189">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-189">False</span></span>                                            |
| <span data-ttu-id="7bb40-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bb40-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bb40-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bb40-191">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7bb40-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bb40-192">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bb40-193">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-194">Search-Flags</span></span>           | <span data-ttu-id="7bb40-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb40-195">0x00000000</span></span>                                       |
| <span data-ttu-id="7bb40-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-196">System-Flags</span></span>           | <span data-ttu-id="7bb40-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bb40-197">0x00000010</span></span>                                       |
| <span data-ttu-id="7bb40-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bb40-198">Classes used in</span></span>        | [<span data-ttu-id="7bb40-199">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="7bb40-199">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7bb40-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7bb40-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7bb40-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-201">Entry</span></span> | <span data-ttu-id="7bb40-202">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-202">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7bb40-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bb40-203">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-204">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bb40-205">System-Only</span></span>            | <span data-ttu-id="7bb40-206">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-206">False</span></span>                                            |
| <span data-ttu-id="7bb40-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bb40-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7bb40-208">True</span><span class="sxs-lookup"><span data-stu-id="7bb40-208">True</span></span>                                             |
| <span data-ttu-id="7bb40-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bb40-209">Is Indexed</span></span>             | <span data-ttu-id="7bb40-210">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-210">False</span></span>                                            |
| <span data-ttu-id="7bb40-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bb40-211">In Global Catalog</span></span>      | <span data-ttu-id="7bb40-212">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-212">False</span></span>                                            |
| <span data-ttu-id="7bb40-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bb40-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bb40-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bb40-214">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7bb40-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bb40-215">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bb40-216">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-217">Search-Flags</span></span>           | <span data-ttu-id="7bb40-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb40-218">0x00000000</span></span>                                       |
| <span data-ttu-id="7bb40-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-219">System-Flags</span></span>           | <span data-ttu-id="7bb40-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bb40-220">0x00000010</span></span>                                       |
| <span data-ttu-id="7bb40-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bb40-221">Classes used in</span></span>        | [<span data-ttu-id="7bb40-222">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="7bb40-222">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7bb40-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bb40-223">Windows Server 2008</span></span>



| <span data-ttu-id="7bb40-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-224">Entry</span></span> | <span data-ttu-id="7bb40-225">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-225">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7bb40-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bb40-226">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-227">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bb40-228">System-Only</span></span>            | <span data-ttu-id="7bb40-229">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-229">False</span></span>                                            |
| <span data-ttu-id="7bb40-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bb40-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7bb40-231">True</span><span class="sxs-lookup"><span data-stu-id="7bb40-231">True</span></span>                                             |
| <span data-ttu-id="7bb40-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bb40-232">Is Indexed</span></span>             | <span data-ttu-id="7bb40-233">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-233">False</span></span>                                            |
| <span data-ttu-id="7bb40-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bb40-234">In Global Catalog</span></span>      | <span data-ttu-id="7bb40-235">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-235">False</span></span>                                            |
| <span data-ttu-id="7bb40-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bb40-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bb40-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bb40-237">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7bb40-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bb40-238">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bb40-239">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-240">Search-Flags</span></span>           | <span data-ttu-id="7bb40-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb40-241">0x00000000</span></span>                                       |
| <span data-ttu-id="7bb40-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-242">System-Flags</span></span>           | <span data-ttu-id="7bb40-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bb40-243">0x00000010</span></span>                                       |
| <span data-ttu-id="7bb40-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bb40-244">Classes used in</span></span>        | [<span data-ttu-id="7bb40-245">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="7bb40-245">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7bb40-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7bb40-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7bb40-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-247">Entry</span></span> | <span data-ttu-id="7bb40-248">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-248">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7bb40-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bb40-249">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-250">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bb40-251">System-Only</span></span>            | <span data-ttu-id="7bb40-252">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-252">False</span></span>                                            |
| <span data-ttu-id="7bb40-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bb40-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7bb40-254">True</span><span class="sxs-lookup"><span data-stu-id="7bb40-254">True</span></span>                                             |
| <span data-ttu-id="7bb40-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bb40-255">Is Indexed</span></span>             | <span data-ttu-id="7bb40-256">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-256">False</span></span>                                            |
| <span data-ttu-id="7bb40-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bb40-257">In Global Catalog</span></span>      | <span data-ttu-id="7bb40-258">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-258">False</span></span>                                            |
| <span data-ttu-id="7bb40-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bb40-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bb40-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bb40-260">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7bb40-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bb40-261">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bb40-262">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-263">Search-Flags</span></span>           | <span data-ttu-id="7bb40-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb40-264">0x00000000</span></span>                                       |
| <span data-ttu-id="7bb40-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-265">System-Flags</span></span>           | <span data-ttu-id="7bb40-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bb40-266">0x00000010</span></span>                                       |
| <span data-ttu-id="7bb40-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bb40-267">Classes used in</span></span>        | [<span data-ttu-id="7bb40-268">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="7bb40-268">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7bb40-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bb40-269">Windows Server 2012</span></span>



| <span data-ttu-id="7bb40-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bb40-270">Entry</span></span> | <span data-ttu-id="7bb40-271">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb40-271">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="7bb40-272">ID do link</span><span class="sxs-lookup"><span data-stu-id="7bb40-272">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7bb40-273">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="7bb40-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="7bb40-274">System-Only</span></span>            | <span data-ttu-id="7bb40-275">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-275">False</span></span>                                            |
| <span data-ttu-id="7bb40-276">É de valor único</span><span class="sxs-lookup"><span data-stu-id="7bb40-276">Is-Single-Valued</span></span>       | <span data-ttu-id="7bb40-277">True</span><span class="sxs-lookup"><span data-stu-id="7bb40-277">True</span></span>                                             |
| <span data-ttu-id="7bb40-278">É indexado</span><span class="sxs-lookup"><span data-stu-id="7bb40-278">Is Indexed</span></span>             | <span data-ttu-id="7bb40-279">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-279">False</span></span>                                            |
| <span data-ttu-id="7bb40-280">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="7bb40-280">In Global Catalog</span></span>      | <span data-ttu-id="7bb40-281">Falso</span><span class="sxs-lookup"><span data-stu-id="7bb40-281">False</span></span>                                            |
| <span data-ttu-id="7bb40-282">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="7bb40-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="7bb40-283">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="7bb40-283">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="7bb40-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7bb40-284">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7bb40-285">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="7bb40-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-286">Search-Flags</span></span>           | <span data-ttu-id="7bb40-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7bb40-287">0x00000000</span></span>                                       |
| <span data-ttu-id="7bb40-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7bb40-288">System-Flags</span></span>           | <span data-ttu-id="7bb40-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7bb40-289">0x00000010</span></span>                                       |
| <span data-ttu-id="7bb40-290">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="7bb40-290">Classes used in</span></span>        | [<span data-ttu-id="7bb40-291">**NTDS-serviço**</span><span class="sxs-lookup"><span data-stu-id="7bb40-291">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="7bb40-292">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bb40-292">Remarks</span></span>

<span data-ttu-id="7bb40-293">Cada floresta Active Directory contém um atributo DS-Heuristics que contém configurações para toda a floresta.</span><span class="sxs-lookup"><span data-stu-id="7bb40-293">Each Active Directory forest contains a DS-Heuristics attribute that contains settings for the entire forest.</span></span> <span data-ttu-id="7bb40-294">O atributo DS-Heuristics é um atributo do objeto "CN = serviço de diretório, CN = Windows NT, CN = Services, CN = Configuration <Domain> ".</span><span class="sxs-lookup"><span data-stu-id="7bb40-294">The DS-Heuristics attribute is an attribute of the "CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,<Domain>" object.</span></span>

<span data-ttu-id="7bb40-295">DS-Heuristics é uma cadeia de caracteres Unicode na qual cada caractere contém um valor para uma única configuração de todo o domínio.</span><span class="sxs-lookup"><span data-stu-id="7bb40-295">DS-Heuristics is a Unicode string in which each character contains a value for a single domain-wide setting.</span></span> <span data-ttu-id="7bb40-296">A cadeia de caracteres de DS-Heuristics usa o formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="7bb40-296">The DS-Heuristics string takes the following format.</span></span>

``` syntax
|<1>|<2>|<3>|<4>|<5>|<6>|<7>|<8>|<9>|<10>|<11>|<12>|<13>|<14>|<15>|<16>|<17>|<18>|<19>|<20>|<21>|<22>|<23>|<24>|<25>|
```

<span data-ttu-id="7bb40-297">Para fornecer validação de dados, cada décimo caractere é definido como o número de caractere dividido por dez.</span><span class="sxs-lookup"><span data-stu-id="7bb40-297">To provide data validation, each tenth character is set to the character number divided by ten.</span></span> <span data-ttu-id="7bb40-298">Por exemplo, o décimo caractere é ' 1 '; o caractere de vigésimo é ' 2 ' e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7bb40-298">For example, the tenth character is '1'; the twentieth character is '2', and so on.</span></span>

<span data-ttu-id="7bb40-299">Um caractere que não está definido é considerado um ' 0 '.</span><span class="sxs-lookup"><span data-stu-id="7bb40-299">Any character that is not set is assumed to be a '0'.</span></span> <span data-ttu-id="7bb40-300">Se o atributo DS-Heuristics não for definido, todos os valores serão considerados como ' 0 '.</span><span class="sxs-lookup"><span data-stu-id="7bb40-300">If the DS-Heuristics attribute is not set, all values are assumed to be '0'.</span></span> <span data-ttu-id="7bb40-301">Atualmente, há 25 caracteres sendo usados e não é necessário preencher a cadeia de caracteres para completar todos os 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="7bb40-301">There are currently 25 characters being used and it is not necessary to pad the string to fill all 25 characters.</span></span> <span data-ttu-id="7bb40-302">Por exemplo, se o caractere mais alto que está sendo usado for 7, a cadeia de caracteres "0000002" será aceitável.</span><span class="sxs-lookup"><span data-stu-id="7bb40-302">For example, if the highest character being used is 7, then the string "0000002" is acceptable.</span></span>

<span data-ttu-id="7bb40-303">Para obter detalhes sobre cada caractere, confira [dSHeuristics em \[ MS-ADTS \] Active Directory especificação técnica](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span><span class="sxs-lookup"><span data-stu-id="7bb40-303">For details about each character, see [dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5).</span></span>

### <a name="anr-search-filters"></a><span data-ttu-id="7bb40-304">Filtros de pesquisa ANR</span><span class="sxs-lookup"><span data-stu-id="7bb40-304">ANR Search Filters</span></span>

<span data-ttu-id="7bb40-305">Os caracteres 1, 2 e 4 são usados para modificar o comportamento dos filtros de pesquisa ANR.</span><span class="sxs-lookup"><span data-stu-id="7bb40-305">Characters 1, 2, and 4 are used to modify the behavior of ANR search filters.</span></span> <span data-ttu-id="7bb40-306">Se o caractere 1 estiver definido como ' 1 ', a expansão do filtro ANR para incluir o   -  **sobrenome** de especificado (quando o espaço for encontrado) será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7bb40-306">If character 1 is set to '1', then the expansion of the ANR filter to include **GivenName** - **Surname** (when space is found) is disabled.</span></span> <span data-ttu-id="7bb40-307">Se o caractere 2 estiver definido como ' 1 ', a expansão do filtro ANR para incluir o **sobrenome**  -  **especificado** será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7bb40-307">If character 2 is set to '1', the expansion of the ANR filter to include **Surname** - **GivenName** is disabled.</span></span> <span data-ttu-id="7bb40-308">Se um espaço inserido estiver presente na cadeia de caracteres de pesquisa, a cadeia de caracteres de pesquisa será dividida normalmente em duas cadeias de caracteres, que são comparadas por pares com os atributos **especificado** e **sobrenome** .</span><span class="sxs-lookup"><span data-stu-id="7bb40-308">If an embedded space is present in the search string, the search string will normally be divided into two strings, which are compared pair-wise against the **GivenName** and **Surname** attributes.</span></span> <span data-ttu-id="7bb40-309">Definir os caracteres 1 e 2 para ' 1 ' impedirá que essas correspondências sejam tentadas.</span><span class="sxs-lookup"><span data-stu-id="7bb40-309">Setting characters 1 and 2 to '1' will prevent those matches from being attempted.</span></span> <span data-ttu-id="7bb40-310">Essa correspondência poderá ser desabilitada se o administrador tiver certeza de que a pesquisa por "Jeff Smith" sempre seria fornecida como "Jeff Smith" e não "Smith, Jeff".</span><span class="sxs-lookup"><span data-stu-id="7bb40-310">This matching might be disabled if the administrator is confident that searches for "Jeff Smith" would always be provided as "jeff smith" and not "smith, jeff".</span></span> <span data-ttu-id="7bb40-311">Normalmente, apenas uma ou outra correspondência seria suprimida, de acordo com a Convenção local.</span><span class="sxs-lookup"><span data-stu-id="7bb40-311">Normally only one or the other match would be suppressed, according to local convention.</span></span>

<span data-ttu-id="7bb40-312">Se o caractere 4 estiver definido como ' 1 ', Active Directory executará "resolução de apelido preventivo".</span><span class="sxs-lookup"><span data-stu-id="7bb40-312">If the character 4 is set to '1' then Active Directory will perform "pre-emptive nickname resolution".</span></span> <span data-ttu-id="7bb40-313">Ou seja, se a cadeia de caracteres de pesquisa corresponder exatamente ao apelido de exatamente um objeto no escopo da pesquisa, esse objeto será retornado como resultado da pesquisa e o restante da ANR será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bb40-313">That is, if the search string exactly matches the nickname of exactly one object in the search scope, that one object is returned as the result of the search, and the rest of ANR is skipped.</span></span> <span data-ttu-id="7bb40-314">Observe que, embora o restante da pesquisa ANR esteja disponível por meio de LDAP, a resolução de apelidos preventivos (também conhecida como "ajuste de apelido") está disponível somente por meio de MAPI.</span><span class="sxs-lookup"><span data-stu-id="7bb40-314">Note that while the rest of ANR searching is available through LDAP, pre-emptive nickname resolution (also known as "nickname snap") is available only through MAPI.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bb40-315">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bb40-315">See also</span></span>

<dl> <dt>

<span data-ttu-id="7bb40-316">[dSHeuristics em \[ MS-ADTS \] Active Directory especificação técnica](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span><span class="sxs-lookup"><span data-stu-id="7bb40-316">[dSHeuristics in \[MS-ADTS\] Active Directory Technical Specification](/openspecs/windows_protocols/ms-adts/e5899be4-862e-496f-9a38-33950617d2c5)</span></span>
</dt> </dl>

 

