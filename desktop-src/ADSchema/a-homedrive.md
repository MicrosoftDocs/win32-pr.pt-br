---
title: Home-Drive atributo
description: Especifica a letra da unidade para a qual mapear o caminho UNC especificado por homeDirectory.
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- Esquema de Home-Drive do atributo AD
- Esquema de AD do atributo homeDrive
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce9bff87662cc3b9da962b0c5647e79e90a3068
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105754412"
---
# <a name="home-drive-attribute"></a><span data-ttu-id="11bfc-105">Home-Drive atributo</span><span class="sxs-lookup"><span data-stu-id="11bfc-105">Home-Drive attribute</span></span>

<span data-ttu-id="11bfc-106">Especifica a letra da unidade para a qual mapear o caminho UNC especificado por [**HomeDirectory**](a-homedirectory.md).</span><span class="sxs-lookup"><span data-stu-id="11bfc-106">Specifies the drive letter to which to map the UNC path specified by [**homeDirectory**](a-homedirectory.md).</span></span> <span data-ttu-id="11bfc-107">A letra da unidade deve ser especificada no formato \*DriveLetter \* \* \*:\*\*, em que *DriveLetter* é a letra da unidade a ser mapeada.</span><span class="sxs-lookup"><span data-stu-id="11bfc-107">The drive letter must be specified in the form *DriveLetter\*\*\*:*\* where *DriveLetter* is the letter of the drive to map.</span></span> <span data-ttu-id="11bfc-108">A *DriveLetter* deve ser uma letra maiúscula única e a vírgula (:) é necessário.</span><span class="sxs-lookup"><span data-stu-id="11bfc-108">The *DriveLetter* must be a single, uppercase letter and the colon (:) is required.</span></span>



| <span data-ttu-id="11bfc-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bfc-109">Entry</span></span> | <span data-ttu-id="11bfc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="11bfc-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="11bfc-111">CN</span><span class="sxs-lookup"><span data-stu-id="11bfc-111">CN</span></span>                | <span data-ttu-id="11bfc-112">Home-Drive</span><span class="sxs-lookup"><span data-stu-id="11bfc-112">Home-Drive</span></span>                                                                        |
| <span data-ttu-id="11bfc-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="11bfc-113">Ldap-Display-Name</span></span> | <span data-ttu-id="11bfc-114">homeDrive</span><span class="sxs-lookup"><span data-stu-id="11bfc-114">homeDrive</span></span>                                                                         |
| <span data-ttu-id="11bfc-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="11bfc-115">Size</span></span>              | <span data-ttu-id="11bfc-116">2 bytes</span><span class="sxs-lookup"><span data-stu-id="11bfc-116">2 bytes</span></span>                                                                           |
| <span data-ttu-id="11bfc-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="11bfc-117">Update Privilege</span></span>  | <span data-ttu-id="11bfc-118">O administrador de domínio define esse valor.</span><span class="sxs-lookup"><span data-stu-id="11bfc-118">The domain administrator sets this value.</span></span>                                         |
| <span data-ttu-id="11bfc-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="11bfc-119">Update Frequency</span></span>  | <span data-ttu-id="11bfc-120">Quando o registro de um usuário é criado e sempre que a unidade principal precisa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="11bfc-120">When the record of a user is created and whenever the home drive needs to change.</span></span> |
| <span data-ttu-id="11bfc-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="11bfc-121">Attribute-Id</span></span>      | <span data-ttu-id="11bfc-122">1.2.840.113556.1.4.45</span><span class="sxs-lookup"><span data-stu-id="11bfc-122">1.2.840.113556.1.4.45</span></span>                                                             |
| <span data-ttu-id="11bfc-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="11bfc-123">System-Id-Guid</span></span>    | <span data-ttu-id="11bfc-124">bf967986-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="11bfc-124">bf967986-0de6-11d0-a285-00aa003049e2</span></span>                                              |
| <span data-ttu-id="11bfc-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="11bfc-125">Syntax</span></span>            | [<span data-ttu-id="11bfc-126">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="11bfc-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="11bfc-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="11bfc-127">Implementations</span></span>

-   [<span data-ttu-id="11bfc-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="11bfc-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="11bfc-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="11bfc-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="11bfc-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="11bfc-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="11bfc-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="11bfc-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="11bfc-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="11bfc-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="11bfc-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="11bfc-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="11bfc-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11bfc-134">Windows 2000 Server</span></span>



| <span data-ttu-id="11bfc-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bfc-135">Entry</span></span> | <span data-ttu-id="11bfc-136">Valor</span><span class="sxs-lookup"><span data-stu-id="11bfc-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="11bfc-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="11bfc-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11bfc-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="11bfc-139">System-Only</span></span>            | <span data-ttu-id="11bfc-140">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-140">False</span></span>                             |
| <span data-ttu-id="11bfc-141">É de valor único</span><span class="sxs-lookup"><span data-stu-id="11bfc-141">Is-Single-Valued</span></span>       | <span data-ttu-id="11bfc-142">True</span><span class="sxs-lookup"><span data-stu-id="11bfc-142">True</span></span>                              |
| <span data-ttu-id="11bfc-143">É indexado</span><span class="sxs-lookup"><span data-stu-id="11bfc-143">Is Indexed</span></span>             | <span data-ttu-id="11bfc-144">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-144">False</span></span>                             |
| <span data-ttu-id="11bfc-145">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="11bfc-145">In Global Catalog</span></span>      | <span data-ttu-id="11bfc-146">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-146">False</span></span>                             |
| <span data-ttu-id="11bfc-147">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="11bfc-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="11bfc-148">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="11bfc-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="11bfc-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11bfc-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="11bfc-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11bfc-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="11bfc-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-151">Search-Flags</span></span>           | <span data-ttu-id="11bfc-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-152">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-153">System-Flags</span></span>           | <span data-ttu-id="11bfc-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-154">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-155">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="11bfc-155">Classes used in</span></span>        | [<span data-ttu-id="11bfc-156">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="11bfc-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="11bfc-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11bfc-157">Windows Server 2003</span></span>



| <span data-ttu-id="11bfc-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bfc-158">Entry</span></span> | <span data-ttu-id="11bfc-159">Valor</span><span class="sxs-lookup"><span data-stu-id="11bfc-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="11bfc-160">ID do link</span><span class="sxs-lookup"><span data-stu-id="11bfc-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11bfc-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="11bfc-162">System-Only</span></span>            | <span data-ttu-id="11bfc-163">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-163">False</span></span>                             |
| <span data-ttu-id="11bfc-164">É de valor único</span><span class="sxs-lookup"><span data-stu-id="11bfc-164">Is-Single-Valued</span></span>       | <span data-ttu-id="11bfc-165">True</span><span class="sxs-lookup"><span data-stu-id="11bfc-165">True</span></span>                              |
| <span data-ttu-id="11bfc-166">É indexado</span><span class="sxs-lookup"><span data-stu-id="11bfc-166">Is Indexed</span></span>             | <span data-ttu-id="11bfc-167">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-167">False</span></span>                             |
| <span data-ttu-id="11bfc-168">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="11bfc-168">In Global Catalog</span></span>      | <span data-ttu-id="11bfc-169">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-169">False</span></span>                             |
| <span data-ttu-id="11bfc-170">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="11bfc-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="11bfc-171">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="11bfc-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="11bfc-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11bfc-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="11bfc-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11bfc-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="11bfc-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-174">Search-Flags</span></span>           | <span data-ttu-id="11bfc-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-175">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-176">System-Flags</span></span>           | <span data-ttu-id="11bfc-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-177">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-178">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="11bfc-178">Classes used in</span></span>        | [<span data-ttu-id="11bfc-179">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="11bfc-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="11bfc-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="11bfc-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="11bfc-181">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bfc-181">Entry</span></span> | <span data-ttu-id="11bfc-182">Valor</span><span class="sxs-lookup"><span data-stu-id="11bfc-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="11bfc-183">ID do link</span><span class="sxs-lookup"><span data-stu-id="11bfc-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11bfc-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="11bfc-185">System-Only</span></span>            | <span data-ttu-id="11bfc-186">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-186">False</span></span>                             |
| <span data-ttu-id="11bfc-187">É de valor único</span><span class="sxs-lookup"><span data-stu-id="11bfc-187">Is-Single-Valued</span></span>       | <span data-ttu-id="11bfc-188">True</span><span class="sxs-lookup"><span data-stu-id="11bfc-188">True</span></span>                              |
| <span data-ttu-id="11bfc-189">É indexado</span><span class="sxs-lookup"><span data-stu-id="11bfc-189">Is Indexed</span></span>             | <span data-ttu-id="11bfc-190">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-190">False</span></span>                             |
| <span data-ttu-id="11bfc-191">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="11bfc-191">In Global Catalog</span></span>      | <span data-ttu-id="11bfc-192">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-192">False</span></span>                             |
| <span data-ttu-id="11bfc-193">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="11bfc-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="11bfc-194">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="11bfc-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="11bfc-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11bfc-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="11bfc-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11bfc-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="11bfc-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-197">Search-Flags</span></span>           | <span data-ttu-id="11bfc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-198">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-199">System-Flags</span></span>           | <span data-ttu-id="11bfc-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-200">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-201">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="11bfc-201">Classes used in</span></span>        | [<span data-ttu-id="11bfc-202">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="11bfc-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="11bfc-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11bfc-203">Windows Server 2008</span></span>



| <span data-ttu-id="11bfc-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bfc-204">Entry</span></span> | <span data-ttu-id="11bfc-205">Valor</span><span class="sxs-lookup"><span data-stu-id="11bfc-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="11bfc-206">ID do link</span><span class="sxs-lookup"><span data-stu-id="11bfc-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11bfc-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="11bfc-208">System-Only</span></span>            | <span data-ttu-id="11bfc-209">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-209">False</span></span>                             |
| <span data-ttu-id="11bfc-210">É de valor único</span><span class="sxs-lookup"><span data-stu-id="11bfc-210">Is-Single-Valued</span></span>       | <span data-ttu-id="11bfc-211">True</span><span class="sxs-lookup"><span data-stu-id="11bfc-211">True</span></span>                              |
| <span data-ttu-id="11bfc-212">É indexado</span><span class="sxs-lookup"><span data-stu-id="11bfc-212">Is Indexed</span></span>             | <span data-ttu-id="11bfc-213">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-213">False</span></span>                             |
| <span data-ttu-id="11bfc-214">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="11bfc-214">In Global Catalog</span></span>      | <span data-ttu-id="11bfc-215">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-215">False</span></span>                             |
| <span data-ttu-id="11bfc-216">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="11bfc-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="11bfc-217">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="11bfc-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="11bfc-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11bfc-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="11bfc-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11bfc-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="11bfc-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-220">Search-Flags</span></span>           | <span data-ttu-id="11bfc-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-221">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-222">System-Flags</span></span>           | <span data-ttu-id="11bfc-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-223">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-224">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="11bfc-224">Classes used in</span></span>        | [<span data-ttu-id="11bfc-225">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="11bfc-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="11bfc-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11bfc-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="11bfc-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bfc-227">Entry</span></span> | <span data-ttu-id="11bfc-228">Valor</span><span class="sxs-lookup"><span data-stu-id="11bfc-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="11bfc-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="11bfc-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11bfc-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="11bfc-231">System-Only</span></span>            | <span data-ttu-id="11bfc-232">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-232">False</span></span>                             |
| <span data-ttu-id="11bfc-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="11bfc-233">Is-Single-Valued</span></span>       | <span data-ttu-id="11bfc-234">True</span><span class="sxs-lookup"><span data-stu-id="11bfc-234">True</span></span>                              |
| <span data-ttu-id="11bfc-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="11bfc-235">Is Indexed</span></span>             | <span data-ttu-id="11bfc-236">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-236">False</span></span>                             |
| <span data-ttu-id="11bfc-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="11bfc-237">In Global Catalog</span></span>      | <span data-ttu-id="11bfc-238">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-238">False</span></span>                             |
| <span data-ttu-id="11bfc-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="11bfc-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="11bfc-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="11bfc-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="11bfc-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11bfc-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="11bfc-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11bfc-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="11bfc-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-243">Search-Flags</span></span>           | <span data-ttu-id="11bfc-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-244">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-245">System-Flags</span></span>           | <span data-ttu-id="11bfc-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-246">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="11bfc-247">Classes used in</span></span>        | [<span data-ttu-id="11bfc-248">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="11bfc-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="11bfc-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11bfc-249">Windows Server 2012</span></span>



| <span data-ttu-id="11bfc-250">Entrada</span><span class="sxs-lookup"><span data-stu-id="11bfc-250">Entry</span></span> | <span data-ttu-id="11bfc-251">Valor</span><span class="sxs-lookup"><span data-stu-id="11bfc-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="11bfc-252">ID do link</span><span class="sxs-lookup"><span data-stu-id="11bfc-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="11bfc-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="11bfc-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="11bfc-254">System-Only</span></span>            | <span data-ttu-id="11bfc-255">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-255">False</span></span>                             |
| <span data-ttu-id="11bfc-256">É de valor único</span><span class="sxs-lookup"><span data-stu-id="11bfc-256">Is-Single-Valued</span></span>       | <span data-ttu-id="11bfc-257">True</span><span class="sxs-lookup"><span data-stu-id="11bfc-257">True</span></span>                              |
| <span data-ttu-id="11bfc-258">É indexado</span><span class="sxs-lookup"><span data-stu-id="11bfc-258">Is Indexed</span></span>             | <span data-ttu-id="11bfc-259">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-259">False</span></span>                             |
| <span data-ttu-id="11bfc-260">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="11bfc-260">In Global Catalog</span></span>      | <span data-ttu-id="11bfc-261">Falso</span><span class="sxs-lookup"><span data-stu-id="11bfc-261">False</span></span>                             |
| <span data-ttu-id="11bfc-262">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="11bfc-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="11bfc-263">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="11bfc-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="11bfc-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="11bfc-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="11bfc-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="11bfc-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="11bfc-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-266">Search-Flags</span></span>           | <span data-ttu-id="11bfc-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-267">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="11bfc-268">System-Flags</span></span>           | <span data-ttu-id="11bfc-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="11bfc-269">0x00000010</span></span>                        |
| <span data-ttu-id="11bfc-270">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="11bfc-270">Classes used in</span></span>        | [<span data-ttu-id="11bfc-271">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="11bfc-271">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="11bfc-272">Confira também</span><span class="sxs-lookup"><span data-stu-id="11bfc-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bfc-273">**homeDirectory**</span><span class="sxs-lookup"><span data-stu-id="11bfc-273">**homeDirectory**</span></span>](a-homedirectory.md)
</dt> </dl>

 

 





