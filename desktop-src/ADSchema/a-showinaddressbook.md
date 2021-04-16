---
title: Atributo de catálogo de mostrar-no-endereço
description: Esse atributo é usado para indicar em quais livros de endereços MAPI um objeto será exibido.
ms.assetid: de00da4d-7c04-4d1d-b375-ce3b5eb2f50f
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos do livro show-in-address
- Esquema de AD do atributo showInAddressBook
topic_type:
- apiref
api_name:
- Show-In-Address-Book
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44632604c539278c67e9dd46537d8e797e2d70d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456175"
---
# <a name="show-in-address-book-attribute"></a><span data-ttu-id="37e43-105">Atributo de catálogo de mostrar-no-endereço</span><span class="sxs-lookup"><span data-stu-id="37e43-105">Show-In-Address-Book attribute</span></span>

<span data-ttu-id="37e43-106">Esse atributo é usado para indicar em quais livros de endereços MAPI um objeto será exibido.</span><span class="sxs-lookup"><span data-stu-id="37e43-106">This attribute is used to indicate in which MAPI address books an object will appear.</span></span> <span data-ttu-id="37e43-107">Normalmente, ele é mantido pelo serviço de atualização de destinatário do Exchange.</span><span class="sxs-lookup"><span data-stu-id="37e43-107">It is usually maintained by the Exchange Recipient Update Service.</span></span>



| <span data-ttu-id="37e43-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e43-108">Entry</span></span> | <span data-ttu-id="37e43-109">Valor</span><span class="sxs-lookup"><span data-stu-id="37e43-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="37e43-110">CN</span><span class="sxs-lookup"><span data-stu-id="37e43-110">CN</span></span>                | <span data-ttu-id="37e43-111">Mostrar catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="37e43-111">Show-In-Address-Book</span></span>                    |
| <span data-ttu-id="37e43-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="37e43-112">Ldap-Display-Name</span></span> | <span data-ttu-id="37e43-113">showInAddressBook</span><span class="sxs-lookup"><span data-stu-id="37e43-113">showInAddressBook</span></span>                       |
| <span data-ttu-id="37e43-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="37e43-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="37e43-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="37e43-115">Update Privilege</span></span>  | <span data-ttu-id="37e43-116">Isso é usado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="37e43-116">This is used by the system.</span></span>             |
| <span data-ttu-id="37e43-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="37e43-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="37e43-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="37e43-118">Attribute-Id</span></span>      | <span data-ttu-id="37e43-119">1.2.840.113556.1.4.644</span><span class="sxs-lookup"><span data-stu-id="37e43-119">1.2.840.113556.1.4.644</span></span>                  |
| <span data-ttu-id="37e43-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="37e43-120">System-Id-Guid</span></span>    | <span data-ttu-id="37e43-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="37e43-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="37e43-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="37e43-122">Syntax</span></span>            | [<span data-ttu-id="37e43-123">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="37e43-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="37e43-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="37e43-124">Implementations</span></span>

-   [<span data-ttu-id="37e43-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="37e43-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="37e43-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="37e43-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="37e43-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="37e43-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="37e43-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="37e43-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="37e43-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="37e43-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="37e43-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="37e43-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="37e43-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="37e43-131">Windows 2000 Server</span></span>



| <span data-ttu-id="37e43-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e43-132">Entry</span></span> | <span data-ttu-id="37e43-133">Valor</span><span class="sxs-lookup"><span data-stu-id="37e43-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="37e43-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="37e43-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e43-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e43-136">System-Only</span></span>            | <span data-ttu-id="37e43-137">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-137">False</span></span>                                                |
| <span data-ttu-id="37e43-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37e43-138">Is-Single-Valued</span></span>       | <span data-ttu-id="37e43-139">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-139">False</span></span>                                                |
| <span data-ttu-id="37e43-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="37e43-140">Is Indexed</span></span>             | <span data-ttu-id="37e43-141">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-141">False</span></span>                                                |
| <span data-ttu-id="37e43-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37e43-142">In Global Catalog</span></span>      | <span data-ttu-id="37e43-143">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-143">False</span></span>                                                |
| <span data-ttu-id="37e43-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37e43-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e43-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37e43-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="37e43-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e43-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e43-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-148">Search-Flags</span></span>           | <span data-ttu-id="37e43-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-149">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-150">System-Flags</span></span>           | <span data-ttu-id="37e43-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-151">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-152">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37e43-152">Classes used in</span></span>        | [<span data-ttu-id="37e43-153">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="37e43-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="37e43-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="37e43-154">Windows Server 2003</span></span>



| <span data-ttu-id="37e43-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e43-155">Entry</span></span> | <span data-ttu-id="37e43-156">Valor</span><span class="sxs-lookup"><span data-stu-id="37e43-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="37e43-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="37e43-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e43-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e43-159">System-Only</span></span>            | <span data-ttu-id="37e43-160">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-160">False</span></span>                                                |
| <span data-ttu-id="37e43-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37e43-161">Is-Single-Valued</span></span>       | <span data-ttu-id="37e43-162">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-162">False</span></span>                                                |
| <span data-ttu-id="37e43-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="37e43-163">Is Indexed</span></span>             | <span data-ttu-id="37e43-164">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-164">False</span></span>                                                |
| <span data-ttu-id="37e43-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37e43-165">In Global Catalog</span></span>      | <span data-ttu-id="37e43-166">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-166">False</span></span>                                                |
| <span data-ttu-id="37e43-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37e43-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e43-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37e43-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="37e43-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e43-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e43-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-171">Search-Flags</span></span>           | <span data-ttu-id="37e43-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-172">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-173">System-Flags</span></span>           | <span data-ttu-id="37e43-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-174">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37e43-175">Classes used in</span></span>        | [<span data-ttu-id="37e43-176">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="37e43-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="37e43-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="37e43-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="37e43-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e43-178">Entry</span></span> | <span data-ttu-id="37e43-179">Valor</span><span class="sxs-lookup"><span data-stu-id="37e43-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="37e43-180">ID do link</span><span class="sxs-lookup"><span data-stu-id="37e43-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e43-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e43-182">System-Only</span></span>            | <span data-ttu-id="37e43-183">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-183">False</span></span>                                                |
| <span data-ttu-id="37e43-184">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37e43-184">Is-Single-Valued</span></span>       | <span data-ttu-id="37e43-185">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-185">False</span></span>                                                |
| <span data-ttu-id="37e43-186">É indexado</span><span class="sxs-lookup"><span data-stu-id="37e43-186">Is Indexed</span></span>             | <span data-ttu-id="37e43-187">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-187">False</span></span>                                                |
| <span data-ttu-id="37e43-188">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37e43-188">In Global Catalog</span></span>      | <span data-ttu-id="37e43-189">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-189">False</span></span>                                                |
| <span data-ttu-id="37e43-190">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37e43-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e43-191">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37e43-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="37e43-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e43-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e43-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-194">Search-Flags</span></span>           | <span data-ttu-id="37e43-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-195">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-196">System-Flags</span></span>           | <span data-ttu-id="37e43-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-197">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-198">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37e43-198">Classes used in</span></span>        | [<span data-ttu-id="37e43-199">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="37e43-199">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="37e43-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37e43-200">Windows Server 2008</span></span>



| <span data-ttu-id="37e43-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e43-201">Entry</span></span> | <span data-ttu-id="37e43-202">Valor</span><span class="sxs-lookup"><span data-stu-id="37e43-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="37e43-203">ID do link</span><span class="sxs-lookup"><span data-stu-id="37e43-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e43-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e43-205">System-Only</span></span>            | <span data-ttu-id="37e43-206">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-206">False</span></span>                                                |
| <span data-ttu-id="37e43-207">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37e43-207">Is-Single-Valued</span></span>       | <span data-ttu-id="37e43-208">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-208">False</span></span>                                                |
| <span data-ttu-id="37e43-209">É indexado</span><span class="sxs-lookup"><span data-stu-id="37e43-209">Is Indexed</span></span>             | <span data-ttu-id="37e43-210">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-210">False</span></span>                                                |
| <span data-ttu-id="37e43-211">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37e43-211">In Global Catalog</span></span>      | <span data-ttu-id="37e43-212">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-212">False</span></span>                                                |
| <span data-ttu-id="37e43-213">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37e43-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e43-214">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37e43-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="37e43-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e43-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e43-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-217">Search-Flags</span></span>           | <span data-ttu-id="37e43-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-218">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-219">System-Flags</span></span>           | <span data-ttu-id="37e43-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-220">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-221">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37e43-221">Classes used in</span></span>        | [<span data-ttu-id="37e43-222">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="37e43-222">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="37e43-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37e43-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="37e43-224">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e43-224">Entry</span></span> | <span data-ttu-id="37e43-225">Valor</span><span class="sxs-lookup"><span data-stu-id="37e43-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="37e43-226">ID do link</span><span class="sxs-lookup"><span data-stu-id="37e43-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e43-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e43-228">System-Only</span></span>            | <span data-ttu-id="37e43-229">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-229">False</span></span>                                                |
| <span data-ttu-id="37e43-230">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37e43-230">Is-Single-Valued</span></span>       | <span data-ttu-id="37e43-231">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-231">False</span></span>                                                |
| <span data-ttu-id="37e43-232">É indexado</span><span class="sxs-lookup"><span data-stu-id="37e43-232">Is Indexed</span></span>             | <span data-ttu-id="37e43-233">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-233">False</span></span>                                                |
| <span data-ttu-id="37e43-234">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37e43-234">In Global Catalog</span></span>      | <span data-ttu-id="37e43-235">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-235">False</span></span>                                                |
| <span data-ttu-id="37e43-236">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37e43-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e43-237">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37e43-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="37e43-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e43-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e43-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-240">Search-Flags</span></span>           | <span data-ttu-id="37e43-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-241">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-242">System-Flags</span></span>           | <span data-ttu-id="37e43-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-243">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-244">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37e43-244">Classes used in</span></span>        | [<span data-ttu-id="37e43-245">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="37e43-245">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="37e43-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37e43-246">Windows Server 2012</span></span>



| <span data-ttu-id="37e43-247">Entrada</span><span class="sxs-lookup"><span data-stu-id="37e43-247">Entry</span></span> | <span data-ttu-id="37e43-248">Valor</span><span class="sxs-lookup"><span data-stu-id="37e43-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="37e43-249">ID do link</span><span class="sxs-lookup"><span data-stu-id="37e43-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="37e43-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="37e43-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="37e43-251">System-Only</span></span>            | <span data-ttu-id="37e43-252">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-252">False</span></span>                                                |
| <span data-ttu-id="37e43-253">É de valor único</span><span class="sxs-lookup"><span data-stu-id="37e43-253">Is-Single-Valued</span></span>       | <span data-ttu-id="37e43-254">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-254">False</span></span>                                                |
| <span data-ttu-id="37e43-255">É indexado</span><span class="sxs-lookup"><span data-stu-id="37e43-255">Is Indexed</span></span>             | <span data-ttu-id="37e43-256">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-256">False</span></span>                                                |
| <span data-ttu-id="37e43-257">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="37e43-257">In Global Catalog</span></span>      | <span data-ttu-id="37e43-258">Falso</span><span class="sxs-lookup"><span data-stu-id="37e43-258">False</span></span>                                                |
| <span data-ttu-id="37e43-259">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="37e43-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="37e43-260">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="37e43-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="37e43-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="37e43-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="37e43-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="37e43-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-263">Search-Flags</span></span>           | <span data-ttu-id="37e43-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-264">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="37e43-265">System-Flags</span></span>           | <span data-ttu-id="37e43-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="37e43-266">0x00000010</span></span>                                           |
| <span data-ttu-id="37e43-267">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="37e43-267">Classes used in</span></span>        | [<span data-ttu-id="37e43-268">**Destinatário de email**</span><span class="sxs-lookup"><span data-stu-id="37e43-268">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





