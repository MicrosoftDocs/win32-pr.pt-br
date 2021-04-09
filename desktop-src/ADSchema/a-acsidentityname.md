---
title: Atributo ACS-Identity-Name
description: Esse atributo contém o DN de um usuário ou uma UO e é a identidade de um usuário ou um grupo de usuários ao qual essa política de QoS se aplica.
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- ACS-Identity-Name-esquema de atributo do AD
- Esquema de AD do atributo aCSIdentityName
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33ef1db92b908ef8474dfb125aca678d3c22d09f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104087173"
---
# <a name="acs-identity-name-attribute"></a><span data-ttu-id="bf7bd-105">Atributo ACS-Identity-Name</span><span class="sxs-lookup"><span data-stu-id="bf7bd-105">ACS-Identity-Name attribute</span></span>

<span data-ttu-id="bf7bd-106">Esse atributo contém o DN de um usuário ou uma UO e é a identidade de um usuário ou um grupo de usuários ao qual essa política de QoS se aplica.</span><span class="sxs-lookup"><span data-stu-id="bf7bd-106">This attribute contains the DN of a user or OU and is the identity of a user or a group of users to which this QoS policy applies.</span></span>



| <span data-ttu-id="bf7bd-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf7bd-107">Entry</span></span> | <span data-ttu-id="bf7bd-108">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bf7bd-109">CN</span><span class="sxs-lookup"><span data-stu-id="bf7bd-109">CN</span></span>                | <span data-ttu-id="bf7bd-110">ACS-Identity-Name</span><span class="sxs-lookup"><span data-stu-id="bf7bd-110">ACS-Identity-Name</span></span>                           |
| <span data-ttu-id="bf7bd-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="bf7bd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bf7bd-112">aCSIdentityName</span><span class="sxs-lookup"><span data-stu-id="bf7bd-112">aCSIdentityName</span></span>                             |
| <span data-ttu-id="bf7bd-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="bf7bd-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="bf7bd-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="bf7bd-114">Update Privilege</span></span>  | <span data-ttu-id="bf7bd-115">Administrador de domínio</span><span class="sxs-lookup"><span data-stu-id="bf7bd-115">Domain administrator</span></span>                        |
| <span data-ttu-id="bf7bd-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="bf7bd-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bf7bd-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bf7bd-117">Attribute-Id</span></span>      | <span data-ttu-id="bf7bd-118">1.2.840.113556.1.4.784</span><span class="sxs-lookup"><span data-stu-id="bf7bd-118">1.2.840.113556.1.4.784</span></span>                      |
| <span data-ttu-id="bf7bd-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="bf7bd-119">System-Id-Guid</span></span>    | <span data-ttu-id="bf7bd-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="bf7bd-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span></span>        |
| <span data-ttu-id="bf7bd-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf7bd-121">Syntax</span></span>            | [<span data-ttu-id="bf7bd-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bf7bd-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="bf7bd-123">Implementations</span></span>

-   [<span data-ttu-id="bf7bd-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bf7bd-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bf7bd-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bf7bd-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bf7bd-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bf7bd-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bf7bd-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf7bd-130">Windows 2000 Server</span></span>



| <span data-ttu-id="bf7bd-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf7bd-131">Entry</span></span> | <span data-ttu-id="bf7bd-132">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bf7bd-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf7bd-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7bd-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7bd-135">System-Only</span></span>            | <span data-ttu-id="bf7bd-136">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-136">False</span></span>                                        |
| <span data-ttu-id="bf7bd-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf7bd-137">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7bd-138">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-138">False</span></span>                                        |
| <span data-ttu-id="bf7bd-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf7bd-139">Is Indexed</span></span>             | <span data-ttu-id="bf7bd-140">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-140">False</span></span>                                        |
| <span data-ttu-id="bf7bd-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf7bd-141">In Global Catalog</span></span>      | <span data-ttu-id="bf7bd-142">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-142">False</span></span>                                        |
| <span data-ttu-id="bf7bd-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7bd-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf7bd-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bf7bd-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7bd-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7bd-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-147">Search-Flags</span></span>           | <span data-ttu-id="bf7bd-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7bd-148">0x00000000</span></span>                                   |
| <span data-ttu-id="bf7bd-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-149">System-Flags</span></span>           | <span data-ttu-id="bf7bd-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7bd-150">0x00000010</span></span>                                   |
| <span data-ttu-id="bf7bd-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf7bd-151">Classes used in</span></span>        | [<span data-ttu-id="bf7bd-152">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bf7bd-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf7bd-153">Windows Server 2003</span></span>



| <span data-ttu-id="bf7bd-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf7bd-154">Entry</span></span> | <span data-ttu-id="bf7bd-155">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bf7bd-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf7bd-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7bd-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7bd-158">System-Only</span></span>            | <span data-ttu-id="bf7bd-159">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-159">False</span></span>                                        |
| <span data-ttu-id="bf7bd-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf7bd-160">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7bd-161">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-161">False</span></span>                                        |
| <span data-ttu-id="bf7bd-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf7bd-162">Is Indexed</span></span>             | <span data-ttu-id="bf7bd-163">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-163">False</span></span>                                        |
| <span data-ttu-id="bf7bd-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf7bd-164">In Global Catalog</span></span>      | <span data-ttu-id="bf7bd-165">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-165">False</span></span>                                        |
| <span data-ttu-id="bf7bd-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7bd-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf7bd-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bf7bd-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7bd-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7bd-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-170">Search-Flags</span></span>           | <span data-ttu-id="bf7bd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7bd-171">0x00000000</span></span>                                   |
| <span data-ttu-id="bf7bd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-172">System-Flags</span></span>           | <span data-ttu-id="bf7bd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7bd-173">0x00000010</span></span>                                   |
| <span data-ttu-id="bf7bd-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf7bd-174">Classes used in</span></span>        | [<span data-ttu-id="bf7bd-175">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bf7bd-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bf7bd-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bf7bd-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf7bd-177">Entry</span></span> | <span data-ttu-id="bf7bd-178">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bf7bd-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf7bd-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7bd-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7bd-181">System-Only</span></span>            | <span data-ttu-id="bf7bd-182">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-182">False</span></span>                                        |
| <span data-ttu-id="bf7bd-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf7bd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7bd-184">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-184">False</span></span>                                        |
| <span data-ttu-id="bf7bd-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf7bd-185">Is Indexed</span></span>             | <span data-ttu-id="bf7bd-186">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-186">False</span></span>                                        |
| <span data-ttu-id="bf7bd-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf7bd-187">In Global Catalog</span></span>      | <span data-ttu-id="bf7bd-188">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-188">False</span></span>                                        |
| <span data-ttu-id="bf7bd-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7bd-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf7bd-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bf7bd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7bd-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7bd-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-193">Search-Flags</span></span>           | <span data-ttu-id="bf7bd-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7bd-194">0x00000000</span></span>                                   |
| <span data-ttu-id="bf7bd-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-195">System-Flags</span></span>           | <span data-ttu-id="bf7bd-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7bd-196">0x00000010</span></span>                                   |
| <span data-ttu-id="bf7bd-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf7bd-197">Classes used in</span></span>        | [<span data-ttu-id="bf7bd-198">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bf7bd-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf7bd-199">Windows Server 2008</span></span>



| <span data-ttu-id="bf7bd-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf7bd-200">Entry</span></span> | <span data-ttu-id="bf7bd-201">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bf7bd-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf7bd-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7bd-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7bd-204">System-Only</span></span>            | <span data-ttu-id="bf7bd-205">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-205">False</span></span>                                        |
| <span data-ttu-id="bf7bd-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf7bd-206">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7bd-207">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-207">False</span></span>                                        |
| <span data-ttu-id="bf7bd-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf7bd-208">Is Indexed</span></span>             | <span data-ttu-id="bf7bd-209">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-209">False</span></span>                                        |
| <span data-ttu-id="bf7bd-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf7bd-210">In Global Catalog</span></span>      | <span data-ttu-id="bf7bd-211">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-211">False</span></span>                                        |
| <span data-ttu-id="bf7bd-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7bd-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf7bd-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bf7bd-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7bd-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7bd-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-216">Search-Flags</span></span>           | <span data-ttu-id="bf7bd-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7bd-217">0x00000000</span></span>                                   |
| <span data-ttu-id="bf7bd-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-218">System-Flags</span></span>           | <span data-ttu-id="bf7bd-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7bd-219">0x00000010</span></span>                                   |
| <span data-ttu-id="bf7bd-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf7bd-220">Classes used in</span></span>        | [<span data-ttu-id="bf7bd-221">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bf7bd-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf7bd-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bf7bd-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf7bd-223">Entry</span></span> | <span data-ttu-id="bf7bd-224">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bf7bd-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf7bd-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7bd-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7bd-227">System-Only</span></span>            | <span data-ttu-id="bf7bd-228">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-228">False</span></span>                                        |
| <span data-ttu-id="bf7bd-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf7bd-229">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7bd-230">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-230">False</span></span>                                        |
| <span data-ttu-id="bf7bd-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf7bd-231">Is Indexed</span></span>             | <span data-ttu-id="bf7bd-232">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-232">False</span></span>                                        |
| <span data-ttu-id="bf7bd-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf7bd-233">In Global Catalog</span></span>      | <span data-ttu-id="bf7bd-234">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-234">False</span></span>                                        |
| <span data-ttu-id="bf7bd-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7bd-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf7bd-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bf7bd-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7bd-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7bd-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-239">Search-Flags</span></span>           | <span data-ttu-id="bf7bd-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7bd-240">0x00000000</span></span>                                   |
| <span data-ttu-id="bf7bd-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-241">System-Flags</span></span>           | <span data-ttu-id="bf7bd-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7bd-242">0x00000010</span></span>                                   |
| <span data-ttu-id="bf7bd-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf7bd-243">Classes used in</span></span>        | [<span data-ttu-id="bf7bd-244">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bf7bd-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf7bd-245">Windows Server 2012</span></span>



| <span data-ttu-id="bf7bd-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="bf7bd-246">Entry</span></span> | <span data-ttu-id="bf7bd-247">Valor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="bf7bd-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="bf7bd-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf7bd-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="bf7bd-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf7bd-250">System-Only</span></span>            | <span data-ttu-id="bf7bd-251">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-251">False</span></span>                                        |
| <span data-ttu-id="bf7bd-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="bf7bd-252">Is-Single-Valued</span></span>       | <span data-ttu-id="bf7bd-253">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-253">False</span></span>                                        |
| <span data-ttu-id="bf7bd-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="bf7bd-254">Is Indexed</span></span>             | <span data-ttu-id="bf7bd-255">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-255">False</span></span>                                        |
| <span data-ttu-id="bf7bd-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="bf7bd-256">In Global Catalog</span></span>      | <span data-ttu-id="bf7bd-257">Falso</span><span class="sxs-lookup"><span data-stu-id="bf7bd-257">False</span></span>                                        |
| <span data-ttu-id="bf7bd-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="bf7bd-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf7bd-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="bf7bd-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="bf7bd-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf7bd-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf7bd-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="bf7bd-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-262">Search-Flags</span></span>           | <span data-ttu-id="bf7bd-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf7bd-263">0x00000000</span></span>                                   |
| <span data-ttu-id="bf7bd-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf7bd-264">System-Flags</span></span>           | <span data-ttu-id="bf7bd-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf7bd-265">0x00000010</span></span>                                   |
| <span data-ttu-id="bf7bd-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="bf7bd-266">Classes used in</span></span>        | [<span data-ttu-id="bf7bd-267">**ACS-política**</span><span class="sxs-lookup"><span data-stu-id="bf7bd-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





