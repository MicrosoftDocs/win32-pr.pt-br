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
# <a name="phone-ip-primary-attribute"></a><span data-ttu-id="39717-106">Atributo de telefone-IP-primário</span><span class="sxs-lookup"><span data-stu-id="39717-106">Phone-Ip-Primary attribute</span></span>

<span data-ttu-id="39717-107">O endereço TCP/IP do telefone.</span><span class="sxs-lookup"><span data-stu-id="39717-107">The TCP/IP address for the phone.</span></span> <span data-ttu-id="39717-108">Usado por telefonia.</span><span class="sxs-lookup"><span data-stu-id="39717-108">Used by Telephony.</span></span>



| <span data-ttu-id="39717-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="39717-109">Entry</span></span> | <span data-ttu-id="39717-110">Valor</span><span class="sxs-lookup"><span data-stu-id="39717-110">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39717-111">CN</span><span class="sxs-lookup"><span data-stu-id="39717-111">CN</span></span>                | <span data-ttu-id="39717-112">Telefone-IP-primário</span><span class="sxs-lookup"><span data-stu-id="39717-112">Phone-Ip-Primary</span></span>                                                                 |
| <span data-ttu-id="39717-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="39717-113">Ldap-Display-Name</span></span> | <span data-ttu-id="39717-114">ipPhone</span><span class="sxs-lookup"><span data-stu-id="39717-114">ipPhone</span></span>                                                                          |
| <span data-ttu-id="39717-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="39717-115">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="39717-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="39717-116">Update Privilege</span></span>  | <span data-ttu-id="39717-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="39717-117">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="39717-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="39717-118">Update Frequency</span></span>  | <span data-ttu-id="39717-119">Quando o registro do usuário é criado e sempre que o número de telefone precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="39717-119">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="39717-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="39717-120">Attribute-Id</span></span>      | <span data-ttu-id="39717-121">1.2.840.113556.1.4.721</span><span class="sxs-lookup"><span data-stu-id="39717-121">1.2.840.113556.1.4.721</span></span>                                                           |
| <span data-ttu-id="39717-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="39717-122">System-Id-Guid</span></span>    | <span data-ttu-id="39717-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="39717-123">4d146e4a-48d4-11d1-a9c3-0000f80367c1</span></span>                                             |
| <span data-ttu-id="39717-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="39717-124">Syntax</span></span>            | [<span data-ttu-id="39717-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="39717-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="39717-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="39717-126">Implementations</span></span>

-   [<span data-ttu-id="39717-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="39717-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="39717-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="39717-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="39717-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="39717-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="39717-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="39717-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="39717-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="39717-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="39717-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="39717-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="39717-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39717-133">Windows 2000 Server</span></span>



| <span data-ttu-id="39717-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="39717-134">Entry</span></span> | <span data-ttu-id="39717-135">Valor</span><span class="sxs-lookup"><span data-stu-id="39717-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="39717-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="39717-136">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39717-137">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="39717-138">System-Only</span></span>            | <span data-ttu-id="39717-139">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-139">False</span></span>                                                              |
| <span data-ttu-id="39717-140">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39717-140">Is-Single-Valued</span></span>       | <span data-ttu-id="39717-141">True</span><span class="sxs-lookup"><span data-stu-id="39717-141">True</span></span>                                                               |
| <span data-ttu-id="39717-142">É indexado</span><span class="sxs-lookup"><span data-stu-id="39717-142">Is Indexed</span></span>             | <span data-ttu-id="39717-143">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-143">False</span></span>                                                              |
| <span data-ttu-id="39717-144">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39717-144">In Global Catalog</span></span>      | <span data-ttu-id="39717-145">True</span><span class="sxs-lookup"><span data-stu-id="39717-145">True</span></span>                                                               |
| <span data-ttu-id="39717-146">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39717-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="39717-147">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39717-147">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="39717-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39717-148">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39717-149">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-150">Search-Flags</span></span>           | <span data-ttu-id="39717-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39717-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="39717-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-152">System-Flags</span></span>           | <span data-ttu-id="39717-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39717-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="39717-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39717-154">Classes used in</span></span>        | [<span data-ttu-id="39717-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="39717-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="39717-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="39717-156">Windows Server 2003</span></span>



| <span data-ttu-id="39717-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="39717-157">Entry</span></span> | <span data-ttu-id="39717-158">Valor</span><span class="sxs-lookup"><span data-stu-id="39717-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="39717-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="39717-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39717-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="39717-161">System-Only</span></span>            | <span data-ttu-id="39717-162">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-162">False</span></span>                                                              |
| <span data-ttu-id="39717-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39717-163">Is-Single-Valued</span></span>       | <span data-ttu-id="39717-164">True</span><span class="sxs-lookup"><span data-stu-id="39717-164">True</span></span>                                                               |
| <span data-ttu-id="39717-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="39717-165">Is Indexed</span></span>             | <span data-ttu-id="39717-166">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-166">False</span></span>                                                              |
| <span data-ttu-id="39717-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39717-167">In Global Catalog</span></span>      | <span data-ttu-id="39717-168">True</span><span class="sxs-lookup"><span data-stu-id="39717-168">True</span></span>                                                               |
| <span data-ttu-id="39717-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39717-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="39717-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39717-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="39717-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39717-171">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39717-172">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-173">Search-Flags</span></span>           | <span data-ttu-id="39717-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39717-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="39717-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-175">System-Flags</span></span>           | <span data-ttu-id="39717-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39717-176">0x00000010</span></span>                                                         |
| <span data-ttu-id="39717-177">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39717-177">Classes used in</span></span>        | [<span data-ttu-id="39717-178">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="39717-178">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="39717-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="39717-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="39717-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="39717-180">Entry</span></span> | <span data-ttu-id="39717-181">Valor</span><span class="sxs-lookup"><span data-stu-id="39717-181">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="39717-182">ID do link</span><span class="sxs-lookup"><span data-stu-id="39717-182">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39717-183">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="39717-184">System-Only</span></span>            | <span data-ttu-id="39717-185">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-185">False</span></span>                                                              |
| <span data-ttu-id="39717-186">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39717-186">Is-Single-Valued</span></span>       | <span data-ttu-id="39717-187">True</span><span class="sxs-lookup"><span data-stu-id="39717-187">True</span></span>                                                               |
| <span data-ttu-id="39717-188">É indexado</span><span class="sxs-lookup"><span data-stu-id="39717-188">Is Indexed</span></span>             | <span data-ttu-id="39717-189">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-189">False</span></span>                                                              |
| <span data-ttu-id="39717-190">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39717-190">In Global Catalog</span></span>      | <span data-ttu-id="39717-191">True</span><span class="sxs-lookup"><span data-stu-id="39717-191">True</span></span>                                                               |
| <span data-ttu-id="39717-192">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39717-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="39717-193">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39717-193">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="39717-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39717-194">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39717-195">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-196">Search-Flags</span></span>           | <span data-ttu-id="39717-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39717-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="39717-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-198">System-Flags</span></span>           | <span data-ttu-id="39717-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39717-199">0x00000010</span></span>                                                         |
| <span data-ttu-id="39717-200">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39717-200">Classes used in</span></span>        | [<span data-ttu-id="39717-201">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="39717-201">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="39717-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39717-202">Windows Server 2008</span></span>



| <span data-ttu-id="39717-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="39717-203">Entry</span></span> | <span data-ttu-id="39717-204">Valor</span><span class="sxs-lookup"><span data-stu-id="39717-204">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="39717-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="39717-205">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39717-206">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="39717-207">System-Only</span></span>            | <span data-ttu-id="39717-208">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-208">False</span></span>                                                              |
| <span data-ttu-id="39717-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39717-209">Is-Single-Valued</span></span>       | <span data-ttu-id="39717-210">True</span><span class="sxs-lookup"><span data-stu-id="39717-210">True</span></span>                                                               |
| <span data-ttu-id="39717-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="39717-211">Is Indexed</span></span>             | <span data-ttu-id="39717-212">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-212">False</span></span>                                                              |
| <span data-ttu-id="39717-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39717-213">In Global Catalog</span></span>      | <span data-ttu-id="39717-214">True</span><span class="sxs-lookup"><span data-stu-id="39717-214">True</span></span>                                                               |
| <span data-ttu-id="39717-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39717-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="39717-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39717-216">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="39717-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39717-217">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39717-218">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-219">Search-Flags</span></span>           | <span data-ttu-id="39717-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39717-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="39717-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-221">System-Flags</span></span>           | <span data-ttu-id="39717-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39717-222">0x00000010</span></span>                                                         |
| <span data-ttu-id="39717-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39717-223">Classes used in</span></span>        | [<span data-ttu-id="39717-224">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="39717-224">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="39717-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="39717-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="39717-226">Entrada</span><span class="sxs-lookup"><span data-stu-id="39717-226">Entry</span></span> | <span data-ttu-id="39717-227">Valor</span><span class="sxs-lookup"><span data-stu-id="39717-227">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="39717-228">ID do link</span><span class="sxs-lookup"><span data-stu-id="39717-228">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39717-229">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="39717-230">System-Only</span></span>            | <span data-ttu-id="39717-231">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-231">False</span></span>                                                              |
| <span data-ttu-id="39717-232">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39717-232">Is-Single-Valued</span></span>       | <span data-ttu-id="39717-233">True</span><span class="sxs-lookup"><span data-stu-id="39717-233">True</span></span>                                                               |
| <span data-ttu-id="39717-234">É indexado</span><span class="sxs-lookup"><span data-stu-id="39717-234">Is Indexed</span></span>             | <span data-ttu-id="39717-235">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-235">False</span></span>                                                              |
| <span data-ttu-id="39717-236">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39717-236">In Global Catalog</span></span>      | <span data-ttu-id="39717-237">True</span><span class="sxs-lookup"><span data-stu-id="39717-237">True</span></span>                                                               |
| <span data-ttu-id="39717-238">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39717-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="39717-239">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39717-239">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="39717-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39717-240">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39717-241">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-242">Search-Flags</span></span>           | <span data-ttu-id="39717-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39717-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="39717-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-244">System-Flags</span></span>           | <span data-ttu-id="39717-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39717-245">0x00000010</span></span>                                                         |
| <span data-ttu-id="39717-246">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39717-246">Classes used in</span></span>        | [<span data-ttu-id="39717-247">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="39717-247">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="39717-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39717-248">Windows Server 2012</span></span>



| <span data-ttu-id="39717-249">Entrada</span><span class="sxs-lookup"><span data-stu-id="39717-249">Entry</span></span> | <span data-ttu-id="39717-250">Valor</span><span class="sxs-lookup"><span data-stu-id="39717-250">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="39717-251">ID do link</span><span class="sxs-lookup"><span data-stu-id="39717-251">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="39717-252">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="39717-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="39717-253">System-Only</span></span>            | <span data-ttu-id="39717-254">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-254">False</span></span>                                                              |
| <span data-ttu-id="39717-255">É de valor único</span><span class="sxs-lookup"><span data-stu-id="39717-255">Is-Single-Valued</span></span>       | <span data-ttu-id="39717-256">True</span><span class="sxs-lookup"><span data-stu-id="39717-256">True</span></span>                                                               |
| <span data-ttu-id="39717-257">É indexado</span><span class="sxs-lookup"><span data-stu-id="39717-257">Is Indexed</span></span>             | <span data-ttu-id="39717-258">Falso</span><span class="sxs-lookup"><span data-stu-id="39717-258">False</span></span>                                                              |
| <span data-ttu-id="39717-259">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="39717-259">In Global Catalog</span></span>      | <span data-ttu-id="39717-260">True</span><span class="sxs-lookup"><span data-stu-id="39717-260">True</span></span>                                                               |
| <span data-ttu-id="39717-261">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="39717-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="39717-262">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="39717-262">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="39717-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="39717-263">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="39717-264">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="39717-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-265">Search-Flags</span></span>           | <span data-ttu-id="39717-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="39717-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="39717-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="39717-267">System-Flags</span></span>           | <span data-ttu-id="39717-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="39717-268">0x00000010</span></span>                                                         |
| <span data-ttu-id="39717-269">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="39717-269">Classes used in</span></span>        | [<span data-ttu-id="39717-270">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="39717-270">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





