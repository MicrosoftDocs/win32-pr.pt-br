---
title: User-Parameters atributo
description: Parâmetros do usuário.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- Esquema de User-Parameters do atributo AD
- Esquema de AD do atributo userparameters
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c1d593f0a655dea4fa3ddb25753de712ab83cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104500026"
---
# <a name="user-parameters-attribute"></a><span data-ttu-id="77e25-105">User-Parameters atributo</span><span class="sxs-lookup"><span data-stu-id="77e25-105">User-Parameters attribute</span></span>

<span data-ttu-id="77e25-106">Parâmetros do usuário.</span><span class="sxs-lookup"><span data-stu-id="77e25-106">Parameters of the user.</span></span> <span data-ttu-id="77e25-107">Aponta para uma cadeia de caracteres Unicode que é reservada para uso por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="77e25-107">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="77e25-108">Essa cadeia de caracteres pode ser uma cadeia de caracteres nula ou pode ter qualquer número de caracteres antes do caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="77e25-108">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="77e25-109">Os produtos da Microsoft usam esse membro para armazenar dados de usuário específicos para o programa individual.</span><span class="sxs-lookup"><span data-stu-id="77e25-109">Microsoft products use this member to store user data specific to the individual program.</span></span>



| <span data-ttu-id="77e25-110">Entrada</span><span class="sxs-lookup"><span data-stu-id="77e25-110">Entry</span></span> | <span data-ttu-id="77e25-111">Valor</span><span class="sxs-lookup"><span data-stu-id="77e25-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="77e25-112">CN</span><span class="sxs-lookup"><span data-stu-id="77e25-112">CN</span></span>                | <span data-ttu-id="77e25-113">User-Parameters</span><span class="sxs-lookup"><span data-stu-id="77e25-113">User-Parameters</span></span>                             |
| <span data-ttu-id="77e25-114">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="77e25-114">Ldap-Display-Name</span></span> | <span data-ttu-id="77e25-115">userparameters</span><span class="sxs-lookup"><span data-stu-id="77e25-115">userParameters</span></span>                              |
| <span data-ttu-id="77e25-116">Tamanho</span><span class="sxs-lookup"><span data-stu-id="77e25-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="77e25-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="77e25-117">Update Privilege</span></span>  | <span data-ttu-id="77e25-118">Modificado por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="77e25-118">Modified by applications.</span></span>                   |
| <span data-ttu-id="77e25-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="77e25-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="77e25-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="77e25-120">Attribute-Id</span></span>      | <span data-ttu-id="77e25-121">1.2.840.113556.1.4.138</span><span class="sxs-lookup"><span data-stu-id="77e25-121">1.2.840.113556.1.4.138</span></span>                      |
| <span data-ttu-id="77e25-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="77e25-122">System-Id-Guid</span></span>    | <span data-ttu-id="77e25-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="77e25-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="77e25-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="77e25-124">Syntax</span></span>            | [<span data-ttu-id="77e25-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="77e25-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="77e25-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="77e25-126">Implementations</span></span>

-   [<span data-ttu-id="77e25-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="77e25-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="77e25-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="77e25-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="77e25-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="77e25-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="77e25-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="77e25-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="77e25-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="77e25-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="77e25-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="77e25-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="77e25-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="77e25-133">Windows 2000 Server</span></span>



| <span data-ttu-id="77e25-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="77e25-134">Entry</span></span> | <span data-ttu-id="77e25-135">Valor</span><span class="sxs-lookup"><span data-stu-id="77e25-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77e25-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="77e25-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77e25-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="77e25-138">System-Only</span></span>            | <span data-ttu-id="77e25-139">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-139">False</span></span>                             |
| <span data-ttu-id="77e25-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77e25-140">Is-Single-Valued</span></span>       | <span data-ttu-id="77e25-141">True</span><span class="sxs-lookup"><span data-stu-id="77e25-141">True</span></span>                              |
| <span data-ttu-id="77e25-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="77e25-142">Is Indexed</span></span>             | <span data-ttu-id="77e25-143">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-143">False</span></span>                             |
| <span data-ttu-id="77e25-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77e25-144">In Global Catalog</span></span>      | <span data-ttu-id="77e25-145">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-145">False</span></span>                             |
| <span data-ttu-id="77e25-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77e25-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="77e25-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77e25-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77e25-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77e25-148">Range-Lower</span></span>            | <span data-ttu-id="77e25-149">0</span><span class="sxs-lookup"><span data-stu-id="77e25-149">0</span></span>                                 |
| <span data-ttu-id="77e25-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77e25-150">Range-Upper</span></span>            | <span data-ttu-id="77e25-151">32767</span><span class="sxs-lookup"><span data-stu-id="77e25-151">32767</span></span>                             |
| <span data-ttu-id="77e25-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-152">Search-Flags</span></span>           | <span data-ttu-id="77e25-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77e25-153">0x00000000</span></span>                        |
| <span data-ttu-id="77e25-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-154">System-Flags</span></span>           | <span data-ttu-id="77e25-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77e25-155">0x00000010</span></span>                        |
| <span data-ttu-id="77e25-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77e25-156">Classes used in</span></span>        | [<span data-ttu-id="77e25-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="77e25-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="77e25-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77e25-158">Windows Server 2003</span></span>



| <span data-ttu-id="77e25-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="77e25-159">Entry</span></span> | <span data-ttu-id="77e25-160">Valor</span><span class="sxs-lookup"><span data-stu-id="77e25-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77e25-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="77e25-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77e25-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="77e25-163">System-Only</span></span>            | <span data-ttu-id="77e25-164">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-164">False</span></span>                             |
| <span data-ttu-id="77e25-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77e25-165">Is-Single-Valued</span></span>       | <span data-ttu-id="77e25-166">True</span><span class="sxs-lookup"><span data-stu-id="77e25-166">True</span></span>                              |
| <span data-ttu-id="77e25-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="77e25-167">Is Indexed</span></span>             | <span data-ttu-id="77e25-168">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-168">False</span></span>                             |
| <span data-ttu-id="77e25-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77e25-169">In Global Catalog</span></span>      | <span data-ttu-id="77e25-170">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-170">False</span></span>                             |
| <span data-ttu-id="77e25-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77e25-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="77e25-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77e25-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77e25-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77e25-173">Range-Lower</span></span>            | <span data-ttu-id="77e25-174">0</span><span class="sxs-lookup"><span data-stu-id="77e25-174">0</span></span>                                 |
| <span data-ttu-id="77e25-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77e25-175">Range-Upper</span></span>            | <span data-ttu-id="77e25-176">32767</span><span class="sxs-lookup"><span data-stu-id="77e25-176">32767</span></span>                             |
| <span data-ttu-id="77e25-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-177">Search-Flags</span></span>           | <span data-ttu-id="77e25-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77e25-178">0x00000000</span></span>                        |
| <span data-ttu-id="77e25-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-179">System-Flags</span></span>           | <span data-ttu-id="77e25-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77e25-180">0x00000010</span></span>                        |
| <span data-ttu-id="77e25-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77e25-181">Classes used in</span></span>        | [<span data-ttu-id="77e25-182">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="77e25-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="77e25-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="77e25-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="77e25-184">Entrada</span><span class="sxs-lookup"><span data-stu-id="77e25-184">Entry</span></span> | <span data-ttu-id="77e25-185">Valor</span><span class="sxs-lookup"><span data-stu-id="77e25-185">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77e25-186">ID do link</span><span class="sxs-lookup"><span data-stu-id="77e25-186">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77e25-187">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="77e25-188">System-Only</span></span>            | <span data-ttu-id="77e25-189">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-189">False</span></span>                             |
| <span data-ttu-id="77e25-190">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77e25-190">Is-Single-Valued</span></span>       | <span data-ttu-id="77e25-191">True</span><span class="sxs-lookup"><span data-stu-id="77e25-191">True</span></span>                              |
| <span data-ttu-id="77e25-192">É indexado</span><span class="sxs-lookup"><span data-stu-id="77e25-192">Is Indexed</span></span>             | <span data-ttu-id="77e25-193">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-193">False</span></span>                             |
| <span data-ttu-id="77e25-194">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77e25-194">In Global Catalog</span></span>      | <span data-ttu-id="77e25-195">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-195">False</span></span>                             |
| <span data-ttu-id="77e25-196">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77e25-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="77e25-197">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77e25-197">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77e25-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77e25-198">Range-Lower</span></span>            | <span data-ttu-id="77e25-199">0</span><span class="sxs-lookup"><span data-stu-id="77e25-199">0</span></span>                                 |
| <span data-ttu-id="77e25-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77e25-200">Range-Upper</span></span>            | <span data-ttu-id="77e25-201">32767</span><span class="sxs-lookup"><span data-stu-id="77e25-201">32767</span></span>                             |
| <span data-ttu-id="77e25-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-202">Search-Flags</span></span>           | <span data-ttu-id="77e25-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77e25-203">0x00000000</span></span>                        |
| <span data-ttu-id="77e25-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-204">System-Flags</span></span>           | <span data-ttu-id="77e25-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77e25-205">0x00000010</span></span>                        |
| <span data-ttu-id="77e25-206">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77e25-206">Classes used in</span></span>        | [<span data-ttu-id="77e25-207">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="77e25-207">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="77e25-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77e25-208">Windows Server 2008</span></span>



| <span data-ttu-id="77e25-209">Entrada</span><span class="sxs-lookup"><span data-stu-id="77e25-209">Entry</span></span> | <span data-ttu-id="77e25-210">Valor</span><span class="sxs-lookup"><span data-stu-id="77e25-210">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77e25-211">ID do link</span><span class="sxs-lookup"><span data-stu-id="77e25-211">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77e25-212">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="77e25-213">System-Only</span></span>            | <span data-ttu-id="77e25-214">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-214">False</span></span>                             |
| <span data-ttu-id="77e25-215">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77e25-215">Is-Single-Valued</span></span>       | <span data-ttu-id="77e25-216">True</span><span class="sxs-lookup"><span data-stu-id="77e25-216">True</span></span>                              |
| <span data-ttu-id="77e25-217">É indexado</span><span class="sxs-lookup"><span data-stu-id="77e25-217">Is Indexed</span></span>             | <span data-ttu-id="77e25-218">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-218">False</span></span>                             |
| <span data-ttu-id="77e25-219">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77e25-219">In Global Catalog</span></span>      | <span data-ttu-id="77e25-220">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-220">False</span></span>                             |
| <span data-ttu-id="77e25-221">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77e25-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="77e25-222">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77e25-222">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77e25-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77e25-223">Range-Lower</span></span>            | <span data-ttu-id="77e25-224">0</span><span class="sxs-lookup"><span data-stu-id="77e25-224">0</span></span>                                 |
| <span data-ttu-id="77e25-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77e25-225">Range-Upper</span></span>            | <span data-ttu-id="77e25-226">32767</span><span class="sxs-lookup"><span data-stu-id="77e25-226">32767</span></span>                             |
| <span data-ttu-id="77e25-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-227">Search-Flags</span></span>           | <span data-ttu-id="77e25-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77e25-228">0x00000000</span></span>                        |
| <span data-ttu-id="77e25-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-229">System-Flags</span></span>           | <span data-ttu-id="77e25-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77e25-230">0x00000010</span></span>                        |
| <span data-ttu-id="77e25-231">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77e25-231">Classes used in</span></span>        | [<span data-ttu-id="77e25-232">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="77e25-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="77e25-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77e25-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="77e25-234">Entrada</span><span class="sxs-lookup"><span data-stu-id="77e25-234">Entry</span></span> | <span data-ttu-id="77e25-235">Valor</span><span class="sxs-lookup"><span data-stu-id="77e25-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77e25-236">ID do link</span><span class="sxs-lookup"><span data-stu-id="77e25-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77e25-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="77e25-238">System-Only</span></span>            | <span data-ttu-id="77e25-239">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-239">False</span></span>                             |
| <span data-ttu-id="77e25-240">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77e25-240">Is-Single-Valued</span></span>       | <span data-ttu-id="77e25-241">True</span><span class="sxs-lookup"><span data-stu-id="77e25-241">True</span></span>                              |
| <span data-ttu-id="77e25-242">É indexado</span><span class="sxs-lookup"><span data-stu-id="77e25-242">Is Indexed</span></span>             | <span data-ttu-id="77e25-243">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-243">False</span></span>                             |
| <span data-ttu-id="77e25-244">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77e25-244">In Global Catalog</span></span>      | <span data-ttu-id="77e25-245">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-245">False</span></span>                             |
| <span data-ttu-id="77e25-246">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77e25-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="77e25-247">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77e25-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77e25-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77e25-248">Range-Lower</span></span>            | <span data-ttu-id="77e25-249">0</span><span class="sxs-lookup"><span data-stu-id="77e25-249">0</span></span>                                 |
| <span data-ttu-id="77e25-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77e25-250">Range-Upper</span></span>            | <span data-ttu-id="77e25-251">32767</span><span class="sxs-lookup"><span data-stu-id="77e25-251">32767</span></span>                             |
| <span data-ttu-id="77e25-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-252">Search-Flags</span></span>           | <span data-ttu-id="77e25-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77e25-253">0x00000000</span></span>                        |
| <span data-ttu-id="77e25-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-254">System-Flags</span></span>           | <span data-ttu-id="77e25-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77e25-255">0x00000010</span></span>                        |
| <span data-ttu-id="77e25-256">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77e25-256">Classes used in</span></span>        | [<span data-ttu-id="77e25-257">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="77e25-257">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="77e25-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77e25-258">Windows Server 2012</span></span>



| <span data-ttu-id="77e25-259">Entrada</span><span class="sxs-lookup"><span data-stu-id="77e25-259">Entry</span></span> | <span data-ttu-id="77e25-260">Valor</span><span class="sxs-lookup"><span data-stu-id="77e25-260">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="77e25-261">ID do link</span><span class="sxs-lookup"><span data-stu-id="77e25-261">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77e25-262">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="77e25-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="77e25-263">System-Only</span></span>            | <span data-ttu-id="77e25-264">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-264">False</span></span>                             |
| <span data-ttu-id="77e25-265">É de valor único</span><span class="sxs-lookup"><span data-stu-id="77e25-265">Is-Single-Valued</span></span>       | <span data-ttu-id="77e25-266">True</span><span class="sxs-lookup"><span data-stu-id="77e25-266">True</span></span>                              |
| <span data-ttu-id="77e25-267">É indexado</span><span class="sxs-lookup"><span data-stu-id="77e25-267">Is Indexed</span></span>             | <span data-ttu-id="77e25-268">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-268">False</span></span>                             |
| <span data-ttu-id="77e25-269">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="77e25-269">In Global Catalog</span></span>      | <span data-ttu-id="77e25-270">Falso</span><span class="sxs-lookup"><span data-stu-id="77e25-270">False</span></span>                             |
| <span data-ttu-id="77e25-271">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="77e25-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="77e25-272">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="77e25-272">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="77e25-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77e25-273">Range-Lower</span></span>            | <span data-ttu-id="77e25-274">0</span><span class="sxs-lookup"><span data-stu-id="77e25-274">0</span></span>                                 |
| <span data-ttu-id="77e25-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77e25-275">Range-Upper</span></span>            | <span data-ttu-id="77e25-276">32767</span><span class="sxs-lookup"><span data-stu-id="77e25-276">32767</span></span>                             |
| <span data-ttu-id="77e25-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-277">Search-Flags</span></span>           | <span data-ttu-id="77e25-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77e25-278">0x00000000</span></span>                        |
| <span data-ttu-id="77e25-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77e25-279">System-Flags</span></span>           | <span data-ttu-id="77e25-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77e25-280">0x00000010</span></span>                        |
| <span data-ttu-id="77e25-281">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="77e25-281">Classes used in</span></span>        | [<span data-ttu-id="77e25-282">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="77e25-282">**User**</span></span>](c-user.md)<br/> |



 

 





