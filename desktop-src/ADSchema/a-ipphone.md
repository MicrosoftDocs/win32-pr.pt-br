---
title: Atributo de telefone-IP-primário
description: O endereço TCP/IP do telefone. Usado por telefonia.
ms.assetid: b51f28e4-4677-4798-87f1-2bd952a528ea
ms.tgt_platform: multiple
keywords:
- Esquema do AD-IP-primário de atributo de telefone
- Esquema de AD do atributo ipPhone
topic_type:
- apiref
api_name:
- Phone-Ip-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4f16d29f6b3f45c5a229d76ec30c0dd7efdea2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086670"
---
# <a name="phone-ip-primary-attribute"></a><span data-ttu-id="166ea-106">Atributo de telefone-IP-primário</span><span class="sxs-lookup"><span data-stu-id="166ea-106">Phone-Ip-Primary attribute</span></span>

<span data-ttu-id="166ea-107">O endereço TCP/IP do telefone.</span><span class="sxs-lookup"><span data-stu-id="166ea-107">The TCP/IP address for the phone.</span></span> <span data-ttu-id="166ea-108">Usado por telefonia.</span><span class="sxs-lookup"><span data-stu-id="166ea-108">Used by Telephony.</span></span>



| <span data-ttu-id="166ea-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="166ea-109">Entry</span></span> | <span data-ttu-id="166ea-110">Valor</span><span class="sxs-lookup"><span data-stu-id="166ea-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="166ea-111">CN</span><span class="sxs-lookup"><span data-stu-id="166ea-111">CN</span></span>                | <span data-ttu-id="166ea-112">Telefone-IP-primário</span><span class="sxs-lookup"><span data-stu-id="166ea-112">Phone-Ip-Primary</span></span>                                                                 |
| <span data-ttu-id="166ea-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="166ea-113">Ldap-Display-Name</span></span> | <span data-ttu-id="166ea-114">ipPhone</span><span class="sxs-lookup"><span data-stu-id="166ea-114">ipPhone</span></span>                                                                          |
| <span data-ttu-id="166ea-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="166ea-115">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="166ea-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="166ea-116">Update Privilege</span></span>  | <span data-ttu-id="166ea-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="166ea-117">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="166ea-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="166ea-118">Update Frequency</span></span>  | <span data-ttu-id="166ea-119">Quando o registro do usuário é criado e sempre que o número de telefone precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="166ea-119">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="166ea-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="166ea-120">Attribute-Id</span></span>      | <span data-ttu-id="166ea-121">1.2.840.113556.1.4.721</span><span class="sxs-lookup"><span data-stu-id="166ea-121">1.2.840.113556.1.4.721</span></span>                                                           |
| <span data-ttu-id="166ea-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="166ea-122">System-Id-Guid</span></span>    | <span data-ttu-id="166ea-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="166ea-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="166ea-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="166ea-124">Syntax</span></span>            | [<span data-ttu-id="166ea-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="166ea-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="166ea-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="166ea-126">Implementations</span></span>

-   [<span data-ttu-id="166ea-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="166ea-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="166ea-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="166ea-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="166ea-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="166ea-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="166ea-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="166ea-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="166ea-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="166ea-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="166ea-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="166ea-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="166ea-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="166ea-133">Windows 2000 Server</span></span>



| <span data-ttu-id="166ea-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="166ea-134">Entry</span></span> | <span data-ttu-id="166ea-135">Valor</span><span class="sxs-lookup"><span data-stu-id="166ea-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="166ea-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="166ea-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="166ea-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="166ea-138">System-Only</span></span>            | <span data-ttu-id="166ea-139">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-139">False</span></span>                                                              |
| <span data-ttu-id="166ea-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="166ea-140">Is-Single-Valued</span></span>       | <span data-ttu-id="166ea-141">True</span><span class="sxs-lookup"><span data-stu-id="166ea-141">True</span></span>                                                               |
| <span data-ttu-id="166ea-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="166ea-142">Is Indexed</span></span>             | <span data-ttu-id="166ea-143">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-143">False</span></span>                                                              |
| <span data-ttu-id="166ea-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="166ea-144">In Global Catalog</span></span>      | <span data-ttu-id="166ea-145">True</span><span class="sxs-lookup"><span data-stu-id="166ea-145">True</span></span>                                                               |
| <span data-ttu-id="166ea-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="166ea-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="166ea-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="166ea-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="166ea-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="166ea-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="166ea-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-150">Search-Flags</span></span>           | <span data-ttu-id="166ea-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="166ea-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="166ea-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-152">System-Flags</span></span>           | <span data-ttu-id="166ea-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="166ea-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="166ea-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="166ea-154">Classes used in</span></span>        | [<span data-ttu-id="166ea-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="166ea-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="166ea-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="166ea-156">Windows Server 2003</span></span>



| <span data-ttu-id="166ea-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="166ea-157">Entry</span></span> | <span data-ttu-id="166ea-158">Valor</span><span class="sxs-lookup"><span data-stu-id="166ea-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="166ea-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="166ea-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="166ea-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="166ea-161">System-Only</span></span>            | <span data-ttu-id="166ea-162">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-162">False</span></span>                                                              |
| <span data-ttu-id="166ea-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="166ea-163">Is-Single-Valued</span></span>       | <span data-ttu-id="166ea-164">True</span><span class="sxs-lookup"><span data-stu-id="166ea-164">True</span></span>                                                               |
| <span data-ttu-id="166ea-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="166ea-165">Is Indexed</span></span>             | <span data-ttu-id="166ea-166">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-166">False</span></span>                                                              |
| <span data-ttu-id="166ea-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="166ea-167">In Global Catalog</span></span>      | <span data-ttu-id="166ea-168">True</span><span class="sxs-lookup"><span data-stu-id="166ea-168">True</span></span>                                                               |
| <span data-ttu-id="166ea-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="166ea-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="166ea-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="166ea-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="166ea-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="166ea-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="166ea-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-173">Search-Flags</span></span>           | <span data-ttu-id="166ea-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="166ea-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="166ea-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-175">System-Flags</span></span>           | <span data-ttu-id="166ea-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="166ea-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="166ea-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="166ea-177">Classes used in</span></span>        | [<span data-ttu-id="166ea-178">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="166ea-178">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="166ea-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="166ea-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="166ea-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="166ea-180">Entry</span></span> | <span data-ttu-id="166ea-181">Valor</span><span class="sxs-lookup"><span data-stu-id="166ea-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="166ea-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="166ea-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="166ea-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="166ea-184">System-Only</span></span>            | <span data-ttu-id="166ea-185">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-185">False</span></span>                                                              |
| <span data-ttu-id="166ea-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="166ea-186">Is-Single-Valued</span></span>       | <span data-ttu-id="166ea-187">True</span><span class="sxs-lookup"><span data-stu-id="166ea-187">True</span></span>                                                               |
| <span data-ttu-id="166ea-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="166ea-188">Is Indexed</span></span>             | <span data-ttu-id="166ea-189">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-189">False</span></span>                                                              |
| <span data-ttu-id="166ea-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="166ea-190">In Global Catalog</span></span>      | <span data-ttu-id="166ea-191">True</span><span class="sxs-lookup"><span data-stu-id="166ea-191">True</span></span>                                                               |
| <span data-ttu-id="166ea-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="166ea-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="166ea-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="166ea-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="166ea-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="166ea-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="166ea-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-196">Search-Flags</span></span>           | <span data-ttu-id="166ea-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="166ea-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="166ea-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-198">System-Flags</span></span>           | <span data-ttu-id="166ea-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="166ea-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="166ea-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="166ea-200">Classes used in</span></span>        | [<span data-ttu-id="166ea-201">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="166ea-201">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="166ea-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="166ea-202">Windows Server 2008</span></span>



| <span data-ttu-id="166ea-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="166ea-203">Entry</span></span> | <span data-ttu-id="166ea-204">Valor</span><span class="sxs-lookup"><span data-stu-id="166ea-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="166ea-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="166ea-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="166ea-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="166ea-207">System-Only</span></span>            | <span data-ttu-id="166ea-208">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-208">False</span></span>                                                              |
| <span data-ttu-id="166ea-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="166ea-209">Is-Single-Valued</span></span>       | <span data-ttu-id="166ea-210">True</span><span class="sxs-lookup"><span data-stu-id="166ea-210">True</span></span>                                                               |
| <span data-ttu-id="166ea-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="166ea-211">Is Indexed</span></span>             | <span data-ttu-id="166ea-212">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-212">False</span></span>                                                              |
| <span data-ttu-id="166ea-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="166ea-213">In Global Catalog</span></span>      | <span data-ttu-id="166ea-214">True</span><span class="sxs-lookup"><span data-stu-id="166ea-214">True</span></span>                                                               |
| <span data-ttu-id="166ea-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="166ea-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="166ea-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="166ea-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="166ea-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="166ea-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="166ea-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-219">Search-Flags</span></span>           | <span data-ttu-id="166ea-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="166ea-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="166ea-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-221">System-Flags</span></span>           | <span data-ttu-id="166ea-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="166ea-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="166ea-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="166ea-223">Classes used in</span></span>        | [<span data-ttu-id="166ea-224">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="166ea-224">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="166ea-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="166ea-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="166ea-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="166ea-226">Entry</span></span> | <span data-ttu-id="166ea-227">Valor</span><span class="sxs-lookup"><span data-stu-id="166ea-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="166ea-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="166ea-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="166ea-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="166ea-230">System-Only</span></span>            | <span data-ttu-id="166ea-231">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-231">False</span></span>                                                              |
| <span data-ttu-id="166ea-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="166ea-232">Is-Single-Valued</span></span>       | <span data-ttu-id="166ea-233">True</span><span class="sxs-lookup"><span data-stu-id="166ea-233">True</span></span>                                                               |
| <span data-ttu-id="166ea-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="166ea-234">Is Indexed</span></span>             | <span data-ttu-id="166ea-235">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-235">False</span></span>                                                              |
| <span data-ttu-id="166ea-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="166ea-236">In Global Catalog</span></span>      | <span data-ttu-id="166ea-237">True</span><span class="sxs-lookup"><span data-stu-id="166ea-237">True</span></span>                                                               |
| <span data-ttu-id="166ea-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="166ea-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="166ea-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="166ea-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="166ea-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="166ea-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="166ea-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-242">Search-Flags</span></span>           | <span data-ttu-id="166ea-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="166ea-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="166ea-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-244">System-Flags</span></span>           | <span data-ttu-id="166ea-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="166ea-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="166ea-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="166ea-246">Classes used in</span></span>        | [<span data-ttu-id="166ea-247">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="166ea-247">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="166ea-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="166ea-248">Windows Server 2012</span></span>



| <span data-ttu-id="166ea-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="166ea-249">Entry</span></span> | <span data-ttu-id="166ea-250">Valor</span><span class="sxs-lookup"><span data-stu-id="166ea-250">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="166ea-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="166ea-251">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="166ea-252">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="166ea-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="166ea-253">System-Only</span></span>            | <span data-ttu-id="166ea-254">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-254">False</span></span>                                                              |
| <span data-ttu-id="166ea-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="166ea-255">Is-Single-Valued</span></span>       | <span data-ttu-id="166ea-256">True</span><span class="sxs-lookup"><span data-stu-id="166ea-256">True</span></span>                                                               |
| <span data-ttu-id="166ea-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="166ea-257">Is Indexed</span></span>             | <span data-ttu-id="166ea-258">Falso</span><span class="sxs-lookup"><span data-stu-id="166ea-258">False</span></span>                                                              |
| <span data-ttu-id="166ea-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="166ea-259">In Global Catalog</span></span>      | <span data-ttu-id="166ea-260">True</span><span class="sxs-lookup"><span data-stu-id="166ea-260">True</span></span>                                                               |
| <span data-ttu-id="166ea-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="166ea-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="166ea-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="166ea-262">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="166ea-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="166ea-263">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="166ea-264">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="166ea-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-265">Search-Flags</span></span>           | <span data-ttu-id="166ea-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="166ea-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="166ea-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="166ea-267">System-Flags</span></span>           | <span data-ttu-id="166ea-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="166ea-268">0x00000010</span></span>                                                         |
| <span data-ttu-id="166ea-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="166ea-269">Classes used in</span></span>        | [<span data-ttu-id="166ea-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="166ea-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





