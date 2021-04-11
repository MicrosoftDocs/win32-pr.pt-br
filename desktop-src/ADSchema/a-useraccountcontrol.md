---
title: Atributo de controle de conta de usuário
description: Sinalizadores que controlam o comportamento da conta de usuário.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo de controle de conta de usuário
- Esquema do AD do atributo userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086977"
---
# <a name="user-account-control-attribute"></a><span data-ttu-id="27c1d-105">Atributo de controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="27c1d-105">User-Account-Control attribute</span></span>

<span data-ttu-id="27c1d-106">Sinalizadores que controlam o comportamento da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="27c1d-106">Flags that control the behavior of the user account.</span></span>



| <span data-ttu-id="27c1d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="27c1d-107">Entry</span></span> | <span data-ttu-id="27c1d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="27c1d-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="27c1d-109">CN</span><span class="sxs-lookup"><span data-stu-id="27c1d-109">CN</span></span>                | <span data-ttu-id="27c1d-110">Controle de conta de usuário</span><span class="sxs-lookup"><span data-stu-id="27c1d-110">User-Account-Control</span></span>                  |
| <span data-ttu-id="27c1d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="27c1d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="27c1d-112">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="27c1d-112">userAccountControl</span></span>                    |
| <span data-ttu-id="27c1d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="27c1d-113">Size</span></span>              | <span data-ttu-id="27c1d-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="27c1d-114">4 bytes.</span></span>                              |
| <span data-ttu-id="27c1d-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="27c1d-115">Update Privilege</span></span>  | <span data-ttu-id="27c1d-116">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="27c1d-116">This value is set by the system.</span></span>      |
| <span data-ttu-id="27c1d-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="27c1d-117">Update Frequency</span></span>  | <span data-ttu-id="27c1d-118">Cada vez que a política de conta é alterada.</span><span class="sxs-lookup"><span data-stu-id="27c1d-118">Each time the account policy changes.</span></span> |
| <span data-ttu-id="27c1d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27c1d-119">Attribute-Id</span></span>      | <span data-ttu-id="27c1d-120">1.2.840.113556.1.4.8</span><span class="sxs-lookup"><span data-stu-id="27c1d-120">1.2.840.113556.1.4.8</span></span>                  |
| <span data-ttu-id="27c1d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="27c1d-121">System-Id-Guid</span></span>    | <span data-ttu-id="27c1d-122">bf967a68-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="27c1d-122">bf967a68-0de6-11d0-a285-00aa003049e2</span></span>  |
| <span data-ttu-id="27c1d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="27c1d-123">Syntax</span></span>            | [<span data-ttu-id="27c1d-124">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="27c1d-124">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="27c1d-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="27c1d-125">Implementations</span></span>

-   [<span data-ttu-id="27c1d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="27c1d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="27c1d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27c1d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27c1d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27c1d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27c1d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27c1d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27c1d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27c1d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27c1d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27c1d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="27c1d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27c1d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="27c1d-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="27c1d-133">Entry</span></span> | <span data-ttu-id="27c1d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="27c1d-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27c1d-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="27c1d-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27c1d-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="27c1d-137">System-Only</span></span>            | <span data-ttu-id="27c1d-138">Falso</span><span class="sxs-lookup"><span data-stu-id="27c1d-138">False</span></span>                             |
| <span data-ttu-id="27c1d-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27c1d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="27c1d-140">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-140">True</span></span>                              |
| <span data-ttu-id="27c1d-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="27c1d-141">Is Indexed</span></span>             | <span data-ttu-id="27c1d-142">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-142">True</span></span>                              |
| <span data-ttu-id="27c1d-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27c1d-143">In Global Catalog</span></span>      | <span data-ttu-id="27c1d-144">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-144">True</span></span>                              |
| <span data-ttu-id="27c1d-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27c1d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="27c1d-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27c1d-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27c1d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27c1d-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27c1d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27c1d-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27c1d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-149">Search-Flags</span></span>           | <span data-ttu-id="27c1d-150">0x00000019</span><span class="sxs-lookup"><span data-stu-id="27c1d-150">0x00000019</span></span>                        |
| <span data-ttu-id="27c1d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-151">System-Flags</span></span>           | <span data-ttu-id="27c1d-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="27c1d-152">0x00000012</span></span>                        |
| <span data-ttu-id="27c1d-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27c1d-153">Classes used in</span></span>        | [<span data-ttu-id="27c1d-154">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="27c1d-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="27c1d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27c1d-155">Windows Server 2003</span></span>



| <span data-ttu-id="27c1d-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="27c1d-156">Entry</span></span> | <span data-ttu-id="27c1d-157">Valor</span><span class="sxs-lookup"><span data-stu-id="27c1d-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27c1d-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="27c1d-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27c1d-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="27c1d-160">System-Only</span></span>            | <span data-ttu-id="27c1d-161">Falso</span><span class="sxs-lookup"><span data-stu-id="27c1d-161">False</span></span>                             |
| <span data-ttu-id="27c1d-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27c1d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="27c1d-163">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-163">True</span></span>                              |
| <span data-ttu-id="27c1d-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="27c1d-164">Is Indexed</span></span>             | <span data-ttu-id="27c1d-165">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-165">True</span></span>                              |
| <span data-ttu-id="27c1d-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27c1d-166">In Global Catalog</span></span>      | <span data-ttu-id="27c1d-167">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-167">True</span></span>                              |
| <span data-ttu-id="27c1d-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27c1d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="27c1d-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27c1d-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27c1d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27c1d-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27c1d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27c1d-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27c1d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-172">Search-Flags</span></span>           | <span data-ttu-id="27c1d-173">0x00000019</span><span class="sxs-lookup"><span data-stu-id="27c1d-173">0x00000019</span></span>                        |
| <span data-ttu-id="27c1d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-174">System-Flags</span></span>           | <span data-ttu-id="27c1d-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="27c1d-175">0x00000012</span></span>                        |
| <span data-ttu-id="27c1d-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27c1d-176">Classes used in</span></span>        | [<span data-ttu-id="27c1d-177">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="27c1d-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27c1d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27c1d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27c1d-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="27c1d-179">Entry</span></span> | <span data-ttu-id="27c1d-180">Valor</span><span class="sxs-lookup"><span data-stu-id="27c1d-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27c1d-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="27c1d-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27c1d-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="27c1d-183">System-Only</span></span>            | <span data-ttu-id="27c1d-184">Falso</span><span class="sxs-lookup"><span data-stu-id="27c1d-184">False</span></span>                             |
| <span data-ttu-id="27c1d-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27c1d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="27c1d-186">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-186">True</span></span>                              |
| <span data-ttu-id="27c1d-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="27c1d-187">Is Indexed</span></span>             | <span data-ttu-id="27c1d-188">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-188">True</span></span>                              |
| <span data-ttu-id="27c1d-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27c1d-189">In Global Catalog</span></span>      | <span data-ttu-id="27c1d-190">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-190">True</span></span>                              |
| <span data-ttu-id="27c1d-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27c1d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="27c1d-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27c1d-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27c1d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27c1d-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27c1d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27c1d-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27c1d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-195">Search-Flags</span></span>           | <span data-ttu-id="27c1d-196">0x00000019</span><span class="sxs-lookup"><span data-stu-id="27c1d-196">0x00000019</span></span>                        |
| <span data-ttu-id="27c1d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-197">System-Flags</span></span>           | <span data-ttu-id="27c1d-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="27c1d-198">0x00000012</span></span>                        |
| <span data-ttu-id="27c1d-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27c1d-199">Classes used in</span></span>        | [<span data-ttu-id="27c1d-200">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="27c1d-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27c1d-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27c1d-201">Windows Server 2008</span></span>



| <span data-ttu-id="27c1d-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="27c1d-202">Entry</span></span> | <span data-ttu-id="27c1d-203">Valor</span><span class="sxs-lookup"><span data-stu-id="27c1d-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27c1d-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="27c1d-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27c1d-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="27c1d-206">System-Only</span></span>            | <span data-ttu-id="27c1d-207">Falso</span><span class="sxs-lookup"><span data-stu-id="27c1d-207">False</span></span>                             |
| <span data-ttu-id="27c1d-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27c1d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="27c1d-209">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-209">True</span></span>                              |
| <span data-ttu-id="27c1d-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="27c1d-210">Is Indexed</span></span>             | <span data-ttu-id="27c1d-211">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-211">True</span></span>                              |
| <span data-ttu-id="27c1d-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27c1d-212">In Global Catalog</span></span>      | <span data-ttu-id="27c1d-213">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-213">True</span></span>                              |
| <span data-ttu-id="27c1d-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27c1d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="27c1d-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27c1d-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27c1d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27c1d-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27c1d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27c1d-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27c1d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-218">Search-Flags</span></span>           | <span data-ttu-id="27c1d-219">0x00000019</span><span class="sxs-lookup"><span data-stu-id="27c1d-219">0x00000019</span></span>                        |
| <span data-ttu-id="27c1d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-220">System-Flags</span></span>           | <span data-ttu-id="27c1d-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="27c1d-221">0x00000012</span></span>                        |
| <span data-ttu-id="27c1d-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27c1d-222">Classes used in</span></span>        | [<span data-ttu-id="27c1d-223">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="27c1d-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27c1d-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27c1d-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27c1d-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="27c1d-225">Entry</span></span> | <span data-ttu-id="27c1d-226">Valor</span><span class="sxs-lookup"><span data-stu-id="27c1d-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27c1d-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="27c1d-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27c1d-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="27c1d-229">System-Only</span></span>            | <span data-ttu-id="27c1d-230">Falso</span><span class="sxs-lookup"><span data-stu-id="27c1d-230">False</span></span>                             |
| <span data-ttu-id="27c1d-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27c1d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="27c1d-232">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-232">True</span></span>                              |
| <span data-ttu-id="27c1d-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="27c1d-233">Is Indexed</span></span>             | <span data-ttu-id="27c1d-234">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-234">True</span></span>                              |
| <span data-ttu-id="27c1d-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27c1d-235">In Global Catalog</span></span>      | <span data-ttu-id="27c1d-236">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-236">True</span></span>                              |
| <span data-ttu-id="27c1d-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27c1d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="27c1d-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27c1d-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27c1d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27c1d-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27c1d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27c1d-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27c1d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-241">Search-Flags</span></span>           | <span data-ttu-id="27c1d-242">0x00000019</span><span class="sxs-lookup"><span data-stu-id="27c1d-242">0x00000019</span></span>                        |
| <span data-ttu-id="27c1d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-243">System-Flags</span></span>           | <span data-ttu-id="27c1d-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="27c1d-244">0x00000012</span></span>                        |
| <span data-ttu-id="27c1d-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27c1d-245">Classes used in</span></span>        | [<span data-ttu-id="27c1d-246">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="27c1d-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27c1d-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27c1d-247">Windows Server 2012</span></span>



| <span data-ttu-id="27c1d-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="27c1d-248">Entry</span></span> | <span data-ttu-id="27c1d-249">Valor</span><span class="sxs-lookup"><span data-stu-id="27c1d-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="27c1d-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="27c1d-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27c1d-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="27c1d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="27c1d-252">System-Only</span></span>            | <span data-ttu-id="27c1d-253">Falso</span><span class="sxs-lookup"><span data-stu-id="27c1d-253">False</span></span>                             |
| <span data-ttu-id="27c1d-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="27c1d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="27c1d-255">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-255">True</span></span>                              |
| <span data-ttu-id="27c1d-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="27c1d-256">Is Indexed</span></span>             | <span data-ttu-id="27c1d-257">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-257">True</span></span>                              |
| <span data-ttu-id="27c1d-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="27c1d-258">In Global Catalog</span></span>      | <span data-ttu-id="27c1d-259">True</span><span class="sxs-lookup"><span data-stu-id="27c1d-259">True</span></span>                              |
| <span data-ttu-id="27c1d-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="27c1d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="27c1d-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="27c1d-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="27c1d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27c1d-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="27c1d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27c1d-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="27c1d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-264">Search-Flags</span></span>           | <span data-ttu-id="27c1d-265">0x00000019</span><span class="sxs-lookup"><span data-stu-id="27c1d-265">0x00000019</span></span>                        |
| <span data-ttu-id="27c1d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27c1d-266">System-Flags</span></span>           | <span data-ttu-id="27c1d-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="27c1d-267">0x00000012</span></span>                        |
| <span data-ttu-id="27c1d-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="27c1d-268">Classes used in</span></span>        | [<span data-ttu-id="27c1d-269">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="27c1d-269">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="27c1d-270">Comentários</span><span class="sxs-lookup"><span data-stu-id="27c1d-270">Remarks</span></span>

<span data-ttu-id="27c1d-271">Esse valor de atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="27c1d-271">This attribute value can be zero or a combination of one or more of the following values.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="27c1d-272">Valor hexadecimal</span><span class="sxs-lookup"><span data-stu-id="27c1d-272">Hexadecimal value</span></span></th>
<th><span data-ttu-id="27c1d-273">Identificador (definido em IADs. h)</span><span class="sxs-lookup"><span data-stu-id="27c1d-273">Identifier (defined in iads.h)</span></span></th>
<th><span data-ttu-id="27c1d-274">Descrição</span><span class="sxs-lookup"><span data-stu-id="27c1d-274">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27c1d-275">0x00000001</span><span class="sxs-lookup"><span data-stu-id="27c1d-275">0x00000001</span></span></td>
<td><span data-ttu-id="27c1d-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-277">O script de logon é executado.</span><span class="sxs-lookup"><span data-stu-id="27c1d-277">The logon script is executed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-278">0x00000002</span><span class="sxs-lookup"><span data-stu-id="27c1d-278">0x00000002</span></span></td>
<td><span data-ttu-id="27c1d-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-280">A conta de usuário está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="27c1d-280">The user account is disabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-281">0x00000008</span><span class="sxs-lookup"><span data-stu-id="27c1d-281">0x00000008</span></span></td>
<td><span data-ttu-id="27c1d-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-283">O diretório base é necessário.</span><span class="sxs-lookup"><span data-stu-id="27c1d-283">The home directory is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27c1d-284">0x00000010</span></span></td>
<td><span data-ttu-id="27c1d-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-286">A conta está bloqueada no momento.</span><span class="sxs-lookup"><span data-stu-id="27c1d-286">The account is currently locked out.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-287">0x00000020</span><span class="sxs-lookup"><span data-stu-id="27c1d-287">0x00000020</span></span></td>
<td><span data-ttu-id="27c1d-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-289">Nenhuma senha é necessária.</span><span class="sxs-lookup"><span data-stu-id="27c1d-289">No password is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-290">0x00000040</span><span class="sxs-lookup"><span data-stu-id="27c1d-290">0x00000040</span></span></td>
<td><span data-ttu-id="27c1d-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-292">O usuário não pode alterar a senha.</span><span class="sxs-lookup"><span data-stu-id="27c1d-292">The user cannot change the password.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="27c1d-293">Você não pode atribuir as configurações de permissão de PASSWD_CANT_CHANGE modificando diretamente o atributo UserAccountControl.</span><span class="sxs-lookup"><span data-stu-id="27c1d-293">You cannot assign the permission settings of PASSWD_CANT_CHANGE by directly modifying the UserAccountControl attribute.</span></span> <span data-ttu-id="27c1d-294">Para obter mais informações e um exemplo de código que mostra como impedir que um usuário altere a senha, consulte o <a href="/windows/desktop/ADSI/user-cannot-change-password">usuário não pode alterar a senha</a>.</span><span class="sxs-lookup"><span data-stu-id="27c1d-294">For more information and a code example that shows how to prevent a user from changing the password, see <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="27c1d-295">:</span><span class="sxs-lookup"><span data-stu-id="27c1d-295">:</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-296">0x00000080</span><span class="sxs-lookup"><span data-stu-id="27c1d-296">0x00000080</span></span></td>
<td><span data-ttu-id="27c1d-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-298">O usuário pode enviar uma senha criptografada.</span><span class="sxs-lookup"><span data-stu-id="27c1d-298">The user can send an encrypted password.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-299">0x00000100</span><span class="sxs-lookup"><span data-stu-id="27c1d-299">0x00000100</span></span></td>
<td><span data-ttu-id="27c1d-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-301">Essa é uma conta para usuários cuja conta primária está em outro domínio.</span><span class="sxs-lookup"><span data-stu-id="27c1d-301">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="27c1d-302">Essa conta fornece acesso de usuário a esse domínio, mas não a qualquer domínio que confie nesse domínio.</span><span class="sxs-lookup"><span data-stu-id="27c1d-302">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="27c1d-303">Também conhecido como uma conta de usuário local.</span><span class="sxs-lookup"><span data-stu-id="27c1d-303">Also known as a local user account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-304">0x00000200</span><span class="sxs-lookup"><span data-stu-id="27c1d-304">0x00000200</span></span></td>
<td><span data-ttu-id="27c1d-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-306">Esse é um tipo de conta padrão que representa um usuário típico.</span><span class="sxs-lookup"><span data-stu-id="27c1d-306">This is a default account type that represents a typical user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-307">0x00000800</span><span class="sxs-lookup"><span data-stu-id="27c1d-307">0x00000800</span></span></td>
<td><span data-ttu-id="27c1d-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-309">Essa é uma permissão para confiar na conta de um domínio do sistema que confia em outros domínios.</span><span class="sxs-lookup"><span data-stu-id="27c1d-309">This is a permit to trust account for a system domain that trusts other domains.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-310">0x00001000</span><span class="sxs-lookup"><span data-stu-id="27c1d-310">0x00001000</span></span></td>
<td><span data-ttu-id="27c1d-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-312">Esta é uma conta de computador para um computador que seja membro deste domínio.</span><span class="sxs-lookup"><span data-stu-id="27c1d-312">This is a computer account for a computer that is a member of this domain.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-313">0x00002000</span><span class="sxs-lookup"><span data-stu-id="27c1d-313">0x00002000</span></span></td>
<td><span data-ttu-id="27c1d-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-315">Essa é uma conta de computador para um controlador de domínio de backup do sistema que é membro deste domínio.</span><span class="sxs-lookup"><span data-stu-id="27c1d-315">This is a computer account for a system backup domain controller that is a member of this domain.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-316">0x00004000</span><span class="sxs-lookup"><span data-stu-id="27c1d-316">0x00004000</span></span></td>
<td><span data-ttu-id="27c1d-317">N/D</span><span class="sxs-lookup"><span data-stu-id="27c1d-317">N/A</span></span></td>
<td><span data-ttu-id="27c1d-318">Não usado.</span><span class="sxs-lookup"><span data-stu-id="27c1d-318">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-319">0x00008000</span><span class="sxs-lookup"><span data-stu-id="27c1d-319">0x00008000</span></span></td>
<td><span data-ttu-id="27c1d-320">N/D</span><span class="sxs-lookup"><span data-stu-id="27c1d-320">N/A</span></span></td>
<td><span data-ttu-id="27c1d-321">Não usado.</span><span class="sxs-lookup"><span data-stu-id="27c1d-321">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-322">0x00010000</span><span class="sxs-lookup"><span data-stu-id="27c1d-322">0x00010000</span></span></td>
<td><span data-ttu-id="27c1d-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-324">A senha desta conta nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="27c1d-324">The password for this account will never expire.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-325">0x00020000</span><span class="sxs-lookup"><span data-stu-id="27c1d-325">0x00020000</span></span></td>
<td><span data-ttu-id="27c1d-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-327">Esta é uma conta de logon MNS.</span><span class="sxs-lookup"><span data-stu-id="27c1d-327">This is an MNS logon account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-328">0x00040000</span><span class="sxs-lookup"><span data-stu-id="27c1d-328">0x00040000</span></span></td>
<td><span data-ttu-id="27c1d-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-330">O usuário deve fazer logon usando um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="27c1d-330">The user must log on using a smart card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-331">0x00080000</span><span class="sxs-lookup"><span data-stu-id="27c1d-331">0x00080000</span></span></td>
<td><span data-ttu-id="27c1d-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-333">A conta de serviço (conta de usuário ou de computador), sob a qual um serviço é executado, é confiável para delegação de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="27c1d-333">The service account (user or computer account), under which a service runs, is trusted for Kerberos delegation.</span></span> <span data-ttu-id="27c1d-334">Qualquer serviço desse tipo pode representar um cliente solicitando o serviço.</span><span class="sxs-lookup"><span data-stu-id="27c1d-334">Any such service can impersonate a client requesting the service.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-335">0x00100000</span><span class="sxs-lookup"><span data-stu-id="27c1d-335">0x00100000</span></span></td>
<td><span data-ttu-id="27c1d-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-337">O contexto de segurança do usuário não será delegado a um serviço, mesmo que a conta de serviço esteja definida como confiável para delegação de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="27c1d-337">The security context of the user will not be delegated to a service even if the service account is set as trusted for Kerberos delegation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-338">0x00200000</span><span class="sxs-lookup"><span data-stu-id="27c1d-338">0x00200000</span></span></td>
<td><span data-ttu-id="27c1d-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-340">Restrinja esta entidade para usar apenas os tipos de criptografia DES (padrão de criptografia de dados) para chaves.</span><span class="sxs-lookup"><span data-stu-id="27c1d-340">Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-341">0x00400000</span><span class="sxs-lookup"><span data-stu-id="27c1d-341">0x00400000</span></span></td>
<td><span data-ttu-id="27c1d-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-343">Essa conta não requer pré-autenticação Kerberos para logon.</span><span class="sxs-lookup"><span data-stu-id="27c1d-343">This account does not require Kerberos pre-authentication for logon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27c1d-344">0x00800000</span><span class="sxs-lookup"><span data-stu-id="27c1d-344">0x00800000</span></span></td>
<td><span data-ttu-id="27c1d-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-346">A senha do usuário expirou.</span><span class="sxs-lookup"><span data-stu-id="27c1d-346">The user password has expired.</span></span> <span data-ttu-id="27c1d-347">Esse sinalizador é criado pelo sistema usando dados do atributo <a href="a-pwdlastset.md"><strong>pwd-Last-Set</strong></a> e da política de domínio.</span><span class="sxs-lookup"><span data-stu-id="27c1d-347">This flag is created by the system using data from the <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> attribute and the domain policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27c1d-348">0x01000000</span><span class="sxs-lookup"><span data-stu-id="27c1d-348">0x01000000</span></span></td>
<td><span data-ttu-id="27c1d-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="27c1d-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="27c1d-350">A conta está habilitada para delegação.</span><span class="sxs-lookup"><span data-stu-id="27c1d-350">The account is enabled for delegation.</span></span> <span data-ttu-id="27c1d-351">Esta é uma configuração sensível à segurança; as contas com essa opção habilitada devem ser estritamente controladas.</span><span class="sxs-lookup"><span data-stu-id="27c1d-351">This is a security-sensitive setting; accounts with this option enabled should be strictly controlled.</span></span> <span data-ttu-id="27c1d-352">Essa configuração permite que um serviço em execução na conta assuma uma identidade do cliente e se autentique como esse usuário para outros servidores remotos na rede.</span><span class="sxs-lookup"><span data-stu-id="27c1d-352">This setting enables a service running under the account to assume a client identity and authenticate as that user to other remote servers on the network.</span></span></td>
</tr>
</tbody>
</table>



 

