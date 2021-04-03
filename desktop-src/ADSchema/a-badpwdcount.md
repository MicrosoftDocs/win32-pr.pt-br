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
# <a name="bad-pwd-count-attribute"></a><span data-ttu-id="6922d-105">Atributo Bad-pwd-Count</span><span class="sxs-lookup"><span data-stu-id="6922d-105">Bad-Pwd-Count attribute</span></span>

<span data-ttu-id="6922d-106">O número de vezes que o usuário tentou fazer logon na conta usando uma senha incorreta.</span><span class="sxs-lookup"><span data-stu-id="6922d-106">The number of times the user tried to log on to the account using an incorrect password.</span></span> <span data-ttu-id="6922d-107">Um valor de 0 indica que o valor é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6922d-107">A value of 0 indicates that the value is unknown.</span></span>



| <span data-ttu-id="6922d-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-108">Entry</span></span> | <span data-ttu-id="6922d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="6922d-110">CN</span><span class="sxs-lookup"><span data-stu-id="6922d-110">CN</span></span>                | <span data-ttu-id="6922d-111">Má-pwd-Count</span><span class="sxs-lookup"><span data-stu-id="6922d-111">Bad-Pwd-Count</span></span>                             |
| <span data-ttu-id="6922d-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6922d-112">Ldap-Display-Name</span></span> | <span data-ttu-id="6922d-113">badPwdCount</span><span class="sxs-lookup"><span data-stu-id="6922d-113">badPwdCount</span></span>                               |
| <span data-ttu-id="6922d-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6922d-114">Size</span></span>              | <span data-ttu-id="6922d-115">4 bytes</span><span class="sxs-lookup"><span data-stu-id="6922d-115">4 bytes</span></span>                                   |
| <span data-ttu-id="6922d-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6922d-116">Update Privilege</span></span>  | <span data-ttu-id="6922d-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="6922d-117">This value is set by the system.</span></span>          |
| <span data-ttu-id="6922d-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6922d-118">Update Frequency</span></span>  | <span data-ttu-id="6922d-119">Cada vez que o usuário insere uma senha inadequada.</span><span class="sxs-lookup"><span data-stu-id="6922d-119">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="6922d-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-120">Attribute-Id</span></span>      | <span data-ttu-id="6922d-121">1.2.840.113556.1.4.12</span><span class="sxs-lookup"><span data-stu-id="6922d-121">1.2.840.113556.1.4.12</span></span>                     |
| <span data-ttu-id="6922d-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6922d-122">System-Id-Guid</span></span>    | <span data-ttu-id="6922d-123">bf96792e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6922d-123">bf96792e-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="6922d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="6922d-124">Syntax</span></span>            | [<span data-ttu-id="6922d-125">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="6922d-125">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="6922d-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="6922d-126">Implementations</span></span>

-   [<span data-ttu-id="6922d-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6922d-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6922d-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6922d-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6922d-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6922d-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6922d-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6922d-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6922d-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6922d-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6922d-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6922d-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6922d-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6922d-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6922d-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6922d-134">Windows 2000 Server</span></span>



| <span data-ttu-id="6922d-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-135">Entry</span></span> | <span data-ttu-id="6922d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6922d-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="6922d-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="6922d-139">System-Only</span></span>            | <span data-ttu-id="6922d-140">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-140">False</span></span>                             |
| <span data-ttu-id="6922d-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6922d-141">Is-Single-Valued</span></span>       | <span data-ttu-id="6922d-142">True</span><span class="sxs-lookup"><span data-stu-id="6922d-142">True</span></span>                              |
| <span data-ttu-id="6922d-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="6922d-143">Is Indexed</span></span>             | <span data-ttu-id="6922d-144">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-144">False</span></span>                             |
| <span data-ttu-id="6922d-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6922d-145">In Global Catalog</span></span>      | <span data-ttu-id="6922d-146">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-146">False</span></span>                             |
| <span data-ttu-id="6922d-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6922d-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="6922d-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6922d-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6922d-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6922d-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6922d-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6922d-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6922d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-151">Search-Flags</span></span>           | <span data-ttu-id="6922d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6922d-152">0x00000000</span></span>                        |
| <span data-ttu-id="6922d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-153">System-Flags</span></span>           | <span data-ttu-id="6922d-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6922d-154">0x00000011</span></span>                        |
| <span data-ttu-id="6922d-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6922d-155">Classes used in</span></span>        | [<span data-ttu-id="6922d-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="6922d-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6922d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6922d-157">Windows Server 2003</span></span>



| <span data-ttu-id="6922d-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-158">Entry</span></span> | <span data-ttu-id="6922d-159">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6922d-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="6922d-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6922d-162">System-Only</span></span>            | <span data-ttu-id="6922d-163">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-163">False</span></span>                             |
| <span data-ttu-id="6922d-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6922d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6922d-165">True</span><span class="sxs-lookup"><span data-stu-id="6922d-165">True</span></span>                              |
| <span data-ttu-id="6922d-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="6922d-166">Is Indexed</span></span>             | <span data-ttu-id="6922d-167">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-167">False</span></span>                             |
| <span data-ttu-id="6922d-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6922d-168">In Global Catalog</span></span>      | <span data-ttu-id="6922d-169">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-169">False</span></span>                             |
| <span data-ttu-id="6922d-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6922d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6922d-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6922d-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6922d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6922d-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6922d-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6922d-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6922d-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-174">Search-Flags</span></span>           | <span data-ttu-id="6922d-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6922d-175">0x00000000</span></span>                        |
| <span data-ttu-id="6922d-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-176">System-Flags</span></span>           | <span data-ttu-id="6922d-177">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6922d-177">0x00000011</span></span>                        |
| <span data-ttu-id="6922d-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6922d-178">Classes used in</span></span>        | [<span data-ttu-id="6922d-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="6922d-179">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6922d-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="6922d-180">ADAM</span></span>



| <span data-ttu-id="6922d-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-181">Entry</span></span> | <span data-ttu-id="6922d-182">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="6922d-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="6922d-183">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6922d-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-184">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="6922d-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="6922d-185">System-Only</span></span>            | <span data-ttu-id="6922d-186">True</span><span class="sxs-lookup"><span data-stu-id="6922d-186">True</span></span>                                                              |
| <span data-ttu-id="6922d-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6922d-187">Is-Single-Valued</span></span>       | <span data-ttu-id="6922d-188">True</span><span class="sxs-lookup"><span data-stu-id="6922d-188">True</span></span>                                                              |
| <span data-ttu-id="6922d-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="6922d-189">Is Indexed</span></span>             | <span data-ttu-id="6922d-190">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-190">False</span></span>                                                             |
| <span data-ttu-id="6922d-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6922d-191">In Global Catalog</span></span>      | <span data-ttu-id="6922d-192">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-192">False</span></span>                                                             |
| <span data-ttu-id="6922d-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6922d-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="6922d-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6922d-194">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="6922d-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6922d-195">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="6922d-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6922d-196">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="6922d-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-197">Search-Flags</span></span>           | <span data-ttu-id="6922d-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6922d-198">0x00000000</span></span>                                                        |
| <span data-ttu-id="6922d-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-199">System-Flags</span></span>           | <span data-ttu-id="6922d-200">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6922d-200">0x00000011</span></span>                                                        |
| <span data-ttu-id="6922d-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6922d-201">Classes used in</span></span>        | [<span data-ttu-id="6922d-202">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="6922d-202">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6922d-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6922d-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6922d-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-204">Entry</span></span> | <span data-ttu-id="6922d-205">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6922d-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="6922d-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="6922d-208">System-Only</span></span>            | <span data-ttu-id="6922d-209">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-209">False</span></span>                             |
| <span data-ttu-id="6922d-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6922d-210">Is-Single-Valued</span></span>       | <span data-ttu-id="6922d-211">True</span><span class="sxs-lookup"><span data-stu-id="6922d-211">True</span></span>                              |
| <span data-ttu-id="6922d-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="6922d-212">Is Indexed</span></span>             | <span data-ttu-id="6922d-213">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-213">False</span></span>                             |
| <span data-ttu-id="6922d-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6922d-214">In Global Catalog</span></span>      | <span data-ttu-id="6922d-215">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-215">False</span></span>                             |
| <span data-ttu-id="6922d-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6922d-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="6922d-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6922d-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6922d-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6922d-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6922d-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6922d-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6922d-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-220">Search-Flags</span></span>           | <span data-ttu-id="6922d-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6922d-221">0x00000000</span></span>                        |
| <span data-ttu-id="6922d-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-222">System-Flags</span></span>           | <span data-ttu-id="6922d-223">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6922d-223">0x00000011</span></span>                        |
| <span data-ttu-id="6922d-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6922d-224">Classes used in</span></span>        | [<span data-ttu-id="6922d-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="6922d-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6922d-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6922d-226">Windows Server 2008</span></span>



| <span data-ttu-id="6922d-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-227">Entry</span></span> | <span data-ttu-id="6922d-228">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6922d-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="6922d-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="6922d-231">System-Only</span></span>            | <span data-ttu-id="6922d-232">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-232">False</span></span>                             |
| <span data-ttu-id="6922d-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6922d-233">Is-Single-Valued</span></span>       | <span data-ttu-id="6922d-234">True</span><span class="sxs-lookup"><span data-stu-id="6922d-234">True</span></span>                              |
| <span data-ttu-id="6922d-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="6922d-235">Is Indexed</span></span>             | <span data-ttu-id="6922d-236">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-236">False</span></span>                             |
| <span data-ttu-id="6922d-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6922d-237">In Global Catalog</span></span>      | <span data-ttu-id="6922d-238">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-238">False</span></span>                             |
| <span data-ttu-id="6922d-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6922d-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="6922d-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6922d-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6922d-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6922d-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6922d-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6922d-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6922d-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-243">Search-Flags</span></span>           | <span data-ttu-id="6922d-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6922d-244">0x00000000</span></span>                        |
| <span data-ttu-id="6922d-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-245">System-Flags</span></span>           | <span data-ttu-id="6922d-246">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6922d-246">0x00000011</span></span>                        |
| <span data-ttu-id="6922d-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6922d-247">Classes used in</span></span>        | [<span data-ttu-id="6922d-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="6922d-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6922d-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6922d-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6922d-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-250">Entry</span></span> | <span data-ttu-id="6922d-251">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6922d-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="6922d-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="6922d-254">System-Only</span></span>            | <span data-ttu-id="6922d-255">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-255">False</span></span>                             |
| <span data-ttu-id="6922d-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6922d-256">Is-Single-Valued</span></span>       | <span data-ttu-id="6922d-257">True</span><span class="sxs-lookup"><span data-stu-id="6922d-257">True</span></span>                              |
| <span data-ttu-id="6922d-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="6922d-258">Is Indexed</span></span>             | <span data-ttu-id="6922d-259">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-259">False</span></span>                             |
| <span data-ttu-id="6922d-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6922d-260">In Global Catalog</span></span>      | <span data-ttu-id="6922d-261">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-261">False</span></span>                             |
| <span data-ttu-id="6922d-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6922d-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="6922d-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6922d-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6922d-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6922d-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6922d-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6922d-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6922d-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-266">Search-Flags</span></span>           | <span data-ttu-id="6922d-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6922d-267">0x00000000</span></span>                        |
| <span data-ttu-id="6922d-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-268">System-Flags</span></span>           | <span data-ttu-id="6922d-269">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6922d-269">0x00000011</span></span>                        |
| <span data-ttu-id="6922d-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6922d-270">Classes used in</span></span>        | [<span data-ttu-id="6922d-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="6922d-271">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6922d-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6922d-272">Windows Server 2012</span></span>



| <span data-ttu-id="6922d-273">Entrada</span><span class="sxs-lookup"><span data-stu-id="6922d-273">Entry</span></span> | <span data-ttu-id="6922d-274">Valor</span><span class="sxs-lookup"><span data-stu-id="6922d-274">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="6922d-275">ID do link</span><span class="sxs-lookup"><span data-stu-id="6922d-275">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6922d-276">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="6922d-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="6922d-277">System-Only</span></span>            | <span data-ttu-id="6922d-278">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-278">False</span></span>                             |
| <span data-ttu-id="6922d-279">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6922d-279">Is-Single-Valued</span></span>       | <span data-ttu-id="6922d-280">True</span><span class="sxs-lookup"><span data-stu-id="6922d-280">True</span></span>                              |
| <span data-ttu-id="6922d-281">É indexado</span><span class="sxs-lookup"><span data-stu-id="6922d-281">Is Indexed</span></span>             | <span data-ttu-id="6922d-282">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-282">False</span></span>                             |
| <span data-ttu-id="6922d-283">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6922d-283">In Global Catalog</span></span>      | <span data-ttu-id="6922d-284">Falso</span><span class="sxs-lookup"><span data-stu-id="6922d-284">False</span></span>                             |
| <span data-ttu-id="6922d-285">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6922d-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="6922d-286">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6922d-286">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="6922d-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6922d-287">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="6922d-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6922d-288">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="6922d-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-289">Search-Flags</span></span>           | <span data-ttu-id="6922d-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6922d-290">0x00000000</span></span>                        |
| <span data-ttu-id="6922d-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6922d-291">System-Flags</span></span>           | <span data-ttu-id="6922d-292">0x00000011</span><span class="sxs-lookup"><span data-stu-id="6922d-292">0x00000011</span></span>                        |
| <span data-ttu-id="6922d-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6922d-293">Classes used in</span></span>        | [<span data-ttu-id="6922d-294">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="6922d-294">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6922d-295">Comentários</span><span class="sxs-lookup"><span data-stu-id="6922d-295">Remarks</span></span>

<span data-ttu-id="6922d-296">Esse atributo não é replicado e é mantido separadamente em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="6922d-296">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span>

<span data-ttu-id="6922d-297">Esse atributo é redefinido em um controlador de domínio específico quando o usuário faz logon com êxito no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="6922d-297">This attribute is reset on a specific domain controller when the user successfully logs onto that domain controller.</span></span>

 

 





