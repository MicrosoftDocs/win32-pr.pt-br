---
title: Atributo Bad-pwd-Count
description: O número de vezes que o usuário tentou fazer logon na conta usando uma senha incorreta.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Atributo AD Bad-pwd-Count
- Esquema de AD do atributo badPwdCount
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086757"
---
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="06e19-105">Atributo Bad-pwd-Count</span><span class="sxs-lookup"><span data-stu-id="06e19-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="06e19-106">O número de vezes que o usuário tentou fazer logon na conta usando uma senha incorreta.</span><span class="sxs-lookup"><span data-stu-id="06e19-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="06e19-107">Um valor de 0 indica que o valor é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="06e19-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="06e19-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-108">Entry</span></span> | <span data-ttu-id="06e19-109">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="06e19-110">CN</span><span class="sxs-lookup"><span data-stu-id="06e19-110">CN</span></span>                | <span data-ttu-id="06e19-111">Má-pwd-Count</span><span class="sxs-lookup"><span data-stu-id="06e19-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="06e19-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="06e19-112">Ldap-Display-Name</span></span> | <span data-ttu-id="06e19-113">badPwdCount</span><span class="sxs-lookup"><span data-stu-id="06e19-113">badPwdCount</span></span>                               |
| <span data-ttu-id="06e19-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="06e19-114">Size</span></span>              | <span data-ttu-id="06e19-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="06e19-115">4 bytes</span></span>                                   |
| <span data-ttu-id="06e19-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="06e19-116">Update Privilege</span></span>  | <span data-ttu-id="06e19-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="06e19-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="06e19-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="06e19-118">Update Frequency</span></span>  | <span data-ttu-id="06e19-119">Cada vez que o usuário insere uma senha inadequada.</span><span class="sxs-lookup"><span data-stu-id="06e19-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="06e19-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-120">Attribute-Id</span></span>      | <span data-ttu-id="06e19-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="06e19-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="06e19-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="06e19-122">System-Id-Guid</span></span>    | <span data-ttu-id="06e19-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="06e19-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="06e19-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e19-124">Syntax</span></span>            | [<span data-ttu-id="06e19-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="06e19-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="06e19-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="06e19-126">Implementations</span></span>

-   [<span data-ttu-id="06e19-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="06e19-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="06e19-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="06e19-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="06e19-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="06e19-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="06e19-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="06e19-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="06e19-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="06e19-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="06e19-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="06e19-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="06e19-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="06e19-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="06e19-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="06e19-134">Windows 2000 Server</span></span>



| <span data-ttu-id="06e19-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-135">Entry</span></span> | <span data-ttu-id="06e19-136">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="06e19-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="06e19-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="06e19-139">System-Only</span></span>            | <span data-ttu-id="06e19-140">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-140">False</span></span>                             |
| <span data-ttu-id="06e19-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06e19-141">Is-Single-Valued</span></span>       | <span data-ttu-id="06e19-142">True</span><span class="sxs-lookup"><span data-stu-id="06e19-142">True</span></span>                              |
| <span data-ttu-id="06e19-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="06e19-143">Is Indexed</span></span>             | <span data-ttu-id="06e19-144">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-144">False</span></span>                             |
| <span data-ttu-id="06e19-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06e19-145">In Global Catalog</span></span>      | <span data-ttu-id="06e19-146">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-146">False</span></span>                             |
| <span data-ttu-id="06e19-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06e19-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="06e19-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06e19-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="06e19-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06e19-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="06e19-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06e19-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="06e19-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-151">Search-Flags</span></span>           | <span data-ttu-id="06e19-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06e19-152">0x00000000</span></span>                        |
| <span data-ttu-id="06e19-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-153">System-Flags</span></span>           | <span data-ttu-id="06e19-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06e19-154">0x00000011</span></span>                        |
| <span data-ttu-id="06e19-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06e19-155">Classes used in</span></span>        | [<span data-ttu-id="06e19-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="06e19-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="06e19-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="06e19-157">Windows Server 2003</span></span>



| <span data-ttu-id="06e19-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-158">Entry</span></span> | <span data-ttu-id="06e19-159">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="06e19-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="06e19-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="06e19-162">System-Only</span></span>            | <span data-ttu-id="06e19-163">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-163">False</span></span>                             |
| <span data-ttu-id="06e19-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06e19-164">Is-Single-Valued</span></span>       | <span data-ttu-id="06e19-165">True</span><span class="sxs-lookup"><span data-stu-id="06e19-165">True</span></span>                              |
| <span data-ttu-id="06e19-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="06e19-166">Is Indexed</span></span>             | <span data-ttu-id="06e19-167">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-167">False</span></span>                             |
| <span data-ttu-id="06e19-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06e19-168">In Global Catalog</span></span>      | <span data-ttu-id="06e19-169">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-169">False</span></span>                             |
| <span data-ttu-id="06e19-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06e19-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="06e19-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06e19-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="06e19-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06e19-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="06e19-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06e19-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="06e19-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-174">Search-Flags</span></span>           | <span data-ttu-id="06e19-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06e19-175">0x00000000</span></span>                        |
| <span data-ttu-id="06e19-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-176">System-Flags</span></span>           | <span data-ttu-id="06e19-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06e19-177">0x00000011</span></span>                        |
| <span data-ttu-id="06e19-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06e19-178">Classes used in</span></span>        | [<span data-ttu-id="06e19-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="06e19-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="06e19-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="06e19-180">ADAM</span></span>



| <span data-ttu-id="06e19-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-181">Entry</span></span> | <span data-ttu-id="06e19-182">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="06e19-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="06e19-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="06e19-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="06e19-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="06e19-185">System-Only</span></span>            | <span data-ttu-id="06e19-186">True</span><span class="sxs-lookup"><span data-stu-id="06e19-186">True</span></span>                                                              |
| <span data-ttu-id="06e19-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06e19-187">Is-Single-Valued</span></span>       | <span data-ttu-id="06e19-188">True</span><span class="sxs-lookup"><span data-stu-id="06e19-188">True</span></span>                                                              |
| <span data-ttu-id="06e19-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="06e19-189">Is Indexed</span></span>             | <span data-ttu-id="06e19-190">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-190">False</span></span>                                                             |
| <span data-ttu-id="06e19-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06e19-191">In Global Catalog</span></span>      | <span data-ttu-id="06e19-192">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-192">False</span></span>                                                             |
| <span data-ttu-id="06e19-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06e19-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="06e19-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06e19-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="06e19-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06e19-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="06e19-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06e19-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="06e19-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-197">Search-Flags</span></span>           | <span data-ttu-id="06e19-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06e19-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="06e19-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-199">System-Flags</span></span>           | <span data-ttu-id="06e19-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06e19-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="06e19-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06e19-201">Classes used in</span></span>        | [<span data-ttu-id="06e19-202">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="06e19-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="06e19-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="06e19-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="06e19-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-204">Entry</span></span> | <span data-ttu-id="06e19-205">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="06e19-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="06e19-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="06e19-208">System-Only</span></span>            | <span data-ttu-id="06e19-209">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-209">False</span></span>                             |
| <span data-ttu-id="06e19-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06e19-210">Is-Single-Valued</span></span>       | <span data-ttu-id="06e19-211">True</span><span class="sxs-lookup"><span data-stu-id="06e19-211">True</span></span>                              |
| <span data-ttu-id="06e19-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="06e19-212">Is Indexed</span></span>             | <span data-ttu-id="06e19-213">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-213">False</span></span>                             |
| <span data-ttu-id="06e19-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06e19-214">In Global Catalog</span></span>      | <span data-ttu-id="06e19-215">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-215">False</span></span>                             |
| <span data-ttu-id="06e19-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06e19-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="06e19-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06e19-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="06e19-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06e19-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="06e19-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06e19-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="06e19-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-220">Search-Flags</span></span>           | <span data-ttu-id="06e19-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06e19-221">0x00000000</span></span>                        |
| <span data-ttu-id="06e19-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-222">System-Flags</span></span>           | <span data-ttu-id="06e19-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06e19-223">0x00000011</span></span>                        |
| <span data-ttu-id="06e19-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06e19-224">Classes used in</span></span>        | [<span data-ttu-id="06e19-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="06e19-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="06e19-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06e19-226">Windows Server 2008</span></span>



| <span data-ttu-id="06e19-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-227">Entry</span></span> | <span data-ttu-id="06e19-228">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="06e19-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="06e19-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="06e19-231">System-Only</span></span>            | <span data-ttu-id="06e19-232">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-232">False</span></span>                             |
| <span data-ttu-id="06e19-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06e19-233">Is-Single-Valued</span></span>       | <span data-ttu-id="06e19-234">True</span><span class="sxs-lookup"><span data-stu-id="06e19-234">True</span></span>                              |
| <span data-ttu-id="06e19-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="06e19-235">Is Indexed</span></span>             | <span data-ttu-id="06e19-236">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-236">False</span></span>                             |
| <span data-ttu-id="06e19-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06e19-237">In Global Catalog</span></span>      | <span data-ttu-id="06e19-238">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-238">False</span></span>                             |
| <span data-ttu-id="06e19-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06e19-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="06e19-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06e19-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="06e19-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06e19-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="06e19-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06e19-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="06e19-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-243">Search-Flags</span></span>           | <span data-ttu-id="06e19-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06e19-244">0x00000000</span></span>                        |
| <span data-ttu-id="06e19-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-245">System-Flags</span></span>           | <span data-ttu-id="06e19-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06e19-246">0x00000011</span></span>                        |
| <span data-ttu-id="06e19-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06e19-247">Classes used in</span></span>        | [<span data-ttu-id="06e19-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="06e19-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="06e19-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06e19-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="06e19-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-250">Entry</span></span> | <span data-ttu-id="06e19-251">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="06e19-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="06e19-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="06e19-254">System-Only</span></span>            | <span data-ttu-id="06e19-255">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-255">False</span></span>                             |
| <span data-ttu-id="06e19-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06e19-256">Is-Single-Valued</span></span>       | <span data-ttu-id="06e19-257">True</span><span class="sxs-lookup"><span data-stu-id="06e19-257">True</span></span>                              |
| <span data-ttu-id="06e19-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="06e19-258">Is Indexed</span></span>             | <span data-ttu-id="06e19-259">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-259">False</span></span>                             |
| <span data-ttu-id="06e19-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06e19-260">In Global Catalog</span></span>      | <span data-ttu-id="06e19-261">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-261">False</span></span>                             |
| <span data-ttu-id="06e19-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06e19-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="06e19-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06e19-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="06e19-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06e19-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="06e19-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06e19-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="06e19-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-266">Search-Flags</span></span>           | <span data-ttu-id="06e19-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06e19-267">0x00000000</span></span>                        |
| <span data-ttu-id="06e19-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-268">System-Flags</span></span>           | <span data-ttu-id="06e19-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06e19-269">0x00000011</span></span>                        |
| <span data-ttu-id="06e19-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06e19-270">Classes used in</span></span>        | [<span data-ttu-id="06e19-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="06e19-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="06e19-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06e19-272">Windows Server 2012</span></span>



| <span data-ttu-id="06e19-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="06e19-273">Entry</span></span> | <span data-ttu-id="06e19-274">Valor</span><span class="sxs-lookup"><span data-stu-id="06e19-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="06e19-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="06e19-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="06e19-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="06e19-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="06e19-277">System-Only</span></span>            | <span data-ttu-id="06e19-278">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-278">False</span></span>                             |
| <span data-ttu-id="06e19-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="06e19-279">Is-Single-Valued</span></span>       | <span data-ttu-id="06e19-280">True</span><span class="sxs-lookup"><span data-stu-id="06e19-280">True</span></span>                              |
| <span data-ttu-id="06e19-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="06e19-281">Is Indexed</span></span>             | <span data-ttu-id="06e19-282">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-282">False</span></span>                             |
| <span data-ttu-id="06e19-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="06e19-283">In Global Catalog</span></span>      | <span data-ttu-id="06e19-284">Falso</span><span class="sxs-lookup"><span data-stu-id="06e19-284">False</span></span>                             |
| <span data-ttu-id="06e19-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="06e19-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="06e19-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="06e19-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="06e19-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="06e19-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="06e19-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="06e19-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="06e19-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-289">Search-Flags</span></span>           | <span data-ttu-id="06e19-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="06e19-290">0x00000000</span></span>                        |
| <span data-ttu-id="06e19-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="06e19-291">System-Flags</span></span>           | <span data-ttu-id="06e19-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="06e19-292">0x00000011</span></span>                        |
| <span data-ttu-id="06e19-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="06e19-293">Classes used in</span></span>        | [<span data-ttu-id="06e19-294">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="06e19-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="06e19-295">Comentários</span><span class="sxs-lookup"><span data-stu-id="06e19-295">Remarks</span></span>

<span data-ttu-id="06e19-296">Esse atributo não é replicado e é mantido separadamente em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="06e19-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="06e19-297">Esse atributo é redefinido em um controlador de domínio específico quando o usuário faz logon com êxito no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="06e19-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 





